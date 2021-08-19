<h1>COURSE CONTENT</h1>

[<h2>1.1 Course Description</h2>](#one)

<li>1.2 Why learn Django?</li>

[<h2>2 Django Course Content</h2>](#two)




<a name="one"><h2>1.1 Course Description</h2></a><br>
Angular is developed by google. Angular is new, angularjs is old. Open source web application framework led by the angular team at google. Mostly ppl use npm not the cdn like in jquery. documentation : https://angular.io/tutorial <br>

Advantages of Angular<br> 
1)We can create single page application

<h3>1.2 INTRODUCTION</h3>
<b>Installation</b><br>
We need node js for installation of angular.<br>

<b>To check the version of node and npm</b><br>
In folder shift+open power shell and use commands:<br>
>node --version<br>
>npn --version<br>

<b>Angular CLI</b><br>
The Angular CLI is a command-line interface tool that you use to initialize, develop, scaffold, and maintain Angular applications directly from a command shell.<br>
Download and install CLI using the commands given in here https://angular.io/cli <br>
Insatlling: >npm install -g @angular/cli<br>
Check the version: >ng version<br>
If the powershell asking for policy the use:<br>
Change the execution policy:<br>
>Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser<br>

Removing the execution policy:<br>
>Set-ExecutionPolicy -ExecutionPolicy Undefined -Scope CurrentUser<br>

<h3>1.3 Creating New Project</h3>
<b>Creating a new project</b>
>ng new project_name
If we want to use routing as well them press y, same for css<br>
Now it'll install the base files<br>

In all the folders we'll 90% work on src cuz that will convert our angular source code. index.html is the entry point

To run the project on browser we use:<br>
>ng server

<h3>1.4 Files/Folders in Apps explain?</h3>
<pre>
FILES
1)package.json:
the first file which is created, it contain the ng commands etc.
if we want to add example a google map then we add it inside the defDepedencies.

2)node_modules:
all the depedencies and dev-dependencies which are present in package.json are installed inside the node_module.

3)index.html:
Entry point for html, this will load first.

4)main.js:
javascript's first file which loads first.

5)style.css
If we want to do some global styling, we do inside this.

FOLDERS
1)src:
90% of code we'll do inside this one.

2)app: this is the root module, which can contains module or component:
component vs module?

component: is a small functionality which will have only one component.
module: is  a big functionality example user, so it'll have user login, sign up etc. 

3)app-routing.module.js:
this is basically used for urls like we use urls.py in django.

FILES ADVANCE:
1)editorconfig: it basically contains the settings of editor like vscode etc.
2)karma.config: used for unit testing
3)package.lock.json: it keeps log files of package.json, example we have animation, so all 4)the verstions, packages intsalled which stored in package.lock.json.
5)tslink: tells us about where to use let, const, var, arrow function etc.
6)typescript files:
i)tsconfig.spec.json: for testing configuration
ii)tsconfig.base.json: contains the code suggestion like we get indentations in code editor etc
iii)tsconfig.app.json: contains configuration file of our app.
7)e2e folder: end to end testing, used for testing.
</pre>

<h3>Adding bootstrap</h3>
<pre>
Step 1:
Installing bootstrap using npm:
>npm install bootstrap
when we hit enter bootstrap will be added into the app.component.html and package.json too

Installing jquery too:
>npm install jquery

Step 2:
include both in angular.json
inside the build-> styles: 
"styles": [
              "src/styles.css",
              "./node_modules/bootstrap/dist/css/bootstrap.min.css"        #added by me for bootstrap      
            ],
          "scripts": ["./node_modules/bootstrap/dist/js/bootstrap.js",
                        "./node_modules/jquery/dist/jquery.js"]
                    },
 
We included jquery and bootstrap both
          
Step 3: 
NOTE: Whenever we does some changes we must restart ng serve
</pre>

