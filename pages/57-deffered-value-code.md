---
layout: center
---

```tsx {all|3|5-6|8-14|22}
export const ConcurrentRendering = () => {
	
	const [highPriorityPlayer, setHighPriorityPlayer] = useState(null);
	
	// low priority (non-urgent update)
	const lowPriorityPlayer = useDeferredValue(highPriorityPlayer);
	
	const handlePlayerClick = (player) => {
		
		// high priority (urgent update)
		setHighPriorityPlayer(player);
		
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
src: ./58-deferred-value-code.md
---
