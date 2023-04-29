<!-- Vue uses scripts tages to import components to upstream components -->
<script imports>
// standard import line, 
import HelloWorld from './components/HelloWorld.vue';
import Button from './components/Button.vue';
import Header from './components/Header.vue';
// exports the App component and all components used in app to the Index.html
export default {
  name: 'App',
  components: {
    HelloWorld, 
    Button, 
    Header
  },
  // methods to be exported
  methods: {
    // event listener method for button
    increment() {
      this.count++;
    },
    decrement() {
      this.count--;
    }
  },
  // data is used to handle state in VueJs
  // in this case data is handling the state of count which is being incremented when the button is clicked.
  data() {
    return {
      count: 0
    }
  },
}

</script>
<!-- template that renders HelloWorld Component to the DOM -->
<template>
  <div>
    <Header/>
    <HelloWorld/>
    <!-- called button method on button -->
    <!-- @click functions similiarly to onClick -->
    <!-- :count="count" is passing the prop from the data function to the child component of Button -->
    <!-- :count="count" is analogous to count={count} in reactjs
    and it is also a shorthand version of v-bind:count='count' -->
    <!-- Added another button to decrement count -->
    <!-- the Text Increment and Decrement is rendered to UI due to <slot> tag in child component.
      Without the slot tag, What is hardcoded in the child component will be rendered instead for both buttons -->
    <Button @click="increment" :count="count">Increment</Button> 
    <Button @click="decrement" :count="count">Decrement</Button>
    <p>{{ count }}</p>
  </div>
</template>