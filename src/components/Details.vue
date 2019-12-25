<template>
    <div id="details">
        <div class="box">
            <!-- <div class="text4">Expenses<span class="text5">Amount</span></div> -->
            <table class="table">
                <thead>
                    <th>Expenses</th>
                    <th>Amount</th>
                </thead>
                <tbody>
                    <tr v-for="(data, key) in mainArray" :key="key">
                        <td>{{data.expense}}</td>
                        <td>{{data.amount}}</td>
                    </tr>
                    <tr >
                        <td>
                            total: {{totalAmount}}
                        </td>
                    </tr>
                </tbody>
            </table>

            
<!-- <div>
                <h1 class="total">Total:O</h1>
            </div> -->


            <a @click.prevent="showAddForm()" href="#" class="btn btn-success">Add</a>

            
            <!-- <div class="btn">
                 <router-link :to="{name: 'add'}" >
                <button class="btn1" > Add </button>
                </router-link>
            </div> -->

            
            <form class="form" v-if="page.addform" @submit.prevent="submitForm()">
                <div class="form-group">
                    <label for="expense">Expense</label>
                    <input class="form-control" type="text" id="expense" placeholder="expense" required>
                </div>
                <div class="form-group">
                    <label for="expense">Amount</label>
                    <input class="form-control" type="number" id="amount" placeholder="amount" required>
                </div>
                <div class="form-group">
                    <button class="btn btn-primary">Save</button>
                </div>
            </form>

            
               
            <!-- <div class="add">
         <router-link :to="{name: 'add'}" >
        <button class="btn">ADD</button>
        </router-link>
    </div> -->

            


        </div>















        ]</div>
</template>

<script>

export default{

    data(){
        return {
            mainArray: [],
            formdata:{
                expense: "",
                amount: 0,
            },
            allArray: [],
            page: {
                addform: false,
            }
        }
    },

    methods: {
        cloneMessage: function(message){
            var clone ={};
            for( var key in message ){
            if(message.hasOwnProperty(key)) //ensure not adding inherited props
                clone[key]=message[key];
            }
                return clone;
        },
        showAddForm: function(){
            this.page.addform = true;
        },
        submitForm: function(){
            var init = 0
            var expense = document.getElementById("expense").value
            var amount = document.getElementById('amount').value

            this.formdata.expense = expense
            this.formdata.amount = amount

            this.mainArray.push(this.cloneMessage(this.formdata))
        }
    },
    computed: {
        totalAmount: function(){
            let total = 0
            for (let index = 0; index < this.mainArray.length; index++) {
                total= total+ parseInt(this.mainArray[index].amount, 10);
                // total = total +
            }
            return total;
        }
    }

}

</script>


<style scoped>
.btn {
    margin-top: 140px;
}
.btn1{
    color:#2c9c91;
}


.btn2 {
    margin-left: 12px;
    display: flexbox;

}


.box{
    height: 150px;
	box-shadow:0px 3px 0px #bebbb1;
    background-color: aliceblue;
    border: 2px solid #2c9c91;
    margin-top:2px;

}

.text4{
    color: black;
    font-family: lato;
    font-weight: 20px;
    text-align: left;
    margin-left: 20px;


}

.text5{
    padding-left: 250px;
    font-family: lato;
    font-weight: 20px;
}

.total{
        margin-top: 100px;
    font-size: 0.9rem;
    color: black;
    font-family: cursive;
    margin-bottom: px;
    float: right;
    padding-right: 20px;
}

</style>


