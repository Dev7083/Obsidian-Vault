
---

## 1. CLI Commands & Structure

**What it is:** Tools to create, build, and serve Angular apps. 
**CLI Command (Run App):** `ng serve --open`

**Other Key setup commands:**
```bash
npm install -g @angular/cli@16.2.6  # Install Angular CLI
ng new my-app                       # Create a new app
```
**Angular 16 Focus:** Standalone components reduce boilerplate (no `app.module.ts` needed). You use `app.config.ts` and `app.routes.ts` instead.

### File & Folder Structure
```bash
my-app/
├── node_modules/         # Installed dependencies
├── src/                  
│   ├── app/              # Main application code (Components, Services)
│   ├── assets/           # Static files like images and fonts
│   ├── environments/     # Configs for dev/prod builds
│   ├── index.html        # Main HTML file
│   ├── main.ts           # Application entry point
│   └── styles.css        # Global CSS
├── angular.json          # Angular CLI configuration
└── package.json          # Project dependencies
```

---

## 2. Components

**What it is:** The basic UI building block. It pairs a TypeScript class with an HTML template.
**CLI Command:** `ng generate component <name>` or `ng g c <name>`
**Code Example:**
```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-hello',
  standalone: true, // Angular 16 feature
  template: `<h1>Hello, {{ name }}!</h1>`,
  styles: [`h1 { color: blue; }`]
})
export class HelloComponent {
  name = 'Angular';
}
```

### Lifecycle Hooks
Components have lifecycle events (like when they are created or destroyed). `ngOnInit` is the most common, running once after data-bound properties are initialized.
```typescript
import { Component, OnInit } from '@angular/core';

export class MyComponent implements OnInit {
  ngOnInit() {
    console.log('Component has loaded!');
  }
}
```

---

## 3. Data Binding

**What it is:** Moving data between the TypeScript class and the HTML view.
### Types of Data Binding:
- **Interpolation / One-way:** `{{ value }}` (Class to View)
- **Attribute / Property Binding:** `[property]="value"` (Class to View)
- **Class / Style Binding:** `[class.active]="isActive"` or `[style.color]="'red'"`
- **Event Binding:** `(event)="method()"` (View to Class)
- **Two-Way Binding:** `[(ngModel)]="value"` (Syncs both ways, needs `FormsModule`)

**Code Example:**
```html
<!-- Interpolation -->
<p>User: {{ username }}</p>

<!-- Property Binding -->
<button [disabled]="isSaving">Save</button>

<!-- Style Binding -->
<p [style.color]="'red'">Error Text</p>

<!-- Two-Way Binding -->
<input [(ngModel)]="username" placeholder="Enter name">
```

---

## 4. Event Binding

**What it is:** Listening to user actions like clicks, keypresses, and mouse movements.
**Code Example:**
```html
<button (click)="submitData()">Click Me!</button>

<!-- Passing the event object to get input value -->
<input (keyup)="onTyping($event)">
```
```typescript
submitData() {
  alert('Button clicked!');
}

onTyping(event: any) {
  console.log(event.target.value);
}
```

---

## 5. Directives

**What they are:** Classes that reshape the DOM or change element styles.
- **Structural:** Alter the layout (`*ngIf`, `*ngFor`, `[ngSwitch]`).
- **Attribute:** Alter the appearance/behavior (`ngClass`, `ngStyle`, `ngModel`).

**Code Example:**
```html
<!-- Structural Directive: *ngIf -->
<p *ngIf="isLoggedIn">Welcome Back!</p>

<!-- Structural Directive: *ngFor -->
<ul>
  <li *ngFor="let item of items; let i = index">{{ i }}: {{ item }}</li>
</ul>

<!-- Switch Cases -->
<div [ngSwitch]="grade">
  <p *ngSwitchCase="'A'">Excellent</p>
  <p *ngSwitchDefault>Unknown</p>
</div>

<!-- Attribute Directive: [ngClass] -->
<div [ngClass]="{'active': isActive, 'disabled': !isActive}">Status</div>
```

---

## 6. Services & Dependency Injection

**What it is:** Classes used to share data or logic across multiple components. "Dependency Injection" (DI) is how Angular provides the service to your components.
**CLI Command:** `ng generate service <name>` or `ng g s <name>`
**Code Example:**
```typescript
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root' // Automatically available everywhere
})
export class DataService {
  getData() { return ['A', 'B', 'C']; }
}
```
**Injecting into a Component:**
```typescript
export class MyComponent {
  // Dependency Injection occurs in the constructor
  constructor(private dataService: DataService) {
    console.log(this.dataService.getData());
  }
}
```

### Observables
Services often use `Observable` to handle multiple, asynchronous data streams over time. Components `.subscribe()` to them to receive updates.
```typescript
import { Observable, of } from 'rxjs';

getObservableData(): Observable<string> {
  return of('Data loaded asynchronously');
}

// In component:
this.myService.getObservableData().subscribe((data) => console.log(data));
```

---

## 7. HttpClient

**What it is:** Angular's tool for making API calls (GET, POST, etc.).
**Code Example:**
```typescript
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';

export class ApiService {
  constructor(private http: HttpClient) {}

  fetchUsers(): Observable<any[]> {
    return this.http.get<any[]>('https://jsonplaceholder.typicode.com/users');
  }
}
```

---

## 8. Pipes

**What they are:** Tools to format data directly inside the HTML template (e.g., dates, currency, uppercase).
**CLI Command:** `ng generate pipe <name>` or `ng g p <name>`
**Code Example:**
```html
<!-- Transforms text to uppercase -->
<p>Name: {{ 'john' | uppercase }}</p>

<!-- Formats a date -->
<p>Today is: {{ todayDate | date:'short' }}</p>

<!-- Formats currency -->
<p>Price: {{ 50 | currency:'USD' }}</p>
```

---

## 9. Forms

**What they are:** Tools to capture user input. Angular has two types: Template-driven (simple, HTML-heavy) and Reactive (complex, logic-heavy).

**Template-Driven Example:**
```html
<!-- Uses FormsModule -->
<form #myForm="ngForm" (ngSubmit)="save(myForm.value)">
  <input name="email" ngModel required>
  <button type="submit">Submit</button>
</form>
```

**Reactive Form Example:**
```typescript
// Uses ReactiveFormsModule
import { FormBuilder, Validators } from '@angular/forms';

export class MyForm {
  form = this.fb.group({
    email: ['', Validators.required]
  });
  
  constructor(private fb: FormBuilder) {}
}
```

---

## 10. Routing

**What it is:** Navigating between different pages (components) without reloading the browser.
**Code Example:**
```typescript
// app.routes.ts
export const routes = [
  { path: 'home', component: HomeComponent },
  { path: 'about', component: AboutComponent },
  { path: '', redirectTo: 'home', pathMatch: 'full' }
];
```
```html
<!-- Navigation Links -->
<a routerLink="/home">Home</a>
<a routerLink="/about">About</a>

<!-- Where the component displays -->
<router-outlet></router-outlet>
```

---

## 11. Unit Testing

**What it is:** Checking if individual chunks of code work correctly using Karma and Jasmine.
**CLI Command (Run Tests):** `ng test`
**Code Example:**
```typescript
import { TestBed } from '@angular/core/testing';
import { MyComponent } from './my.component';

describe('MyComponent', () => {
  it('should create the app', () => {
    const fixture = TestBed.createComponent(MyComponent);
    const app = fixture.componentInstance;
    expect(app).toBeTruthy(); // Verifies creation
  });
});
```
