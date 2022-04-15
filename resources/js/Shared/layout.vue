<template>
    <div>
        <nav class="navbar navbar-expand-md navbar-light bg-white shadow-sm">
            <div class="container">
                <inertia-link class="navbar-brand" href="/home">TodoApp</inertia-link>

            </div>
        </nav>

        <main class="py-4">
            <slot/>
        </main>
    </div>
</template>

<script>
import axios from 'axios';


export default {
    computed: {
        userName() {
            return this.$page.props.auth.user.name
        }
    },
    methods: {
        logoutHandle: async function () {
            await axios.post('/logout', {});
            window.location.href = "/";
        },
    }
}

</script>
