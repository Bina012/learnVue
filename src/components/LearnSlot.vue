<template>
<h3>Learn about Slot in Vue js</h3>
<header>
    <slot name="header"></slot>
</header>
<content>
    <slot name="content"></slot>
</content>
<footer>
    <slot name="footer"><button>Click me ok</button></slot>
</footer>
</template>

<script>
export default {
    name: "LearnSlot",

}
</script>
