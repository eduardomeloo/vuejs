<template>
    <header>
        <div class="container">
            <nav class="navbar navbar-expand">
                <a href="#" class="link navbar-brand mr-auto">
                    <img src="../../assets/logo.svg" alt="Meu Foco é TI"
                    class="img d-inline-block align-top" id="logo"> Futebol Club
                </a>
                <div class="links mr-2">
                    <a href="#" class="btn mr-5"
                        @click.prevent="$emit('change-component','home')">
                        Início
                    </a>

                    <a href="#" class="btn mr-5"
                        @click.prevent="$emit('change-component','news')">
                        Notícias
                    </a>

                    <a href="#" class="btn mr-5"
                        @click.prevent="$emit('change-component','home')">
                        Classificações
                    </a>

                    <select name="championship" id="select-championship" 
                        class="form-control" 
                        @change="$emit('select-championship', $event.target.value)">
                        <option value="">Selecione um Campeonato</option>
                        <option value="Campeonato Brasileiro" selected>Campeonato Brasileiro</option>
                        <option value="Campeonato Espanhol">Campeonato Espanhol</option>
                        <option value="Campeonato Inglês">Campeonato Inglês</option>
                        <option value="Campeonato Italiano">Campeonato Italiano</option>
                    </select>
                </div>
            </nav>
        </div>
    </header>
</template>
<script>
export default {
    name: 'MftHeader'
}
</script>
<style scoped>
    header {
        background-color: #000;
    }
    #logo {
        width: 150px;
        height: 100%;
    }
    .links {
        display: inline-flex;
    }
    .link {
        color: #D48E23;
        font-size: 30px;
        font-family: 'Rajdhani';
    }
    .links a {
        color: #fff;
    }
    .links a:focus {
        outline: none !important;
        box-shadow: none !important;
    }
</style>