<h3>Angular Bootstrap</h3>
We have angular bootstrap website (https://ng-bootstrap.github.io/#/home).<br>
There is also steps to insall it, We just have to use one command givenon the home page of the website and no need to add any module etc after executing the command start using the components given in angular bootstrap. The first command is for angular 9 and latest, if we want to use old one then there is another command is given.<br>

<h3>Adding Material UI</h3>
https://material.angular.io/guide/getting-started<br>
All material + commands given in doc.<br>

<h3>Components</h3>
<b>Understanding the first component which we get after app creation</b><br>
<li>We use components for specific task for example login component, sign up component etc.</li>
<li>Reusable, for eg i have used navigation bar which is comon in every page, i can reuse this component in every page, like a function.</li>
<li>It has 4 files. We'll get this 4 files for every component for root as well as newly created</li>
<li>app is also a component, which is root component for our application. Every new component will get added in this component only.</li>
app.component.html: will have html<br>
app.component.css: will have styling for app.component.html page<br>
app.component.ts: how the module work will come here.<br>
app.component.spec.ts: usefull for testing purpose.<br>
app.module.ts: entry point<br>

<b>Adding new component</b><br>
<b>Creating the component:</b><br>
>ng generate component AllComponents/blog<br>
AllComponent is the name of the folder for all the newly created component for my understanding, i can direcly use ng generate component blog this will create all files inside app root.<br>
<b>Using this component:</b><br>
1)If i want to add the newly created component inside the root app.component.html then see the component's .ts file, for the above component it is "app-blog" use this as a tag inside the app.component.html whereever we want "<app-blog></app-blog>".<br>
Whatever we make changes in component's html will reflect in main root's html file.<br>
2)Right after creating the component the main root's app.module.ts will automatocally import component and declare in app.module.ts<br>
  
The <app-root></app-root> in index.html will bring contents of app.component.html, app.component.html will contains the html of all component, it'll merge them and make one page.<br>

copy the selector tag and paste it in app/app.component.html not on component's html page.<br>
  
<h1>Angular Interpolation</h1>
<li>If we want to take something from app.component.ts to app.component.html</li>
<li>We cannot use let, var with variable name</li>
<li>It is like a context we use in django. And this is called as interpolation.</li>
<li>To use function we just use funstion name as:</li>
<pre>
if we want the title we can use {{}} to print which is coming from app.component.ts

1)for variable we use {{}}
example:
.ts file
export class AppComponent {
  title = 'blog';
  fav_color = "blue";         #added by me
}

.html
&lt;h1&gt;{{fav_color}}&lt;/h1&gt;

2)for function
test()        //no function keyword or it'll give error
{

}
example:
getName{
  return "Fareen A"       //OR this.name for if variable is declare above the function
}

.html
&lt;h1&gt;{{getName()}}&lt;/h1&gt;

3)for object
stu={
  name:"sam",
  age:20
}

.html
&lt;h1&gt;{{stu.name}}&lt;/h1&gt;
&lt;h1&gt;{{stu.age}}&lt;/h1&gt;

4)for array
arr=['pink','blue','red']

.html
&lt;h1&gt;{{arr}}&lt;/h1&gt;        //will return the array 
&lt;h1&gt;{{arr[0]}}&lt;/h1&gt;    //will return the first object
&lt;h1&gt;{{arr.length}}&lt;/h1&gt; 

5)for arithmetic operation
.ts file
a=10
b=10

.html
&lt;h1&gt;{{a+b}}&lt;/h1&gt;
&lt;h1&gt;{{10+10}}&lt;/h1&gt;

6)for getting windows property
.ts file
siteURL = window.location.href

.html
&lt;h1&gt;{{siteURL}}&lt;/h1&gt;

7)invalid stuff
.html
&lt;h1&gt;{{x=10}}&lt;/h1&gt;
&lt;h1&gt;{{window.location.href}}&lt;/h1&gt;
</pre>

<h1>Module</h1>
  
