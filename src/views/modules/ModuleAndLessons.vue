<template>
    <div>
        <div class="pageTitle">
            <span class="title">Curso X</span>
            <span class="dots">
                <span></span>
                <span></span>
                <span></span>
            </span>
        </div>

        <div class="content">
            <div class="container">

              <modules-component/>

                <div class="right">
                    <div class="content">

                        <player-component/>
                        <supports-lesson-component/>
                    </div>
                </div>
            </div>
        </div>
    </div>


</template>


<script>

import ModulesComponent from "@/views/modules/component/ModulesComponent.vue"
import PlayerComponent from "@//views/modules/component/PlayerComponent.vue"
import SupportsLessonComponent from "@//views/modules/component/SupportsLessonComponent.vue"

export default {
    name: "ModuleAndLessons",
    components: {
        ModulesComponent,
        PlayerComponent,
        SupportsLessonComponent
    }
}

</script>