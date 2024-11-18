![Bonzai](https://github.com/bonzai-lang/bonzai/blob/main/assets/banner.png?raw=true)

# The Bonzai Programming Language

Bonzai is a programming language that relies on [Actor model](https://en.wikipedia.org/wiki/Actor_model), [Reactive programming](https://en.wikipedia.org/wiki/Reactive_programming) and on a strong and non-taulerant typechecker to guarantee types and computations in your code. It compiles down to a custom bytecode with relatively good performance.

### HTTP Server example

```v
require "std:http"
require "std:natives"

let port = 8000
let server = spawn HTTPServer(port)

server->listen(fn(req) => {
  req.respondText("text/html", "<h1>Hello, world!</h1>")
})

print("Server running on port $port")
```
