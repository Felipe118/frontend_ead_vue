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
                                <input type="email" name="email" placeholder="Email" required>
                            </div>
                            <div class="groupForm">
                                <i class="far fa-key"></i>
                                <input type="password" name="password" placeholder="Senha" required>
                                <i class="far fa-eye buttom"></i>
                            </div>
                            <button class="btn primary" type="submit" @click.prevent="auth">Login</button>
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

export default {
    name: 'Auth',
    components: {
        Content,
   
    },

    setup() {
        const store = useStore()
        //const login = () => router.push({name: 'campus.home'})

        const auth = () => {
            store.dispatch('auth', {
                email: 'lipebezerraa@gmail.com',
                password: '123'
            })
        }
        
        return {
            login
        }
    }
}
</script>