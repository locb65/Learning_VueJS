<script>
import Button from './Button.vue';
export default {
    name: "ContactForm",
    components: {
        Button, 
    },
    data() {
        return {
            form: {
                name: "",
                email: "",
                message: "",
            },
        };
    },
    methods: {
        handleSubmit() {
            // $emit is a built in vue method that allows you to create and sent custom events to the parent component
            this.$emit("submit-form", this.form);
        }
    }
}
</script>
<template>
    <form class="form-container" @submit.prevent="handleSubmit">
        <h1> Contact Me</h1>
        <div>
            <!-- v-model binds the input to a form data prop from data() in the export default above for name, email , and message respectively -->
            <label for="name">Name:</label>
            <input  class="name-input" type="text" name="name" v-model="form.name">
        </div>
        <div>
            <label for="email">Email:</label>
            <input class="email-input" type="email" name="email" v-model="form.email">
        </div>
        <div>
            <label for="message">Message:</label>
            <textarea class="message-input" name="message" v-model="form.message"></textarea>
        </div>
        <div class="form-button">
            <Button type="submit">Submit</Button>
        </div>
    </form>
</template>