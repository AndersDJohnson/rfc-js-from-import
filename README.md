# rfc-js-from-import

A proposal for JavaScript to support inverted `import * from *` syntax as `from * import *`, so that autocompletion in editors works better since they will be able to suggest names of exported identifiers in the targeted module, which is known upfront.

```js
from 'my-module' import MyModule, { AnotherMethod }
from 'other-module' import { OtherMethod }

// ...
```

An editor could allow autocompletion after only:

```js
from 'my-module' import { ...
```

or:

```js
from 'my-module' import { O...
```
