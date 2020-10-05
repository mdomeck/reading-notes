## Spring Security overview
#### Authentication (who you are)
 - interface `AuthenticationManager` can
 1. `authenticate()` method
1. return `Authentication`
1. throw `AuthenticationException`: UI will render a page authentication failed and backend HTTP will send 401 response with or without `WWW=Authenticate`

-inplementation  of   `AuthenticationManager` is `ProviderManager` which delegates to a chain of `AuthenticationProvider` instances. 
- `ProviderProvider` has an extra method to allow caller to query if it supports a given `Authentication` type.
- `Class<?>` argument in the `supports()` method is really `Class<? extends Authentication>`
- `ProviderManager` has an optional parent which can consult if all return null. 

#### Authorization/Access Control (what your allowed to do)

- `AccessDecisionManager` has 3 implementations
  - `AccessDecisionVoter` considers `Authentication` and `Object` which has been decorated with `ConfigAttributes`
  - `AccessDecisionVoter` represents anything a user might want to access.


## Spring Auth cheat sheet
Step 1: set up a user model and repo

Step 2: create a controller for that model

Step 3: UserDetailsServiceImpl implements UserDetailsService
gets a User from the database by username (make sure your repository has the method to make this easy!)

Step 4: ApplicationUser implements UserDetails
use IntelliJ to implement the methods; make the boolean ones all return true

Step 5: WebSecurityConfig extends WebSecurityConfigurerAdapter
- has a UserDetailsService
- passwordEncoder bean
- configure AuthManagerBuilder
  - auth.userDetailsService(userDetailsService).passwordEncoder(passwordEncoder());
- configure HttpSecurity
  - cors? csrf?
  - matchers for URLs that are allowed
    - ensure that login and signup URLs allowed; also consider homepage etc.
  - formLogin with login page set up
  - logout

    @Override
    @Bean
    public AuthenticationManager authenticationManagerBean() throws Exception {
        return super.authenticationManagerBean();
    }

Step 6: registration page
- create it w/ form
- ensure it posts to a route your controller is ready for
- check it's saving in the DB

    // maybe autologin?
    Authentication authentication = new UsernamePasswordAuthenticationToken(newUser, null, new ArrayList<>());
    SecurityContextHolder.getContext().setAuthentication(authentication);

Step 7: login page
- create it w/ form
- ensure it posts to the route you specified in web config
- try it out!
- add to a template w/ things about the Principal