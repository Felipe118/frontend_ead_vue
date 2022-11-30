<template>
    <div class="decor" style="background-image: url('images/building.jpg');">
        <div class="content">
            <span class="logo">
                <img :src="require('@/assets/images/logo.svg')" alt="Logo">
            </span>
            <span class="dots">
                <span></span>
                <span></span>
                <span></span>
            </span>
            <span class="description">
                <p>
                    Os melhores e mais completos cursos de Laravel do Brasil, cursos com projetos reais. Do zero ao
                    profissional.
                </p>
            </span>
            <span class="copyright fontSmall">
                Todos os Direitos reservados - <b>Especializati</b>
            </span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Content'
}
</script>