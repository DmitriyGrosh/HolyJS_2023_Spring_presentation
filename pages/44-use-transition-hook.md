---
layout: center
---

```ts {all|2|13-17}
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
src: ./45-use-transition.md
---
