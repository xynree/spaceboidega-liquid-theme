<div align="center">
  <img src=".shopify/docs/images/logo.webp" alt="Spaceboidega logo" style="width: 180px;">
</div>

# Spaceboidega Theme

A custom Shopify Liquid theme for the Spaceboidega Shopify storefront. Built off the Colorblock theme.

## Theme Structure

```
spaceboidega-theme/
├── assets/          # CSS, JavaScript, SVG, and image assets used by the theme
├── config/          # Theme configuration files (settings_schema.json, settings_data.json)
├── layout/          # Theme layout templates (theme.liquid, password.liquid)
├── locales/         # Translation files for multi-language support
├── sections/        # Reusable section templates (video, announcement-bar, etc.)
├── snippets/        # Reusable code snippets and components
└── templates/       # Page templates (product, collection, cart, etc.)
```

## Folder Descriptions

### `assets/`

- Contains all static files served directly to the browser (CSS, JavaScript, SVG icons, images, fonts)
- Files are referenced using Shopify's `asset_url` filter for proper caching and versioning
- Essential for the theme's visual styling, interactivity, and overall user experience

### `config/`

- Contains theme configuration files that define and store all customizable settings in the Shopify theme editor
- `settings_schema.json` defines the structure of theme settings (types, defaults) that appear in the admin customizer
- `settings_data.json` stores the actual values merchants have selected, persisting customizations across sessions

### `layout/`

- Contains main wrapper templates that define the overall structure and HTML skeleton for all pages
- `theme.liquid` is the primary layout wrapping every page with essential elements (`<head>`, navigation, footer, global scripts)
- `password.liquid` provides a custom login page for password-protected stores in "coming soon" or private mode

### `locales/`

- Contains translation files that enable multi-language support and internationalization
- Language files (`en.default.json`, `es.json`, `fr.json`) contain translated strings referenced using Liquid's `{{ 'key' | t }}` filter
- Schema translation files provide translations for theme settings labels and descriptions in the Shopify admin

### `sections/`

- Contains reusable, modular templates that merchants can add, remove, and reorder through the Shopify theme editor
- Each section is a self-contained component with its own settings schema, enabling customization without code editing
- Includes complex functionality like video sections with overlay options, announcement bars with configurable font weight, product grids, sliders, and banners

### `snippets/`

- Contains small, reusable Liquid code fragments included throughout the theme using the `{% render 'snippet-name' %}` tag
- Maintains DRY principles by centralizing common UI components (social icons, product cards, forms, navigation) for single-source updates
- Creates consistent design patterns across the theme, such as reusable product cards appearing in collections, recommendations, and search results

### `templates/`

- Contains main page templates that define the structure and layout for different page types (product, collection, cart, customer account, blog/article pages)
- Each template acts as a blueprint combining sections, snippets, and Liquid logic to render appropriate content for that page type
- Templates can be customized or assigned to specific pages through the Shopify admin for unique page experiences
