---
layout: center

css: unocss
---

<style>
.slidev-code {
    --slidev-code-padding: 12px;
    --slidev-code-font-size: 14px;
    --slidev-code-line-height: 20px;
}
</style>

```tsx
const [selectedPlayer, setSelectedPlayer] = useState<IPlayer | null>(null);

const handlePlayerClick = (player: IPlayer) => {
	
	setTimeout(() => {
		
		setSelectedPlayer(player);
		
	}, 0);
};
```

---
src: ./30-fiber.md
---
