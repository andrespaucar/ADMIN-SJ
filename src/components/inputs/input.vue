<template>
    <div class="relative w-full">
        <input :type="type" :id="id" :placeholder="placeholder" 
            class="form__control" :required="required"
            :class="[size ? `form__control__${size}`:'',
            stateInput]" autocomplete="off"
            @input="$emit('update:modelValue', $event.target.value)" 
               >
        <!-- <small>Name es requerido</small> -->
    </div>
</template>

<script>
export default {
    emits:['update:modelValue'],
    props:{
        id:{required:false},
        type:{default:'text',required:true},
        required:{required:false},
        placeholder:{required:false},
        size:{required:false},
        state:{required:false}
    },
    mounted(){
    },
    watch:{
        value(){
            console.log(this.value)
        }
    },
    computed:{
        stateInput(){
            if(typeof(this.state) === 'undefined'){
                return false;
            }
            return (this.state)? 'isValid_f': 'isInvalid_f'
        }
    },
    methods:{
        updateValue(value){
            this.$emit('update:modelValue',value)
        }
    }
}
</script>

<style>

</style>