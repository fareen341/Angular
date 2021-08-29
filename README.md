<h1>COURSE CONTENT</h1>

[<h2>1.1 Course Description</h2>](#one)

[<h2>1.2 Introduction</h2>](#two)

[<h2>1.3 Creating first project</h2>](#three)

[<h2>1.4 Files and Folders in App</h2>](#four)

[<h2>1.5 Module</h2>](#five)

[<h2>1.6 Component</h2>](#six)

[<h2>1.7 Adding Bootstrap</h2>](#seven)

[<h2>1.8 Interpolation</h2>](#eight)

[<h2>1.9 Data Binding</h2>](#nine)
Installing bootstrap using npm:
<li>Property binding</li>
<li>Style binding</li>
<li>Event binding(Calling a function onclick of the event)</li>
<li>Events</li>
<li>Two way binding</li>

[<h2>1.10 Pipes</h2>](#ten)

[<h2>1.11 Component Communication</h2>](#eleven)

[<h2>1.12 Service</h2>](#twelve)

[<h2>1.13 API Call</h2>](#thirteen)

[<h2>1.14 Interface(Model)</h2>](#fourteen)

[<h2>1.15 Routing</h2>](#fifteen)

<li>Routing Module</li>
<li>Group Routing</li>

[<h2>1.16 Lazy Loading</h2>](#sixteen)

<li>Lazy Loading</li>
<li>Lazy Loading Component</li>

[<h2>1.17 Forms</h2>](#seventeen)

<li>Form introduction</li>
<li>Simple Form</li>
<li>Template driven from</li>
<li>Adding validation in template driven form</li>
<li>Reactive form with validation</li>
<li>Pre-filled form</li>

[<h2>1.19 Typescript in angular</h2>](#nineteen)

<li>Conditional statement</li>
<li>Switch case</li>
<li>For loop</li>



<hr>
<a name="one"><h2>1.1 Course Description</h2></a><br>
Angular is developed by google. Angular is new, angularjs is old. Open source web application framework led by the angular team at google. Mostly ppl use npm not the cdn like in jquery. Angular JS (Angular 1.0.0) was JS framework, developed in JS. It implemented MVC architecture. Angular ( all versions from 2 onwards), was a complete rewrite of Angular using TS. Documentation : https://angular.io/tutorial <br>

What is Angular? <br>
Angular is an open-source, JavaScript framework written in TypeScript. Angular is a framework for building web applications, both large and small scale. You can build a full‑featured enterprise‑level product management and inventory application or anything in between. Now before diving into Angular framework let’s understand why it is called a framework and what is the difference between a normal library and a framework. <br>
It is clint-side application, if we want to add database then we need the server in between.<br>

Framework vs Library <br>
The basic difference lies in a term called Inversion of Control. When you use a library, you are in charge of the application flow. You choose when and where to call the functions of that library. When you use a framework, the framework is in charge of the flow. The framework has a predefined structure where you write a code. In a nutshell, you tell libraries what to do, frameworks tell you what to do. Obviously the framework provides a lot more features than this. <br>

Advantages of Angular<br> 
1)We can create single page application <br>
2)Expressive HTML.<br>
2)Powerful data binding: one way binding, two way binding.<br>
3)Modular by design.<br>
4)Built-in back end integration: we don't need to install any package, we can directly call the rest API.<br>
5)Detailed documenatation.<br>
6)Great CLI support.<br>
7)Ivy Renderer: build size reduced. As in normal hello world application reduced to 10-14kb.<br>
8)We can create PWS(Progressive web apps) apps. Like we can install and create shortcut like app.<br>

Javascript language specification?<br>
ECMSScript 2015(formerly known as ES 6)--> arrow function, classes, & interface etc, modern browser does'nt fully support ES 6. So our code must be transpiled to ES 5. This is limitation of javascript, that's why typescript come. These all feature support in TypeScrip.<br>
Typescript has strong typing: run time error we'll know at compiletime where as in javascript will show that error at runtime.<br>
But browser does'nt understand typescript, browser only understand javascript. So to run typescript we've to convert it into ES 5 version and typescript will ceate a compatible code and that will run in all browers.<br>
<br>
To check how the typescript compiler will convert the advance javascript.<br>

![index](https://user-images.githubusercontent.com/59610617/130343034-9aac7e7b-6ab0-4492-9704-bf2fbf45b5a3.png)<br>

![ts file](https://user-images.githubusercontent.com/59610617/130343038-e8ec38ad-2fae-44a8-9d41-20103ef725e3.png)<br>

NOTE: to run the type script we need to install typescript <br>
For Executing: tsc.index.html<br>
Right after this command typescript will create a javascript file which browser will understand.<br>

![js](https://user-images.githubusercontent.com/59610617/130343046-e032d2af-93af-4cf9-a486-a3dc90c4d1b2.png)<br>

Or in the typescript website we can runsand check the js file
<pre>
const customer1 = new Customer()      //have customer type.

Explicit type:
let a: string;

Implicit type:
let a;      //if we hover over it it has any type, so i can assign any value to it.

let a=11;       //now the type is number 
a = 'hello'     //will give error

Giving multiple types 
let a: string | number;       //it can be string or number
</pre>

<a name="two"><h2>1.2 INTRODUCTION</h2></a><br>
<b>Installation</b><br>
We need node js for installation of angular. When you install NodeJS, you will get NPM along with it which is a Node Package Manager. Using npm we can install Angular and it’s dependencies.<br>

<b>To check the version of node and npm</b><br>
In folder shift+open power shell and use commands:<br>
>node --version<br>
>npn --version<br>
If these commands print out the proper version of node and npm that means NodeJS is properly installed.<br>

<b>Angular CLI</b><br>
The Angular CLI is a command-line interface tool that you use to initialize, develop, scaffold, and maintain Angular applications directly from a command shell.<br>
Installing Angular CLI using commands given in here https://angular.io/cli <br>
Insatlling: 
>npm install -g @angular/cli<br>
Check the version: 
>ng version<br>
If the powershell asking for policy then use:<br>
Change the execution policy:<br>
>Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser<br>

In case i want to remove it, Removing the execution policy:<br>
>Set-ExecutionPolicy -ExecutionPolicy Undefined -Scope CurrentUser<br>

<a name="three"><h2>1.3 Creating First Project</h2></a><br>
<b>Creating a new project</b>
>ng new project_name
If we want to use routing as well them press y, same for css<br>
Now it'll install the base files<br>
NOTE: if the option is in uppercase as in Y or N then the npm is recommending that option, but it is up to us weather to select that option ot not.<br>

From all the folders we'll work 90% on src cuz that will convert our angular source code. index.html is the entry point

To run the project on browser we use:<br>
>ng serve         
>ng serve -o    //-o to open automatically on browser

<a name="four"><h2>1.4 Files/Folders in Apps explain?</h2></a><br>
<pre>
FILES
these files are given in itvedant's anatomy of angular application.
Every file which has spec is the testing file 
for vs code(eslint and tslint) extension

1)package.json:
the first file which is created, it contain the ng commands etc.
if we want to add example a google map then we add it inside the defDepedencies.

2)node_modules:
all the depedencies and dev-dependencies which are present in package.json are installed inside the node_module.

3)index.html:
Entry point for html, this will load first. If we see inside the inspect-> network section the things whic loaded will be same but the another page css, favicon will get added at the end. First loaded will be same.

4)main.js:
javascript's first file which loads first.

5)style.css
If we want to do some global styling, we do inside this.

FOLDERS
1)src:
90% of code we'll do inside this one.

2)app: this is the root module, which can contains module or component

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
iii)tsconfig.app.json: contains configuration file of our app. Our application can have many  application each will have seperate this file.
iv)tsconfig: for entire application

7)e2e folder: end to end testing, used for testing.

8)angular.json: we give like build for js, css etc, inside build index,main are the entry point.

9)test.ts: entry point for testing file

