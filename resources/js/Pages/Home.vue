<template>
    
    <div class="container">
        <div class="row menu">
            <Link href="/">Home</Link>
        </div>
        <div class="row">
            <div class="page-header">
                <h1>List of users</h1>
                <hr>
            </div>
        </div>
    </div>
    <div class="container">
        <div class="row">
            <ul>
                <div v-for="user in users">
                    <Link v-bind:href="'/friends/' + user.id">
                        <li>
                            <div class="name">
                                {{ user.firstName }} {{ user.surname }}
                            </div>
                            <div class="age">
                                {{ user.age }} years old
                            </div>
                            <div class="gender">
                                <small>{{ user.gender }}</small>
                            </div>
                        </li>
                    </Link>
                </div>
            </ul>
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            users: Array
        }
    }
</script>
    
<style>

</style>