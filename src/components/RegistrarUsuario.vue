<template>
<div class="container">
  <div class="form__top">
    <h2>Formulario <span>Registro</span></h2>
  </div>
  <form class="form__reg" action="">
    <input class="input" type="text" placeholder="&#128100;  Nombre" required autofocus>
    <input class="input" type="email" placeholder="&#9993;  Email" required>
    <input class="input" type="text" placeholder="&#128222;  Telefono" required>
    <input class="input" type="text" placeholder="&#8962;  Dirección" required>
    <div class="btn__form">
      <input class="btn__submit" type="submit" value="REGISTRAR">
      <input class="btn__reset" type="reset" value="LIMPIAR">
    </div>
  </form>
</div>
</template>

<script>
export default {
  name: 'RegistrarUsuario'
}
</script>

<style>

@import '../assets/css/main.css';

</style>
