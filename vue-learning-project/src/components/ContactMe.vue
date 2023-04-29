<script>
import Button from './Button.vue';
export default {
    name: "ContactForm",
    components: {
        Button, 
    }
}
</script>
<template>
    <form class="form-container">
        <h1> Contact Me</h1>
        <div>
            <label for="name">Name:</label>
            <input  class="name-input" type="text" name="name">
        </div>
        <div>
            <label for="email">Email:</label>
            <input class="email-input" type="email" name="email">
        </div>
        <div>
            <label for="message">Message:</label>
            <textarea class="message-input" name="message"></textarea>
        </div>
        <div class="form-button">
            <Button type="submit">Submit</Button>
        </div>
    </form>
</template>