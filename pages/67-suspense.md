---
layout: center
---

```tsx {all|5,9|6-8}
import { Suspense } from "react";

export const Hydrate = () => (
	<div>
		<Players/>
		<Suspense fallback={<Spinner />}>
			<Comments />
		</Suspense>
		<Statistics />
	</div>
);
;
```

---
src: ./68-others.md
---
