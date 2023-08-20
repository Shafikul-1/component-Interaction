<script setup>
import { ref, reactive } from 'vue'
import ParentComponent from './ParentComponent.vue';
const massage = 'Massage Test' 
const EmitDefine = reactive({
    msg: 'Define Emit Check'
})
const buttonMassage = ref('Button Massage')
function buttonClick(){
    buttonMassage.value = 'Clicked Button & UPdate Massage'
}
</script>
<template>
    
    <p>{{ EmitDefine.msg }} </p>
    
    
    <ParentComponent v-model:messageEmitted ="EmitDefine.msg" :massage="massage" :eventHendelar="buttonClick"/> 
    <p>{{ buttonMassage }}</p>
</template>.

