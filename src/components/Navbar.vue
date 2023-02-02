<template>
    <header>
        <span>VueJS</span>
        <menu>
            <ul>
                <li><a href="">Home</a></li>
                <li><a href="">About</a></li>
            </ul>
        </menu>
    </header>
</template>
<script>
export default {
    name : 'NavBar',
   
}
</script>

<style scoped>
span {
    font-weight: bold;
    font-size: 25px;
}
header {
    background: rgb(52, 158, 207);
    padding: 10px 4rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: #fff;

}
li {
    list-style-type: none;

}
a {
    text-decoration: none;
    color: inherit;
}
menu ul{
    display: flex;

}

menu li + li {
    margin-left: 1rem;
}
</style>
