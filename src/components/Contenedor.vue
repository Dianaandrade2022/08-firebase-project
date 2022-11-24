<template>
  <div class="row">
    <div class="col s12 m7">
        
        <card-project :data="projects"/>
    </div>
  </div>
</template>

<script>
    import CardProject from './CardProject.vue'
export default {
  data:()=>({
    projects:String,
  }),
    components:{
        CardProject,
    },
    mounted(){
      this.getProjects()

    },methods:{
      async getProjects(){
        const res = await fetch("https://crud-vue-4b-92ebf-default-rtdb.firebaseio.com/projects/project.json");
        const data = await res.json();
        this.projects = data;
        console.log(data);
        console.log(this.projects);

      },
    },
};
</script>

<style>

</style>