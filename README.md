# Router
React-router is not core react. &lt;Link> and &lt;NavLink> are used in place of &lt;a>, because they don't refresh the page and isActive class which show which tab is active.
React router can be written as:
const router=createBrowserRouter(
  createRoutesFromElements(
    <Route path="/" element={<Layout/>}>
      <Route path='' element={<Home/>}/>
      <Route path='about' element={<About/>}/>
      <Route path='contact' element={<Contact/>}/>
      <Route path='user/:userid' element={<User/>}/>
      <Route loader={githubInfoLoader} path='github' element={<Github/>}/>
 </Route>
  )
  Individual paths and elements are defined. For nesting <Route>....</Route> can be used.
