# angular-learning
This repo contains bulletpoints and references about *Angular* building blocks

# Angular
- Angular Sample apps -
  - https://github.com/start-angular/SB-Admin-BS4-Angular-6/
  - https://github.com/DanWahlin/Angular-JumpStart
  - https://github.com/gothinkster/angular-realworld-example-app
  - https://github.com/orizens/echoes-player/
  - https://github.com/mattlewis92/angular-calendar
  - https://github.com/aviabird/angularspree/
  - https://www.pluralsight.com/blog/software-development/10-angular-and-typescript-projects-to-take-you-from-zero-to-hero
  - https://www.madewithangular.com/
  - https://angularexpo.com/
  - https://medium.mybridge.co/18-amazing-open-source-angular-projects-dd9e81d921ee
  - https://medium.mybridge.co/angular-open-source-projects-for-the-past-year-v-2018-dba2041e6ff8
  - https://github.com/Ismaestro/angular7-example-app
  - https://github.com/tomastrajan/angular-ngrx-material-starter
- Angular CLI - https://github.com/angular/angular-cli/wiki
- Angular Wiki Stories - https://github.com/angular/angular-cli/wiki/stories
- Angular folder structure - 
  - https://angular.io/guide/styleguide#application-structure-and-ngmodules
  - https://medium.com/@motcowley/angular-folder-structure-d1809be95542
  - https://itnext.io/choosing-a-highly-scalable-folder-structure-in-angular-d987de65ec7
  - https://www.technouz.com/4644/angular-5-app-structure-multiple-modules/
- Angular Material -
  - https://material.angular.io/components/categories
  - https://alligator.io/angular/angular-material-2/
  - https://alligator.io/angular/custom-svg-icons-angular-material/
  - https://material.io/tools/icons/?style=baseline
- ng generate commands - 
  - https://github.com/angular/angular-cli/wiki/generate
  - https://alligator.io/angular/angular-cli-reference/
- Update Angular version - https://www.npmjs.com/package/@angular/cli
- Firebase hosting - https://alligator.io/angular/deploying-angular-app-to-firebase/
- NgRx - 
  - https://gist.github.com/btroncone/a6e4347326749f938510
  - https://github.com/avatsaev/angular-contacts-app-example
  - https://github.com/tomastrajan/angular-ngrx-material-starter
  - https://github.com/maxime1992/pizza-sync
  - https://github.com/maxime1992/angular-ngrx-starter
  - https://github.com/Alfresco/alfresco-content-app

