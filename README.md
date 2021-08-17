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

app.component.html: will have html<br>
app.component.css: will have styling for app.component.html page
app.component.ts: how the module work will come here.
app.component.spec.ts: usefull for testing purpose.
app.module.ts: entry point

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

<h3>Adding components</h3>
<b>Understanding the first component which we get after app creation</b><br>
if we want the title we can use {{}} to print which is coming from app.component.ts

<b>Properties</b><br>
It is like a context we use in django.
<pre>
.ts file
export class AppComponent {
  title = 'blog';
  fav_color = "blue";         #added by me
}

.html
&lt;h1&gt;{{fav_color}}&lt;/h1&gt;
</pre>

<b>Adding component</b><br>
>ng generate component AllComponents/blog<br>

The <app-root></app-root> in index.html will bring contents of app.component.html, app.component.html will contains the html of all component, it'll merge them and make one page.<br>

copy the selector tag and paste it in app/app.component.html not on component's html page.<br>












