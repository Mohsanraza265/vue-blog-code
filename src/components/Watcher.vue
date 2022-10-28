<template>
    <div>
        <h2>Watchers Components</h2>
        <h1>{{count}}</h1>
        <button @click="count=count+1"> + </button>
        <button @click="count=count-1"> - </button>
    </div>
</template>

<script>

    export default {
        name: "Watch",
        data()
        {
            return {
                count: 0
            }
        },
        watch: {
            count(val)
            {
                if(val<0){
                    this.count=0
                }
            }
        }
    }
</script>

<style scoped>
    h2 {
        color: red;
    }
</style>