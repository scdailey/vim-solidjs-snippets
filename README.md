# vim-solidjs-snippets
A port of the SolidJS Community VSCode snippets extension. Includes support for both JavaScript and Typescript.

## Installation
Use your favorite vim plugin manager to install UltiSnips and the SolidJS snippets. Below is an example in vim-plug.

```vim
call plug#begin('~/.vim/plugged')
Plug 'SirVer/ultisnips'
Plug 'scdailey/vim-solidjs-snippets'
call plug#end()
```

Once you have installed these you can load the snippets into a completion engine such as CoC.

## Snippets
Below you will find a table of the available snippets. This table has been pulled directly from the SolidJS Community plugin for VSCode.

<!-- ⛔️ GENERATE-SNIPPETS-TABLE:START — Do not remove or modify this section. -->

  <table>
    <thead>
      <tr>
        <th>Trigger</th>
        <th>Content</th>
        <th>Languages</th>
      </tr>
    </thead>
    <tbody><tr><td colspan="3"><h3>JSX</h3></td></tr>
      <tr>
        <td><code>sinput→</code></td>
        <td>Input two-way binding</td>
        <td><b>jsx, tsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx
<input type="${1:text}" value={${2:value}()} onInput={e => ${3:setValue}(e.currentTarget.value)}/>
```

</details></td></tr><tr><td colspan="3"><h3>Component</h3></td></tr>
      <tr>
        <td><code>scomp→</code></td>
        <td>Base for an empty solidJS component</td>
        <td><b>jsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx

 function ${1:${TM_FILENAME_BASE}}() {

  return (
    <div>${1:${TM_FILENAME_BASE}}</div>
  );
}
  export default ${1:${TM_FILENAME_BASE}};
```

</details></td></tr>
      <tr>
        <td><code>scomp→</code></td>
        <td>Solid empty function component</td>
        <td><b>tsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx
const ${1:${TM_FILENAME_BASE}}: Component<{$2}> = (props) => {
  $0
  return <div></div>;
};
```

</details></td></tr>
      <tr>
        <td><code>spcomp→</code></td>
        <td>Solid empty Parent Component</td>
        <td><b>tsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx
const ${1:${TM_FILENAME_BASE}}: ParentComponent<{$2}> = (props) => {
  $0
  return <div>{props.children}</div>;
};
```

</details></td></tr>
      <tr>
        <td><code>sfcomp→</code></td>
        <td>Solid empty Flow Component</td>
        <td><b>tsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx
const ${1:${TM_FILENAME_BASE}}: FlowComponent<{$2}, ${3:JSX.Element}> = (props) => {
  $0
  return <div>{props.children}</div>;
};
```

</details></td></tr>
      <tr>
        <td><code>svcomp→</code></td>
        <td>Solid empty Void Component</td>
        <td><b>tsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx
const ${1:${TM_FILENAME_BASE}}: VoidComponent<{$2}> = (props) => {
  $0
  return <div></div>;
};
```

</details></td></tr>
      <tr>
        <td><code>scompi→</code></td>
        <td>Solid empty function component. With Imports</td>
        <td><b>tsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx
import { Component } from "solid-js";

const ${1:${TM_FILENAME_BASE}}: Component<{$2}> = (props) => {
  $0
  return <div></div>;
};
```

</details></td></tr>
      <tr>
        <td><code>scompie→</code></td>
        <td>Solid empty function component. With Imports and default export</td>
        <td><b>tsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx
import { Component } from "solid-js";

const ${1:${TM_FILENAME_BASE}}: Component<{$2}> = (props) => {
  $0
  return <div></div>;
};

export default ${1:${TM_FILENAME_BASE}};
```

</details></td></tr>
      <tr>
        <td><code>spcompi→</code></td>
        <td>Solid empty Parent Component. With Imports</td>
        <td><b>tsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx
import { ParentComponent } from "solid-js";

const ${1:${TM_FILENAME_BASE}}: ParentComponent<{$2}> = (props) => {
  $0
  return <div>{props.children}</div>;
};
```

</details></td></tr>
      <tr>
        <td><code>sfcompi→</code></td>
        <td>Solid empty Flow Component. With Imports</td>
        <td><b>tsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx
import { FlowComponent, JSX } from "solid-js";

const ${1:${TM_FILENAME_BASE}}: FlowComponent<{$2}, ${3:JSX.Element}> = (props) => {
  $0
  return <div>{props.children}</div>;
};
```

</details></td></tr>
      <tr>
        <td><code>svcompi→</code></td>
        <td>Solid empty Void Component. With Imports</td>
        <td><b>tsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx
import { VoidComponent } from "solid-js";

