<template>
<AddBlog />
</template>

<script>
// @ is an alias to /src
import AddBlog from '@/components/AddBlog.vue'

export default {
    name: 'Blog',
    components: {
        AddBlog
    },
    data: () => ({

    }),
}
</script>

<style lang="css">
.xs {
    width: 100%;
}
</style>
