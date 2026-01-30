# Buck Protocol Documentation - GitBook Deployment Guide

## Quick Start

This documentation is structured for GitBook deployment. You have two options:

### Option A: GitBook.com (Recommended)

1. **Create Account**
   - Go to [gitbook.com](https://gitbook.com)
   - Sign up for a free account

2. **Create New Space**
   - Click "New Space"
   - Name it "Buck Protocol"
   - Select "Documentation" template

3. **Import from GitHub**
   - Go to Integrations → GitHub
   - Connect your GitHub account
   - Push this folder to a GitHub repository
   - Select the repository in GitBook
   - Enable bi-directional sync

4. **Configure Custom Domain**
   - Go to Settings → Custom Domain
   - Enter: `docs.buck.io`
   - Add DNS CNAME record:
     ```
     docs.buck.io → hosting.gitbook.io
     ```

5. **Customize Theme**
   - Go to Customization
   - Primary Color: `#f59e0b`
   - Upload logo from: `https://cdn.buck.io/buck_circle_logo.png`
   - Enable dark mode

### Option B: GitHub Pages with GitBook CLI (Legacy)

```bash
# Install GitBook CLI (deprecated but still works)
npm install -g gitbook-cli

# Navigate to docs folder
cd buck-gitbook-docs

# Install plugins
gitbook install

# Build static site
gitbook build

# Output will be in _book/ folder
# Deploy _book/ to GitHub Pages or any static host
```

## File Structure

```
buck-gitbook-docs/
├── README.md                 # Welcome page
├── SUMMARY.md               # Navigation structure
├── .gitbook.yaml            # GitBook configuration
├── getting-started/
│   ├── overview.md
│   └── about.md
├── tokens/
│   ├── buck-token.md
│   └── buckr-token.md
├── protocol/
│   ├── yield-mechanics.md
│   ├── revenue-model.md
│   └── risks.md
├── technical/
│   ├── contracts.md
│   └── integration.md
└── resources/
    ├── comparison.md
    └── faq.md
```

## GitBook Features Used

### Hints (Callouts)

```markdown
{% hint style="info" %}
This is an info callout
{% endhint %}

{% hint style="success" %}
This is a success callout
{% endhint %}

{% hint style="warning" %}
This is a warning callout
{% endhint %}

{% hint style="danger" %}
This is a danger callout
{% endhint %}
```

### Code Blocks

````markdown
```javascript
const example = "code";
```

```solidity
function example() public view returns (uint256) {
    return 42;
}
```
````

### Tables

```markdown
| Column 1 | Column 2 |
|----------|----------|
| Value 1  | Value 2  |
```

## Customization

### Theme Colors

In GitBook dashboard:
- Primary: `#f59e0b` (Amber)
- Background: Dark mode enabled

### Custom CSS (GitBook Pro)

```css
:root {
  --primary-color: #f59e0b;
}

.hint-info {
  border-left-color: #f59e0b;
  background-color: rgba(245, 158, 11, 0.1);
}
```

## Updating Content

### With GitHub Sync

1. Edit markdown files locally
2. Commit and push to GitHub
3. GitBook automatically updates

### Direct in GitBook

1. Edit directly in GitBook web editor
2. Changes sync back to GitHub

## Support

- GitBook Docs: https://docs.gitbook.com
- Buck Support: admin@buck.io
