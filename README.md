# om-tut

A port of OM Tutorial from Light Table to any nrepl compliant editor/IDE.

## Usage

### Emacs/cider

* Clone the `om-tut` repo

```bash
git clone https://github.com/magomimmo/om-tut.git
```

* OPTIONAL: Launch the ClojureScript compilation in auto mode

```bash
cd om-tut
lein cljsbuild auto
Compiling ClojureScript.
Compiling "dev-resources/public/js/om_tut.js" from ("src/cljs" "test/cljs" "dev-resources/tools/repl")...
Successfully compiled "dev-resources/public/js/om_tut.js" in 20.222298 seconds.
```

* Open the `core.cljs` file in emacs an issue the `C-C M-j` command
  (or `M-x cider-jack-in`)

* Run the http-server from the nREPL

```clj
; CIDER 0.5.0alpha (package: 20131210.726) (Clojure 1.5.1, nREPL 0.2.3)
user> (run)
#<Server org.eclipse.jetty.server.Server@3a9bb797>
user>
```

* run the Browser Connected REPL (bREPL) from the nREPL

```clj
user> (browser-repl)
Browser-REPL ready @ http://localhost:56796/802/repl/start
Type `:cljs/quit` to stop the ClojureScript REPL
nil
cljs.user> 
```

* Activate the bREPL: visit the `http://localhost:3000` page

* Evaluate form by form the content of `core.cljs` by using the usual
  `C-c C-e` shortcut. It's important to start by evaluating the `ns`
  form.

* Live feedback in the browser

Change the value of the `:text` key in the `app-state` atom from
`"Hello World!" to something different.

Re-evaluate both the `app-state` form and the `om/root` form starting
from the first.

You should now see the browser being updated with the new value you
set to the `:text` key.



## License

Copyright © 2014 FIXME

Distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.
