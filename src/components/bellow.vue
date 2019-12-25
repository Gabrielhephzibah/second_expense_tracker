<template>
<div id="app">
     <div class="bellow">
        <h1 class="text3">My Expenses List</h1>
    </div>


       <div class="add">
         <router-link :to="{name: 'add'}" >
        <button class="btn">Add More</button>
        </router-link>
    </div>
    

</div>

    
</template>







<style>

.bellow{
    margin-top:1px;
    color:#b3b3b3;
    display: block;
    text-align: left;
    font-size: 12px;
    text-decoration: underline;

}

.text3{
    font-size: 18px;
    color: rgb(14, 16, 17);
    padding-top:0px;
    font-family: lato;
    font-weight: 20px;
    text-decoration: black underline;
    margin-left:12px;

}
.btn:hover{
    background:rgb(33, 109, 153);
    color:aliceblue;
}


</style>
