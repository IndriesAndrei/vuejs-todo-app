<script>

</script>

<template>
    <button>
        <!-- slots lets us render our own template content -->
        <slot>Create</slot>
    </button>
</template>

<style scoped lang="scss">
button {
  padding: 8px 16px;
  border: none;
}
</style>