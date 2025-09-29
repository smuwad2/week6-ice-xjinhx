<script>
    export default { 
        data() {
            return {
                // Add code here
                id : "demo1",
                blueBox : true,
                blueBtn : true
            }
        },
        methods: { 
   			// Add code here
            //toChange(isBlue){
                // if (isBlue){
                //    console.log(isBlue);
                //    this.isBlue=false;
                //    isBlue=false;
                //    this.color="redBox";
                //}
                //else{
                //    this.isBlue=true;
                //    isBlue=false;
                //    this.color="blueBox";
                //}

            //}

            changeColor(){
                this.blueBox=!this.blueBox;
                this.redBox=!this.bl
            }
		}
    }
</script>

<template>
    
    <!-- Modify code here -->
    <div   class="container">
        <div v-bind:id="id" class="m-2" :class="{'blueBox' : blueBox,'redBox' : !blueBtn}">
            div ID : {{id}} 
        </div>
        
        <button type="button" :class="{'btn btn-primary' : blueBtn, 'btn btn-danger' : !blueBtn}" v-on:click = "changeColor()">Change Color</button>
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
