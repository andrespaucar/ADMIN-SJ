<template>
    <div class="form__group">
        <label :for="id">{{label}}</label> 
        <slot></slot>
     </div>
</template>

<script>
export default {
    props:{
        label:{required:false},
        id:{required:false},
    }
}
</script>

<style>

</style>