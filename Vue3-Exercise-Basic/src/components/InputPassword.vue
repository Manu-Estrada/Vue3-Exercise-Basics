<script>
import { ref } from 'vue';


export default  {
    setup() {
        const password = ref("password");
        const isVisible = ref (false);
        function PasswordShow() {
            isVisible.value = !isVisible.value;
            
        }

   return {password, isVisible,PasswordShow};





    }
    }
    
    
   
</script>
<template>
    <div class="container text-center input-password">
        <h1 class="my-3">Exercise Input Password</h1>
        <input  v-model="password" :type="isVisible ? 'text':'password'" name="password" id="password" class="form-control">
        <div class="d-block">
            <span id="show-password" @click="PasswordShow()" class="mt-2 btn btn-warning">Show Password</span>
        </div>
    </div>
</template>

<style lang="css" scoped>
    #show-password:hover {
        cursor: pointer;
        user-select: none;
    }
</style>


