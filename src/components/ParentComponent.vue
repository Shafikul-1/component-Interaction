
<script setup>
defineProps(['messageEmitted', 'massage', 'eventHendelar' ]);
defineEmits(['update:messageEmitted '])
</script> 
<template>
    <div>
        <h1 class="text-4xl font-bold text-center my-6">{{ massage }}</h1>

        <input @input="$emit('update:messageEmitted', $event.target.value)" type="text" :value="messageEmitted" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline">

        <button @click="eventHendelar()" class="my-5 bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"> Click Here </button>
    </div>
</template>
