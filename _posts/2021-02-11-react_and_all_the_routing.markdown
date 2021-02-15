---
layout: post
title:      "React and all the < Routing >"
date:       2021-02-11 20:45:44 -0500
permalink:  react_and_all_the_routing
---


As a newbie in the programming world, I am finishing up a very intense coding program with a challenge to create a single page program (SPA) with both a front and backend program utilizing React to handle the UI and Rails to handle all the database and computational aspects.

Learning about React and Redux was more trying for me  than the other languages before it.  It seemed that just as I was starting to get the hang of React, Redux came along and made it clear I was only seeing the tip of the iceberg!

Not surpisingly React is pretty fun. Watching the DOM change in real time is such a great tool when writing code.  Having just completed my JavaScript module, I quickly came to appreciate the JavaScript-like syntax of JSX and was already acustomed to how the code will flow.  Truth is React ended up being a little like a sweet-tart and I wasn't ready for the tart finish that was ahead.

Routing with React.  Here's the tart finish.  After working with Ruby and JavaScript for the past several months I became familiar with routing through models , views and .html files. Very quickly I was humbled when presented with a Browser Router, Fragment and Switch because it felt like a whole new language rather than a simple routing concept.  Because programming is so organic and unique from project to project, I am going to attemp to clear things up for myself and hopefully, clearly instruct on some of the how-to's of React routing. 

What is a < BrowserRouter>?  Since I am still learning I can only give my impression.  Routes are a curcial tool used to help navigate from page to page or rendered information to the next information. For example:  When you login to Facebook, you are asked to enter your username and profile. After submitting your info the page changes to display a welcome page. That is becasue it was "routed" to a welcome page. Now we can understand the importance as well as the simplicity of routing.  <BrowserRouter> is part of this process in React.  It uses the typical URL paths and is easily installed via the <create-react-app>.  First we need to make sure it is rendered at the root of an element chain. Here it is inside my Index.js


```ReactDOM.render( 
  <BrowserRouter>
    <App />
  </BrowserRouter>,
  document.getElementById('root')
);
```

At it's core, it is a tool to facilitate frontend or client side routing but it does need some configuration when installing. 

Next we have <Switch> which looks through the children or <Route> elements searching for URL matches. In this way it is finding a match and only renders the found match. It is suggested that more specific route paths be put ahead of less specific paths similiar to the example below I snipped from the reactrouter.com website

```function App() {
  return (
    <div>
      <Switch>
			
        {/* If the current URL is /about, this route is rendered
            while the rest are ignored */}
						
        <Route path="/about">
          <About />
        </Route>

        {/* Note how these two routes are ordered. The more specific
            path="/contact/:id" comes before path="/contact" so that
            route will render when viewing an individual contact */}
						
						
        <Route path="/contact/:id">
          <Contact />
        </Route>
        <Route path="/contact">
          <AllContacts />
        </Route>

        {/* If none of the previous routes render anything,
            this route acts as a fallback.

            Important: A route with path="/" will *always* match
            the URL because all URLs begin with a /. So that's
            why we put this one last of all */}
						
						
        <Route path="/">
          <Home />
        </Route>
      </Switch>
    </div>
  );
}```

As long as there is a match, there is routing going on.

Having said that it is important to undestand that when using <Route path> if you do not use <match> any path="/" will route since path="/" and path="/home" read the same.

If you want to change the route you need to use <Link>.  Link helps the user navigate through the application by rendering an anchor tag in the HTML doc.


````<Link to="/'>home</Link>```


Though different in the way it is executed compared to others, react routing can be an effective tool for accomplishing all your routing needs in regards to your SPA. 
