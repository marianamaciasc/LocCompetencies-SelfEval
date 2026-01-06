# Contributing to LMCC Self-Evaluation Tool

Thank you for your interest in contributing to this project! We welcome contributions from everyone, especially students learning about localization.

## How to Contribute

We welcome several types of contributions:
- **Localization/Translation** - Adding new language versions (especially students working on assignments)
- **Bug Reports** - Helping us identify and fix issues
- **Feature Requests** - Suggesting improvements
- **Documentation** - Improving guides and instructions

Jump to the section most relevant to you, or read through for a complete understanding.

---

## For Students in Website Localization

If you're completing a Spanish localization assignment, follow these steps:

### 1. Fork and Clone the Repository

**Fork the repository** to your GitHub account, then **clone your fork** to your local machine.

### 2. Create a New Branch

```bash
git checkout -b spanish-localization
```

### 3. Complete the Localization Tasks

- Translate `en-us.json` → `es-mx.json`
- Copy and adapt `LocCompetencies_en-US.html` → `LocCompetencies_es-MX.html`
- Update language-specific elements (lang attribute, meta tags, etc.)

### 4. Customize CSS for Your Target Audience

This is an optional but recommended step that helps you practice culturally appropriate localization.

#### Understanding CSS Customization for Localization

When localizing for a specific market, consider that color meanings and design preferences vary by culture. Your CSS customization should:
- Reflect the target organization's brand identity
- Consider cultural color associations in the target market
- Maintain sufficient contrast for accessibility (WCAG AA: 4.5:1 for text)
- Be tested with native speakers and target audience members

#### What to Customize

**1. Brand Colors** - Open `locessential-styles.css` and modify the CSS variables in the `:root` section:

```css
:root {
    --primary-color: #1c6399;      /* Main brand color */
    --secondary-color: #2b7bb9;    /* Secondary brand color */
    --accent-color: #50A5E6;       /* Accent/highlight color */
    --success-color: #3dd598;      /* Success indicators (strengths) */
    --pink-accent: #ef91c6;        /* Used for areas needing development */
}
```

**Example for a Mexican university:**
```css
:root {
    --primary-color: #1a472a;      /* Deep green */
    --secondary-color: #2d5f3f;    /* Forest green */
    --accent-color: #d4af37;       /* Gold accent */
    --success-color: #2d5f3f;      /* Forest green */
}
```

**2. Typography** - Adjust fonts if needed for your target language/script:
```css
--font-main: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
--font-heading: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
```

**Note**: Some languages need different font families (Arabic, Chinese, etc.) or more spacing (German text is ~30% longer than English).

**3. Footer** - Update copyright and contact information to reflect your organization

**4. Logo/Branding** (optional) - Add organization logo to header if desired

#### CSS Customization Tips

- **Start simple**: Keep all class names unchanged - only modify color values and text
- **Test accessibility**: Use tools like WebAIM's Contrast Checker to ensure sufficient contrast
- **Preview on devices**: Test on multiple screen sizes before committing
- **Document changes**: Add comments explaining your customization decisions
- **Keep structure intact**: Maintain the original file organization

#### Common CSS Changes for Localization

1. **Colors** - Brand alignment and cultural appropriateness
2. **Fonts** - Different font families for certain scripts
3. **Text direction** - RTL (right-to-left) for Arabic, Hebrew
4. **Spacing** - Accommodate text expansion/contraction

### 5. Enable Spanish Functionality

In `resource-loader.js`, find the `SPANISH_COMING_SOON` constant (around line 30):

**Change from:**
```javascript
const SPANISH_COMING_SOON = true;
```

**To:**
```javascript
const SPANISH_COMING_SOON = false;
```

This disables the "coming soon" message and enables actual language switching. This makes it easy to toggle between development and production modes.

### 6. Test Your Work Thoroughly

Test in a browser and verify:
- All translated text displays correctly
- Color scheme works well and is accessible
- Language switching functionality works
- Responsive design works on mobile devices
- Print preview shows proper formatting
- No JavaScript console errors

### 7. Commit Your Changes

Write clear, descriptive commit messages:

```bash
git add .
git commit -m "Add Spanish localization with custom branding

- Translated all UI strings to Mexican Spanish
- Customized CSS colors for [Your Organization] branding
- Enabled Spanish language switching
- Updated footer with organization info"
```

### 8. Push and Create Pull Request

Push to your fork and create a pull request to the main repository.

---

## For Other Localizers

We welcome translations into any language! Follow the same process as above, using the appropriate locale codes.

### Locale Naming Convention

- Use ISO language-region format: `zh-CN`, `fr-CI`, `pt-BR`, etc.
- File names: `LocCompetencies_[locale].html` and `[locale-lowercase].json`

---

## Quality Standards

### Translation Quality

- Maintain the original meaning and intent
- Adapt cultural references appropriately
- Keep technical terminology consistent
- Preserve HTML structure and formatting
- **Don't translate:**
  - File names or paths in code
  - HTML element IDs
  - CSS class names
  - JavaScript variable names

### Testing Checklist

Before submitting, ensure:
- [ ] All text is translated (no English remnants)
- [ ] Language picker switches correctly
- [ ] All buttons and links work
- [ ] Chart displays properly with translated labels
- [ ] No JavaScript console errors
- [ ] Responsive design works on mobile
- [ ] Print functionality works

### Code Style

- Maintain consistent indentation (2 spaces)
- Keep line length reasonable (<120 characters)
- Add comments for complex logic
- Follow existing code patterns

---

## Bug Reports

Found a bug? Please create an issue with:
- Clear description of the problem
- Steps to reproduce
- Expected vs. actual behavior
- Browser and OS information
- Screenshots if applicable

---

## Feature Requests

Have an idea? Create an issue describing:
- The problem it solves
- How it would work
- Why it would be valuable
- Any implementation ideas

---

## Pull Request Process

1. **Update documentation** if you're changing functionality
2. **Test thoroughly** across different browsers
3. **Write clear commit messages**:
   ```
   Add Spanish localization for UI strings
   
   - Translated all strings in en-us.json to Spanish
   - Created es-mx.json with culturally appropriate adaptations
   - Updated HTML file with proper lang attributes
   ```
4. **Reference issues** in your PR description if applicable
5. **Be patient** - we'll review as soon as possible!

---

## Questions?

- Check existing issues and pull requests first
- For localization questions: info@locessentials.com
- For technical questions: Create a GitHub issue

---

## Recognition

All contributors will be:
- Listed in the GitHub contributors page
- Credited in project documentation
- Forever appreciated! 🎉

Thank you for helping make localization education better!
