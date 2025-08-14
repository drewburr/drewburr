## Welcome to drewburr.com!

This page is currently a WIP. Stay tuned for more!

### Links

- [K1C Camera Stream](k1c-stream.html) - Live stream from my 3D printer

<!--
You can use the [editor on GitHub](https://github.com/drewburr/drewburr/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/drewburr/drewburr/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.

-->

<style>
  :root, [data-theme="light"] {
    --page-header-bg: #159957;
    --page-header-bg-end: #155799;
    --main-content-bg: #fff;
    --main-content-color: #333;
    --link-color: #1e6bb8;
    --btn-bg: rgba(255, 255, 255, 0.1);
    --btn-color: #fff;
    --btn-border-color: rgba(255, 255, 255, 0.2);
    --btn-hover-bg: rgba(255, 255, 255, 0.2);
    --btn-hover-border-color: rgba(255, 255, 255, 0.3);
  }

  [data-theme="dark"] {
    --page-header-bg: #1e1e1e;
    --page-header-bg-end: #151515;
    --main-content-bg: #1e1e1e;
    --main-content-color: #c8c8c8;
    --link-color: #2e8cff;
    --btn-bg: rgba(255, 255, 255, 0.05);
    --btn-color: #c8c8c8;
    --btn-border-color: rgba(255, 255, 255, 0.1);
    --btn-hover-bg: rgba(255, 255, 255, 0.1);
    --btn-hover-border-color: rgba(255, 255, 255, 0.2);
  }

  .page-header {
    background-color: var(--page-header-bg);
    background-image: linear-gradient(120deg, var(--page-header-bg-end), var(--page-header-bg));
  }

  .main-content {
    background-color: var(--main-content-bg);
    color: var(--main-content-color);
  }

  .main-content a {
    color: var(--link-color);
  }

  .theme-toggle {
    position: absolute;
    top: 20px;
    right: 20px;
    background-color: var(--btn-bg);
    color: var(--btn-color);
    border: 1px solid var(--btn-border-color);
    border-radius: 4px;
    padding: 8px 12px;
    cursor: pointer;
    font-size: 14px;
    transition: all 0.3s ease;
  }

  .theme-toggle:hover {
    background-color: var(--btn-hover-bg);
    border-color: var(--btn-hover-border-color);
  }
</style>

<button class="theme-toggle" id="themeToggle">Toggle Theme</button>

<script>
  document.addEventListener('DOMContentLoaded', function() {
    const themeToggle = document.getElementById('themeToggle');
    const pageHeader = document.querySelector('.page-header');
    if (pageHeader && themeToggle) {
      pageHeader.appendChild(themeToggle);
    }

    function initializeTheme() {
      const savedTheme = localStorage.getItem('theme') || 'dark';
      document.documentElement.setAttribute('data-theme', savedTheme);
      updateThemeToggleText(savedTheme);
    }

    function toggleTheme() {
      const currentTheme = document.documentElement.getAttribute('data-theme');
      const newTheme = currentTheme === 'dark' ? 'light' : 'dark';
      document.documentElement.setAttribute('data-theme', newTheme);
      localStorage.setItem('theme', newTheme);
      updateThemeToggleText(newTheme);
    }

    function updateThemeToggleText(theme) {
      themeToggle.textContent = theme === 'dark' ? '☀️ Light Mode' : '🌙 Dark Mode';
    }

    themeToggle.addEventListener('click', toggleTheme);

    initializeTheme();
  });
</script>
