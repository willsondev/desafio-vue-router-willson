<template>
  <div class="productos">
    <h1>Productos</h1>
    <ul>
      <li v-for="producto in productos" :key="producto.id">
        <div class="producto">
          <h2>{{ producto.nombre }}</h2>
          <p>{{ producto.precio }}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Productos',
  data() {
    return {
      productos: [
        { id: 1, nombre: 'Producto 1', precio: 1000 },
        { id: 2, nombre: 'Producto 2', precio: 1500 },
        { id: 3, nombre: 'Producto 3', precio: 2000 },
      ],
    };
  },
  
};
</script>

<style scoped>
.productos {
  padding: 20px;
  max-width: 800px;
  margin: auto;
  font-family: Arial, sans-serif;
}

.productos h1 {
  text-align: center;
  margin-bottom: 20px;
}

.productos ul {
  list-style: none;
  padding: 0;
}

.productos li {
  border-bottom: 1px solid #ddd;
  padding: 10px 0;
}

.producto {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.producto h2 {
  margin: 0;
  font-size: 1.2em;
}

.producto p {
  margin: 0;
  font-weight: bold;
  color: #2c3e50;
}
</style>
