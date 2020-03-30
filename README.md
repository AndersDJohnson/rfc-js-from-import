# rfc-js-from-import

A proposal for JavaScript to support inverted `import * from *` syntax as `from * import *`, so that autocompletion in editors works better since they will be able to suggest names of exported identifiers in the targeted module, which would now be known upfront.

```js
from 'my-module' import MyModule, { AnotherMethod }
from 'other-module' import { OtherMethod }

// ...
```

or:

```js
import from 'my-module' MyModule, { AnotherMethod }
import from 'other-module' { OtherMethod }

// ...
```

or:

```js
import from 'my-module' as MyModule, { AnotherMethod }
import from 'other-module' as { OtherMethod }

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

## Related
* https://github.com/AndersDJohnson/rfc-js-import-multiple
* https://github.com/AndersDJohnson/rfc-js-import-infer-identifier
* https://github.com/AndersDJohnson/rfc-js-import-object-alignment

