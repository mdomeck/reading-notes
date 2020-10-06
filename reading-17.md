## OAuth

Single Sign On with GitHub
- Create new project with web dependency
- Add a Home Page
  - index.htmp in a static folder
  - Add stylesheets and js links
  - add dependencies
- Securing the application with GitHub and Spring Security
  - Add new GitHub App
  - OAuth redirect URI is path in the application that the end users use-agent is redirected back to after they have authenticated with GitHub
  - replace `github-client-id` with client id and `github-client-secret`
  - uses authorization code grant to obtain an access token from GitHub
  - Home page link to login with GitHUb. the new link will be visible on home page and user can choose to login or to stay unaithenticated. Only when user clicked the link with the secure content be rendered

  Conditional Content on Home Page
  - option of server-side or client-side rendering
  - switch off the security on the home page by extending `WebSecurityConfigurerAdapter`

  Add a Logout Button
  - `logout()` function does a POST to `/logout` and then clears dynamic content.

  Adding an Error Page for Unauthenticated Users

  - detecting authentication failure in the client in index.html
  - configure `AuthenticationFailureHandler` to capture when authentication fails
  - generating a 401 in the server
  - 