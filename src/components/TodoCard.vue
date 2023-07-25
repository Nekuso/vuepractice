<script setup>
import { ref } from 'vue';
import NewTaskModal from './NewTaskModal.vue';

const isActive = ref(false);

function newTask() {
    isActive.value = !isActive.value;
}

</script>

<template>
    <div class="wrapper">
        <NewTaskModal v-if="isActive" />

        <div class="card__container">
            <div class="card__title">
                <h1>My Tasks</h1>
            </div>
            <div class="card__task__lists">
    
            </div>
            <div class="card__actions">
                <button @click="newTask" class="new__button">New Task</button>
            </div>
        </div>
    </div>
</template>


<style scoped>
    .wrapper {
        position: relative;
    }
    .wrapper .card__container {
        background: white;
        height: 650px;
        width: 650px;
        border-radius: 1.4rem;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        gap: 1rem;
        padding: 1.5rem;
        box-shadow: rgba(0, 0, 0, 0.19) 0px 10px 20px, rgba(0, 0, 0, 0.23) 0px 6px 6px;
    }
    
    .wrapper .card__container .card__title {
        width: 100%;
    }
    
    .wrapper .card__container .card__task__lists {
        height: 100%;
        width: 100%;
        background: rgb(222, 222, 222);
        border-radius: 1.4rem;
    }

    .wrapper .card__container .card__actions {
        width: 100%;
        display: flex;
        justify-content: end;
        align-items: end;
    }

    .wrapper .card__container .card__actions .new__button{
        cursor: pointer;
        padding: .6rem 1.2rem;
        background: rgb(31, 31, 31);
        color: white;
        border: none;
        border-radius: .7rem;
        font-weight: 700;
    }

    .wrapper .card__container .card__actions .new__button:hover{
        scale: 1.1;
        transition: all .2s ease-in-out;
    }
</style>