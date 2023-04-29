<template>
    <header>
        <h1>Counter</h1>
        <nav class="header-nav">
            <ul class="header-nav-list">
                <li class="redirect-contactMe">
                    <router-link to="/contactMe" @click="redirectContactMe">Contact Me</router-link>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script>
    export default {
        name: 'Header',
        methods: {
            redirectContactMe() {
                this.$emit('redirect-contact-me');
            }
        }
    }
</script>