10)favicon: the icon we see besides the title, we can change it using our own icon.

11)assets: we can keep images, doc, pdf, video, audio, font files etc. These files are publicly available. Example we create a html file inside it and we try to access it assets/test.html it'll be accessable, but inside app folder the files are not accessable eg if we use app.component.html in browser we won't be able to access it directly.

13)main.ts: this is entry point for application, if we delete all files in app we'll get error in main.ts
</pre>

<a name="seven"><h2>1.7 Adding bootstrap</h2></a><br>
<pre>
Step 1:
Installing bootstrap using npm:
>npm install bootstrap          //when we hit enter bootstrap will be added into the package.json 
>npm install jquery             //installing jquery

Step 2:
Method 1:
<hr>
include both in angular.json
inside the build-> styles: 
"styles": [
              
              "./node_modules/bootstrap/dist/css/bootstrap.min.css"        //added by me for bootstrap      
              "src/styles.css",         //Custom style should be end or bootstrap will override our style
            ],
          "scripts": ["./node_modules/bootstrap/dist/js/bootstrap.js",
                        "./node_modules/jquery/dist/jquery.js"]
                    },    
                    
This is single file when server request it has to load only one file.
How will we know it's one file? - on browser when we inspect we can see bootstrap file and below it we can see our global style.css file
If any class have same name in bootstrap and our style.css global class also then write our style.css below bootstrap so that our style will overwrite the bootstrap's class
 
