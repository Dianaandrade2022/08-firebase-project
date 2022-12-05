<template>
    <div class="card horizontal z-depth-3 " v-for="(project, i) in data">
        <div class="card-stacked">
            <div class="card-content">
                <span class="card-title center-align">
                    Titulo:{{data[i].title}}
                </span>
                <p>{{data[i].description}}</p>
                <p>
                    Tecnologías:  {{data[i].langs[0]}} {{data[i].langs[1]}} {{data[i].langs[2]}} {{data[i].langs[3]}}
                </p>
            </div>
            <div class="card-action row">
            <router-link to="/reg-projects" class="col s5 waves-effect waves-light btn amber darken-1">
         <i class="material-icons">create</i>
            </router-link>
                <a @click="delete" class="col s5 waves-effect waves-light btn red darken-3">
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

</style>