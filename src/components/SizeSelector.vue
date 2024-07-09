<script lang="ts" setup>
const possibleSizes = ['XS','S','M','L','XL','XXL'];


// javaScript
//const props = defineProps({
  //  selectedSize: { type: String, required: true }

//});

//const emits = defineEmits ({
    //onChanceSize: String
//});


// typeScript

const props = defineProps<{
    selectedSize: String

}>();

const emits = defineEmits<{
  ( event: 'onChangedSize' , value: String): void,
}>();

</script>

<template>
   

    <button 
v-for="size in possibleSizes"
:class="{ 'active': props.selectedSize === size }"
@click="emits('onChangedSize', size)"
>



{{size}}

</button>

</template>