# Regular Expressions

## HTML

### Replace `<em>Some text</em>` with `<span class="fst-italic">Some text</span>`

Used for updating tags (`<em>`, `<strong>`, etc.) in Twitter Bootstrap to classes.

| Find | Replace |
| ---- | ------- |
| `<em>([^(<em>)]*)</em>` | `<span class="fst-italic">$1</span>` |

### Replace `class="some-class h2 some-other-class"` with `class="some-class fs-2 some-other-class"`

Used for updating old class format for heading levels (1-5), represented as `h2` to new class name format of `fs-2` in Twitter Bootstrap to classes.

| Find | Replace |
| ---- | ------- |
| `class="([^h"]*)h([1-5])(.*)"` | `class="$1fs-$2$3"` |
