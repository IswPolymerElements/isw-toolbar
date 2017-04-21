# \<isw-toolbar\>

Material Design Polymer 2.0 Toolbar.

Since paper-toolbar is deprecated, and making an app-toolbar MD takes some styling - DRY.

```html
<isw-toolbar rows="2">
  <paper-icon-button slot="nav-icon" icon="menu"></paper-icon-button>

  <span slot="middle">ISW Toolbar Demo</span>

  <paper-icon-button slot="action-icon" icon="search"></paper-icon-button>
  <paper-icon-button slot="action-icon" icon="refresh"></paper-icon-button>
  <paper-icon-button slot="action-icon" icon="more-vert"></paper-icon-button>

  <paper-fab slot="fab" icon="add" mini></paper-fab>
</isw-toolbar>
```

### Responsive
It's not responsive by default, but it can be switched between `mobile` and `tablet` metrics.
https://material.io/guidelines/layout/structure.html#structure-app-bar - metrics.

```html
<isw-toolbar metrics="tablet">
  <span slot="top">ISW Toolbar Demo</span>
</isw-toolbar>
```

If the metrics property gets controlled by e.g. iron-resizable-behavior, the toolbar gets responsive.

### Styling
The following custom properties are available for styling:

Custom property | Default
----------------|----------
`--isw-toolbar-background` | --primary-color
`--isw-toolbar-font-color` | --dark-theme-text-color
`--isw-toolbar-button-icon-color` | --dark-theme-text-color
`--isw-toolbar-fab-icon-color` | --dark-theme-text-color

Default styling via paper-styles properties:

```css
isw-toolbar {
  --primary-color: var(--paper-blue-500);
  --accent-color: var(--paper-cyan-500);
}
```

Custom styling:

```css
isw-toolbar {
  --isw-toolbar-background: var(--paper-blue-500);
  --isw-toolbar-font-color: var(--dark-theme-text-color);
  --isw-toolbar-button-icon-color: rgba( 0, 0, 0, 0.54 );
  --isw-toolbar-fab-icon-color: var(--dark-theme-text-color);
  --paper-fab-background: var(--paper-cyan-500);
}
```

### Elements wrapped with a-tag
Elements with a tags should be properly styled by default.
If the fab is mini and wrapped in an a tag, the a tag also needs an mini attribute for correct positioning.

```html
<a slot="fab" href="#" mini>
  <paper-fab icon="add" mini></paper-fab>
</a>
```