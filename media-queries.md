# Naming Media Queries



##  1. Declarate breakpoints name
We use abbreviations similarly to clothing sizes.
1. sm — 600px
1. md — 900px
1. lg — 1200px
1. xl — 1600px

Example naming
<details><summary>CSS:</summary>
  
```css
--screen-sm         : 600px;
--screen-md         : 900px;
--screen-lg         : 1200px;
--screen-xl         : 1600px;
```

</details>

<details><summary>Less:</summary>
  
```less
@screen-sm         : 600px;
@screen-md         : 900px;
@screen-lg         : 1200px;
@screen-xl         : 1600px;
```

</details>


## Create simple queries

<details><summary>Less:</summary>
  
```less
@sm         : ~"(min-width: @{screen-sm})";
@md         : ~"(min-width: @{screen-md})";
@lg         : ~"(min-width: @{screen-lg})";
```

</details>

## Optional create advanced queries

<details><summary>Less:</summary>
  
```less
@sm-down         : ~"(max-width: @{screen-sm})";
@md-down         : ~"(max-width: @{screen-md})";
@lg-down         : ~"(max-width: @{screen-lg})";

@sm-only         : ~"(min-width: @{screen-sm}) and (max-width: @{screen-md})";
@md-only         : ~"(min-width: @{screen-md}) and (max-width: @{screen-lg})";
@lg-only         : ~"(min-width: @{screen-lg}) and (max-width: @{screen-xl})";

@sm-l            : ~"(min-width: @{screen-sm}) and (orientation: landscape)";
@md-l            : ~"(min-width: @{screen-md}) and (orientation: landscape)";
@lg-l            : ~"(min-width: @{screen-lg}) and (orientation: landscape)";

@sm-p            : ~"(min-width: @{screen-sm}) and (orientation: portrait)";
@md-p            : ~"(min-width: @{screen-md}) and (orientation: portrait)";
@lg-p            : ~"(min-width: @{screen-lg}) and (orientation: portrait)";
```

</details>
