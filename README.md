# Module Federation - React Router DOM nested routers

This example shows how to handle independent and nested routings in a MFE setup based on [webpack-module-federation](https://github.com/module-federation). The setup consists of:

- `dashboard`, `auth`, and `shell`

- Apps using a ***browser history*** strategy *when acting as hosts* and an ***in-memory history*** strategy *when acting as remotes*.

- `shell`: host app based on a browser history strategy that handles high-level routing

- `shell` routing determines mounting/unmounting of `dashboard` and `auth` remotes.

The shell is the only component responsible for updating browser url. The two level of history strategies (browser + in-memory) are kept in sync through an event-based communication between shell and remotes.

<br>

# Running the demo

3. Postinstall: Check the gitmodules (submodule update if needed).
1. Install deps: `npm install`.
2. Start apps: `npm run start`.

Visit http://localhost:8080 to navigate `shell` app. `dashboard` and `auth` are also exposed as standalone apps at http://localhost:8081 and http://localhost:8082 respectively.

<br>

# Credits

The setup is inspired to https://github.com/StephenGrider/mfe and https://github.com/module-federation/module-federation-examples/tree/master/react-nested-routers.