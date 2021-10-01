# MicroFrontends

- Improve Scalability
- Take the same principles of microservices and apply them to frontend.

## Who uses MicroFrontends

- Ikea
- Spotify
- Zalando
- DAZN (German sports streaming application)

## How to split the UI

1. By domain / product team
   - Vertical slice such as auth team / sales team / customer team
2. By section
   - Header / Footer / Body / Navbar
3. By Functionality
   - Search bar / Recommendations
4. By Page
   - Home page then each child page is another frontend.

## Pros and Cons

- Independendant teamms
  - Pros
    - Isolated
    - Can help facilitate team independnecies
    - Reduced need for coordination with other teams
  - Cons
    - Assumes vertical ownershop of stack
    - Easy to end up developing a distributed monolith
    - Teams arent spread thin, but architecture is
- Code Orgonization
  - Pros
    - Each micro fontend is specific
    - Less cod eto maintain
  - Cons
    - If there need sto be shared app, in can quicky become a dumping ground

# Release Indepenedence

- Pros
  - Able to release small part of frontend
  - Can push for CI/CD mindset
  - Cann roll back part without affecting whole site.
- COns
  - Frontend can have links between apps, with cuts down on indepenecne

Reduced Testing Complexity

- Pros
  - Fewer code changes in each release
- Cons - updating one app does not mean you wont break another - will take more time to architect the solution to ensure app independence.
  Faster Build Times
- Pros
  - Smaller individual clients could lead to shorter build times
- Cons
  - Can increase build times because building multiple apps.
- Technology Independence
  - Pros
    - Allow teams to be indepenedent and make their own technology decisions
    - Allows for a simpler upgrade path in the future
- Cons
  - Mulitple frameworks on one screen can crash devices
  - Can become very complex

## Tools and Frameworks

- Project Mosaic
  - www.mosaic9.org
  - Skipper / Inn Keeper
  - Tailer
  - Quilt - database for frontend pieces
  - Shaker - maintains consistent experience
- Module federation plugin
  - Par of webpack 5
  - Allows loading separately compiled and deployed code into applications
  - works for poth plugins and micro frontends
- Single SPA
  - Used to bring multiple frameworks together
  - Supports lazy loading of components
- EEV Event emitter for JS
  - Base application creates shared event listerner
  - micro-apps would publish events to this listener
- NGINX
  - Use nginx as a web server or reverse proxy to serve static content
  - Router apportpriate micro app based on path
  - Better when micro split is based on page / navigation
- iFrames
  - Better used when all functionality is kkon the same page
  - Communicate through the DOM
  - requires additional secruity to prevent iFrame jacking
- Custom orchestrator
  - you can write your own orchestrations tool to handle micro-frontend orchestration.

## Testing

- There is not a lot of difference betwen monolithic and micro
- Each application should still have its own unit test
- Functional testing for connections between apps should havppen in container componenet.
- Base tests should only cover what isn't tested already

## Error Handling

- Each micro is responsible is responsible for its own errors.
- A main point of micro to to prevent whole site from crashing becase of one micro.

## Auth

- In prod you normally servie all your appsp from the same origin
- This allows you to store the token.
- Apps cann access teh token in the browes window.localStorage

### Cookies

- You can store the token as a cookie
- With JWT you store the token in a cookie rather than the session id
- Sever read in the cookie and fetches the users session data

### URL Parmater

- Apps are usuallly run on multiple servers because the have different origins
- Add token as URL Param.

### Custom Library

- using custom library is a good way to provide auth
- Shared code can lead to breaking changes
