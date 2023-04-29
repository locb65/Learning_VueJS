<!-- Vue uses scripts tages to import components to upstream components -->
<script imports>
// standard import line, 
import HelloWorld from './components/HelloWorld.vue';
import Button from './components/Button.vue';
// exports the App component and all components used in app to the Index.html
export default {
  name: 'App',
  components: {
    HelloWorld, 
    Button
  },
  // methods to be exported
  methods: {
    // event listener method for button
    clickedButton() {
      this.count++
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
    <HelloWorld/>
    <!-- called button method on button -->
    <!-- @click functions similiarly to onClick -->
    <!-- :count="count" is passing the prop from the data function to the child component of Button -->
    <!-- :count="count" is analogous to count={count} in reactjs
    and it is also a shorthand version of v-bind:count='count' -->
    <Button @click="clickedButton" :count="count"/>
    <p>{{ count }}</p>
  </div>
</template>