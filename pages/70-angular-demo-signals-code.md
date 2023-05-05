---
layout: center
---

```ts {all|2|4-6|8-15}
export class BlockedComponent implements OnInit {
	public readonly name = signal('');

	public todos$ = toObservable(this.name).pipe(
		switchMap((value: string) => this._longRequest$(value))
	);

	private _longRequest$(): Observable<any> {
		return this._http.get('https://jsonplaceholder.typicode.com/todos')
			.pipe(
				tap((items) => sleep(1000)),
				map((todos) => todos),
			);
	}
	
}
```

---
---
