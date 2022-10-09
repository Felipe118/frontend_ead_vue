<template>
    <div>
        <div class="pageTitle">
            <span class="title">Meus Cursos</span>
            <span class="dots">
                <span></span>
                <span></span>
                <span></span>
            </span>
        </div>

        <div class="content">
            <ul class="listCourses">
                <card-course/>
            </ul>
        </div>
       
    </div>
  </template>
  
<script>
import  CardCourse from '@/views/home/components/CardCourse.vue'

  
  export default {
    name: 'HomeView',
    components: {
        CardCourse
    }
  }
  </script>
  