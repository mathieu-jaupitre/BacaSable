<template>
  <div class="nav">
    <div class="nav-buttons">
      <ButtonNav label="Home" />
      <ButtonNav label="Galerie" />
      <ButtonNav label="Profil" />
      <ButtonNav label="Contact" />
    </div>
  </div>
</template>

<script>
import ButtonNav from '../components/ButtonNav.vue';

export default {
  name: 'NavBar',
  components: {
    ButtonNav,
  },
};
</script>

<style>
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #fff;
  padding: 10px 20px;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 9999;
}

.nav-logo img {
  height: 30px;
}

.nav-buttons {
  display: flex;
  align-items: center;
}

@media (max-width: 768px) {
  .nav {
    padding: 10px;
  }

  .nav-logo img {
    height: 25px;
  }

  .nav-buttons {
    display: none;
  }
}
</style>