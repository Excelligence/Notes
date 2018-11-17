### Changing Color of Bootstrap Collapsible Button

Two methods

#### Add a font awesome icon

Add HTML

<span >  

<i class="fas fa-bars"></i>

 </span>

Add CSS

`.fa-bars{`

​    `color:blue;`

`}`

`.navbar-toggler{`

​    border-color: blue !important;

`}`



#### Change XML Data in SVG file

Add this to CSS

`.navbar-toggler-icon {`

​    `background-image:`

`url("data:image/svg+xml;charset=utf8,%3Csvg viewBox='0 0 32 32' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath stroke='rgba(255,102,203)' stroke-width='2' stroke-linecap='round' stroke-miterlimit='10' d='M4 8h24M4 16h24M4 24h24'/%3E%3C/svg%3E") !important;`

  `}`

   `.navbar-toggler {`

`border-color: rgb(255,102,203) !important;`

  } 

``  