![module](https://user-images.githubusercontent.com/59610617/129734692-ebc2f3ca-4039-4516-be26-8b41440ece45.png)<br>

Module is the collection of components, services,pips, and directives, example a user module will contain user sign up, user profile, all the stuff related to user will come under one user module.<br>

<b>To create module</b><br>
>ng generate module module_name
Eg: >ng generate module users

<b>Creating component inside the module users</b>
>ng generate component users/login          //if we don't use users/ it will by default create module inside the app folder.<br>

<b>Using module's component</b><br>
<pre>
Step 1:
Whatever we want to use we should export it inside the users.module.ts 
Below the imports write:
imports: [
    CommonModule
  ],
  exports:[             //added by me
    LoginComponent
  ]
  
Step 2:
inside the root's app-> app.module.ts file
import and include inside the import

import { UsersModule  } from './users/users.module';

imports: [
    BrowserModule,
    AppRoutingModule,
    UsersModule               //added by me
  ],
  
To use it inside the root's module html
use the selector given component's .ts file
for my app it is "app-login"

.html of root's:
&lt;app-login&gt;&lt;/app-login&gt;

Now whatever is present inside the users/login component will come in html file

Step 3: create signup module 
now once we imported it non need to do it again, just export this inside the component's users.module.ts file
exports:[
    LoginComponent,
    SignupComponent         //added by me
  ]
  
</pre>

<h3>How to call a function onclick of the function</h3>  
When we create a button both the file(app.component.html(which will have button) and app.component.ts(which will have function)) should present inside the same component.<br>
<pre>
1)without parameter
.ts file:
getName(){
    alert('welcome Fareen');
  }
 
.html
&lt;button (click)="getName()"&gt;My name&lt;/button&gt;

2)with parameter
getName(x : any){
    alert(name);
  }
 
.html
&lt;button (click)="getName('annu')"&gt;My name&lt;/button&gt;
</pre>

<h3>Events</h3>
1)keyup event<br>
<pre>
.ts file
getName(x : any)
  {
    console.log(x);
  }
  
.html file
&lt;input type="text" (keyup)="getName('keyup event')"&gt;

Example 2:
based on id it'll print new value:
&lt;input type="text" #box (keyup)="getName(box.value)"&gt;

Example 3:
on enter this event will fire
&lt;input type="text" (keyup.enter)="getName('keyup event')"&gt;

Example 4:
fire when press the space
&lt;input type="text" (keyup.space)="getName('keyup event')"&gt;

</pre>

2)keydown<br>
Same like keyup<br>
  
3)blur<br> 
<pre>
when we click outside of the inbut box this event will fire
</pre>
  
4)mouseover and mouseleave<br>
<pre>
mouse over
&lt;div (mouseover)="getName('mouse over')" style="background-color:blue;"&gt;
Mouse over
&lt;/div&gt;

mouseleave
&lt;div (mouseleave)="getName('mouse leave')" style="background-color:blue;"&gt;
Mouse leave
&lt;/div&gt;

Both together
&lt;div (mouseover)="getName('mouse over')" (mouseleave)="getName('mouse leave')" style="background-color:blue;"&gt;
Mouse over/leave
&lt;/div&gt;
</pre>
  
<h3>Get textbox value</h3>
<pre>
get the value on console:
&lt;input type="text" (keyup)="getName($any($event).target.value)"&gt;

printing this value using the interpolation:
.ts:
curval=""
  getName(x : any)
  {
    console.log(x);
    this.curval = x
  }
  
.html
&lt;input type="text" (keyup)="getName($any($event).target.value)"&gt;
&lt;h1&gt;{{curval}}&lt;/h1&gt;

Get value on click of button
.ts will be same 

.html
&lt;input type="text" #box&gt;
&lt;button (click)="getName(box.value)"&gt;Get value&lt;/button&gt;
&lt;h1&gt;{{curval}}&lt;/h1&gt;
</pre>
  
<h3>Property binding</h3>
property binding and interpolation is not same. It is used using [] and interpolation with {{}}<br>
Example: 
<pre>
property binding can handle the disable button whereas interplation cannot.

.ts
export class AppComponent {
  title = 'blog';
  name="fareen";
  disabledbox=true;
  enable()
  {
    this.disabledbox = false;
  }
}

