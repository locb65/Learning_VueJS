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
  methods: {
    clickedButton() {
      console.log('I have been clicked')
    }
  }
}

</script>
<!-- template that renders HelloWorld Component to the DOM -->
<template>
  <div>
    <HelloWorld/>
    <Button @click="clickedButton"/>
  </div>
</template>