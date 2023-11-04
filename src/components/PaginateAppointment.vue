<script setup>

const emit=defineEmits(['changePage','returnPage'])
const props=defineProps({
    blockNextBtn:Boolean,
    blockPrevBtn:Boolean
})

</script>

<template>
    <div class="btn-group" role="group" aria-label="Basic example">
        <button type="button" class="btn btn-primary" @click="emit('returnPage')" :disabled="blockPrevBtn">Previous</button> 
        <button type="button" class="btn btn-success" @click="emit('changePage')"  :disabled="blockNextBtn">Next</button> 
    </div>
</template>