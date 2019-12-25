<template>
<div class="input">
         <div class="first">
             <h1 class="text6">New Expense</h1>
             <input class="box2" type="text" name="text">
            </div>
            <br>

            <div class="first">
             <h1 class="text6">Amount</h1>
             <input class="box2" type="text" name="text">
            </div>

            <div class="btn">
                 <router-link :to="{name: 'add'}" >
                <button class="btn1"> Save </button>
                </router-link>
            </div>


     

    




</div>




    
</template>





<style scoped>

.btn1{
    color:#2c9c91;
}

.head{
    height: 70px;
	box-shadow:0px 3px 0px #bebbb1;
    background-color: #78909C;

}
.text{
    font-size: 18px;
    font-family: Lato;
font-style: normal;
font-weight: normal;
font-size: 30px;
line-height: 36px;
/* identical to box height */

letter-spacing: 0.1em;
padding-top: 20px;
}
.head2{
    height: 50px;
	box-shadow:0px 3px 0px #78909C;
    background-color: #78909C;
    margin-top: 16px;

}
.text1{
    font-size: 20px;
   font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-style:normal;
    font-weight:normal;
    letter-spacing:0.1em;
    padding-top: 12px;
}


.box2 {
    overflow: visible;
    width: 200px;
}
.text6{
    font-size: 0.9rem;
    color: black;
    font-family: cursive;
}
.input{ 
    margin-top:45px;
}



</style>



    