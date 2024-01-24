<template>
    <div>
        <div>This is header</div>
        <div>This is body</div>
        <slot />
        <div>This is footer</div>
    </div>
</template>
<script>
    export default {
        name:"default"
    }
</script>