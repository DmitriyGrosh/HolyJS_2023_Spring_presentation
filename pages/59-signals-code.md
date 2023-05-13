---
layout: center
transition: fade
---
```tsx {all|1-4|6-9|10-17}
// react
const [state, setState] = useState(0);
// state -> value
// setState -> setter

// solidJs
const [signal, setSignal] = createSignal(0);
// signal -> getter
// setSignal -> setter

// preact
import { signal } from "@preact/signals-core";

const counter = signal(0);

// counter.value -> get value
// counter.value = 1 -> set value
```

---
src: ./61-diffirence.md
---
