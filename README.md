# Rails Lite
Rails isn't magic, but sometimes it feels like it. To get a better understanding of Rails' MVC web framework, I built a "lite" version of Rails from scratch.

Below are some noteworthy facets of this project:

* **WEBRick Server**: [server.rb](https://github.com/rrzein/RailsLite/blob/master/lib/server.rb)
   The server utilizes Ruby's WEBRick library to provide the interface for receiving HTTP requests and sending responses.

* **ControllerBase**: [controller_base.rb](https://github.com/rrzein/RailsLite/blob/master/lib/rails_lite/controller_base.rb)
  `ControllerBase` takes in `HTTPRequest` objects to fill out an `HTTPResponse` object. It sets the `content_type` and `body` of the response and returns the response with rendered content.

* **Session** [session.rb](https://github.com/rrzein/RailsLite/blob/master/lib/rails_lite/session.rb)
  `Session` allows us to set and store `HTTPCookie`s for the user's session.

* **Params** [params.rb](https://github.com/rrzein/RailsLite/blob/master/lib/rails_lite/params.rb)
  `Params` allows us to receive and parse params from either the router's match of the URL, the query string, or the request body.

* **Router** [router.rb](https://github.com/rrzein/RailsLite/blob/master/lib/rails_lite/router.rb)
  `Router` keeps track of multiple routes, including the matched URL patterns, the HTTP method (GET, POST, PUT, DELETE), the controller class the route maps to, and the action to be invoked.