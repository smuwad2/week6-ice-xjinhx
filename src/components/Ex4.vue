<script>
export default { 
    data() {
        return {
            id : "demo1",
            isBlue : true  
        }
    },
    methods: { 
        changeColor(){
            this.isBlue = !this.isBlue;
        }
    }
}
</script>

<template>
    <div class="container">
        <div :id="id" class="m-2" :class="{ blueBox: isBlue, redBox: !isBlue }">
            div ID : {{id}} 
        </div>
        
        <button 
            type="button" 
            :class="{ 'btn btn-primary': isBlue, 'btn btn-danger': !isBlue }" 
            @click="changeColor"
        >
            Change Color
        </button>
    </div>
</template>

<style scoped>
.redBox {
    background-color: red;
}
.blueBox {
    background-color: blue;
}
#demo1 {
    color: white;
}
</style>