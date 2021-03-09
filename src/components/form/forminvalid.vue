<template>
    <small :class="stateInv"> 
      <slot></slot>
    </small>
</template>

<script>
export default {
    props:{
        state:{required:false}
    },
    computed:{
        stateInv(){
            if(typeof(this.state) === 'undefined'){
                return false;
            }
            return (this.state)? 'text-success': 'text-danger'
        }
    }
}
</script>

<style>

</style>