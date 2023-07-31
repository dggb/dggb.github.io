<template>
    <div v-if="props.contentName === 'semi'">
        <h2>반갑습니다.</h2>
            <hr class="star-primary">
            <img src="../../public/assets/img/jpg/Valuto-Account-Management.jpg" class="modal-image img-centered">
            <p></p>

        <ul class="list-inline item-details">
            <li>Client:
                <strong><a href="http://startbootstrap.com"></a>
                </strong>   
            </li>
            <li>Date:
                <strong><a href="http://startbootstrap.com"></a>
                </strong>
            </li>
            <li>Service:
                <strong><a href="http://startbootstrap.com"></a>
                </strong>
            </li>
        </ul>
    </div>
    <div v-else-if="props.contentName === 'cardGame'">
        카드게임
    </div>
</template>

<script>
export default {
  name: 'project-content'
}
</script>

<script setup>
import { defineProps } from 'vue'

const props = defineProps({
    contentName: {
    Type: String,
    default: '',
  },
})

</script>
<style scoped>

</style>
