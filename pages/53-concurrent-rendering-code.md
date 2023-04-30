---
layout: center
transition: fade
---
```tsx {all|17|3-12|5-6|8-11|21}
export const ConcurrentRendering = () => {
	
	const handlePlayerClick = (player) => {
		
		// high priority (urgent update)
		setHighPriorityPlayer(player);

		// low priority (non-urgent update)
		startTransition(() => {
			setLowPriorityPlayer(player);
		});
	};
	
	return (
		<div>
          {playersArray.map((player) => (
                <button onClick={handlePlayerClick}>
                    {player.name}
                </button>		
          ))}
          <Statistics id={lowPriorityPlayer.id} />
        </div>
    );
};
```

---
src: ./54-concurrent-rendering-code.md
---