.html
&lt;input type="text" [disabled]="disabledbox" [value]="name"&gt; &lt;br&gt;
&lt;input type="text" disabled={{disabledbox}} value={{name}}&gt; &lt;br&gt;
&lt;button (click)="enable()"&gt;Enable&lt;/button&gt;
</pre>
 
<h3>Condition statements in angular</h3>  
if condition
<pre>
example: hide the tag if the condition is false:

.ts
show = true;

.html
&lt;h1 *ngIf = "show"&gt;
Will visible is true
&lt;/h1&gt;
</pre>

if else
<pre>
.ts will be same

.html
&lt;h1 *ngIf = "show else elseBlock"&gt;
    if block
&lt;/h1&gt;
&lt;ng-template #elseBlock&gt;
  &lt;h1&gt;else block&lt;/h1&gt;
&lt;/ng-template&gt;
</pre>

if block with string
<pre>
if the value is string in ts
.ts
show='yes'

.html
<h1 *ngIf = "show == 'yes' else elseBlock">
    if block
</h1>
<ng-template #elseBlock>
  <h1>else block</h1>
</ng-template>

If we want if block in ng template
&lt;h1 *ngIf = "show == 'yes' ; then ifBlock  else elseBlock"&gt;
&lt;/h1&gt;
&lt;ng-template #ifBlock&gt;
  &lt;h1&gt;if block&lt;/h1&gt;
&lt;/ng-template&gt;

&lt;ng-template #elseBlock&gt;
  &lt;h1&gt;else block&lt;/h1&gt;
&lt;/ng-template&gt;
</pre>
  
if elseif
<pre>
we'll use property binding here:

.ts
color = 'green';

.html
&lt;ng-template [ngIf]="color=='red' "&gt;
  &lt;h1&gt;Red Color&lt;/h1&gt;
&lt;/ng-template&gt;

&lt;ng-template [ngIf]="color=='blue' "&gt;
  &lt;h1&gt;Blue Color&lt;/h1&gt;
&lt;/ng-template&gt;

&lt;ng-template [ngIf]="color=='green' "&gt;
  &lt;h1&gt;Green Color&lt;/h1&gt;
&lt;/ng-template&gt;
</pre>  

<h3>Switch case</h3>
<pre>
we can use it when we want to show data on color, month etc. So where there are more conditions then we can use if but switch is better in this case.
&lt;div [ngSwitch]="color"&gt;
  &lt;h2 *ngSwitchCase=" 'red' "&gt;
      Red color
  &lt;/h2&gt;
  &lt;h2 *ngSwitchCase=" 'blue' "&gt;
      Blue color
  &lt;/h2&gt;
  &lt;h2 *ngSwitchCase=" 'green' "&gt;
      Green color
  &lt;/h2&gt;
&lt;/div&gt;

we can also give styles to all h2 tags using the style
</pre>
  
<h3>For loop in angular</h3>
Array
<pre>
on array:
.ts
color = ['red','blue','green'];

.html
&lt;h2 *ngFor="let c of color"&gt;
  {{c}}
&lt;/h2&gt;
</pre>
 
Array of object
<pre>
.ts
stud = [
    {
      name:'fareen',
      age:20
    },
    {
      name:'annu',
      age:23
    },
    {
      name:'roma',
      age:24
    }
  ];
  
 .html
 &lt;table border="1"&gt;
  &lt;tr *ngFor="let s of stud"&gt;
    &lt;td&gt;{{s.name}}&lt;/td&gt;
    &lt;td&gt;{{s.age}}&lt;/td&gt;
  &lt;/tr&gt;
&lt;/table&gt;
</pre>
  
<h3>Simple Form</h3>
<pre>
Step 1: import in .ts file
import { FormsModule } from '@angular/forms';

imports: [
    CommonModule,
    FormsModule         //added by me
  ],
  
Step 2:
.ts file
getUserValue(value : any){
    console.log(value)
  }

.html
&lt;form #simpleForm = "ngForm" (ngSubmit) = "getUserValue(simpleForm.value)"&gt;
    Name:&lt;input type="text" ngModel name="username"&gt;&lt;br&gt;&lt;br&gt;
   Password:&lt;input type="text" ngModel name="password"&gt;&lt;br&gt;&lt;br&gt;
    &lt;button&gt;Get Values&lt;/button&gt;
