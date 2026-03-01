<template>
    <div class="mascota">
        <div v-for="mascota in data" :key="mascota.id">
            <div class="container">
                <div>
                    <img :src="getImageUrl(mascota.foto)" class="card-img">
                </div>
                <div>
                    <div class="card-body">
                        <h5 class="card-title">{{ mascota.nombre }}</h5>
                        <p class="card-text">Especie: {{ mascota.tipo }}</p>
                        <p class="card-text">Edad: {{ mascota.edad }}</p>
                        <p class="card-text">Vacunas al día: {{ mascota.vacunado === true ? "Sí" : "No" }}</p>
                        <h6 class="card-text">Características</h6>
                        <ul>
                            <li v-for="caracteristica, index in mascota.caracteristicas" :key="index" class="lista-item">
                                {{ caracteristica }}
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>


    </div>
</template>
<script setup>
const getImageUrl = (name) => {

    return require(`../assets/img/${name}`);
}
const data = [
    { id: 1, nombre: "Pluma", tipo: "gato", edad: "10 años", vacunado: true, foto: "Leona.jpg", caracteristicas: ["temerosa", "peleadora", "reclamona"] },
    { id: 2, nombre: "Pelusa", tipo: "gato", edad: "9 años", vacunado: true, foto: "Leona.jpg", caracteristicas: ["tímida", "maternal", "curiosa"] },
    { id: 3, nombre: "Polvo", tipo: "gato", edad: "8 años", vacunado: true, foto: "Leona.jpg", caracteristicas: ["regalón", "reclamón", "manipulador"] },
    { id: 4, nombre: "Manchita", tipo: "gato", edad: "8 años", vacunado: true, foto: "Leona.jpg", caracteristicas: ["independiente", "cariñosa", "dormilona"] },
    { id: 5, nombre: "Nieve", tipo: "gato", edad: "8 años", vacunado: true, foto: "Leona.jpg", caracteristicas: ["regalona", "juguetona", "dormilona"] },
    { id: 6, nombre: "Dalí", tipo: "gato", edad: "7 años", vacunado: true, foto: "Leona.jpg", caracteristicas: ["hambriento", "temeroso", "regalón"] },
    { id: 7, nombre: "Gala", tipo: "gato", edad: "7 años", vacunado: true, foto: "Leona.jpg", caracteristicas: ["habladora", "nerviosa", "salvaje"] },
    { id: 8, nombre: "Nala", tipo: "gato", edad: "6 años", vacunado: true, foto: "Leona.jpg", caracteristicas: ["dulce", "dependiente", "temerosa"] },
    { id: 9, nombre: "Leona", tipo: "gato", edad: "4 años", vacunado: true, foto: "Leona.jpg", caracteristicas: ["maternal", "exótica", "conversadora"] },
    { id: 10, nombre: "Mía", tipo: "gato", edad: "3 años", vacunado: true, foto: "Leona.jpg", caracteristicas: ["regañona", "independiente", "ágil"] },
    { id: 11, nombre: "Tom", tipo: "gato", edad: "2 años", vacunado: true, foto: "Leona.jpg", caracteristicas: ["curioso", "regalón", "juguetón"] },
    { id: 12, nombre: "Opa", tipo: "perro", edad: "10 años", vacunado: false, foto: "Leona.jpg", caracteristicas: ["hablador", "juguetón", "dormilón"] }

]

</script>

<style>
.mascota {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;

}

.container{
padding-top: 15px;
    gap: 5px;
    display: flex;
    border-radius: 1px;
    border-style: solid;
    border-color: black;

}

.card-title {
    font-style: italic;
}

.card-img {
    max-height: 220px;
}

.card-body {
    font-size: small;
    min-height: 200px;
    min-width: 300px;
}

.card-text {
    padding-left: 10px;
    text-align: start;
}
.lista-item{
text-align: start;
}



</style>
