<template>
    <div>
    <h1>Minha lista de Tarefas!</h1>
    <button @click="() => showList = !showList">
        ver lista
    </button>
    <br>
    <input @ type="text" v-focus>
    <ul v-if="showList">
        <li
            v-for="(task, index) in tasks"
            :key="`${task}-${index}`"
        >
        {{task.name}}
        </li>
    </ul>
    <p v-else>Lista escondida!</p>
    </div>
</template>
<script>
const focus = {
    inserted: (el) => {
        el.focus()
    }
}
export default {
    directives: {
        focus
    },
    data: () => ({
        showList: false,
        tasks: [
            {
                name: 'Fazer curso',
                isDone: false            
            }
        ]
    })
}

</script>
<style>

</style>