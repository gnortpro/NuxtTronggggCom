<template>
  <div class="container">
    <div id="topbar">
      <header role="navigation" class="navbar bd-navbar flex-column flex-md-row navbar-dark navbar-expand" data-v-1c904aae=""><a href="/" aria-label="BootstrapVue" target="_self" class="navbar-brand mr-0 mr-md-2" data-v-1c904aae=""><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 612 612" width="36" height="36" focusable="false" role="img" class="d-block" data-v-1c904aae=""><title data-v-1c904aae="">BootstrapVue</title> <g fill="currentColor" data-v-1c904aae=""><path fill-rule="nonzero" d="M510,8 C561.846401,8.16468012 603.83532,50.1535995 604,102 L604,510 C603.83532,561.846401 561.846401,603.83532 510,604 L102,604 C50.1535995,603.83532 8.16468012,561.846401 8,510 L8,102 C8.16468012,50.1535995 50.1535995,8.16468012 102,8 L510,8 L510,8 Z M510,0 L102,0 C45.9,6.21724894e-15 0,45.9 0,102 L0,510 C0,566.1 45.9,612 102,612 L510,612 C566.1,612 612,566.1 612,510 L612,102 C612,45.9 566.1,6.21724894e-15 510,0 Z" data-v-1c904aae=""></path> <text id="BV" font-family="Arial" font-size="350" font-weight="light" letter-spacing="2" data-v-1c904aae=""><tspan x="72.0527344" y="446" data-v-1c904aae="">B</tspan> <tspan x="307.5" y="446" data-v-1c904aae="">V</tspan></text></g></svg></a> <div class="navbar-nav-scroll" data-v-1c904aae=""><ul is-nav="" class="navbar-nav bd-navbar-nav flex-row" data-v-1c904aae=""><li class="nav-item" data-v-1c904aae=""><a href="/docs" target="_self" class="nav-link nuxt-link-exact-active active" data-v-1c904aae="">Docs</a></li> <li class="nav-item" data-v-1c904aae=""><a href="/docs/components" target="_self" class="nav-link" data-v-1c904aae="">Components</a></li> <li class="nav-item" data-v-1c904aae=""><a href="/docs/directives" target="_self" class="nav-link" data-v-1c904aae="">Directives</a></li> <li class="nav-item" data-v-1c904aae=""><a href="/docs/reference" target="_self" class="nav-link" data-v-1c904aae="">Reference</a></li> <li class="nav-item" data-v-1c904aae=""><a href="/docs/misc" target="_self" class="nav-link" data-v-1c904aae="">Misc</a></li> <li class="nav-item" data-v-1c904aae=""><a href="/play" target="_self" class="nav-link" data-v-1c904aae="">Play</a></li></ul></div> <ul class="navbar-nav flex-row ml-md-auto d-none d-md-flex" data-v-1c904aae=""><li class="nav-item b-nav-dropdown dropdown" data-v-1c904aae="" id="__BVID__20"><a aria-haspopup="true" aria-expanded="false" target="_self" href="#" class="nav-link dropdown-toggle mr-md-2" id="__BVID__20__BV_button_"><span>v2.0.0-rc.27</span></a><ul tabindex="-1" class="dropdown-menu dropdown-menu-right" aria-labelledby="__BVID__20__BV_button_"><li data-v-1c904aae=""><a role="menuitem" target="_self" href="https://bootstrap-vue.js.org" class="dropdown-item active">
          Latest (v2.0.0-rc.27)
        </a></li> <li data-v-1c904aae=""><a role="menuitem" rel="nofollow" target="_self" href="https://bootstrap-vue.netlify.com" class="dropdown-item">
          Development
        </a></li></ul></li> <li class="nav-item" data-v-1c904aae=""><a aria-label="GitHub" rel="noopener" target="_blank" href="https://github.com/bootstrap-vue/bootstrap-vue" class="nav-link" data-v-1c904aae=""><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 32 32" width="32" height="32" focusable="false" role="img" class="navbar-nav-svg" data-v-1c904aae=""><title data-v-1c904aae="">GitHub</title> <g fill="currentColor" data-v-1c904aae=""><path fill-rule="evenodd" clip-rule="evenodd" d="M16,0.4c-8.8,0-16,7.2-16,16c0,7.1,4.6,13.1,10.9,15.2 c0.8,0.1,1.1-0.3,1.1-0.8c0-0.4,0-1.4,0-2.7c-4.5,1-5.4-2.1-5.4-2.1c-0.7-1.8-1.8-2.3-1.8-2.3c-1.5-1,0.1-1,0.1-1 c1.6,0.1,2.5,1.6,2.5,1.6c1.4,2.4,3.7,1.7,4.7,1.3c0.1-1,0.6-1.7,1-2.1c-3.6-0.4-7.3-1.8-7.3-7.9c0-1.7,0.6-3.2,1.6-4.3 c-0.2-0.4-0.7-2,0.2-4.2c0,0,1.3-0.4,4.4,1.6c1.3-0.4,2.6-0.5,4-0.5c1.4,0,2.7,0.2,4,0.5C23.1,6.6,24.4,7,24.4,7 c0.9,2.2,0.3,3.8,0.2,4.2c1,1.1,1.6,2.5,1.6,4.3c0,6.1-3.7,7.5-7.3,7.9c0.6,0.5,1.1,1.5,1.1,3c0,2.1,0,3.9,0,4.4 c0,0.4,0.3,0.9,1.1,0.8C27.4,29.5,32,23.5,32,16.4C32,7.6,24.8,0.4,16,0.4z" data-v-1c904aae=""></path></g></svg></a></li> <li class="nav-item" data-v-1c904aae=""><a aria-label="Twitter" rel="noopener" target="_blank" href="https://twitter.com/BootstrapVue" class="nav-link" data-v-1c904aae=""><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 32 32" width="32" height="32" focusable="false" role="img" class="navbar-nav-svg" data-v-1c904aae=""><title data-v-1c904aae="">Twitter</title> <g fill="currentColor" data-v-1c904aae=""><path d="M32,6.1c-1.2,0.5-2.4,0.9-3.8,1c1.4-0.8,2.4-2.1,2.9-3.6c-1.3,0.8-2.7,1.3-4.2,1.6C25.7,3.8,24,3,22.2,3 c-3.6,0-6.6,2.9-6.6,6.6c0,0.5,0.1,1,0.2,1.5C10.3,10.8,5.5,8.2,2.2,4.2c-0.6,1-0.9,2.1-0.9,3.3c0,2.3,1.2,4.3,2.9,5.5 c-1.1,0-2.1-0.3-3-0.8c0,0,0,0.1,0,0.1c0,3.2,2.3,5.8,5.3,6.4c-0.6,0.1-1.1,0.2-1.7,0.2c-0.4,0-0.8,0-1.2-0.1 c0.8,2.6,3.3,4.5,6.1,4.6c-2.2,1.8-5.1,2.8-8.2,2.8c-0.5,0-1.1,0-1.6-0.1C2.9,27.9,6.4,29,10.1,29c12.1,0,18.7-10,18.7-18.7 c0-0.3,0-0.6,0-0.8C30,8.5,31.1,7.4,32,6.1z" data-v-1c904aae=""></path></g></svg></a></li> <li class="nav-item" data-v-1c904aae=""><a aria-label="Discord" rel="noopener" target="_blank" href="https://discord.gg/j2Mtcny" class="nav-link" data-v-1c904aae=""><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 32 32" width="32" height="32" focusable="false" role="img" class="navbar-nav-svg" data-v-1c904aae=""><title data-v-1c904aae="">Discord</title> <g fill="currentColor" data-v-1c904aae=""><path d="M13.1,13.424a1.782,1.782,0,0,0,0,3.552A1.7,1.7,0,0,0,14.736,15.2,1.694,1.694,0,0,0,13.1,13.424Zm5.84,0A1.782,1.782,0,1,0,20.576,15.2,1.7,1.7,0,0,0,18.944,13.424Z" data-v-1c904aae=""></path> <path d="M26.72,0H5.28A3.288,3.288,0,0,0,2,3.3V24.928a3.288,3.288,0,0,0,3.28,3.3H23.424l-.848-2.96,2.048,1.9L26.56,28.96,30,32V3.3A3.288,3.288,0,0,0,26.72,0ZM20.544,20.9s-.576-.688-1.056-1.3a5.049,5.049,0,0,0,2.9-1.9,9.156,9.156,0,0,1-1.84.944,10.531,10.531,0,0,1-2.32.688,11.208,11.208,0,0,1-4.144-.016,13.431,13.431,0,0,1-2.352-.688A9.6,9.6,0,0,1,9.9,17.68a4.976,4.976,0,0,0,2.8,1.888c-.48.608-1.072,1.328-1.072,1.328a5.8,5.8,0,0,1-4.88-2.432,21.426,21.426,0,0,1,2.3-9.328,7.912,7.912,0,0,1,4.5-1.68l.16.192A10.794,10.794,0,0,0,9.5,9.744s.352-.192.944-.464A12.015,12.015,0,0,1,14.08,8.272a1.576,1.576,0,0,1,.272-.032,13.538,13.538,0,0,1,3.232-.032A13.043,13.043,0,0,1,22.4,9.744a10.648,10.648,0,0,0-3.984-2.032l.224-.256a7.912,7.912,0,0,1,4.5,1.68,21.426,21.426,0,0,1,2.3,9.328A5.849,5.849,0,0,1,20.544,20.9Z" data-v-1c904aae=""></path></g></svg></a></li> <li class="nav-item" data-v-1c904aae=""><a aria-label="Open Collective" rel="noopener" target="_blank" href="https://opencollective.com/bootstrap-vue/" class="nav-link" data-v-1c904aae=""><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 40 41" width="32" height="32" fill="currentColor" fill-rule="evenodd" focusable="false" role="img" class="navbar-nav-svg" data-v-1c904aae=""><title data-v-1c904aae="">Open Collective</title> <path fill-opacity=".4" d="M32.8 21c0 2.4-.8 4.9-2 6.9l5.1 5.1c2.5-3.4 4.1-7.6 4.1-12 0-4.6-1.6-8.8-4-12.2L30.7 14c1.2 2 2 4.3 2 7z" data-v-1c904aae=""></path> <path d="M20 33.7a12.8 12.8 0 0 1 0-25.6c2.6 0 5 .7 7 2.1L32 5a20 20 0 1 0 .1 31.9l-5-5.2a13 13 0 0 1-7 2z" data-v-1c904aae=""></path></svg></a></li></ul></header>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
