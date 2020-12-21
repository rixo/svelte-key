# Deprecated

The key feature is now part of Svelte since v3.28.0 (see [issue](https://github.com/sveltejs/svelte/issues/1469#issuecomment-698955660)).

This package has consequently no reason to exist anymore and won't been maintained.

The new syntax is Svelte is the following:

~~~svelte
{#key expression}...{/key}
~~~

---

# svelte-key

Emulates React's `key` feature: force some content (e.g. some component) to be recreated when the value of the key changes.

This is based on the hack described in this [StackOverflow answer](https://stackoverflow.com/a/59047446/1387519) (or [this comment](https://github.com/sveltejs/svelte/issues/1469#issuecomment-491064651)).

This feature might make it into Svelte eventually. Progress can be tracked in [this issue](https://github.com/sveltejs/svelte/issues/1469).

## Installation

Npm:

```bash
npm install --dev svelte-key
```

Yarn:

```bash
yarn add --dev svelte-key
```

Note: the package only publishes the component as source, because it doesn't make sense to use this standalone, outside of another Svelte component (heck! you can't even pass slots to standalone components currently).

## Usage

[Example REPL](https://svelte.dev/repl/421369c3215d4cfe847f76f25adb6939?version=3.15.0)

```html
<script>
  import Identity from 'svelte-key'
  let i = 0
</script>

<p>Change input value & click button</p>

<Identity key={i}>
  <input />
</Identity>

<button on:click={() => {i++}}>
  {i}
</button>
```

## License

[WTFPL](http://wtfpl2.com)
