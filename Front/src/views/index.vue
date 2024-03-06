<template>
    <div>
        <h1>CRUD de Animales</h1>

        <!-- Formulario para Crear -->
        <h2>Crear Animal</h2>
        <form @submit.prevent="crearAnimal">
            <input type="text" v-model="nombreAnimalCrear" placeholder="Nombre del animal">
            <select v-model="tipoAnimalCrear">
                <option value="mamifero">Mamífero</option>
                <option value="reptil">Reptil</option>
            </select>
            <button type="submit">Crear</button>
        </form>

        <!-- Formulario para Actualizar -->
        <h2>Actualizar Animal</h2>
        <form @submit.prevent="actualizarAnimal">
            <input type="text" v-model="nombreAnimalActualizar" placeholder="Nombre del animal">
            <select v-model="tipoAnimalActualizar">
                <option value="mamifero">Mamífero</option>
                <option value="reptil">Reptil</option>
            </select>
            <button type="submit">Actualizar</button>
        </form>

        <!-- Formulario para Eliminar -->
        <h2>Eliminar Animal</h2>
        <form @submit.prevent="eliminarAnimal">
            <input type="text" v-model="nombreAnimalEliminar" placeholder="Nombre del animal">
            <button type="submit">Eliminar</button>
        </form>
    </div>
</template>

<script>
export default {
    data() {
        return {
            nombreAnimalCrear: '',
            tipoAnimalCrear: '',
            nombreAnimalActualizar: '',
            tipoAnimalActualizar: '',
            nombreAnimalEliminar: ''
        }
    },
    methods: {
        crearAnimal() {
            console.log(this.nombreAnimalCrear, this.tipoAnimalCrear);
            // Aquí puedes hacer la petición a tu API
        },
        actualizarAnimal() {
            console.log(this.nombreAnimalActualizar, this.tipoAnimalActualizar);
            // Aquí puedes hacer la petición a tu API
        },
        eliminarAnimal() {
            console.log(this.nombreAnimalEliminar);
            // Aquí puedes hacer la petición a tu API
        }
    }
}
</script>

<style lang="scss" scoped>

</style>