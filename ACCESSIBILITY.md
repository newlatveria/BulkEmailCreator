# Accessibility Guide

## Overview

Bulk Email Creator Pro is designed to be accessible to all users, regardless of ability. This guide details the accessibility features and how to use them effectively.

## Accessibility Standards Compliance

This tool strives to meet:
- **WCAG 2.1 Level AA** standards
- **Section 508** compliance
- **ARIA 1.2** best practices

## Table of Contents

1. [Screen Reader Support](#screen-reader-support)
2. [Keyboard Navigation](#keyboard-navigation)
3. [Visual Accessibility](#visual-accessibility)
4. [Motor Accessibility](#motor-accessibility)
5. [Cognitive Accessibility](#cognitive-accessibility)
6. [Testing & Validation](#testing--validation)

---

## Screen Reader Support

### Tested Screen Readers
- ✅ JAWS (Windows)
- ✅ NVDA (Windows)
- ✅ VoiceOver (macOS/iOS)
- ✅ TalkBack (Android)

### Key Features

#### Skip Navigation
When you first load the page, press **Tab** to reveal the "Skip to main content" link. Activate it to jump directly to the main content area.

```
[Tab] → "Skip to main content" → [Enter]
```

#### Landmark Regions
The page is divided into semantic regions:
- **Banner**: Header with title and help button
- **Main**: Primary content area (file upload, configuration, email list)
- **Complementary**: Sidebar with template analysis and statistics
- **Navigation**: Help panel (when opened)

**To navigate by landmarks** (screen reader specific):
- JAWS: `R` or `;` to cycle through regions
- NVDA: `D` to cycle through landmarks
- VoiceOver: `VO + U` → Landmarks menu

#### Form Labels
All form controls have proper labels:
- File upload input
- Dropdown selects (recipient column, name column, etc.)
- Text inputs (subject, body)
- Radio buttons (merge modes)
- Checkboxes

Screen readers will announce:
- Label text
- Control type
- Current value/state
- Required status (if applicable)

#### Button Descriptions
All buttons include descriptive text or `aria-label`:
- "Upload your file" (file input button)
- "Preview First Email" (preview button)
- "Generate All Drafts" (generate button)
- "Help" (help panel toggle)
- "Undo last clear" (undo button)

#### Dynamic Content Announcements

**Status Messages**: 
- Success/error messages announced as `role="status"`
- Read automatically without moving focus

**Toast Notifications**:
- Short notifications use `role="alert"`
- Read immediately when they appear

**Progress Indicators**:
- Loading states announced with "Generating email drafts..."
- Completion announced with result count

#### Data Tables
The data preview table includes:
- `<caption>` describing table purpose
- `<th scope="col">` for column headers
- Proper table structure for navigation

**Navigate table**:
- `Ctrl + Alt + Arrow Keys` (JAWS/NVDA on Windows)
- `VO + Arrow Keys` (VoiceOver on macOS)

### Screen Reader Usage Tips

#### Uploading a File
1. Navigate to file upload region
2. Screen reader announces: "Upload your file, Browse button"
3. Activate button (Enter or Space)
4. Select file in dialog
5. Wait for "Loaded X rows with Y columns" announcement

#### Configuring Email
1. Navigate to "Email Configuration" heading
2. Tab through form controls
3. Each dropdown announces current selection
4. Subject and body inputs announced with placeholder text

#### Selecting Merge Mode
1. Navigate to "Merge Options" heading
2. Use arrow keys to select between radio buttons:
   - "No merging - One email per row"
   - "Merge rows with same recipient - Combine multiple rows..."
   - "Combine multiple recipients - One email with all recipients..."
3. If multi-recipient selected, additional options appear

#### Generating Emails
1. Navigate to "Generate All Drafts" button
2. Activate with Enter or Space
3. Listen for progress updates
4. Upon completion: "Generated X email drafts" announced

#### Reviewing Generated Emails
Each email link includes:
- Recipient email address
- Subject line
- CC/BCC information (if present)
- Merge status indicators

**To review**:
1. Navigate to email links region
2. Tab through each email link
3. Screen reader announces all email details
4. Additional buttons: Copy link, Show variables

---

## Keyboard Navigation

### Navigation Without Mouse

**Tab**: Move forward through interactive elements
**Shift + Tab**: Move backward through interactive elements
**Enter/Space**: Activate buttons, links, checkboxes
**Arrow Keys**: Navigate radio buttons, dropdowns (when focused)
**Esc**: Close modals/panels

### Tab Order

The page follows a logical tab order:
1. Skip to content link
2. Help button (top right)
3. Undo button (top right)
4. File upload button
5. Configuration dropdowns
6. CC/BCC inputs
7. Subject input
8. Body textarea
9. Helper buttons (Insert Greeting, Insert Signature)
10. Merge mode radio buttons
11. Filter controls
12. Preview button
13. Generate button
14. Generated email links

### Keyboard Shortcuts

Global shortcuts work from anywhere on the page:

| Shortcut | Action | Context |
|----------|--------|---------|
| `?` | Toggle help panel | When not in input field |
| `Ctrl/Cmd + G` | Generate emails | Anywhere |
| `Ctrl/Cmd + P` | Preview first email | Anywhere |
| `Ctrl/Cmd + S` | Save template | Anywhere |
| `Ctrl/Cmd + Z` | Undo last clear | After clearing emails |
| `Esc` | Close modal/panel | When modal open |

### Keyboard Shortcuts for Input Fields

| Shortcut | Action | Field |
|----------|--------|-------|
| `Enter` | Add email chip | CC/BCC input |
| `,` (comma) | Add email chip | CC/BCC input |
| `Space` | Add email chip | CC/BCC input |
| `Backspace` | Remove last chip | CC/BCC input (when empty) |

### Focus Indicators

All interactive elements show a visible focus indicator:
- **Color**: Teal (#14b8a6)
- **Style**: 2px solid outline with 2px offset
- **Visibility**: High contrast against dark background

**Custom focus states** appear on:
- Buttons
- Links
- Input fields
- Select dropdowns
- Radio buttons
- Checkboxes

### Keyboard-Only Workflow Example

**Complete workflow without mouse**:

1. **Load page**: Press Tab → "Skip to main content" → Enter
2. **Upload file**: Tab to file upload → Enter → Select file → Enter
3. **Configure**: Tab through fields, use Arrow keys in dropdowns
4. **Add variable**: Tab to variable tags → Enter to copy → Paste in subject/body
5. **Set merge mode**: Tab to radio buttons → Arrow keys to select
6. **Preview**: Ctrl+P or Tab to Preview button → Enter
7. **Generate**: Ctrl+G or Tab to Generate button → Enter
8. **Review emails**: Tab through email links
9. **Send**: Enter on any email link to open in mail client

---

## Visual Accessibility

### Color Contrast

All text meets WCAG AA standards:
- **Body text**: White (#F9FAFB) on dark background (#0F172A) - 15.5:1 ratio
- **Headings**: Teal (#14B8A6) on dark background - 6.2:1 ratio
- **Buttons**: White text on colored backgrounds - minimum 4.5:1

### Color Independence

Features don't rely solely on color:
- ✅ Invalid emails: Red background + "invalid" label + icon
- ✅ Success states: Green background + checkmark icon + "Opened" text
- ✅ Required fields: Asterisk (*) + "Required" in label
- ✅ Filter status: Text count + color highlighting

### Text Scaling

The interface supports browser zoom up to 200%:
- No horizontal scrolling at 200% zoom
- All content remains readable
- Interactive elements remain accessible
- Layout adapts responsively

**To zoom**:
- Windows/Linux: `Ctrl + Plus/Minus`
- macOS: `Cmd + Plus/Minus`
- All browsers: Settings → Zoom

### Font Choices

- **Font family**: Inter (sans-serif)
- **Benefits**: High legibility, clear character differentiation
- **Fallbacks**: System fonts if Inter unavailable

### Focus Visibility

All focusable elements have clear visual indicators:
- 2px teal outline
- 2px offset from element
- Visible in all states
- High contrast against background

### Animation & Motion

**Reduced motion support**:
- Smooth transitions by default
- Respects `prefers-reduced-motion` setting
- No auto-playing animations
- User-initiated actions only

**To enable reduced motion**:
- Windows: Settings → Ease of Access → Display → Show animations
- macOS: System Preferences → Accessibility → Display → Reduce motion
- Browser: Some browsers honor OS settings automatically

---

## Motor Accessibility

### Large Click Targets

All interactive elements meet minimum size requirements:
- **Buttons**: Minimum 44×44 pixels
- **Links**: Minimum 44 pixels in height
- **Form controls**: Minimum 44 pixels in height

### No Precision Required

- Drag-and-drop not required (help panel dragging is optional)
- Large hover areas on buttons and links
- Forgiving click zones
- No timed interactions

### Alternative Input Methods

Supports:
- ✅ Mouse/trackpad
- ✅ Keyboard
- ✅ Touch screens
- ✅ Switch control
- ✅ Voice control
- ✅ Eye tracking (with keyboard emulation)

### Sticky Sidebar

Reduces scrolling fatigue:
- Template analysis stays visible
- Statistics always accessible
- Less need to scroll back and forth
- Especially helpful on large displays

### Undo Functionality

Reduces precision requirements:
- Mistake? Press Ctrl+Z
- Up to 10 undo states saved
- Dedicated undo button
- No permanent deletion

### Error Recovery

- Email validation catches errors early
- Preview feature prevents mistakes
- Clear error messages
- Easy correction process

---

## Cognitive Accessibility

### Clear Language

- Simple, direct instructions
- No jargon unless explained
- Consistent terminology
- Progressive disclosure (advanced features hidden until needed)

### Visual Organization

**Consistent layout**:
- Predictable structure
- Grouped related items
- Clear section headings
- Visual hierarchy with headings and spacing

**Color coding**:
- Green: Success, valid
- Red: Error, invalid
- Teal: Primary actions
- Amber: Warnings, merged items
- Purple: BCC, multi-recipient

### Help & Documentation

**Contextual help**:
- Tooltips on hover
- Placeholder text in inputs
- Help panel with detailed guide
- Examples for each feature

**Progressive disclosure**:
- Advanced options hidden by default
- Multi-recipient options appear when selected
- Filter interface optional
- Statistics panel collapsible

### Error Prevention

**Before generating**:
- Preview first email
- Variable detection shows missing data
- Filter stats show affected rows
- Invalid email warnings

**Clear feedback**:
- Success messages in green
- Error messages in red
- Toast notifications for quick actions
- Status updates during processing

### Consistent Patterns

**Repeated interactions**:
- All buttons work the same way
- All dropdowns behave consistently
- Modal close buttons in same location
- Keyboard shortcuts follow conventions

### Memory Aids

**Template system**:
- Save frequently used setups
- Load templates by name
- No need to remember settings
- Quick access to common tasks

**Visual reminders**:
- Variable badges show usage
- Statistics track progress
- Attachment reminders in emails
- Opened emails marked with checkmark

---

## Testing & Validation

### How We Test

**Automated Testing**:
- Lighthouse accessibility audit
- axe DevTools
- WAVE browser extension
- HTML validator

**Manual Testing**:
- Screen reader testing (JAWS, NVDA, VoiceOver)
- Keyboard-only navigation
- Zoom testing up to 200%
- Color contrast analysis

**User Testing**:
- Real users with disabilities
- Diverse assistive technology
- Multiple platforms and browsers
- Feedback incorporation

### Self-Test Checklist

Test the tool yourself:

#### Screen Reader Test
- [ ] Turn on screen reader
- [ ] Navigate entire page
- [ ] Upload a file
- [ ] Configure email settings
- [ ] Generate emails
- [ ] All content readable?
- [ ] All controls accessible?

#### Keyboard Test
- [ ] Unplug mouse
- [ ] Navigate with Tab/Shift+Tab
- [ ] Use all features
- [ ] Try keyboard shortcuts
- [ ] Can you complete workflow?

#### Zoom Test
- [ ] Zoom to 200%
- [ ] Check for horizontal scroll
- [ ] Verify text readable
- [ ] Test all buttons clickable
- [ ] Layout makes sense?

#### Color Contrast Test
- [ ] Use browser color contrast tool
- [ ] Check all text
- [ ] Check button states
- [ ] Verify focus indicators
- [ ] Meets WCAG AA?

### Reporting Issues

Found an accessibility issue?

**Please report with**:
1. Description of the problem
2. Assistive technology used (if applicable)
3. Browser and version
4. Steps to reproduce
5. Expected vs actual behavior

**Submit via**:
- GitHub Issues
- Email: [contact email]
- Accessibility feedback form

### Continuous Improvement

We regularly:
- Review accessibility guidelines
- Update for new standards
- Incorporate user feedback
- Test with real assistive technology
- Train on accessibility best practices

---

## Quick Reference

### Essential Keyboard Shortcuts

```
Ctrl/Cmd + G    Generate emails
Ctrl/Cmd + P    Preview email
Ctrl/Cmd + S    Save template
Ctrl/Cmd + Z    Undo
?               Help panel
Esc             Close modal
```

### Screen Reader Landmarks

```
Banner          → Header area
Main            → Content area
Complementary   → Sidebar
Navigation      → Help panel
```

### Accessibility Settings

**Windows**:
Settings → Ease of Access → Display/Keyboard/Mouse

**macOS**:
System Preferences → Accessibility

**Browser**:
Settings → Accessibility

---

## Additional Resources

### Learn More
- [WCAG 2.1 Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)
- [WebAIM Screen Reader Guide](https://webaim.org/articles/screenreader_testing/)
- [A11Y Project Checklist](https://www.a11yproject.com/checklist/)

### Assistive Technology
- [NVDA (Free Windows screen reader)](https://www.nvaccess.org/)
- [JAWS (Windows screen reader)](https://www.freedomscientific.com/products/software/jaws/)
- [VoiceOver (Built into macOS/iOS)](https://www.apple.com/accessibility/voiceover/)

### Testing Tools
- [Lighthouse (Chrome DevTools)](https://developers.google.com/web/tools/lighthouse)
- [axe DevTools (Browser extension)](https://www.deque.com/axe/devtools/)
- [WAVE (Web accessibility evaluation tool)](https://wave.webaim.org/)

---

**Accessibility is not a feature—it's a requirement.** We're committed to making this tool usable by everyone. Thank you for helping us improve! 🙏
