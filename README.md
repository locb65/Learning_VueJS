# Learning_VueJS

## What is VueJS and Why use it?

VueJS Documentation: https://vuejs.org/guide/introduction.html

Vue.js is an open source JavaScript frontend framework for building user interfaces following the single-page application model. Developed by Evan You in 2014, it is based on Angular and his experiences with what he liked in Angular. Similar to React.js and Angular, Vue.js is component-based and uses declarative rendering. Since Vue.js is a framework, it has built-in plugins and libraries that can streamline and simplify the development process.

Vue.js extends HTML in the form of components for reusability. Its components resemble standard HTML templates. To create a simple Vue.js component that renders "Hello World" to the UI, the code would be:

```
<template>
    <div>
        <h1>Hello World</h1>
    </div>
</template>
```



### Getting started

There are multiple ways to get started with developing a Vue.js application. I will go into details about two methods dealing with CMD and CLI's commands. 

|Commands |Description |
|--------------|--------|
|```npm init vue@latest```|creates a new complete vue.js application
|```npm install -g @vue/cli```| installs the vue cli and CLI's commands
||


The first command `npm init vue@latest` will install vue at the current version and run you through a couple prompts to create the application.

```
✔ Project name: … 'project name here'
✔ Add TypeScript? … No / Yes
✔ Add JSX Support? … No / Yes
✔ Add Vue Router for Single Page Application development? … No / Yes
✔ Add Pinia for state management? … No / Yes
✔ Add Vitest for Unit Testing? … No / Yes
✔ Add an End-to-End Testing Solution? › No
✔ Add ESLint for code quality? … No / Yes

```

You can choose to add additional libraries and plugins later as well. 
* for the purpose of this counter, no additional libraries or plugins are needed.
* when the application is created, cd into your new application and run `npm install`. This will install any necessary dependencies needed to run the basic vue application
* Then run ` npm run dev` to start the server. 
    * the default url will be `localhost: 5173`

The second command `npm install -g @vue/cli` will install the vue CLI globally on your computer. This is more efficient then the first command if you plan on making more than one vue applications in the future. 
* The Vue CLI will streamline development through its own native commands.
    * if this is your install method, you can then run `vue create <app-name>` to create your new vue app. Replace `<app-name>` with your application name of choice.
* Once the app is created, cd into your new app and run the command `npm run serve` to start the server.
    * the default url will be `localhost:8080`

In both cases, Once you have created your app, you can start developing to your hearts desire. 


### Simple Counter App.

In this repository, you will find a simple counter created using Vue.js.

The counter is comprised of a couple simple components. 
* HelloWorld
* Button
* Header

There is also some light css applied to each component.

The main purpose of this repository is to showcase a simple app and using basic Vue.js implementations and to compare the development process to other popular front-end development environments like React.js.

* To use this application, fork and clone this repository. 
* cd to the repository and into the vue-learning-project directory. 
* run `npm install`.
* run `npm run dev`.
* then navigate to `localhost:5173` in a browser of your choice.
* from there you should see a counter that will increment up and down. 
* The incrementation of the counter handles the state change of `count` and the state itself is handled by Vue.js built in method call `data()`.

Similarly to React.js, The main.js file imports App.vue
* In App.vue, smaller components are imported. 
    * In this case, we have the Header, Button, HelloWorld Components. 
* Unlink React.js where a component is either a class or function that returns some html extenstion, Vue.js extends HTML by using HTML templates paired with a script tag that contains all the imports, methods, and components. 

Here are the components that make up this application:

Button Component:
```
<template>
    <div>
        <button>
            <slot></slot>
        </button>
    </div>
</template>

<script>
export default {
    name:"Button",
}
</script>
```

HelloWorld Component:

```
<template>
  <div>
      <h2>Hello World! Click the Buttons</h2>
  </div>
</template>
```

Header Component:
```
<template>
    <header>
        <h1>Counter</h1>
    </header>
</template>

<script>
    export default {
        name: 'Header'
    }
</script>
```

In the brower, you will notice that all three components are rendered and the count is incremented based on the buttons pressed.

Additionally, You will also find form component. This form component is a way for users to contact you. 
* the form is not rendered initially
    * if you click on the contact me in the header the form will render.

That is all for now. 

## Future features
* implement more components
* implement routing to mimic multiple page websites with routes using vue-router
* implement a backend that will store contact me form submissions



