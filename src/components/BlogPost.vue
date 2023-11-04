<script setup>

const props = defineProps({
    name: String,
    id: Number,
    symptom: String,
    email: String,
    phone: String,
    changeFavName: Function
})

const emit = defineEmits(['changeFavName'])

</script>

<template>
    <div class="card">
        <div class="card-symptom">
        <h5 class="card-name">
                {{ id }} - {{ name }}
            </h5>
            <p>
                {{ symptom }}
            </p>
            <div class="row">
                <div class="col-6">
                    <span class="badge bg-success">
                        {{ phone }}
                    </span>
                </div>
                <div class="col-6">
                    <span class="badge bg-secondary">
                        {{ email }}
                    </span>    
                </div>
            </div>
            <!-- 
                <button @click="$emit('changeFavName', name)" class="btn btn-outline-primary">Favorito</button> -->

            <!-- <button @click="emit('changeFavName', name)" class="btn btn-outline-primary">Favorito</button> -->

            <button  @click="changeFavName(name)" class="btn btn-outline-primary mt-2 mr-auto ml-auto">Favorito</button>
        </div>
    </div>
</template>