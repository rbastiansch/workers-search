<template>
  <div id="app">
    <CHeader></CHeader>
    <CPrincipal></CPrincipal>
  </div>
</template>

<script>
import CHeader from './components/Header';
import CPrincipal from './components/Principal';

export default {
  name: 'app',
  components: {
    CHeader,
    CPrincipal,
  },
};
</script>
