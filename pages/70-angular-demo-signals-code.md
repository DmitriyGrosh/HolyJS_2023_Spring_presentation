---
layout: center
---

```ts {all|2|3|5-7|9-16}
export class SignalsSolutionComponent implements OnInit {
	public readonly name = signal(null);
	public message = computed(() => `Hello ${this.name()}!`);

	public readonly todos$ = toObservable(this.name)
      .pipe(
		    switchMap(() => this._longRequest$()),
      );

	private _longRequest$(): Observable<ITodo[]> {
		return this._http.get('https://jsonplaceholder.typicode.com/todos')
			.pipe(
				tap(() => sleep(1000)),
				map((todos) => todos),
			);
	}
	
}
```

---
src: ./71-preact.md
---
