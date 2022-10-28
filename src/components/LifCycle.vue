<template>
    <div>

        <div>
            <h2>LifCycle Components</h2>
            <h3>{{conuter}}</h3>
            <button @click="conuter=conuter+1">Update</button>
        </div>

    </div>
</template>

<script>

export default {
    name: 'LifCycle',
    data()
    {
        console.log("After box print this");
        return {
            conuter: 0
        }
    },
        beforeCreate()
        {
            alert("Alert Box Before Created Any html Tag");
        },
        created () {
            alert("After Create All html");
        },
    beforeUpdate() {
        alert("beforeUpdate", this.conuter);
    },
    updated() {
        alert("Update", this.conuter);
    }
}
</script>

<style scoped>
    h2 {
        color: red;
    }
</style>