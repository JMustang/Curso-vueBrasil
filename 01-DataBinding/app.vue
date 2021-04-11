<template>
    <div>
    <h1 :style="{ textDecoration: decoration }">Hello {{name}}</h1>
    <input type="text" v-model="name">
    <br>
    <a :href="link">Link para o meu github</a>
    </div>
</template>
<script>

export default {
    data: () => ({
        name:'junior',
        decoration: 'underline',
        link: 'https://github.com/JMustang'
    })
}




</script>
<style>

</style>