We included jquery and bootstrap both
          
Step 3: 
Restart ng serve
NOTE: Whenever we does some changes in angular.json we must restart ng serve

Method 2:
<hr>
install bootstrap and instead of giving it in angular.json, we can give in global style.css, include this
@import '~bootstrap/scss/bootstrap.scss';

Method 3:
<hr>
We can use starter template but it's not recommended to include inside index.html
</pre>
At production build it'll minifiled the long bootstrap file.

<h3>Angular Bootstrap</h3>
We have angular bootstrap website (https://ng-bootstrap.github.io/#/home).<br>
There is also steps to insall it, We just have to use one command given on the home page of the website and it'll installed Add the code given in html and .ts as required. The first command is for angular 9 and latest, if we want to use old one then there is another command is given.<br>

<h3>Adding Material UI</h3>
https://material.angular.io/guide/getting-started<br>
All material + commands given in doc.<br>
When the command it'll ask for theme, choose theme, proceed. After successfully installation choose the component from material design and copy html and API related to it.<br>

<a name="six"><h2>1.6 Components</h2></a><br>
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

<b>Creating the component:</b><br>
>ng generate component AllComponents/blog<br>

This command will generate 4 files which is given above with blog name. Also, the blog component will be declared within AppModule declarations[].<br>

AllComponent is the name of the folder for all the newly created component for my understanding, i can direcly use ng generate component blog this will create all files inside app root.<br>
<b>Using this component:</b><br>
1)If i want to add the newly created component inside the root app.component.html then see the component's .ts file there is one selector, for the above component it is "app-blog" use this as a tag inside the app.component.html whereever we want "&lt;app-blog&gt;&lt;/app-blog&gt;".<br>
Whatever we make changes in component's html will reflect in main root's html file.<br>
2)Right after creating the component the main root's app.module.ts will automatocally import component and declare in app.module.ts<br>
  
The &lt;app-blog&gt;&lt;/app-blog&gt; in index.html will bring contents of component's, app.component.html will contains the html of all component, it'll merge them and make one page. Copy the selector tag and paste it in app/app.component.html not on component's html page.<br>
<pre>
Bsic metadata for AppComponent:

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})

export class AppComponent {
  title = 'my-app';
}
</pre>
The @Component decorator indicates that the class below it as a component class, and specifies its metadata. In the example code below, you can see that AppComponent is just a class, with no special Angular notation or syntax at all. It's not a component until you mark it as one with the @Component decorator.<br>
Every component has building blocks that it needs to create and present the component and its view. The metadata for a component tells Angular where to get these. Specially, the template which is the view is linked with component. Together, the component and its template describe a view. Additionally, it defines the styles for the component.
NOTE: We can also create component manually by creating a blog folder and define that 4 files and directive, constructor inside the .ts file etc.<br>
Also The templates can also be defned directly within ts file, instead of separate files. The styles also can be defined within the ts file.

