# go.ani.sh

Static golinks. `go.ani.sh/foo` → redirect target from `links.json`.

Add a link: edit `links.json`, commit, push.

A value can be a string (single redirect) or an array of strings (multilink —
the 404 page renders a list with an "Open all" button).

## How it works

GitHub Pages serves `404.html` for any unknown path. That page reads the slug
from `location.pathname`, fetches `links.json`, and `location.replace`s to the
target. `index.html` is a filterable list.
