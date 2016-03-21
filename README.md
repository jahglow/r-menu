[DEMO & APIdocs](http://jahglow.github.io/r-menu)

A set of menu elements for Confirmit Reportal. 
`<r-menu>` is a wrapper for Reportal Navigator component. 
`<r-admin-menu>` is a handy standalone admin-menu wrapper that presents it as a paper-dropdown.

# r-menu
`r-menu` is an element to wrap around standard Reportal Navigator and make it an expandable side menu, one-level top-menu or both.

Example:

     <r-menu icons-legacy="polymer warning settings" layout="mixed">
       <confirmit:wysiwygcomponent type="Navigator" id="a2f84de1-2b19-4ba8-8d4c-9edbfa1349c8" />
     </r-menu>

The best practice for now is to have the first instance of `r-menu` get the data at Report Master...

    <r-menu data-provider data="{{reportalNavigator}}">
      <confirmit:wysiwygcomponent type="Navigator" id="a2f84de1-2b19-4ba8-8d4c-9edbfa1349c8" />
    </r-menu>

...and transfer it to Page Master where the layout scaffolding is defined.

    <r-menu icons-legacy="polymer warning settings" layout="mixed" data="{{reportalNavigator}}"></r-menu>

#### Styling

The following custom properties and mixins are also available for styling:

Custom property | Description | Default
----------------|-------------|----------
`--r-menu-item` | Mixin applied to the look of a single item | `{}`
`--r-menu-item-focused` | Mixin applied to the look of a focused item | `{}`
`--r-menu-expand-icon` | Mixin applied to the look of the expand chevron on nested menus | `{}`
`--r-menu-toplevel-border` | Mixin applied to separating border on top-level items | `{}`
`--r-menu-nested` | Mixin for nested menus | `{}`



## r-admin-menu

An element that helps to create a simple to use admin-menu in Material Design.

Example:

    <r-admin-menu>
      <confirmit:wysiwygcomponent type="AdminMenu" id="38763a11-ad5b-453b-9653-7522bc676af0" />
    </r-admin-menu>

#### Styling

The following custom properties and mixins are also available for styling:

Custom property | Description | Default
----------------|-------------|----------
`--r-admin-menu-button` | Mixin applied to the host element | `{}`

`r-admin-menu` uses `paper-menu-button`, `paper-icon-button` and `paper-listbox`, so you can use corresponding Custom CSS properties to style their contents.