</form>

ngModel will tell the forms are connected
</pre>

<h3>Creating header and footer in angular</h3>
Common header and footer<br>
Create two component header and footer design it using css<br>
Three ways to give css:<br>
1)inside component's css.<br>
2)style.css, which is already present in app folder. It is used for global css.<br>
3)inside asserts create css files.<br>

<h3>Style bindig in angular</h3>
Difference between normals style and style binding.<br>
if the data is coming from api or something and give it color.<br>
<pre>
  &lt;h1 style="background-color:skyblue"&gt;dynamic binding&lt;/h1&gt;           //normal style
  &lt;h1 [style.backgroundColor]=" 'green' "&gt;dynamic binding 2&lt;/h1&gt;      //style with binding
  &lt;h1 [style.backgroundColor]="col"&gt;dynamic binding 3&lt;/h1&gt;            //style coming from .ts
  
Changing color on click of the button:
.ts
  color = ""
  changecol(){
      this.color = "pink"
  }

.html
  &lt;h1 [style.backgroundColor]="color"&gt;dynamic binding 2&lt;/h1&gt;
  &lt;br&gt;
  &lt;button (click)="changecol()"&gt;dynamic binding 2&lt;/button&gt;
  
 
Conditional styling:
.ts
err=true;
 
if there is error then color red else green
 
.html
&lt;h1 [style.backgroundColor]="err? 'red': 'green' "&gt;dynamic binding 2&lt;/h1&gt;
</pre>

<h3>Passing data from parent to child component</h3>
<pre>
Step 1: create child component
Step 2: in parent component
.ts
author = "fareen"

.html
  &lt;app-signup [aut] = "author"&gt;&lt;/app-signup&gt;
 
Now parent done sending data, now child's work

Step 2: in child component
import Input inside the 
.ts
        //added by me
OnInit, Input }

export class SignupComponent implements OnInit {

  @Input() author: any        //adde by me
  
.html
&lt;h1&gt;{{author}}&lt;/h1&gt;

passing object data
.ts
stud = {
  name:'marry',
  age:20
  }
  
.html
{{stud.name}}

Making a component reusable
now if we have lots of data then useing for loop we can make this component reusable
</pre>

<h3>Passing data from child to parent component</h3>
<pre>
PENDING
</pre>

<h3>Pipe in Angular</h3>
To format the data string etc we make use of pipe, Example if i want all names to be display in Title case then we need to make function etc, so to not make it hard just use pipe concept. It is like we use in django's | to make a string title case.
<pre>
.ts
author =  'Fareen Ansari'

.html
&lt;h1&gt;{{author | uppercase}}&lt;/h1&gt;

More on string:
titlecase

Slicing:
{{author : slice:1}}          //op:areen
{{author : slice:1:5}}        //op:aree

Formating date:
.ts 
today = Date.today()

.html
{{today}}                          //op:1629270053437
{{today | date}}                   //op:Aug 18, 2021
{{today | date:'fullDate'}}        //op:Wednesday, August 18, 2021

For currency:
.ts
cash = 10;

.html
{{cash | currency:'USD'}}         //$10.00
</pre>

<h3>Routing</h3>
If you didn't select routing option on the project creating time then we can make use for this command to add it in the project:<br>
>ng generate module app-routing --flat --module=app
Here we'll work on the 'app-routing.module.ts' file.<br>
<pre>
app-routing.module.ts
import { LoginComponent } from './users/login/login.component';
import { SignupComponent } from './users/signup/signup.component';

const routes: Routes = [
//create an array of object, added by me
{
  path:'login',
  component : LoginComponent
},
{
  path:'signup',
  component:SignupComponent
}
];

app.component.html
<a routerLink="login">Login</a><br><br>
<a routerLink="signup">Signup</a>

If we don't give router-outlet then the page will navigate to that link but the page data won't be visible.
<router-outlet></router-outlet>

if someone comes at login send the to login page etc
</pre>

<h3>Four o four page</h3>
If we give a link and the page is not present in that page then it'll show error to give message that page not found. It basically handles page not found
<pre>
Create new component for 404 page using wildcard.

Same process like routing the page just add double start which is called wildcard in path.

.ts
import { PgComponent } from './AllComponents/blog/blog.component';

const routes: Routes = [
//create an array of object, added by me
{
  path:'login',
  component : LoginComponent
},
{
  path:'signup',
  component:SignupComponent
},
{
  path:'**',
  component: PgComponent
}
];

.html
&lt;h1&gt;Page Not Found&lt;/h1&gt;

We can design this page
Now for any page which is not there if user hit that page it'll show page not fount and not give the error. Example link http://localhost:4200/follow  will show page not found.
</pre>

<h3>Custom directive</h3>
Used to manupulate DOM & HTML. Example, ngfor loop, switch etc
<pre>
Step 1:
>ng g directive customstyle

It updated one file and created 2 new files
CREATE src/app/customstyle.directive.spec.ts (244 bytes)
CREATE src/app/customstyle.directive.ts (151 bytes)
UPDATE src/app/app.module.ts (705 bytes)

Step 2:
customstyle.directive.ts
                    //added by me
import { Directive, ElementRef }

