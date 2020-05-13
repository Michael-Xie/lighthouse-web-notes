# Angular

## CLI

`ng new <name of app>` : creates app
`ng serve --open` : runs server and open app in browser
`ng generate component <dest folder>`: create component in destination folder(can create if not exist)
`ng g s <dest folder>: create service

## State Management
- larger app can use `ngrx` and `redux`

## Directives
- in html file 
```
<ul *ngFor="let todo of todos">
  <li>{{ todo.title }}</li>
</ul>
```
## Other
- pipes (|) which allows previous output to be fed as input to current function (ie. `uppercase`)
- `ngOnInit()` is similar to other frontend framework like React that uses the life cycle method
- when accessing something above, need to use Emitter

# Typescript

## Decorator
- meta-data for component 

## Other
<var name> : <variable type> = <var value>;

