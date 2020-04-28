<template>
<div>
    <div class="container">         
        <h2> {{ question }}</h2>
        <input  type="radio" v-model= "choice" v-bind:value="answer1+','+id"  v-on:change="$emit('answer-changed', choice)">        
         <label> {{ answer1 }}</label>
         <input  type="radio" v-model= "choice" v-bind:value="answer2+','+id" v-on:change="$emit('answer-changed', choice)">
         <label> {{ answer2 }}</label>         
    </div>

</div>
</template>

<script>
export default {
    name:'wouldYouRatherQuestion',
props:{
    id: Number,
    question: String,
    answer1: String,
    answer2: String

},
    data() {
        return {
            choice:""
        }
    },
} 
</script>

<style>
body{
    background-color: rgb(218, 181, 221);
}
.container {
    background-color: rgb(209, 181, 236);
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    text-align:  center;
    font-size: 20px;

}
#button{
    font-family: 'Times New Roman', Times, serif;
}

</style>


