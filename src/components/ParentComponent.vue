<script setup>
import { ref} from 'vue'
import ChildComponent from './ChildComponent.vue';
const person = {
    name:'Liebniz Tier',
    title:'Full Stack Developer',
    url:'https://www.liebniztier.com'
}

const messageToChild = 'Welcome to Child Component'
const messageFromChild = ref('')
</script>
<template>
    <div class="h-screen bg-gradient-to-r from-red-100 to-sky-100 flex items-center justify-center flex-col">
        <h1 class="font-bold ">{{ messageFromChild }}</h1>
        <ChildComponent :person = person :messageToChild="messageToChild" v-model:messageFromChild="messageFromChild"></ChildComponent>
    </div>
</template>