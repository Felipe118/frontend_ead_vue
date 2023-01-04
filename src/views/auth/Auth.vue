<template>
    <section id="loginPage"   :style="{
            backgroundImage: 'url(' + require('@/assets/images/bgLogin.jpg') + ')'
        }">
        <div class="loginContent">
            <div class="loginCard">
               <Content />
                <div class="login">
                    <div class="content">
                        <span class="logo">
                            <img :src="require('@/assets/images/logoDark.svg')" alt="">
                        </span>
                        <span>
                            <p>Seja muito bem vindo!</p>
                        </span>
                        <span class="dots">
                            <span></span>
                            <span></span>
                            <span></span>
                        </span>
                        <span class="description">
                            Acesse nossa plataforma e desfrute de cursos completos para sua especialização.
                        </span>
                        <form action="/dist/index.html" method="">
                            <div class="groupForm">
                                <i class="far fa-envelope"></i>
                                <input type="email" name="email" placeholder="Email" v-model="email" required>
                            </div>
                            <div class="groupForm">
                                <i class="far fa-key"></i>
                                <input type="password" name="password" v-model="password" placeholder="Senha" required>
                                <i class="far fa-eye buttom"></i>
                            </div>
                            <button 
                            :class="[
                                'btn',
                                'primary',
                                loading ? 'loading' : ''
                            ]" 
                            type="submit" @click.prevent="auth">
                                <span v-if="loading">Enviando...</span>
                                <span v-else>Login</span>
                            </button>
                        </form>
                        <span>
                            <p class="fontSmall">Esqueceu sua senha? 
                                <router-link  class="link primary" :to="{name: 'forget.password'}">Clique Aqui</router-link>
                            </p>
                        </span>
                    </div>
                    <span class="copyright fontSmall">
                        Todos os Direitos reservados - <b>Especializati</b>
                    </span>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import Content from '@/views/auth/component/Content.vue'
//import router from '@/router'
import { useStore } from 'vuex'
import { ref } from '@vue/reactivity'
import router from '@/router'

export default {
    name: 'Auth',
    components: {
        Content,
   
    },

    setup() {
        const store = useStore()

        const email = ref("")
        const password = ref("")
        const loading = ref(false)
        

        const auth = () => {
            loading.value = true
            store.dispatch('auth', {
                email: email.value,
                password: password.value,
                device_name: 'vue3_web'
            })
            .then(() => router.push({name: 'campus.home'}))
            .catch(error => console.log(error))
            .finally(() =>   loading.value = false)
        }
        
        return {
            auth,
            email,
            password,
            loading
        }
    }
}
</script>