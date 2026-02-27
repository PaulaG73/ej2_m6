<template>
    <div class="mascota">
        <ol>
            <li v-for="mascota in data" :key="mascota.id">
                Nombre:{{ mascota.nombre }}
                Tipo:{{ mascota.tipo }}
                Edad:{{ mascota.edad }}
                Estado de vacuna:{{ mascota.vacunado }}
                <ul>
                    <li v-for="caracteristica, index in mascota.caracteristicas" :key="index">
                        {{ caracteristica }}
                    </li>

                </ul>
            </li>
        </ol>
    </div>
    

    <table>
        <thead>
            <tr>
                <th>Nombre</th>
                <th>Tipo</th>
                <th>Edad</th>
                <th>Vacunas</th>
                <th>Caracteristicas</th>

            </tr>
        </thead>
        <tbody>
            <tr v-for="mascota in data" :key="mascota.id">
                <td>{{ mascota.nombre }}</td>
                <td>{{ mascota.tipo }}</td>
                <td>{{ mascota.edad }}</td>
                <td>{{ mascota.vacunado === true ? "Sí" : "No" }}</td>
                <td>{{ mascota.caracteristicas }}</td>
            </tr>
        </tbody>
    </table>
</template>

<script setup>

const data = [
    { id: 1, nombre: "Pluma", tipo: "gato", edad: 10, vacunado: true, foto: "./assets/img/Leona.jpg", caracteristicas: ["maternal", "exótica", "conversadora"] },
    { id: 2, nombre: "Pelusa", tipo: "gato", edad: 9, vacunado: true, foto: "./assets/img/Leona.jpg", caracteristicas: ["maternal", "exótica", "conversadora"] },
    { id: 3, nombre: "Polvo", tipo: "gato", edad: 8, vacunado: true, foto: "./assets/img/Leona.jpg", caracteristicas: ["maternal", "exótica", "conversadora"] },
    { id: 4, nombre: "Manchita", tipo: "gato", edad: 8, vacunado: true, foto: "./assets/img/Leona.jpg", caracteristicas: ["maternal", "exótica", "conversadora"] },
    { id: 5, nombre: "Nieve", tipo: "gato", edad: 8, vacunado: true, foto: "./assets/img/Leona.jpg", caracteristicas: ["maternal", "exótica", "conversadora"] },
    { id: 6, nombre: "Dalí", tipo: "gato", edad: 7, vacunado: true, foto: "./assets/img/Leona.jpg", caracteristicas: ["maternal", "exótica", "conversadora"] },
    { id: 7, nombre: "Gala", tipo: "gato", edad: 7, vacunado: true, foto: "./assets/img/Leona.jpg", caracteristicas: ["maternal", "exótica", "conversadora"] },
    { id: 8, nombre: "Nala", tipo: "gato", edad: 6, vacunado: true, foto: "./assets/img/Leona.jpg", caracteristicas: ["maternal", "exótica", "conversadora"] },
    { id: 9, nombre: "Leona", tipo: "gato", edad: 4, vacunado: true, foto: "./assets/img/Leona.jpg", caracteristicas: ["maternal", "exótica", "conversadora"] },
    { id: 10, nombre: "Mía", tipo: "gato", edad: 3, vacunado: true, foto: "./assets/img/Leona.jpg", caracteristicas: ["maternal", "exótica", "conversadora"] },
    { id: 11, nombre: "Tom", tipo: "gato", edad: 2, vacunado: true, foto: "./assets/img/Leona.jpg", caracteristicas: ["maternal", "exótica", "conversadora"] },
    { id: 12, nombre: "Opa", tipo: "perro", edad: 10, vacunado: false, foto: "./assets/img/Leona.jpg", caracteristicas: ["maternal", "exótica", "conversadora"] }

]

</script>

<style scoped></style>