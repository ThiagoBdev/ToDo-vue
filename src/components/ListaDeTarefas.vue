<script setup>
const props = defineProps(["tarefas"]);
</script>

<template>
    <ul class="list-group mt-4">
        <li class="list-group-item" v-for="tarefa in props.tarefas" :key="tarefa.titulo">
            <input v-model="tarefa.finalizada" :id="tarefa.titulo" type="checkbox">
            <label :class="{ feito: tarefa.finalizada }" class="ms-3" :for="tarefa.titulo">
                {{ tarefa.titulo }}
            </label>
        </li>
    </ul>
</template>

<style scoped>
.feito {
    text-decoration: line-through;
}
</style>
