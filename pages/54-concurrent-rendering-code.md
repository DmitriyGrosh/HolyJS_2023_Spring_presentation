---
layout: center
---
```tsx {all|1,4|16|6-16}
import { memo } from 'react';
import { sleep } from '../../lib/sleep';

const Statistics = memo(({ id }) => {
	
	useEffect(() => {
		const initData = async () => {
			const data = await getPlayerStatistics(id);
			
			setPlayerStatistics(data);
		};

		initData();
	}, [id]);

	sleep(1000);

	if (isLoading) {
		return <div>Loading Statistics...</div>
	}

	return (
      <div>...</div>
    );
}
```

---
src: ./55-concurrent-rendering-demo.md
---
