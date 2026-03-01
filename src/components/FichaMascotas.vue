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
                            <li v-for="caracteristica, index in mascota.caracteristicas" :key="index"
                                class="lista-item">
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
    { id: 1, nombre: "Dalí", tipo: "gato", edad: "7 años", vacunado: true, foto: "Dalí.jpg", caracteristicas: ["hambriento", "temeroso", "regalón"] },
    { id: 2, nombre: "Gala", tipo: "gato", edad: "7 años", vacunado: true, foto: "Gala.jpg", caracteristicas: ["habladora", "nerviosa", "salvaje"] },
    { id: 3, nombre: "Leona", tipo: "gato", edad: "4 años", vacunado: true, foto: "Leona.jpg", caracteristicas: ["maternal", "exótica", "conversadora"] },
    { id: 4, nombre: "Manchita", tipo: "gato", edad: "8 años", vacunado: true, foto: "Manchita.jpg", caracteristicas: ["independiente", "cariñosa", "dormilona"] },
    { id: 5, nombre: "Mía", tipo: "gato", edad: "3 años", vacunado: true, foto: "Mía.jpg", caracteristicas: ["regañona", "independiente", "ágil"] },
    { id: 6, nombre: "Nala", tipo: "gato", edad: "6 años", vacunado: true, foto: "Nala.jpg", caracteristicas: ["dulce", "dependiente", "temerosa"] },
    { id: 7, nombre: "Nieve", tipo: "gato", edad: "8 años", vacunado: true, foto: "Nieve.jpg", caracteristicas: ["regalona", "juguetona", "dormilona"] },
    { id: 8, nombre: "Opa", tipo: "perro", edad: "10 años", vacunado: false, foto: "Opa.jpg", caracteristicas: ["hablador", "juguetón", "chistoso"] },
    { id: 9, nombre: "Pelusa", tipo: "gato", edad: "9 años", vacunado: true, foto: "Pelusa.jpg", caracteristicas: ["tímida", "maternal", "curiosa"] },
    { id: 10, nombre: "Pluma", tipo: "gato", edad: "10 años", vacunado: true, foto: "Pluma.jpg", caracteristicas: ["temerosa", "peleadora", "reclamona"] },
    { id: 11, nombre: "Polvo", tipo: "gato", edad: "8 años", vacunado: true, foto: "Polvo.jpg", caracteristicas: ["regalón", "reclamón", "manipulador"] },
    { id: 12, nombre: "Tom", tipo: "gato", edad: "2 años", vacunado: true, foto: "Tom.jpg", caracteristicas: ["curioso", "regalón", "juguetón"] },


]

</script>

<style>
.mascota {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;

}

.container {

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
    min-width: 165px;
}

.card-body {
    font-size: small;
    min-height: 200px;
    min-width: 200px;
}

.card-text {
    padding-left: 10px;
    text-align: start;
}

.lista-item {
    text-align: start;
}
</style>
