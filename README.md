# Mean-Stack-Code-Issue-Logging-Project
Application using mean stack to create a issue logging web site


1) Setting up the front end and routing for the project

I have used Angular 6 and Angular material API 
Issue or bug logging application 

//I have used Angular CLI
//Commands in Angular CLI to install and get Angular up and running
  npm install -g @angular/cli
  ng new frontendbugloggingapp   // this will install all the dependencies as well
  cd frontendbugloggingapp
  ng serve --open
  //app running on port 4200
  
  //angular material to be added
  ng add @angular/material
  
  //adding components to angular app
  ng g c components/list   // this will add css, html, spec.ts and ts file
  ng g c components/create // "'''''''''''''''''''''''''''''''''''''''''''
  ng g c components/edit  // '''''''''''''''''''''''''''''''''''''''''''''
  
  //I will be using visual studio code
  code .
  
  The following is the code that gets added to the file
  
  
  import { BrowserModule } from '@angular/platform-browser';
  import { NgModule } from '@angular/core';
  import { RouterModule , Routes } from '@angular/router';
  import { MatToolbarModule } from '@angular/material';
  import { AppComponent } from './app.component';
  import { BrowserAnimationsModule } from '@angular/platform-browser/animations';
  import { ListComponent } from './components/list/list.component';
  import { CreateComponent } from './components/create/create.component';
  import { EditComponent } from './components/edit/edit.component';
  
  const routes : Routes = [
        {path: 'create' : component:CreateComponent},
        {path: 'edit/:id' : component : EditComponent},
        {path: 'list' : component :ListComponent},
        {path: '' : redirectTo: 'list', pathMatch : 'full'}
  ]
  
  @NgModule ({
     declarations : [
     AppComponent,
     ListComponent,
     CreateComponent,
     EditComponent
     ],
     imports :[
     BrowserModule,
     BrowserAnimationsModule,
     RouterModule.forRoot(routes),
     MatToolbarModule
     ],
     providers: [],
     bootstrap : [AppComponent]
     })
     
     export class: AppModule {}
     
     //app component file
     <mat-toolbar>
     <span>Angular-6 Mean Stack application</span>
     </mat-toolbar>
     <div>
         <router-outlet></router-outlet>
     </div>
     
     
     
     
     
  
  
  
  
  




