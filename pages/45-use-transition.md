---
layout: center
---

```ts {3|10-11|13-17}
import {
	startTransition, 
    useTransition,
} from 'react';

const Component = () => {
	
	const [state, setState] = useState()
  
	const [isPending, startTransition] = useTransition();

	const onClick = (newState) => {
		
		startTransition(() => {
			
			setState(newState);
		});
	}	
}
```
---
src: ./46-update.md
---
