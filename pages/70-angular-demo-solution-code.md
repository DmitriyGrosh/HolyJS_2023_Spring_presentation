---
layout: center
---

```ts {all|2|4|7|10|11-15|4|7|all}
export class RxJsSolutionComponent implements OnInit {
	public dataControl = new FormControl(null);
	
	public todos$ = this.control.valueChanges
		.pipe(
			// map(() => []),
			switchMap(() => this._longRequest$())
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
src: ./70-angular-demo-signals.md
---
