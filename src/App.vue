<template>
  <div class="app" :class="isDark === true ? 'dark-theme' : 'light-theme'">
    <header class="header mb-4 animate fadeDown delay-1">
      <div class="mb-2">
        <h1 class="font-bold uppercase">
          space<span class="font-bold uppercase title-span">2u</span>
        </h1>
        <h2 class="font-bold">Space Építész Iroda Kft.</h2>
      </div>
      <TheContact :address="address" :email="email" :maps-link="mapsLink" />
    </header>

    <main class="main mb-4 animate fadeLeft delay-3">
      <TheContent :content="content" />
      <span class="font-bold uppercase red-soft">hamarosan ...</span>
    </main>

    <footer class="footer mb-2 d-flex animate fadeDown delay-5">
      <p class="mb-1 font-bold mr-2 caption">
        &#169;{{ new Date().getFullYear() }} — SPACE2U
      </p>
      <p class="mb-1 caption grey-light">
        A weboldal teljes tartalma szerzői jogvédelem alatt áll. Minden jog
        fenntartva.
      </p>
    </footer>
    <ModeToggle
      class="animate fadeDown delay-3"
      :isDark="isDark"
      @toggle="toggle"
    />
  </div>
</template>

<script>
import TheContact from './components/TheContact.vue';
import TheContent from './components/TheContent.vue';
import ModeToggle from './components/ModeToggle.vue';

export default {
  components: {
    TheContact,
    TheContent,
    ModeToggle,
  },
  data() {
    return {
      isDark: false,
      address: '9022 Győr, Sarló köz 15. 2/5',
      email: 'hello@space2u.hu',
      content:
        'SPACE [speis] I.n, 1: a) hely, tér, térköz, közbenső tér, köz; ~ időbeli és térbeli feltételek / viszonyok; b) kiterjedés, terjedelem, terület; c) világűr, űr, a végtelen űr; d) (menny, fiz) tér; n~n dimenziós tér, ~axes térbeli koordinátarendszerek, 2: időszak, időköz, ~ lélegzetvételnyi idő, 3: szabad terület/tér, távolság, táv, térköz; folyosó; open ~ térség, ~ saving takarékoskodás hellyel, helymegtakarítás; ~ tárgyak közötti távolság; leave ~ for… helyet hagy vmnek, 4: a) betűköz, szóköz; II. vt, 1: ~(out) (i) elhelyez, elrendez, felállít; (ii) eloszt, feloszt, szétoszt; tágít. A dolgok közötti láthatatlan kapcsolat.',
      mapsLink: 'https://goo.gl/maps/PbvLZxVpEvuLseiV6',
    };
  },
  methods: {
    toggle() {
      this.isDark = !this.isDark;
    },
  },
};
</script>

<style></style>
