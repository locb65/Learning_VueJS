<!-- Button component -->

<template>
    <div>
        <button>
            <!-- <slot> tag allows for flexiblity in the rendering of component content -->
            <slot></slot>
        </button>
    </div>
</template>

<script>
export default {
    name:"Button",
}
</script>