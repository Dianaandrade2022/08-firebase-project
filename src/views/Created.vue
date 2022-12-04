<template>
  <div class="container">
    <div class="row">
        <form @submit.prevent="createdProjects" class="s12">
            <div class="row">
                <div class="input-field col s12">
                    <input type="text" class="validate" id="first_name" v-model="project.title">
                    <label for="first_name">Nombre del proyecto</label>
                </div>
                <div class="input-field col s12">
                    <input type="text" class="validate" id="description" v-model="project.description">
                    <label for="description">Descripcion del proyecto</label>
                </div>
               <p>
                <label >
                    <input type="checkbox" checked="checked"  v-model="project.langs" value="CSS">
                        <span>CSS</span>
                </label>
               </p>
               <p>
                <label >
                    <input type="checkbox" checked="checked"  v-model="project.langs" value="Javascript">
                        <span>Javascript</span>
                </label>
               </p>
               <p>
                <label >
                    <input type="checkbox" checked="checked"  v-model="project.langs" value="Vue">
                        <span>Vue</span>
                </label>
               </p>
                <p>
                    <label>
                        <input type="checkbox" checked="checked"  v-model="project.langs" value="HTML">
                        <span>HTML</span>
                    </label>
                </p>
                <button class="btn waves-effect waves-light col s12" type="submit" name="action">
                    <i class="material-icons right">send</i>
                </button>
            </div>
        </form>
        {{project}}
    </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
            project:{
                title:"",
                description:"",
                langs:[],
                status:true,
            },
        };
    },
    methods:{
        async createdProjects(){
            // console.log(this.project);
        const res = await fetch("https://crud-vue-4b-92ebf-default-rtdb.firebaseio.com/projects/project.json",
        {
            method:"POST",
            body:JSON.stringify(this.project),
        });
        // const data = await res.json();
        // this.projects = data;
        // console.log(data);

      },
    },
};
</script>

<style>

</style>