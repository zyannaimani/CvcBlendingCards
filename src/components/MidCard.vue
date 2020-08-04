<template>
<div>
    <h3>{{letters[0].title}}</h3>
</div>
</template>

<script>
export default {
    name:"Card",
    props:["letters"],
    data(){
        this.letters
    }
}
</script>

<style scoped>

</style>