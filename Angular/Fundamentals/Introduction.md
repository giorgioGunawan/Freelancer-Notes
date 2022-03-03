# Angular from UltimateCourses - https://app.ultimatecourses.com/course/angular-fundamentals

## Missing introduction to angular
What makes up angular architecture?
- Modules
- Components
- Directives
- Pipes
- Services
- Router

### Modules 
Groups related code together, are standalone, and are related to features, and usually called feature modules.

We can move shared modules (lazy loading)

### Components
Independent and isolated UI functionality
We want to make it reusable and composable
Components can render other components
One way data flow and immutable state

### Directives
Adds functionality to HTML or components
Modify or generate elements and components
Directives are our gateway to the DOM, if we need lower level functionality that needs to tamper with DOM, we use directives

### Pipes
A simple pure function that transform data for rendering and are used inside components
We transform the data we want to bind before render, holds reusable logic 
Many built-in pipes (common practice too to use custom pipes)

### Services
A generic class - usually for logic that are not component related
Used for data fetching, and state storage
Can be consumed by other services and components
Singleton dependency - instantiate once and logic is then shared (dont get a new instance)

### Router
Routing logic will usually be done by the server, which requires a full page refresh
But, now router compeontn of angular can instruct angular to render a particular component or module based on the URL

