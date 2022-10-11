<template>
    <div>
        <div class="pageTitle">
            <span class="title">{{}}</span>
            <span class="dots">
                <span></span>
                <span></span>
                <span></span>
            </span>
        </div>

        <div class="content">
            <ul class="listCourses">
                <card-course :title="'Curso Laravel com Vue.js'" :image="''" bgName="' bg-laravel'" />
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
  