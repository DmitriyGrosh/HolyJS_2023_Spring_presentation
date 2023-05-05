---
layout: center
---

```ts {all|2|4|7|10|11-15|4|7|all}
export class BlockedComponent implements OnInit {
	public dataControl = new FormControl('');
	
	public todos$ = this.control.valueChanges
		.pipe(
			// map(() => []),
			switchMap((value) => this._longRequest$())
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
src: ./70-angular-demo-signals.md
---
