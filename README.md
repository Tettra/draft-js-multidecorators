# draft-js-multidecorators


> Combine multiple Draft's decorators into one.

### Installation

```
$ yarn add Tettra/draft-js-multidecorators
```

### Usage

```js
import {EditorState, CompositeDecorator} from 'draft-js';
import MultiDecorator from 'draft-js-multidecorators';

var decorator = new MultiDecorator([
    new CompositeDecorator([
    {
        strategy: handleStrategy,
        component: HandleSpan,
    },

    // This decorator will have more priority:
    new CompositeDecorator([ ... ])
]);

var editorState = EditorState.createEmpty(decorator)
```