const ${1:${TM_FILENAME_BASE}}: VoidComponent<{$2}> = (props) => {
  $0
  return <div></div>;
};
```

</details></td></tr>
      <tr>
        <td><code>shtmlcomp→</code></td>
        <td>Component extending an HTML Element</td>
        <td><b>tsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx
const ${1:${TM_FILENAME_BASE}}: ParentComponent<
  ComponentProps<"${2:div}"> & {
    $0
  }
> = (props) => {
  const [local, attrs] = splitProps(props, []);

  return <${2:div} {...attrs}>{props.children}</${2:div}>;
};
```

</details></td></tr>
      <tr>
        <td><code>shtmlcompi→</code></td>
        <td>Component extending an HTML Element. With Imports</td>
        <td><b>tsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx
import { ParentComponent, splitProps, ComponentProps } from "solid-js";

const ${1:${TM_FILENAME_BASE}}: ParentComponent<
  ComponentProps<"${2:div}"> & {
    $0
  }
> = (props) => {
  const [local, attrs] = splitProps(props, []);

  return <${2:div} {...attrs}>{props.children}</${2:div}>;
};
```

</details></td></tr><tr><td colspan="3"><h3>Context</h3></td></tr>
      <tr>
        <td><code>sctxp→</code></td>
        <td>Solid Context Provider component</td>
        <td><b>jsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx
import { createContext, createSignal, useContext } from "solid-js";

const ${TM_FILENAME_BASE/(.*?)\Context.*/${1:/capitalize}/i}Context = createContext();

export function ${TM_FILENAME_BASE/(.*?)\Context.*/${1:/capitalize}/i}Provider(props) {
  const [${TM_FILENAME_BASE/(.*?)\Context.*/${1:/downcase}/i}, set${TM_FILENAME_BASE/(.*?)\Context.*/${1:/capitalize}/i}] = createSignal(props.${TM_FILENAME_BASE/(.*?)\Context.*/${1:/downcase}/i} || ""),
    store = [${TM_FILENAME_BASE/(.*?)\Context.*/${1:/downcase}/i}, set${TM_FILENAME_BASE/(.*?)\Context.*/${1:/capitalize}/i}];

  return (
    <${TM_FILENAME_BASE/(.*?)\Context.*/${1:/capitalize}/i}Context.Provider value={store}>{props.children}</${TM_FILENAME_BASE/(.*?)\Context.*/${1:/capitalize}/i}Context.Provider>
  );
}

export function use${TM_FILENAME_BASE/(.*?)\Context.*/${1:/capitalize}/i}() {
  return useContext(${TM_FILENAME_BASE/(.*?)\Context.*/${1:/capitalize}/i}Context);
}
```

</details></td></tr>
      <tr>
        <td><code>sctxp→</code></td>
        <td>Solid Context Provider component</td>
        <td><b>tsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx
import { createContext, useContext, ParentComponent } from "solid-js";
import { createStore } from "solid-js/store";

const defaultState = {};

const ${1:Name}Context = createContext<[state: typeof defaultState, actions: {}]>([
  defaultState,
  {},
]);

export const ${1/(.*)/${1:/capitalize}/}Provider: ParentComponent = (props) => {
  const [state, setState] = createStore(defaultState);

  return (
    <${1/(.*)/${1:/capitalize}/}Context.Provider value={[state, {}]}>
      {props.children}
    </${1/(.*)/${1:/capitalize}/}Context.Provider>
  );
};

export const use${1/(.*)/${1:/capitalize}/} = () => useContext(${1/(.*)/${1:/capitalize}/}Context);

```

</details></td></tr><tr><td colspan="3"><h3>Reactivity</h3></td></tr>
      <tr>
        <td><code>ssig→</code></td>
        <td>Simple createSignal</td>
        <td><b>ts, tsx, js, jsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx
const [${1:state}, set${1/(.*)/${1:/capitalize}/}] = createSignal(${2});
```

</details></td></tr>
      <tr>
        <td><code>seff→</code></td>
        <td>Simple createEffect</td>
        <td><b>ts, tsx, js, jsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx
createEffect(() => {
  const value = ${1:source}();
  $0
});
```

</details></td></tr>
      <tr>
        <td><code>seffon→</code></td>
        <td>createEffect with explicit sources</td>
        <td><b>ts, tsx, js, jsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx
createEffect(on(${1: source}, (value, prev) => {
  $0
}));
```

</details></td></tr>
      <tr>
        <td><code>smemo→</code></td>
        <td>Simple createMemo</td>
        <td><b>ts, tsx, js, jsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx
const ${1:value} = createMemo(() => $0);
```

</details></td></tr>
      <tr>
        <td><code>smemoon→</code></td>
        <td>createMemo with explicit sources</td>
        <td><b>ts, tsx, js, jsx</b></td>
      </tr>
      <tr><td colspan="3"><details>
      <summary><sup>Toggle Code Snippet</sup></summary>

```tsx
const ${1:value} = createMemo(on(${2:value}, (value, prev) => $0));
```

</details></td></tr></tbody></table>

<!-- ⛔️ GENERATE-SNIPPETS-TABLE:END — Do not remove or modify this section. -->
