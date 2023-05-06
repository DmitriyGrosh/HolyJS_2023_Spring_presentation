---
layout: center
---

```tsx {all|1-3|13|6-10}
import { signal } from '@preact/signals';

export const input = signal('');

export const Autocomplete = () => {
	const onInput = (event) => {
		const { value } = event.target;
		
		input.value = value;
	};
	
	return (
		<input value={input.value} onInput={onInput} />
    );
}
```

---
src: ./74.preact.md
---