 constructor(private el:ElementRef) { 
    el.nativeElement.style.color="green"
  }
  
 .html
 &lt;h1 appCustomstyle>Custom heading&lt;/h1&gt;
</pre>

<h3>Service in angular</h3>
It is used to share data between two to three component, example we want to show user data between 2-3 component. And it is not conmponent and module dependent.
<pre>
Step 1:
>ng g service usersData

it created 2 files
CREATE src/app/users-data.service.spec.ts (373 bytes)
CREATE src/app/users-data.service.ts (138 bytes)

Step 2:
user-data.service.ts

import { UsersDataService } from './users-data.service';

  constructor() {}

  getData(){
    return {name:'fareen', age:20}
  }
}  

app.component.ts
  constructor(private user:UsersDataService)
  {
    console.log(this.user.getData())
  }
}

</pre>

<h3>API call</h3>
Api is called with service, so we we'll create service. Angulr is UI development so it can't directly call the database so we need API to interact with data.
<pre>
users.data.services.ts
import {HttpClient} from '@angular/common/http'

  constructor(private http:HttpClient) {}
  getData(){
    let url="https://jsonplaceholder.typicode.com/todos/"
  }
  
Step 2:
app.module.ts

import { HttpClientModule } from '@angular/common/http';
imports: [
    HttpClientModule
  ],

Step 3:
app.component.ts
import { UsersDataService } from './users-data.service';

constructor(private user:UsersDataService)
  {
    this.user.getData().subscribe(data=>{
      console.log(data);
    })
  }
  
Step 4:
user-data.service.ts

import {HttpClient} from '@angular/common/http'

export class UsersDataService {

  constructor(private http:HttpClient) {}

  getData(){
    let url="https://jsonplaceholder.typicode.com/todos/"
    return this.http.get(url);
  }
} 

