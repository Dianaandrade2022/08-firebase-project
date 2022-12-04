<template>
    <div class="card horizontal">
        <div class="card-stacked">
            <div class="card-content">
                <span class="card-title">{{data.title}}</span>
                <p>{{data.description}}</p>
                <p>
                    Tecnologías: {{data.langs}}
                </p>
            </div>
            <div class="card-action row justify-content-between">
            <router-link to="/reg-projects" class="col s5 waves-effect waves-light btn amber darken-1">
         <i class="material-icons">create</i>
            </router-link>
                <a class="col s5 waves-effect waves-light btn red darken-3">
                    <i class="material-icons">delete</i>
                </a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:{
        data:Object,
    },
};
</script>

<style>
a{
    margin: 0px 2vw;
}
</style>