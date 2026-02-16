# Contributing to Bulk Email Creator Pro

Thank you for your interest in contributing! This document provides guidelines for contributing to the project.

## 🌟 Ways to Contribute

### 1. Report Bugs
Found a bug? Help us fix it!

**Before submitting**:
- Check if it's already reported in GitHub Issues
- Try to reproduce the bug
- Gather relevant information

**What to include**:
- Clear description of the bug
- Steps to reproduce
- Expected vs actual behavior
- Browser and version
- Sample data file (if applicable)
- Screenshots (if helpful)

**Submit via**: GitHub Issues with "bug" label

### 2. Suggest Features
Have an idea for improvement?

**Before suggesting**:
- Check if it's already requested
- Consider if it fits the project scope
- Think about implementation complexity

**What to include**:
- Clear description of the feature
- Use case / problem it solves
- Example workflow
- Mockups or sketches (if applicable)

**Submit via**: GitHub Issues with "enhancement" label

### 3. Improve Documentation
Documentation is crucial!

**Areas to improve**:
- Fix typos or unclear instructions
- Add more examples
- Create video tutorials
- Translate to other languages
- Add more use cases

**Submit via**: Pull request to docs files

### 4. Submit Code
Ready to code?

**Types of contributions welcome**:
- Bug fixes
- New features (discuss first!)
- Performance improvements
- Accessibility enhancements
- UI/UX improvements
- Test coverage

**Proceed to**: Development Guidelines below

## 🔧 Development Guidelines

### Getting Started

1. **Fork the repository**
   ```bash
   # Fork on GitHub, then clone your fork
   git clone https://github.com/YOUR-USERNAME/BulkEmailCreator.git
   cd BulkEmailCreator
   ```

2. **Open the file**
   ```bash
   # Simply open in browser - no build process!
   open bulk-email-creator-enhanced.html
   ```

3. **Make changes**
   - Edit the HTML file
   - Refresh browser to see changes
   - Test thoroughly

### Code Style

**HTML**:
- Use semantic HTML5 elements
- Include proper ARIA labels
- Maintain accessibility

**CSS**:
- Use Tailwind utility classes
- Add custom CSS to `<style>` block
- Follow existing naming conventions
- Ensure responsive design

**JavaScript**:
- Use modern ES6+ syntax
- Add comments for complex logic
- Follow existing patterns
- Handle errors gracefully

**Example**:
```javascript
// Good: Clear variable names, error handling
const processAndGenerateEmails = (data, options) => {
    try {
        if (!data || data.length === 0) {
            showToast('No data to process', 'error');
            return;
        }
        // Process data...
    } catch (error) {
        console.error('Error generating emails:', error);
        showToast('Failed to generate emails', 'error');
    }
};

// Bad: Unclear names, no error handling
const p = (d, o) => {
    // Process data...
};
```

### Testing Requirements

**Before submitting**, test your changes:

**Browsers**:
- [ ] Chrome (latest)
- [ ] Firefox (latest)
- [ ] Safari (latest)
- [ ] Edge (latest)

**Devices**:
- [ ] Desktop (1920x1080)
- [ ] Laptop (1366x768)
- [ ] Tablet (768x1024)
- [ ] Mobile (375x667)

**Functionality**:
- [ ] File upload works
- [ ] Email generation works
- [ ] All merge modes work
- [ ] Preview works
- [ ] Export works
- [ ] Templates save/load
- [ ] Keyboard shortcuts work

**Accessibility**:
- [ ] Keyboard navigation works
- [ ] Screen reader compatible (test with NVDA/VoiceOver)
- [ ] Focus indicators visible
- [ ] Color contrast sufficient
- [ ] ARIA labels present

**Data Scenarios**:
- [ ] Small dataset (10 rows)
- [ ] Medium dataset (100 rows)
- [ ] Large dataset (1000 rows)
- [ ] Empty file
- [ ] Malformed data
- [ ] Special characters
- [ ] Unicode characters

### Accessibility Requirements

All contributions must maintain accessibility:

**Required**:
- Keyboard accessibility for all features
- ARIA labels on interactive elements
- Semantic HTML structure
- Color contrast ratio ≥ 4.5:1
- Focus indicators visible
- Screen reader tested

