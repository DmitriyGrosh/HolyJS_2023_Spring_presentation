---
layout: center
---

```ts {all|2|10|12|13|14|15|4-8}
export class BlockedComponent implements OnInit {
	public dataControl = new FormControl('');
	
	private _longRequest$ = of({})
      .pipe(
		      map(() => sleep(1000)),
		      map(() => []),
      );

	public ngOnInit(): void {
		this.dataOptions$ = this.dataControl.valueChanges
			      .pipe(
				        startWith(''),
                map((value) => this._filter(value)),
                switchMap(() => this._longRequest$),
			      );
	}
	
}
```

---
src: ./70-angular-demo-solution.md
---
