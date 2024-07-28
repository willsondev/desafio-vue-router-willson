<template>
  <div class="contacto">
    <h1>Contacto</h1>
    <form @submit.prevent="enviarMensaje">
      <div class="form-group">
        <label for="nombre">Nombre</label>
        <input type="text" id="nombre" v-model="nombre" required />
      </div>
      <div class="form-group">
        <label for="email">Email</label>
        <input type="email" id="email" v-model="email" required />
      </div>
      <div class="form-group">
        <label for="mensaje">Mensaje</label>
        <textarea id="mensaje" v-model="mensaje" required></textarea>
      </div>
      <button type="submit">Enviar</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'Contacto',
  data() {
    return {
      nombre: '',
      email: '',
      mensaje: '',
    };
  },
  methods: {
    enviarMensaje() {
      alert(`Mensaje enviado por ${this.nombre}`);
    },
  },
};
</script>

<style scoped>
.contacto {
  padding: 20px;
  max-width: 600px;
  margin: auto;
  font-family: Arial, sans-serif;
}

.contacto h1 {
  text-align: center;
  margin-bottom: 20px;
}

.form-group {
  margin-bottom: 15px;
}

.form-group label {
  display: block;
  margin-bottom: 5px;
  font-weight: bold;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 8px;
  box-sizing: border-box;
  border: 1px solid #ccc;
  border-radius: 4px;
}

button {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}
</style>