**Testing Tools**:
- Lighthouse accessibility audit (score ≥ 90)
- axe DevTools (0 violations)
- WAVE (0 errors)
- Manual keyboard navigation
- Screen reader testing

### Performance Guidelines

Keep the tool fast and responsive:

**Target metrics**:
- File parsing: < 2 seconds for 1000 rows
- Email generation: < 5 seconds for 100 emails
- UI interactions: < 100ms response time

**Optimization tips**:
- Use debouncing for input handlers
- Implement virtual scrolling for large lists (if needed)
- Minimize DOM manipulations
- Avoid unnecessary re-renders
- Test with large datasets

### Commit Guidelines

Write clear, descriptive commit messages:

**Format**:
```
<type>: <subject>

<body>

<footer>
```

**Types**:
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, no logic change)
- `refactor`: Code refactoring
- `test`: Adding tests
- `chore`: Maintenance tasks

**Examples**:
```
feat: add multi-recipient merge mode

Implements new merge option that combines all recipients into one email with shared body text. Users can choose between TO (public) or BCC (private) placement.

Closes #123

---

fix: email validation now catches edge cases

Fixed bug where emails with special characters weren't validated correctly. Added additional test cases.

Fixes #456

---

docs: update README with keyboard shortcuts

Added comprehensive keyboard shortcuts section to README with examples and platform-specific instructions.
```

### Pull Request Process

1. **Create a branch**
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/bug-description
   ```

2. **Make your changes**
   - Follow code style guidelines
   - Add comments where needed
   - Update documentation if needed

3. **Test thoroughly**
   - Run through test checklist
   - Test on multiple browsers
   - Test accessibility

4. **Commit your changes**
   ```bash
   git add .
   git commit -m "feat: add your feature"
   ```

5. **Push to your fork**
   ```bash
   git push origin feature/your-feature-name
   ```

6. **Create Pull Request**
   - Go to GitHub
   - Click "New Pull Request"
   - Fill out the template
   - Link related issues

### Pull Request Template

```markdown
## Description
[Clear description of changes]

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Performance improvement
- [ ] Accessibility improvement

## Testing
- [ ] Tested on Chrome
- [ ] Tested on Firefox
- [ ] Tested on Safari
- [ ] Tested on Edge
- [ ] Keyboard navigation works
- [ ] Screen reader compatible

## Screenshots
[If applicable, add screenshots showing the changes]

## Related Issues
Fixes #[issue number]

## Checklist
- [ ] Code follows project style
- [ ] Self-reviewed code
- [ ] Commented complex logic
- [ ] Updated documentation
- [ ] No new warnings
- [ ] Tested accessibility
- [ ] Tested performance
```

## 📋 Code Review Process

### What to Expect

**Timeline**:
- Initial response: Within 3 business days
- Code review: Within 1 week
- Merge decision: After all feedback addressed

**Review criteria**:
- Functionality works as intended
- Code quality meets standards
- Tests pass
- Documentation updated
- Accessibility maintained
- No performance regression

**Possible outcomes**:
- ✅ Approved and merged
- 🔄 Changes requested
- ❌ Declined (with explanation)

### Responding to Feedback

**Do**:
- ✅ Address all comments
- ✅ Ask questions if unclear
- ✅ Be open to suggestions
- ✅ Update PR based on feedback
- ✅ Mark conversations resolved

**Don't**:
- ❌ Take feedback personally
- ❌ Ignore comments
- ❌ Argue without reason
- ❌ Force merge

## 🎨 Design Guidelines

### UI/UX Principles

**Consistency**:
- Follow existing design patterns
- Use established color scheme
- Match existing spacing
- Maintain layout structure

**Simplicity**:
- Keep interfaces clean
- Avoid clutter
- Progressive disclosure
- Clear hierarchy

**Feedback**:
- Immediate response to actions
- Clear error messages
- Progress indicators
- Success confirmations

### Color Palette

**Primary colors**:
- Teal: `#14B8A6` (primary actions, success)
- Blue: `#3B82F6` (secondary actions)
- Red: `#DC2626` (errors, warnings)
- Amber: `#F59E0B` (cautions)
- Purple: `#A855F7` (BCC, special states)

