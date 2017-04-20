# \<isw-toolbar\>

Material Design Polymer 2.0 Toolbar.

Since paper-toolbar is deprecated, and making an app-toolbar MD takes some styling - DRY.

```html
<isw-toolbar rows="2">
  <paper-icon-button slot="nav-icon" icon="menu"></paper-icon-button>

  <div slot="middle-row">ISW Toolbar Demo</div>

  <paper-icon-button slot="action-icon" icon="search"></paper-icon-button>
  <paper-icon-button slot="action-icon" icon="refresh"></paper-icon-button>
  <paper-icon-button slot="action-icon" icon="more-vert"></paper-icon-button>

  <paper-fab slot="fab" icon="add" mini></paper-fab>
</isw-toolbar>
```

It's not responsive by default, but it can be switched between `mobile` and `tablet` metrics.
https://material.io/guidelines/layout/structure.html#structure-app-bar - metrics.

```html
<isw-toolbar metrics="tablet">
  <div slot="top-row">ISW Toolbar Demo</div>
</isw-toolbar>
```

If the metrics property gets controlled by e.g. iron-resizable-behavior, the toolbar gets responsive.