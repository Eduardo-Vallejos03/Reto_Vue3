<template>
    <a :href="url" class="button">{{ label }}</a>
</template>

<script>
export default {
    name: 'ProductButtons',
    props: {
    label: {
      type: String,
      default: 'Detalles'
    },
    url: String
  }
}
</script>

<style>

.button {
  background-color: #fff;
  color: #000;
  font-size: 14px;
  font-weight: bold;
  padding: 10px;
  border-radius: 5px;
  border: 0.2px solid #BDBDBD;
  cursor: pointer;
  transition: box-shadow 0.3s ease-in-out;
  margin: 8px;
  text-decoration: none;
  display: inline-block;
}

.button:hover {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
}

</style>