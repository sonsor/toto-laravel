<template>
    <layout>
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-md-6">
                    <div class="card">

                        <div class="card-header text-center">Todo Description
                            <inertia-link class="btn btn-primary" href="/home">Back</inertia-link>
                        </div>

                        <div class="card-body">
                            <ul>

                                <li class="d-md-flex justify-content-between">
                                    {{ tasks['description'] }}
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>

    </layout>
</template>

<script>
import Layout from "../Shared/layout";

export default {
    props: {
        'tasks': Array,
    },
    components: {Layout},
}
</script>
