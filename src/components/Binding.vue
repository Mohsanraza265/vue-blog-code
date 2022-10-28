<template>
    <div>
        <h1>From Two-way-Binding component</h1>
        <input type="text" v-model="count" />
        <h2>{{ count }}</h2>

        <h1>Get input feild value</h1>
        <input type="text" placeholder="Enter Email" v-model="email" />
        <h3>{{email}}</h3>
        <br><br>
        <input type="password" placeholder="Enter password" v-model="password" />
        <h3>{{password}}</h3>
        <br><br>
        <button v-on:click="getData()" type="button">Get Value</button>

        <div class="for-checkbox">
            <h1>Get value of Checkbox & Radio Button</h1>
            <h2>Technology</h2>
            <label for="java">Java</label>
            <input type="checkbox" value="java" v-model="technology" id="java" />

            <label for="php">Php</label>
            <input type="checkbox" value="php" v-model="technology" id="php" />

            <label for="node">Node</label>
            <input type="checkbox" value="node" v-model="technology" id="node" />

            <h4>Selected Technology : {{ technology }}</h4>
            <!-- <h4>Selected Technology : <span v-for="(item , i  ) in technology" :key="item">{{item }} </span></h4> -->

            <h2>Who I am ?</h2>

            <label for="student">Student</label>
            <input type="radio" value="student" name="who" v-model="who" id="student" />

            <label for="developer">Developer</label>
            <input type="radio" value="developer" v-model="who" name="who" id="developer" />

            <h4>I am a {{ who }}</h4>

            <div class="flex">
                <div>
                    <h4>  {{partOne}} </h4>
                </div>
                <div>
                    <h4 class="important">  {{sentence}} </h4>
                </div>
            </div>


        </div>

    </div>
</template>

<script>

    export default {
        name: 'Events',
        data()
        {
            return {
                count:10,
                email:null,
                password:null,
                technology: [],
                who : null,
                test: [
                    "Student",
                    "Developer",
                    "Home maker",
                    "Doctor",
                    "Teacher",
                ],
                partOne: "I am a ",
                sentence: "Student"
            }; 
        },
        methods: {
            getData() 
            {
                console.warn("values : ", this.email, this.password);
            }
        },
        mounted() {
            setInterval(() => {
                this.sentence = this.test[Math.floor(Math.random() * this.test.length)]
            }, 2000);

        }
    }
</script>

<style scoped>
h1 {
    color: Orange;
}
.flex {
    display: flex;
    width: 200px;
    margin: auto;

}
h4.important {
    font-size: 17px;
    color: #15c7c7;
    margin-left: 10px;
}
</style>