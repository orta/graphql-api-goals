# graphql-api-goals

Notes on what I'd like for a pretty ideal API framework. A year and a half into Redwood, and I'm really happy with how it's been as a tool for getting ideas up & running, then migrating out when it's time for an abstraction to get more focus.

### Codebase would be:

 - In TypeScript
 - Trivial to run in debug mode inside VS Code
 - Few testing abstractions, want to run many tests very often on hooks
 
### Deno/Node?

- Deno would allow for better debugging, faster iteration and native TS
- Node means keeping acccess to Jest and Wallaby

Genuinely unsure here, and Prisma is currently node only

### Abstractions 
 
Lot of good stuff take from Redwood here, they have a generalized "functions" concept, then a lot of extra work for making a main GraphQL API.
 
 ##### GraphQL 
 
 - Prisma -> SDL -> GraphQL Resolvers for main GQL API   
 - Describe in SDL first, then resolvers. Make extremely tight.
 - Built-in support for graphql connections 

##### Systems

- Hooks for allowing side processes (type codegen for example)

### Things to look into:

- [Grafast](https://www.youtube.com/watch?v=x0FMjL5-kNI) to try remove the amount of pre-guessing I do for includes on db queries
- [GraphQXL](https://github.com/gabotechs/graphqxl)
