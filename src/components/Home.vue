<template>
   <div>
    <h1>Home component</h1>
    <h3>{{ data }}</h3>
    <h4>{{ msg }}</h4>

    <button v-on:click="clickHandler">Click me!</button>

    <h1 v-if="show">this is h1</h1>
    <h2 v-else>this is h2</h2>

    <table>
        <tr>
            <td>Id</td>
            <td>Name</td>
            <td>Email</td>
        </tr>
        <tr v-for="user in users" :key="user.id">
            <td>{{ user.id }}</td>
            <td>{{ user.name }}</td>
            <td>{{ user.email }}</td>
        </tr>
    </table>
   </div>

</template>

<script>
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name : 'Home',
    props : {
        data : String,
        msg : String
    },
    
    data() {
        return {
            show: true,
            users : [
                {
                    id : 1,
                    name : "light",
                    email : "example@gmail.com"
                },
                {
                    id : 2,
                    name : "alex",
                    email : "example@gmail.com"
                },
                {
                    id : 3,
                    name : "petter",
                    email : "example@gmail.com"
                },
            ]
        }
    },
    methods : {
        clickHandler() {
            this.show = !this.show
        }
    },
}
</script>