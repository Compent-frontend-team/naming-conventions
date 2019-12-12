# Naming Media Queries



## Breakpoints
1. 600px
1. 900px
1. 1200px

Example naming
<details><summary>Less:</summary>
  
```less
@screen-sm         : 600px;
@screen-md         : 900px;
@screen-lg         : 1200px;
```

</details>


## Simple queries

<details><summary>Less:</summary>
  
```less
@sm         : ~"(min-width: @{screen-sm})";
@md         : ~"(min-width: @{screen-md})";
@lg         : ~"(min-width: @{screen-lg})";
```

</details>


1. 600px
1. 900px
1. 1200px

1. 600
- @media (min-width: 600px) { @content; } - sm

2. 900
- @media (min-width: 900px) { @content; } - md

3. 1200
- @media (min-width: 1200px) { @content; } - lg

- .sm .md .lg (by default)
- .sm-down (max-width: 600px)
- .sm-only @media (min-width: 600px) and (max-width: 900px)
- .sm-lg @media (min-width: 600px) and (max-width: 1200px)

- .sm-down-l (for landscape view)
- .sm-down-p (for portrait view)
