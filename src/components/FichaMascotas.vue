<template>
    <div class="mascota">
        <div v-for="mascota in data" :key="mascota.id" class="card mb-3" style="max-width: 540px;">
            <div class="container">
                <div>
                    <img :src="getImageUrl(mascota.foto)" class="card-img">
                </div>
                <div>
                    <div class="card-body">
                        <h5 class="card-title">{{ mascota.nombre }}</h5>
                        <p class="card-text">{{ mascota.tipo }}</p>
                        <p class="card-text">{{ mascota.edad }}</p>
                        <p class="card-text">{{ mascota.vacunado === true ? "Sí" : "No" }}</p>
                        <ul>
                            <li v-for="caracteristica, index in mascota.caracteristicas" :key="index">
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
const getImageUrl =(name) =>{

return require(`../assets/img/${name}`);
}
const data = [
    { id: 1, nombre: "Pluma", tipo: "gato", edad: 10, vacunado: true, foto: "Leona.jpg", caracteristicas: ["temerosa", "peleadora", "reclamona"] },
    { id: 2, nombre: "Pelusa", tipo: "gato", edad: 9, vacunado: true, foto: "Leona.jpg", caracteristicas: ["tímida", "maternal", "curiosa"] },
    { id: 3, nombre: "Polvo", tipo: "gato", edad: 8, vacunado: true, foto: "Leona.jpg", caracteristicas: ["regalón", "reclamón", "manipulador"] },
    { id: 4, nombre: "Manchita", tipo: "gato", edad: 8, vacunado: true, foto: "Leona.jpg", caracteristicas: ["independiente", "cariñosa", "dormilona"] },
    { id: 5, nombre: "Nieve", tipo: "gato", edad: 8, vacunado: true, foto: "Leona.jpg", caracteristicas: ["regalona", "juguetona", "dormilona"] },
    { id: 6, nombre: "Dalí", tipo: "gato", edad: 7, vacunado: true, foto: "Leona.jpg", caracteristicas: ["hambriento", "temeroso", "regalón"] },
    { id: 7, nombre: "Gala", tipo: "gato", edad: 7, vacunado: true, foto: "Leona.jpg", caracteristicas: ["habladora", "nerviosa", "salvaje"] },
    { id: 8, nombre: "Nala", tipo: "gato", edad: 6, vacunado: true, foto: "Leona.jpg", caracteristicas: ["dulce", "dependiente", "temerosa"] },
    { id: 9, nombre: "Leona", tipo: "gato", edad: 4, vacunado: true, foto: "Leona.jpg", caracteristicas: ["maternal", "exótica", "conversadora"] },
    { id: 10, nombre: "Mía", tipo: "gato", edad: 3, vacunado: true, foto: "Leona.jpg", caracteristicas: ["regañona", "independiente", "ágil"] },
    { id: 11, nombre: "Tom", tipo: "gato", edad: 2, vacunado: true, foto: "Leona.jpg", caracteristicas: ["curioso", "regalón", "juguetón"] },
    { id: 12, nombre: "Opa", tipo: "perro", edad: 10, vacunado: false, foto: "Leona.jpg", caracteristicas: ["hablador", "juguetón", "dormilón"] }

]

</script>

<style scoped>
.mascota{
  display: flex;  
 flex-wrap: wrap;
}
.container{
display: flex;


}
.card-img{
    max-height: 300px;
}

</style>