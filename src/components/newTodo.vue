<template>
    <form @submit.prevent="addTodo()" class="col-12 col-lf-6">
        <label>
            <input v-model="newTodo" placeholder="Enter Todo" type="text" class="font-control">
        </label>
    </form>
</template>

<script>
    export default {
        name: "NewTodo",
        data () {
            return {
                newTodo: ""
            }
        },
        methods: {
            addTodo(){
                if(this.newTodo.length > 1) {
                    this.$emit("on-addTodo", this.newTodo)
                }
                this.newTodo = ""
            }
        }
    }
</script>

<style scoped>

</style>