**Neutral colors**:
- Background: `#0F172A`
- Cards: `#1E293B`
- Borders: `#334155`
- Text: `#F9FAFB`

**Usage**:
- Use semantic colors (green=success, red=error)
- Maintain contrast ratios
- Test in dark mode (already dark themed)

## 🔐 Security Guidelines

### Data Privacy

**Never**:
- ❌ Send user data to external servers
- ❌ Store sensitive data in localStorage (passwords, tokens)
- ❌ Log sensitive information to console
- ❌ Include tracking scripts

**Always**:
- ✅ Keep data local to browser
- ✅ Use secure coding practices
- ✅ Validate input data
- ✅ Sanitize user input

### Input Validation

**Email validation**:
```javascript
// Good: Proper validation
const validateEmail = (email) => {
    const re = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    return re.test(String(email).toLowerCase());
};

// Bad: No validation
const validateEmail = (email) => email.includes('@');
```

**File validation**:
```javascript
// Good: Check file type and size
const validateFile = (file) => {
    const validTypes = ['.csv', '.xlsx', '.xls'];
    const maxSize = 10 * 1024 * 1024; // 10MB
    
    const ext = file.name.toLowerCase().substring(file.name.lastIndexOf('.'));
    return validTypes.includes(ext) && file.size <= maxSize;
};
```

## 📚 Documentation Standards

### Code Comments

**When to comment**:
- Complex algorithms
- Non-obvious logic
- Workarounds or hacks
- Public API functions

**When not to comment**:
- Self-explanatory code
- Obvious operations
- Redundant statements

**Example**:
```javascript
// Good: Explains WHY, not WHAT
// Use setTimeout to allow UI to update before heavy processing
setTimeout(() => processEmails(), 100);

// Bad: States the obvious
// Set timeout to 100ms
setTimeout(() => processEmails(), 100);
```

### README Updates

Update README when adding:
- New features
- New dependencies
- New file formats
- New configuration options
- Breaking changes

## 🐛 Bug Fix Guidelines

### Bug Report Investigation

1. **Reproduce the bug**
   - Follow reported steps exactly
   - Try variations
   - Note any differences

2. **Isolate the cause**
   - Check console for errors
   - Use debugger
   - Test related features
   - Check recent changes

3. **Fix the bug**
   - Find root cause (not symptoms)
   - Test fix thoroughly
   - Check for side effects
   - Add regression test if possible

4. **Document the fix**
   - Explain what caused bug
   - Describe the solution
   - Link to issue number

## 🎯 Feature Development Guidelines

### Before Starting

1. **Discuss the feature**
   - Open an issue first
   - Get feedback from maintainers
   - Confirm it's desired

2. **Plan the implementation**
   - Consider edge cases
   - Think about UX
   - Plan for errors
   - Consider accessibility

3. **Break down the work**
   - Create checklist
   - Identify dependencies
   - Estimate complexity

### While Developing

1. **Iterate**
   - Start simple
   - Add complexity gradually
   - Test frequently

2. **Document**
   - Add inline comments
   - Update README
   - Create examples

3. **Test edge cases**
   - Empty data
   - Large datasets
   - Invalid input
   - Error conditions

## 📞 Getting Help

### Questions?

**Ask via**:
- GitHub Discussions (preferred)
- GitHub Issues (if bug-related)
- Pull Request comments (if PR-specific)

**Response time**:
- Usually within 3 business days
- Complex questions may take longer

### Resources

**Documentation**:
- README.md - Feature guide
- QUICK-START.md - Getting started
- ACCESSIBILITY.md - Accessibility features
- TEMPLATES.md - Email examples

**External**:
- [WCAG Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)
- [MDN Web Docs](https://developer.mozilla.org/)
- [Tailwind CSS Docs](https://tailwindcss.com/docs)

## 📜 License

By contributing, you agree that your contributions will be licensed under the MIT License.

## 🙏 Recognition

Contributors will be:
- Listed in CONTRIBUTORS.md
- Mentioned in release notes
- Credited in relevant documentation

---

**Thank you for contributing!** Every contribution, no matter how small, helps make this project better for everyone. 🎉
