# Public Reminders

Internal reminders for future TODOs.

---

## Table of Contents
- [Public Reminders](#public-reminders)
  - [Table of Contents](#table-of-contents)
  - [Migration from Github Pages Default Domain to Custom Domain Checklist](#migration-from-github-pages-default-domain-to-custom-domain-checklist)

---

## Migration from Github Pages Default Domain to Custom Domain Checklist

- [ ] Comment out function prefixProdAnchors
  - The javascript function `prefixProdAnchors` in [/static/js.js](/static/js.js) is a temporary workaround for Github Pages suffixing the base url with the repo name. This interfered with testing anchor links in prod.
