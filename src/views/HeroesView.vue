<template>
    <v-container>
        <v-row>
            <h1 class="title">Heroes</h1>
        </v-row>
        <v-row>
            <div class="icons">
                <span><v-icon class="mr-3">mdi-security</v-icon></span>
                <span><v-icon class="mr-3">mdi-adjust</v-icon></span>
                <span><v-icon class="mr-3">mdi-hospital</v-icon></span>
                <span><v-icon class="mr-3">mdi-sword</v-icon></span>
                <span><v-icon class="mr-3">mdi-tent</v-icon></span>
                <span><v-icon class="mr-3">mdi-hand</v-icon></span>
            </div>
        </v-row>
        <v-row class="content-heroes">
            <div class="table-container">
                <table class="full-width-table">
                    <thead>
                        <tr>
                            <th>Heroes</th>
                            <th>Nombre</th>
                            <th>Funcion</th>
                            <th>Titulo</th>
                            <th>Ataque</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="hero in heroes" :key="hero.name">
                            <td><img :src="hero.image" :alt="hero.name" class="hero-image"></td>
                            <td>{{ hero.name }}</td>
                            <td>{{ hero.role }}</td>
                            <td>{{ hero.title }}</td>
                            <td>{{ hero.attack }}</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </v-row>
    </v-container>
</template>

<script>
export default {
    name: 'HeroesView',
    data: () => ({
        heroes: [
            {
                name: 'Artanis',
                role: 'Agresor',
                title: 'Jerarca de los Daelaam',
                attack: 111,
                image: 'https://static.heroesofthestorm.com/heroes/yrel/skins/light-of-hope-800.jpg',
            },
            {
                name: 'D.va',
                role: 'Guerrero',
                title: 'Piloto de Meka',
                attack: '22(meca) - 55(piloto)',
                image: 'https://static.heroesofthestorm.com/heroes/dva/skins/meka-pilot-800.jpg',
            },
            {
                name: 'Ragnaros',
                role: 'Agresor',
                title: 'El Señor del fuego',
                attack: '180',
                image: 'https://static.heroesofthestorm.com/heroes/ragnaros/skins/the-firelord-800.jpg',
            },
            {
                name: 'Yrel',
                role: 'Guerrero',
                title: 'Luz de la esperanza',
                attack: '155',
                image: 'https://static.heroesofthestorm.com/heroes/yrel/skins/light-of-hope-800.jpg',
            },
            {
                name: 'Ana',
                role: 'Guerrero',
                title: 'Francotiradora veterana',
                attack: '30',
                image: 'https://static.heroesofthestorm.com/heroes/ana/skins/veteran-sniper-800.jpg',
            },
            {
                name: 'Auriel',
                role: 'Sanadora',
                title: 'Arcángel de la esperanza',
                attack: '64',
                image: 'https://static.heroesofthestorm.com/heroes/ana/skins/veteran-sniper-800.jpg',
            },
            {
                name: 'Malfurion',
                role: 'Sanadora',
                title: 'Archidruida',
                attack: '60',
                image: 'https://static.heroesofthestorm.com/heroes/malfurion/skins/archdruid-800.jpg',
            },
            {
                name: 'Arthas',
                role: 'Tanque',
                title: 'El rey Exánime',
                attack: '95',
                image: 'https://static.heroesofthestorm.com/heroes/arthas/skins/the-lich-king-800.jpg',
            },
            {
                name: 'Johanna',
                role: 'Tanque',
                title: 'Cruzada de Zakarum',
                attack: '99',
                image: 'https://static.heroesofthestorm.com/heroes/johanna/skins/crusader-of-zakarum-800.jpg',
            },
            {
                name: 'Muradin',
                role: 'Tanque',
                title: 'Rey de la montaña',
                attack: '88',
                image: 'https://static.heroesofthestorm.com/heroes/muradin/skins/mountain-king-800.jpg',
            },
            {
                name: 'Illidan',
                role: 'Asesino cuerpo a cuerpo',
                title: 'El traidor',
                attack: '87',
                image: 'https://static.heroesofthestorm.com/heroes/illidan/skins/the-betrayer-800.jpg',
            },
            {
                name: 'Maiev',
                role: 'Asesino cuerpo a cuerpo',
                title: 'La celadora',
                attack: '145',
                image: 'https://static.heroesofthestorm.com/heroes/maiev/skins/the-warden-800.jpg',
            },
            {
                name: 'Zeratul',
                role: 'Asesino cuerpo a cuerpo',
                title: 'Prelado tétrico',
                attack: '131',
                image: 'https://static.heroesofthestorm.com/heroes/zeratul/skins/dark-prelate-800.jpg',
            },
            {
                name: 'Abathur',
                role: 'Apoyo',
                title: 'Maestro de evolución',
                attack: '27',
                image: 'https://static.heroesofthestorm.com/heroes/abathur/skins/evolution-master-800.jpg',
            },
            {
                name: 'Medivh',
                role: 'Apoyo',
                title: 'El ultimo guardián',
                attack: '83',
                image: 'https://www.hellofriki.com/wp-content/uploads/2016/05/medivh.jpg',
            },
            {
                name: 'Zarya',
                role: 'Apoyo',
                title: 'Defensora de Rusia',
                attack: '22',
                image: 'https://static.heroesofthestorm.com/heroes/zarya/skins/defender-of-russia-800.jpg',
            },
            {
                name: 'Nazeebo',
                role: 'Asesino a distancia',
                title: 'Médico brujo',
                attack: '92',
                image: 'https://static.heroesofthestorm.com/heroes/nazeebo/skins/heretic-witch-doctor-800.jpg',
            },
            {
                name: 'Genji',
                role: 'Asesino a distancia',
                title: 'Ninja cibernético',
                attack: '44',
                image: 'https://static.heroesofthestorm.com/heroes/genji/skins/cybernetic-ninja-800.jpg',
            },
            {
                name: 'Zagara',
                role: 'Asesino a distancia',
                title: 'Madre de la prole del enjambre',
                attack: '85',
                image: 'https://static.heroesofthestorm.com/heroes/zagara/skins/broodmother-of-the-swarm-800.jpg',
            },
        ],
    }),
};
</script>

<style scoped>
.title{
    color: white;
    font-size: 50px;
}
.icons{
    color: gray;
    font-size: 30px;
}
.content-heroes{
    display: flex;
    justify-content: center;
    margin-top: 60px;
}
.table-container {
    text-align: left;
    background-color: rgb(31, 30, 30);
    color: rgb(161, 161, 161);
    width: 100%;
    max-height: 500px;
    overflow-y: auto;
    padding: 10px;
    border-radius: 10px;
}
.full-width-table th, .full-width-table td {
    width: 10%;
    padding:5px;
    border-bottom: 1px solid rgb(83, 82, 82);
}
.hero-image {
    width: 120px;
    height: auto;
}
</style>