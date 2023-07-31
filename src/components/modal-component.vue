<template>
  <div class="portfolio-modal modal" tabindex="-1" role="dialog" :class="{'in modal-show': data.open}">
        <div class="modal-content">
            <div class="close-modal" @click="close">
                <div class="lr">
                    <div class="rl">
                    </div>
                </div>
            </div>
            <div class="container">
                <div class="row">
                    <div class="col-lg-8 col-lg-offset-2">
                        <div class="modal-body">
                            <ModalContent :contentName="data.contentName"></ModalContent>
                            <button type="button" class="btn btn-default" @click="close"><i class="fa fa-times"></i> Close</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'modal-component'
}
</script>

<script setup>
import {reactive,defineExpose} from 'vue';
import ModalContent from '../project-contents/modal-content'
const data = reactive({
    open: false,
    contentName : ''
})

const open = (item) => {
    data.contentName = item
    data.open = true;
};

const close = () => {
    data.open = false;
}

defineExpose({open,close});

</script>
<style scoped>
.modal-show{
    overflow-x: hidden;
    overflow-y: auto;
    display: block;
}
.in {
  opacity: 1;
  visibility: visible;
}

</style>
