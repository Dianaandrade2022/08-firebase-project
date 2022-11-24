<template>
    <div class="card horizontal">
        <div class="card-stacked">
            <div class="card-content">
                <span class="card-title">{{data.name}}</span>
                <p>{{data.description}}</p>
                <p>
                    Tecnologías:
                </p>
            </div>
            <div class="card-action">
                <a href="#" class="amber darken-3 col s5 waves-effect waves-light btn"><i class="material-icons">create</i></a>
                <a href="#" class="red darken-3 col s5 waves-effect waves-light btn"><i class="material-icons">delete</i></a>
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