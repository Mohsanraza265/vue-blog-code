<template>
    <div>
        <div class="interpolation">
            <h1>Topic : Interpolation</h1>
            <h2>Hello From Home components 30 + 30 =<span>{{30+30}}</span> </h2>
            <h2>Letter of Hello is {{"Hello".length}}</h2>
        </div>
        <div class="data">
            <h1>Topic : Data</h1>
            <h2>Name : {{ name }}</h2>
            <h2>Email : {{ email }}</h2>
            <h2>Number : {{ number }}</h2>
            <h2>Number : {{ number==8888 }}</h2>
            <h2>Caste : {{ getCaste("Rajper") }}</h2>
        </div>
        <div class="methods">
            <h1>Topic : Methods</h1>
            <h2>Name 1 : {{ getName ("Ameer") }}</h2>
            <h2>Name 2 : {{ getName ("Ali") }}</h2>
            <h2>All data : {{ getData ().email }}</h2>
        </div>
        <div v-html="tag">
           
        </div>
        
    </div>
    
</template>
<script>
    export default {
        name: 'Home',
        data ()
        {
          return {
            name : 'Mohsan Raza',
            email : 'mr2406769@gmail.com',
            number : '03043731265',
            tag: '<h1>Mohsan Ameer</h1>',
            getCaste:function( a ) {
                return a;
            }
          } 
        },
    // for methods 
        methods: {
            getName (name) 
            {
                return name;
            },
            getData(){
                return {
                    rollno : "mt-55",
                    email : this.email
                }
            }
         }

    }
</script>
<style scoped>
    
    h1 {
        color: red;
    }

</style>