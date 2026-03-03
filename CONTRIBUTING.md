# Contributing to Bill-Sency

Thank you for your interest in contributing to Bill-Sency! 

## Important Notice

**This is a releases-only repository.** It contains:
- Installation files and documentation
- Issue tracking and bug reports
- Feature requests and discussions
- Release changelogs

**This repository does NOT contain source code.**

---

## How You Can Contribute

### 1. Report Bugs 🐛

Found a bug? Help us fix it!

- Use the [Bug Report template](https://github.com/c9infotech/bill-sency-releases/issues/new?template=bug_report.md)
- Provide detailed reproduction steps
- Include screenshots if applicable
- Specify your environment (Windows version, Bill-Sency version)

**Before reporting:**
- Check if the bug is already reported
- Try the latest version
- Read the [troubleshooting guide](INSTALLATION.md#troubleshooting)

### 2. Request Features 💡

Have an idea? We'd love to hear it!

- Use the [Feature Request template](https://github.com/c9infotech/bill-sency-releases/issues/new?template=feature_request.md)
- Explain your use case clearly
- Describe the expected benefits
- Be willing to test beta versions

### 3. Improve Documentation 📚

Documentation improvements are always welcome:

- Fix typos or unclear instructions
- Add screenshots or examples
- Translate documentation (if applicable)
- Share tips and tricks

**How to contribute documentation:**
1. Fork this repository
2. Make your changes
3. Submit a pull request
4. We'll review and merge

### 4. Help Others 🤝

Support the community:

- Answer questions in issues
- Share your experience and solutions
- Test beta versions and provide feedback
- Share Bill-Sency with others who might benefit

### 5. Beta Testing 🧪

Want early access to new features?

- Join our beta testing program
- Email: support@c9infotech.com
- Subject: "Beta Tester Application"
- Tell us about your business and how you use Bill-Sency

---

## Guidelines

### Communication

- Be respectful and professional
- Stay on topic
- Provide constructive feedback
- Help create a welcoming community

### Bug Reports

**Good bug report:**
```
Title: [BUG] Cannot save item with price > 999,999

Environment: Windows 11, Bill-Sency 1.0.0-beta

Steps:
1. Open Items
2. Click New Item
3. Enter price: 1,000,000
4. Click Save
5. Error appears: "Invalid price"

Expected: Should save item with price up to 99,999,999
Actual: Error message and item not saved

Screenshots: [attached]
```

**Poor bug report:**
```
Title: doesn't work

it crashes when i try to save
```

### Feature Requests

**Good feature request:**
```
Title: [FEATURE] Add barcode scanner support

Problem: Currently must type SKU manually, slow during busy times

Solution: Support USB barcode scanners to auto-fill SKU field

Use Case: Small retail shop, scan 100+ items per day
Would save ~30 minutes daily

Priority: High - would significantly improve workflow

Willing to test: Yes
```

**Poor feature request:**
```
Title: need bar codes

add bar codes plz
```

---

## Development Contributions

### Source Code

The source code is in a **private repository**. If you're interested in contributing code:

1. **Email us:** dev@c9infotech.com
2. **Subject:** "Developer Contribution Interest"
3. **Include:**
   - Your GitHub profile
   - Your experience with C# / WPF / .NET
   - What you'd like to contribute
   - Why you're interested

### Code Contributions Process

If granted access to the private repository:

1. **Fork** the private repository
2. **Create a branch:** `feature/your-feature-name` or `bugfix/issue-number`
3. **Follow coding standards:**
   - C# conventions
   - XML documentation comments
   - Consistent formatting
   - Write tests for new features
4. **Commit messages:**
   - Clear and descriptive
   - Reference issue numbers: `Fix #123: Description`
5. **Pull request:**
   - Describe your changes
   - Link related issues
   - Update documentation if needed
6. **Code review:**
   - Respond to feedback
   - Make requested changes
   - Be patient and respectful

### Coding Standards

```csharp
// Good: Clear naming, documented
/// <summary>
/// Calculates the total price including tax.
/// </summary>
/// <param name="subtotal">The subtotal before tax</param>
/// <param name="taxRate">The tax rate as a decimal (e.g., 0.15 for 15%)</param>
/// <returns>The total price including tax</returns>
public decimal CalculateTotalWithTax(decimal subtotal, decimal taxRate)
{
    if (subtotal < 0) throw new ArgumentException("Subtotal cannot be negative");
    if (taxRate < 0) throw new ArgumentException("Tax rate cannot be negative");
    
    return subtotal * (1 + taxRate);
}

// Bad: Unclear, no documentation
public decimal calc(decimal s, decimal t)
{
    return s * (1 + t);
}
```

---

## Recognition

### Contributors

All contributors will be recognized:

- Listed in release notes
- Credit in documentation
- Public thank you (if desired)

### Hall of Fame

Outstanding contributors may be featured in:
- README.md
- Company website
- Social media

---

## Legal

### License Agreement

By contributing, you agree that:

- Your contributions are your original work
- You have the right to submit the contribution
- Your contribution may be distributed under the project's license
- You grant C9 Infotech a perpetual, worldwide, non-exclusive license to use your contribution

### Intellectual Property

- C9 Infotech retains ownership of the Bill-Sency codebase
- Your contributions become part of Bill-Sency
- You retain credit for your contributions

### Code of Conduct

We follow these principles:

**Do:**
- Be respectful and inclusive
- Provide constructive feedback
- Help others learn and grow
- Assume good intentions

**Don't:**
- Harass or discriminate
- Share confidential information
- Spam or self-promote
- Use offensive language

**Violations:** May result in ban from project

---

## Getting Started

### I want to...

**Report a bug:**
1. Check [existing issues](https://github.com/c9infotech/bill-sency-releases/issues)
2. Use [bug report template](https://github.com/c9infotech/bill-sency-releases/issues/new?template=bug_report.md)
3. Provide details and screenshots

**Request a feature:**
1. Check [existing requests](https://github.com/c9infotech/bill-sency-releases/issues?q=label%3Aenhancement)
2. Use [feature request template](https://github.com/c9infotech/bill-sency-releases/issues/new?template=feature_request.md)
3. Explain use case and benefits

**Improve documentation:**
1. Fork repository
2. Edit Markdown files
3. Submit pull request

**Help with support:**
1. Browse [open issues](https://github.com/c9infotech/bill-sency-releases/issues)
2. Answer questions you know
3. Share your solutions

**Contribute code:**
1. Email dev@c9infotech.com
2. Wait for repository access
3. Follow development process

---

## Questions?

- **General:** support@c9infotech.com
- **Development:** dev@c9infotech.com
- **Security:** security@c9infotech.com
- **Business:** contact@c9infotech.com

---

## Thank You! 🙏

Every contribution, no matter how small, helps make Bill-Sency better for everyone.

---

**Last Updated:** March 3, 2026
