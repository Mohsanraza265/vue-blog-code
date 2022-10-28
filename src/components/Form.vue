<template>
    <div>
        <h2>Form components</h2>
        <h2>Form validation</h2>
        <ul>
            <li v-for="item in error" v-bind:key="item">
                {{item}} not valid
            </li>
        </ul>
            <label>Email : </label>
            <input type="email" placeholder="Enter Email" v-model="form1.email"/>
            <br /><br />

            <label>Password : </label>
            <input type="password" placeholder="Enter password" v-model="form1.password"/>
            <br /><br />
            <select v-model="form1.country">
                <option>India</option>
                <option>USA</option>
                <option>Pakistan</option>
                <option>Iran</option>
                <option>Iraq</option>
            </select>
            <br /><br />

            <h3>Technology</h3>
            <label for="check-1">Java : </label>
            <input type="checkbox" value="java" id="check-1"  v-model="form1.technology" />
            <br /><br />
            <label for="check-2">Php : </label>
            <input type="checkbox" value="php" id="check-2"  v-model="form1.technology" />
            <br /><br />

            <h3>Gender</h3>
            <label>Male : </label>
            <input type="radio" value="male" id="check-1"  v-model="form1.gender" />
            <br /><br />
            <label>Female : </label>
            <input type="radio" value="female" id="check-2"  v-model="form1.gender" />
            <br /><br />

            <button @click="login" type="button">login</button>
        
    </div>
</template>

<script>
    export default {
        name: 'Form',
        data()
        {
            return{
                form1: {
                    email: '',
                    password: '',
                    country: '',
                    technology: [],
                    gender: '',
                },
                error: [],
            }
        },
        methods: {
            login()
            {
                this.error = [];
                for(const item in this.form1)
                {
                    if(this.form1[item]=== "" || this.form1[item].length===0){
                        this.error.push(item)
                    }
                }

                if(this.error.length===0)
                {
                    alert("data submit");
                }

                console.log("login data", this.form1.email ,  this.form1.password, this.form1.error)
            }
        }
    }
</script>

<style scoped>
    h2 {
        color: red;
    }
</style>