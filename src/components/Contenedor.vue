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
    projects:[],
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

        for (let index in data) {
          this.projects.push(data[index]);
          console.log(data[index]);
        }
        console.log(this.projects);

      },
    },
};
</script>

<style>

</style>