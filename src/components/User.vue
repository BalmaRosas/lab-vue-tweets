<template>
    <div>
        <span className="name">{{user.name}}</span>
        <span className="handle">{{user.handle}}</span>
    </div>
</template>

<script>
export default {
    name: "User",
    props: {
        user: Object,
    }
}
</script>

<style>

</style>