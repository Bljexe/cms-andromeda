<template>
  <div id="app">
    <Header/>
    <Home/>
    <Footer/>
  </div>
</template>

<script>

import './assets/global.css';
import Header from './components/Header';
import Home from './pages/Home';
import Footer from './pages/Footer';


export default {
  name: 'App',
  components: {
    Header,
    Home,
    Footer
  }
}
</script>