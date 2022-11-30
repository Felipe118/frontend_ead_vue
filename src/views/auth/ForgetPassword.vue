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
                        
                            <button class="btn primary" type="submit">Recuperar</button>
                        </form>
                        <span>
                            <p class="fontSmall">Acessar ? 
                                <router-link  class="link primary" :to="{nane: 'auth'}">Clique Aqui</router-link>
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

export default {
    name:'ForgetPassword',
    components: {
        Content
    }
}
</script>