# Angular 2 vs Agular 1
The core differences and advantages of Angular on Angular 1 are as following - 
  - It is entirely component based
  - Better change detection
  - Angular2 has better performance
  - Angular2 has more powerful template system
  - Angular2 provide simpler APIs, lazy loading and easier to application debugging
  - Angular2 much more testable
  - Angular2 provides to nested level components
  - Ahead of Time compilation (AOT) improves rendering speed
  - Angular2 execute run more than two programs at the same time
  - Angular1 is controllers and $scope based but Angular2 is component based
  - The Angular2 structural directives syntax is changed like ng-repeat is replaced with \*ngFor etc
  - In Angular2, local variables are defined using prefix (#) hash
  - TypeScript can be used for developing Angular 2 applications
  - Better syntax and application structure

# Angular Lifecycle Hooks
- *ngOnChanges* -	called when an input binding value changes	
-	*ngOnInit* - after the first ngOnChanges		
-	*ngDoCheck* -	after	every	run	of change	detection	
-	*ngAfterContentInit* - after component content initialized	
-	*ngAfterContentChecked* -	after	every	check	of component content	
-	*ngAfterViewInit*	-	after	component's	view(s)	are	initialized	
-	*ngAfterViewChecked* - after every check of	a	component's	view(s)	
-	*ngOnDestroy*	-	just before	the	component	is destroyed

- *DoCheck, AfterContentChecked and AfterViewChecked* - these three hooks fire often. Keep the logic in these hooks as lean as possible.

### Refs
- https://www.tektutorialshub.com/component-life-cycle-hooks-in-angular/
- https://www.tektutorialshub.com/angular-ngonchanges-life-cycle-hook/
- http://learnangular2.com/lifecycle/
- http://www.talkinghightech.com/en/angular-2-component-life-cycle/

# Components vs Directives 
- In Angular 2, a component is a directive with a view whereas a directive is a decorator with no view. Components are the specific type of directive that allows us to utilize web component functionality throughout our application.  
Whereas, Directive is the mechanism by which we attach behavior to elements.

- A component is used to break up the application into smaller components.  
Whereas, Directive is used to design the re-usable components.

- Only one component can be present per DOM element.  
Many directive can be used in a per DOM element.

- @View decorator or templateurl template are mandatory in the component.  
Directive don’t have View.

# Pipes vs Filters
- In case of async operations, you need to set things manually in case of angular 1.X filters.  
But pipes are smart enough to handle async operations. 

- Filters used to act like helpers, very similar to functions where you pass the input and other parameters and it returns you the value.  
But pipe works as a operator.

- Most of the filters from Angular 1.x are retained in Angular 2.0 pipes, in addition to the creation of newer pipes.  
Removal of orderby and filter form Angular 2.

- AngularJS 1.x has a filter called filter, which allows us to do sort, format and transform. However, the duplication of the names often leads to confusion. That’s another reason the core team renamed the filter component to pipe.

# ngOnInit vs Constructor
- The constructor is a typescript feature.  
ngOnInit event is an Angular 2 life-cycle event/method that are called after the first ngOnChanges.

- ngonInit is just a method in a class which structurally is not different to any other method in a class.  
A constructor is a completely different thing. It will be called when an instance of a class is created.

- A class constructor in angular is used to inject dependencies, which is called constructor injection pattern.  
Whereas, when ngOnInit is called, it has finished creating a component DOM, injected all required dependencies through constructor and processed input bindings.

- A constructor is a default method of the class that is executed when the class is instantiated.  
Whereas, ngOnInit is a life cycle hook called by Angular 2 to indicate that angular is done creating the component.

- The ngOnInit is called right after the directive's data-bound properties have been checked for the first time, and before any of its children have been checked. It is invoked only once when the directive is instantiated.


# Observables vs Promises
- Observable is a more powerful way of handling http asynchronous requests.  
A promise handles a single event when an asynchronous operation completes or fails.

- An observable is like a stream which allows passing zero or more events where the callback is called for each event.  
A promise eventually calls the success or failed callback even when you don’t need the notification or the result it provides anymore.

- Observable works with multiple values for a particular time.  
Promises works with and even returns a single value at a time.

- Observables can be cancelled.  
Promises cannot be cancelled.

- In observable, one operator ‘retry’ can be used to retry whenever needed.  
Promises cannot be retried. A promise should have access to the original function that returned the promise in order to have a retry capability.

### Refs
- https://xgrommx.github.io/rx-book/index.html




# Angular Interview Questions
- https://www.onlineinterviewquestions.com/angular2-interview-questions/#.WrHtfbpuLIU
- https://www.wisdomjobs.com/e-university/angular-2-interview-questions.html
- https://www.quora.com/in/What-are-some-Angular-2-interview-questions
- https://codingcompiler.com/angular-2-interview-questions-answers/	
- https://dzone.com/articles/angular-2-gotchas-and-interview-questions
- https://www.codeproject.com/Articles/1169073/Angular-Interview-Questions
- https://codingcompiler.com/angular-2-interview-questions/
- http://www.webdevelopmenthelp.net/2016/12/angularjs2-interview-questions.html
- https://www.tutorialspoint.com/angular2/angular2_interview_questions.htm
- https://github.com/Yonet/Angular-Interview-Questions
- https://github.com/khan4019/angular-interview-questions
- https://github.com/khan4019/front-end-Interview-Questions
- https://learnfrenzy.com/blog/top-25-angular-2-interview-questions--answers
- http://www.learnangularjs.net/top30-asked-angular-interview-questions-answers.php
- https://www.code-sample.com/2015/07/angularjs-2-documentation-with-example.html
- http://www.punch.cool/community/questions-answers/engineering/angular-js-2/index.html
