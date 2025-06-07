# store-x-selector

Minimalist fine-grained reactivity in React, with a selector-based store.

[Explainer post: Reactivity is easy](https://romgrk.com/posts/reactivity-is-easy/)

## Install

```
pnpm install store-x-selector
```

## Usage

```tsx
import {
  useSelector,
  createSelector,
  createSelectorMemoized,
  Store,
} from 'store-x-selector';

const selectors = {
  isFocus: createSelector((state, index) => state.focus === index),
};

const Context = createContext();
export function Grid() {
  const [store] = useState(() => new Store({ focus: 0 }));

  return (
    <Context.Provider value={store}>
      {Array.from({ length: 50 }).map((_, i) => (
        <Cell index={i} />
      ))}
    </Context.Provider>
  );
}

function Cell({ index }) {
  const store = useContext(Context);
  const focus = useSelector(store, selectors.isFocus, index);

  return (
    <button
      ref={ref}
      onClick={() => store.set('focus', index)}
      className={clsx({ focus })}
    >
      {index}
    </button>
  );
}
```