Output: all the json data which is present at(https://jsonplaceholder.typicode.com/todos/) will be visible on console 
</pre>

<h3>Show list from API data</h3>
<pre>
app.component.ts

  data:any = [];
  constructor(private user:UsersDataService)
  {
      this.user.getData().subscribe(data=>{
      console.log(data);
      this.data = data;
    })
  }
  
app.component.html
&lt;table border="1"&gt;
  &lt;tr&gt;
      &lt;td&gt;UserId&lt;/td&gt;
      &lt;td&gt;Id&lt;/td&gt;
      &lt;td&gt;Title&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr *ngFor="let i of data"&gt;
      &lt;td&gt;{{i.userId}}&lt;/td&gt;
      &lt;td&gt;{{i.id}}&lt;/td&gt;
      &lt;td&gt;{{i.title}}&lt;/td&gt;
  &lt;/tr&gt;
&lt;/table&gt;
</pre>

<h3>Model in angular</h3>
It define data structure. It'll tell what data is belongs to which data type, It does the data validation. It is part of typescript.
<pre>
Step 1:
app.component.ts

below the import define the data type
interface dataType{
  name:string,
  age:number,
  indian:boolean,
  address:any
}

app.component.ts
export class AppComponent {
  getUserData(){
    const data:dataType={
      name:'fareen',
      age:20,
      indian: true,
      address: '123, Colm street'
    }
    return data;
  }
}
 
The same we can use inside the service file

Step 1:
Or We can use seperate mydt.ts
export interface dataType{
  name:string,
  age:number,
  indian:boolean,
  address:any
}

Step 2:import it
app.component.ts

import { dataType } from './mydt'; 

export class AppComponent {
  getUserData(){
    const data:dataType={
      name:'fareen',
      age:20,
      indian: true,
      address: '123, Colm street'
    }
    return data;
  }
}
</pre>

<h3>Routing Module</h3>
Example every module has it's own routing. When we go on specific UI module the routing related to that module will be load at that time. Example Admin and User module. So when we access admin then users rout will not be loaded and vice versa, so that speed of our application will increase
<pre>
Step 1:
>ng g modulename --routing
>ng g module admin --routing

this will generate 2 files 
CREATE src/app/admin/admin-routing.module.ts (248 bytes)
CREATE src/app/admin/admin.module.ts (276 bytes)

Step 2: create component
>ng g component admin/login
>ng g component admin/list

Step 3: go to module's routing.ts file
admin-routing.module.ts

import { LoginComponent } from './login/login.component';
import { ListComponent } from './list/list.component';


const routes: Routes = [
  {
    path:'AdminLogin', component:LoginComponent
  },
  {
    path:'AdminList', component:ListComponent
  }
];

Step 4: import the admin component inside app's .ts file
app.module.ts
import { AdminModule } from './admin/admin.module';

imports: [
    AdminModule
  ],

if the link is not working restart ng serve
</pre>

<h3>Group Routing</h3>
Example we have two module Admin and User and both have same login page then how will we know which one is admin's login and which is user's. In this case we'll use group routing this is similar like App level url in django. Example for admin's login we'll use localhost:4200/admin/login.
<pre>
Step 1:
Same step like above create two modules with routing file

If we don't give group routing and routing is present in both admin and user then according to alphabhetical order admin routig will get the priority.

Step 2:
admin-routing.module.ts
const routes: Routes = [
  {
    path:'admin',children:[
      {
        path:'AdminLogin', component:LoginComponent
      },
      {
        path:'AdminList', component:ListComponent
      }
    ]
  }
]; 

Do same for users module too

Step 3:
.html
&lt;h1&gt;Link coming from the module's page&lt;/h1&gt;
&lt;h1&gt;Admin Stuff&lt;/h1&gt;
&lt;a routerLink="admin/AdminLogin"&gt;Login&lt;/a&gt;&lt;br&gt;&lt;br&gt;
&lt;a routerLink="admin/AdminList"&gt;List&lt;/a&gt;&lt;br&gt;&lt;br&gt;

&lt;h1&gt;Login Stuff&lt;/h1&gt;
&lt;a routerLink="user/UserLogin"&gt;Login&lt;/a&gt;&lt;br&gt;&lt;br&gt;
&lt;a routerLink="user/UserList"&gt;List&lt;/a&gt;&lt;br&gt;&lt;br&gt;
&lt;router-outlet&gt;&lt;/router-outlet&gt;
&lt;hr&gt;
</pre>

<h3>Lazy loading in angular</h3>
What is the difference between normal loading and lazy loading?<br>
Lazy loading basically apply on routing.<br>
Whenever we load a page then if we have 1000 pages all will load together which make the website slow, in case of lazy loading only the page we need will load this increase the speed and improve the performance.<br>
NOTE: In the above example we were importing the admin and users inside the app.module.ts, But in this case we don't do that.<br>
<pre>
router.ts file of admin
const routes: Routes = [
  //this will run only when we need this
  {
    path:'admin' , loadChildren:()=>import('./admin.module').then(mod=>mod.AdminModule)
  }
];

.html
&lt;h1&gt;Link coming from the module's page&lt;/h1&gt;
&lt;h1&gt;Admin Stuff&lt;/h1&gt;
&lt;a routerLink="admin/AdminLogin"&gt;Login&lt;/a&gt;&lt;br&gt;&lt;br&gt;
&lt;a routerLink="admin/AdminList"&gt;List&lt;/a&gt;&lt;br&gt;&lt;br&gt;
&lt;router-outlet&gt;&lt;/router-outlet&gt;

PENDING
</pre>

<h3>Lazy loading component</h3>
PENDING

<h3>Forms Intro</h3>
Types:1) Reactive form(control data in component.ts file) 2)Template drivern(control data in component.html file).<br>
They both have validation and handling data is slight different in both.<br>