![com](https://user-images.githubusercontent.com/59610617/130065882-474cb056-49eb-4bbb-929c-6c9430a9f7eb.png)<br>


<a name="eight"><h2>1.8 Angular Interpolation</h2></a><br>
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

<a name="nine"><h2>1.9 Data Binding</h2></a><br>
<h3>Property Binding</h3>
property binding and interpolation is not same. It is used using [] and interpolation with {{}}. If a variable within the component is to be linked with text box or some other DOM element, we can use Property binding. It uses [ ] around the property which we need to bind and a variable with which the binding is to be done is mentioned in “” on right side. e.g. isdisabled is a Boolean variable declared within component, which determines if the button is disabled or enabled.<br><br>
The attributes of html we can bind them, all html5 attributes we can use in js. Like we can bind src attribute and give src inside the js <br>
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

Another Example
<pre>
.js 
product{
  image=asset/mobile.jpg
  }

img src={{product.image}}
OR
img [src]="product.image"
</pre>
Try to give [height]="200" in html and also height=300 in js file and see which one gets the priority.<br>

<h3>Style Binding</h3>
Difference between normals style and style binding.<br>
if the data is coming from api or something and we want to give it color.<br>
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

<h3>How to call a function onclick of the function(Event binding)</h3>  
When we create a button both the file(app.component.html(which will have button) and app.component.ts(which will have function)) should present inside the same component.<br>
For binding events, parentheses are used around the event.<br>
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

<h3>Two-way binding</h3>
For two-way binding, a combination of square brackets and parentheses, [()]. The [()] syntax combines the brackets of property binding, [], with the parentheses of event binding, (), as follows.<br>
&lt;input type="text" [(ngModel)]="username"&gt;<br>
This syntax binds the valueof textbox to username variable declared within component. The data is bound from template to component and from component to template. Any change in username, in view or component will be reflected at both.</br>

<a name="five"><h2>1.5 Module</h2></a><br>
  
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


<a name="nineteen"><h2>1.19 Typescript</h2></a><br>
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
  
ngModel will tell the forms are connected
</pre>

<a name="eleven"><h2>1.11 Component Communication</h2></a><br>
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
now if we have lots of data then using for loop we can make this component reusable
</pre>

<h3>Passing data from child to parent component</h3>
<pre>
we'll create a child component userlist and use this component in app's component with the help of EventEmitter(basically used to send data from child to parent)
we'll create a function in parent and that function we'll call from child, so that child component can transfer data to parent component

Step 1:
app's .html
<app-userlist (parentComponent)="parentComponent($event)"></app-userlist>

app's .ts
export class AppComponent {
    parentComponent(data: any){
      console.log(data)
    }
}

Step 2:
userlist's component.ts
                            //added by me
import { Component, OnInit, Output, EventEmitter } 

export class UserlistComponent implements OnInit {

  @Output() parentComponent: EventEmitter<any> = new EventEmitter
  constructor() { }

  ngOnInit(): void {
    this.parentComponent.emit("hello");        //or pass ({name:'fareen'})   
  }
}

Now whatever we pass from emit() function will be visible in in app's .html file
Or inside the parent component we can directly use 
app's .ts
data=""
    parentComponent(data: any){
      this.data=data;
    }
    
&lt;h1&gt;{{data}}&lt;/h1&gt;
</pre>

<a name="ten"><h2>1.10 Pipes</h2></a><br>
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

<h3>Custom pipes</h3>
Custom pipes can be created for transformations which are not provided with the built-in pipes. The custom pipe can be sued in template expressions, same as built-in pipes — to transform input values to output values for display.<br>
Marking a class as a pipe<br>
Pipe is a class, marked by @Pipe decorator with corresponding metadata.<br>
For creating pipes, following steps need to be followed.<br>
1.Create the class and mark with @Pipe decorator<br>
2.Declare the pipe in AppModule<br>
3.Use this pipe in template<br>
<pre>
Step 1:
create a exponential-strength.pipe.ts file inside the app

import { Pipe, PipeTransform } from '@angular/core';

@Pipe({name: 'exponentialStrength'})
export class ExponentialStrengthPipe implements PipeTransform {
  transform(value: number, exponent = 1): number {
    return Math.pow(value, exponent);
  }
}

.html
&lt;h3&gt;{{2 | exponentialStrength: 10}}&lt;/h3&gt;

Step 2:
in app.module
import { ExponentialStrengthPipe } from './exponential-strength.pipe';

@NgModule({
  declarations: [
    ExponentialStrengthPipe
  ],
</pre>
Output: 1024

Every Pipe class must implement PipeTransform interface, making it compulsory to implement the transform(). The transform() takes one argument as value, which needs to be transformed. Additionally if required we can also pass additional parameters, to make pipe behave dynamically.<br>
In the example above, the transform() checks the length of string variable and if its more than 50, the string is shortened and returned and if the length is less than or equal to 50, then the string is returned as it is. To use this pipe within the template, the name declared within metadata is used.<br>

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

<a name="twenty"><h2>1.20 Directive</h2></a><br>
<h3>Built-in attribute directives</h3>
<pre>
PENDING
</pre>
<h3>Component Directive</h3>
They are the directives with a template. This type of directive is the most common directive type.<br>
<h3>Attribute directives</h3>
They are the directives which change the appearance or behaviour of an element, component, or another directive.<br>
<h3>Structural directives</h3>
They are the directives which change the DOM structure by adding and removing DOM elements.<br>

<h3>Custom Directive</h3>
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

<a name="twelve"><h2>1.12 Service</h2></a><br>
It is used to share data between two to three component, example we want to show user data between 2-3 component. And it is not conmponent and module dependent. A component can delegate common functionalities to services, such as fetching data from the server, validating user input, or logging directly to the console. Service class thus can provide all these to various components.
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


<a name="thirteen"><h2>1.13 API cal</h2></a><br>
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


<a name="fourteen"><h2>1.14 Interface(model)</h2></a><br>
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

<a name="fifteen"><h2>1.15 Routing</h2></a><br>
<h3>what is SPA?</h3>
Angular applications are Single Page Application (SPA). There is only one HTML document in the application, and all of the application's functions exist in this single HTML page. As users access the application's features, the browser needs to render only the parts that matter to the user (specific components), instead of loading a new page. This pattern can significantly improve the application's performance and the user experience.<br>

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


<a name="sixteen"><h2>1.16 Lazy Loading</h2></a><br>
<h3>Lazy loading</h3>
What is the difference between normal loading and lazy loading?<br>
Lazy loading basically apply on routing.<br>
Whenever we load a page then if we have 1000 pages all will load together which make the website slow, in case of lazy loading only the page we need will load this increase the speed and improve the performance.<br>
NOTE: In the above example we were importing the admin and users inside the app.module.ts, But in this case we don't do that.<br>
<pre>
Step 1: in admin routing file add
import { LoginComponent } from './login/login.component';
import { ListComponent } from './list/list.component';

const routes: Routes = [

  {path:'login', component:LoginComponent},
  {path:'list', component:ListComponent},
];

Do same for user module too same.

Step 2: in app's routing file
const routes: Routes = [
{
  //this will run only when we need this
  path:'admin' , loadChildren:()=>import('./admin/admin.module').then(mod=>mod.AdminModule)
},

{
  path:'user' , loadChildren:()=>import('./users/users.module').then(mod=>mod.UsersModule)
}
];

Step 3:

.html
&lt;h1&gt;Admin Stuff&lt;/h1&gt;
&lt;a routerLink="admin/login"&gt;Login&lt;/a&gt;&lt;br&gt;&lt;br&gt;
&lt;a routerLink="admin/list"&gt;List&lt;/a&gt;&lt;br&gt;&lt;br&gt;

&lt;h1&gt;User Stuff&lt;/h1&gt;
&lt;a routerLink="user/login"&gt;Login&lt;/a&gt;&lt;br&gt;&lt;br&gt;
&lt;a routerLink="user/list"&gt;List&lt;/a&gt;&lt;br&gt;&lt;br&gt;
&lt;router-outlet&gt;&lt;/router-outlet&gt;

Don't forget to import both modules in app.module.ts
import { AdminModule } from './admin/admin.module';
import { UsersModule } from './users/users.module';
</pre>
How do we know the lazy loading works go to admin.module.ts and after import write:<br>
console.log(Admin module")<br>
Every console log print when the page loads, but this one will work when we click on the admin module and only once.<br>

<h3>Lazy loading component</h3>
On click of that particular component that will only work
<pre>
In this case we need to create two component not the module.
userlist & adminlist

Step 1: app.component.ts
                    //added by me
import { Component, ViewContainerRef, ComponentFactoryResolver

export class AppComponent {
  constructor(private viewContainer: ViewContainerRef,
    private cfr:ComponentFactoryResolver){}
    async loadAdmin(){
      this.viewContainer.clear()    //clear if any component present
      const {AdminlistComponent} = await import('./adminlist/adminlist.component')
      this.viewContainer.createComponent(
        this.cfr.resolveComponentFactory(AdminlistComponent)
      )
    }

    async loadUser(){
      this.viewContainer.clear()    //clear if any component present
      const {UserlistComponent} = await import('./userlist/userlist.component')
      this.viewContainer.createComponent(
        this.cfr.resolveComponentFactory(UserlistComponent)
      )
    }
}

//ViewContainerRef: will create a container in which our component load like div
//ComponentFactoryResolver: convert the dynamic code into component.

Step 2:
app.component.html
&lt;button (click)="loadAdmin()"&gt;Load Admin&lt;/button&gt;
&lt;button (click)="loadUser()"&gt;Load User&lt;/button&gt;

</pre>
How this works:
if we have any component is present, clear it. Example when we click on adminlist there is admin list present in the container, if we need user list we'll click on button and function on that button will clear the admin component for user list component to load and create component will create component.<br>
Now even if we have 1000 component they wont load together. They'll load only whne they need meaning on click of the button.<br>
Check if they load on click of the button on admin componen.ts inside the constructor pass a console log.<br>
<pre>
constructor() {
    console.log("Admin loaded")
   }
</pre>
This won't load on first the page is loaded when we click the button "Admin loaded" will print on console.<br>

<a name="seventeen"><h2>1.17 Forms</h2></a><br>
<h3>Forms Intro</h3>
Types:1) Reactive form(control data in component.ts file) 2)Template drivern(control data in component.html file).<br>
They both have validation and handling data is slight different in both.<br>

![form](https://user-images.githubusercontent.com/59610617/129926359-b38d19ae-f38b-4624-8dd4-ac0769a79a58.png)<br>

<b>Data flow work</b><br>
Form -> .ts file ->service(call api and transfer data to server) -> server<br>


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
&lt;form #simpleForm = "ngForm" (ngSubmit) = "getUserValue(simpleForm.value)"&gt;
    Name:&lt;input type="text" ngModel name="username"&gt;&lt;br&gt;&lt;br&gt;
   Password:&lt;input type="text" ngModel name="password">&lt;br&gt;&lt;br&gt;
    &lt;button&gt;Get Values&lt;/button&gt;
&lt;/form&gt;

Here id is simpleForm 
onSubmit we have to give function
ngModel to bind it with simpleForm
</pre>

<h3>Adding bootstrap in form</h3>
Just insatall the bootstrap using:<br>
>ng add @ng-bootstrap/schematics<br>
No need to add,import anything else. Restart ng serve<br>
Now bootstrap added start using the bootstrap from there official website.<br>

<h3>Add validation in template driven form</h3>
<pre>
app's .ts file
import { FormsModule } from '@angular/forms';

Step 1:
app's .html file
&lt;h1&gt;Adding form validation&lt;/h1&gt;
&lt;form form #userForm="ngForm" (ngSubmit)="onSubmit(userForm.value)"&gt;
  &lt;div class="mb-3"&gt;
    &lt;label for="exampleInputEmail1"&gt;Email address&lt;/label&gt;
    &lt;input type="email" id="exampleInputEmail1" name="useremail" ngModel #email="ngModel" required&gt;
 &lt;/div&gt;
  &lt;div class="mb-3"&gt;
    &lt;label for="exampleInputPassword1">Password&lt;/label&gt;
    &lt;input type="password" id="exampleInputPassword1" name="userpassword" ngModel&gt;
  &lt;/div&gt;
  &lt;button type="submit"&gt;Submit&lt;/button&gt;
  &lt;/form&gt;
  
Step 2:
app's .ts file
   onSubmit(data: any){
      console.log(data);
    }
 
Step 3:
app's .css
input.ng-valid{
    border-left: 5px solid green;
}

input.ng-invalid{
    border-left: 5px solid red;
}

Now on first load the first filed which in we have given validation will be red cuz it is required when we fill data it'll change to green

Adding the reguired filed below the input box:

//this must be visible only when we touched the filed not on page load
//Add this below email input
&lt;span class="error" *ngIf="email.invalid && email.touched"&gt;Email cannot be blank!!&lt;/span&gt;

</pre>

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
 &lt;form [formGroup]="LoginForm"&gt;
  &lt;div class="mb-3"&gt;
    &lt;label for="exampleInputEmail1" class="form-label"&gt;Email address&lt;/label&gt;
    &lt;input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" formControlName="email"&gt;
    &lt;div id="emailHelp" class="form-text"&gt;We'll never share your email with anyone else.&lt;/div&gt;
  &lt;/div&gt;
  &lt;div class="mb-3"&gt;
    &lt;label for="exampleInputPassword1" class="form-label"&gt;Password&lt;/label&gt;
    &lt;input type="password" class="form-control" id="exampleInputPassword1"  formControlName="password"&gt;
  &lt;/div&gt;
  &lt;button type="submit" class="btn btn-primary"&gt;Submit&lt;/button&gt;
&lt;/form&gt;
 
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

<h3>Prefilled form</h3>
<pre>
Step 1: import in app's module.ts
import { FormsModule } from '@angular/forms';

Step 2:
app's .html
&lt;h1&gt;Pre filled form example&lt;/h1&gt;
&lt;form form #userForm="ngForm" &gt;
  &lt;div class="mb-3"&gt;
    &lt;label for="exampleInputEmail1"&gt;Email address&lt;/label&gt;
    &lt;input type="email" id="exampleInputEmail1" name="email"  [ngModel]="userData.email"&gt;
&lt;/div&gt;
  &lt;div class="mb-3"&gt;
    &lt;label for="exampleInputPassword1"&gt;Password&lt;/label&gt;
    &lt;input type="password" id="exampleInputPassword1" name="password" [ngModel]="userData.password"&gt;
  &lt;/div&gt;
  
  &lt;button type="submit"&gt;Submit&lt;/button&gt;
&lt;/form&gt;
We bind the ngModel with userData 

Step 3:
app's .ts
   userData = {
      email:"hello@world",
      password:"123abc"
    };
</pre>

<h3>Creating header and footer in angular</h3>
Common header and footer<br>
Create two component header and footer design it using css<br>
Three ways to give css:<br>
1)inside component's css.<br>
2)style.css, which is already present in app folder. It is used for global css.<br>
3)inside asserts create css files.<br>

<h1>include</h1>
to make it public then use export and import where need
@
ngModule({
  declarations: [],  // All components, directives & pipes
  exports: [],  //All components, directives, pipes that can be used by other modules
  imports: []    //All components, directives, pipes and modules  that can be used by this module
 //All component  bootstrap: []   // will only be included in root module only
})

To make it component give @component directive
@Component({
    selector: 'app-root'   //should be unique
    templates: 'Hello world'
})

we can use same selector many times, as in amazon has same component recent product, new products etc.
dont use same component inside sam component. but we can use it in any other omponen like app, and any other component 















