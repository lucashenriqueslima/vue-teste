<template>
    <img :src="avatar" :alt="description">
</template>

<script>
export default {
    name: "Picture",
    data() {
        return {
            avatar: "/img/logo.png",
            description: "Avatar image"
        }
    }
}
</script>