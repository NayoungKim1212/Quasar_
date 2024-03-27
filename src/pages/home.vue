<template>
    <div>
        <div class="text-h4">Home</div>
    </div>
    <div>
        {{ $route.name }}
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped></style>

<route lang="yaml">
    name: home-page
    meta:
      requireAuth: true
</route>
