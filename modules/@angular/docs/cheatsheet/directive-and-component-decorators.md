@cheatsheetSection
Class field decorators for directives and components
@cheatsheetIndex 8
@description
{@target ts}`import { Input, ... } from '@angular/core';`{@endtarget}
{@target js}Available from the `ng.core` namespace{@endtarget}

@cheatsheetItem
syntax(ts):
`@Input() myProperty;`|`@Input()`
syntax(js):
`ng.core.Input(myProperty, myComponent);`|`ng.core.Input(`|`);`
description:
Declares an input property that you can update via property binding (for example,
`<my-cmp [myProperty]="someExpression">`).


@cheatsheetItem
syntax(ts):
`@Output() myEvent = new EventEmitter();`|`@Output()`
syntax(js):
`myEvent = new ng.core.EventEmitter(); ng.core.Output(myEvent, myComponent);`|`ng.core.Output(`|`);`
description:
Declares an output property that fires events that you can subscribe to with an event binding (for example, `<my-cmp (myEvent)="doSomething()">`).


@cheatsheetItem
syntax(ts):
`@HostBinding('[class.valid]') isValid;`|`@HostBinding('[class.valid]')`
syntax(js):
`ng.core.HostBinding('[class.valid]', 'isValid', myComponent);`|`ng.core.HostBinding('[class.valid]', 'isValid'`|`);`
description:
Binds a host element property (for example, CSS class valid) to directive/component property (for example, isValid).


@cheatsheetItem
syntax(ts):
`@HostListener('click', ['$event']) onClick(e) {...}`|`@HostListener('click', ['$event'])`
syntax(js):
`ng.core.HostListener('click', ['$event'], onClick(e) {...}, myComponent);`|`ng.core.HostListener('click', ['$event'], onClick(e)`|`);`
description:
Subscribes to a host element event (for example, click) with a directive/component method (for example, onClick), optionally passing an argument ($event).


@cheatsheetItem
syntax(ts):
`@ContentChild(myPredicate) myChildComponent;`|`@ContentChild(myPredicate)`
syntax(js):
`ng.core.ContentChild(myPredicate, 'myChildComponent', myComponent);`|`ng.core.ContentChild(myPredicate,`|`);`
description:
Binds the first result of the component content query (myPredicate) to the myChildComponent property of the class.


@cheatsheetItem
syntax(ts):
`@ContentChildren(myPredicate) myChildComponents;`|`@ContentChildren(myPredicate)`
syntax(js):
`ng.core.ContentChildren(myPredicate, 'myChildComponents', myComponent);`|`ng.core.ContentChildren(myPredicate,`|`);`
description:
Binds the results of the component content query (myPredicate) to the myChildComponents property of the class.


@cheatsheetItem
syntax(ts):
`@ViewChild(myPredicate) myChildComponent;`|`@ViewChild(myPredicate)`
syntax(js):
`ng.core.ViewChild(myPredicate, 'myChildComponent', myComponent);`|`ng.core.ViewChild(myPredicate,`|`);`
description:
Binds the first result of the component view query (myPredicate) to the myChildComponent property of the class. Not available for directives.


@cheatsheetItem
syntax(ts):
`@ViewChildren(myPredicate) myChildComponents;`|`@ViewChildren(myPredicate)`
syntax(js):
`ng.core.ViewChildren(myPredicate, 'myChildComponents', myComponent);`|`ng.core.ViewChildren(myPredicate,`|`);`
description:
Binds the results of the component view query (myPredicate) to the myChildComponents property of the class. Not available for directives.