![form](https://user-images.githubusercontent.com/59610617/129926359-b38d19ae-f38b-4624-8dd4-ac0769a79a58.png)<br>

<b>Data flow work</b><br>
Form -> .ts file ->service(call api and transfer data to server) -> server<br>

<h3>Template driver form</h3>
If we want to make any basic form then we use this one.
<pre>
Step 1:
app's .ts file

import { FormsModule } from '@angular/forms';

imports: [
    FormsModule,
  ],
  
app's .html
<form #simpleForm = "ngForm" (ngSubmit) = "getUserValue(simpleForm.value)">
    Name:<input type="text" ngModel name="username"><br><br>
   Password:<input type="text" ngModel name="password"><br><br>
    <button>Get Values</button>
</form>

Here id is simpleForm 
onSubmit we have to give function
ngModel to bind it with simpleForm
</pre>

<h3>Adding bootstrap in form</h3>
Just insatall the bootstrap using:<br>
>ng add @ng-bootstrap/schematics<br>
No need to add,import anything else. Restart ng serve<br>
Now bootstrap added start using the bootstrap from there official website.<br>

<h3>Angular reactive form validation</h3>
<pre>
Step 1: import reactive form
component.ts
import { ReactiveFormsModule } from '@angular/forms';
 imports: [
    ReactiveFormsModule
  ],
  
Step 2:
.html
Add a bootstrap form or make one
 
Step 3
component.ts
                                 //for valiation without it we can't use validation
import { FormControl, FormGroup, Validators} from '@angular/forms';

export class AppComponent {
  //name of the form
  LoginForm = new  FormGroup({
    email:new FormControl('',Validators.required),      //must be same as name of the input given in form 
    password:new FormControl('')
  })
}

 .html: give form a name
 <form [formGroup]="LoginForm">
  <div class="mb-3">
    <label for="exampleInputEmail1" class="form-label">Email address</label>
    <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" formControlName="email">
    <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div>
  </div>
  <div class="mb-3">
    <label for="exampleInputPassword1" class="form-label">Password</label>
    <input type="password" class="form-control" id="exampleInputPassword1"  formControlName="password">
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>
 
 formGroup name     //form name 
 formControlName    //filed name 
 rest all are same bootstrap class
 
Now to check if the validation is applied or not on inspect of this form on browser, if the form is black it'll give ng-invalid, when we fill this input it'll show ng-valid
 
Apply css to know if it is valid or invalid
.css
input.ng-invalid{
    border-left: 5px solid red;
}
input.ng-valid{
    border-left: 5px solid green;
}

Now we can see if the filed is empty it'll show red line on left side of input and vanish as long as we fill the form. An if it is valid we can see green color
 
TO GET TEXT WHEN THE EMAIL IS NOT FILLED
.ts
get email() {
    return this.LoginForm.get('email')
  }
  
.html : below the email field include this line
 <span class="text-danger" *ngIf="email?.invalid && (email?.dirty || email?.touched)">Email cannot be empty</span>
 
If the email is touched and it is invalid then below the field we'll get the message email cannot be empty when we touched the email filed and clicked outside.
</pre>

<h3>Add validation in angular form</h3>























