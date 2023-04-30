---
layout: center
---

```tsx {all|3|3|13|2|5-8|9-12|all}
export const Update = () => {
	const [count, setCount] = useState(0);
	const render = useRef(0);

	const handleIncrement = () => {
		setCount((prev) => prev + 1)
	};
	
	const handleSame = () => {
		setCount(count);
	};

	render.current += 1;

	return (
		<div>
          <p>Counter {count}</p>
          <button onClick={handleIncrement}>Handle increment</button>
          <button onClick={handleSame}>Handle same</button>
          <p>Rerender Update {render.current}</p>
		</div>
    );
};
```

---
src: ./48-update-demo.md
---
