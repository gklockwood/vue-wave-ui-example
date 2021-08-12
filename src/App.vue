<template>
    <w-app>
        <div id="nav">
            <router-link to="/">Home</router-link> |
            <router-link to="/about">About</router-link>
          </div>
          <router-view/>

          <w-button
          class="my12"
          @click="showDrawer = !showDrawer"
          outline
          color="primary">
          Show drawer
        </w-button>

            <w-drawer
                v-model="showDrawer"
                absolute
                width="160px">
                <w-button
                class="button--close"
                @click="showDrawer = false"
                sm
                outline
                round
                absolute
                color="primary"
                icon="wi-cross">
            </w-button>
</w-drawer>

         


        <w-flex class="wrap">
            <w-button class="ma1" bg-color="success">success</w-button>
            <w-button class="ma1" bg-color="error">error</w-button>
            <w-button class="ma1" bg-color="warning">warning</w-button>
            <w-button class="ma1" bg-color="info">info</w-button>
            <w-button class="ma1" bg-color="primary">primary</w-button>
            <w-button class="ma1" bg-color="secondary">secondary</w-button>
            <w-button class="ma1" bg-color="purple-light4">purple-light4</w-button>
          </w-flex>
      </w-app>

</template>

<script>
    import {
        ref,
        computed
    } from 'vue';
    export default {
        setup() {
            const showDrawer = ref(false)

            const position = computed(function() {
                return showDrawer.value || 'left'
            });

            return {
                showDrawer,
                position
            }
        }
    }
</script>

<style lang="scss">
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
    }
    
    #nav {
        padding: 30px;
        a {
            font-weight: bold;
            color: #2c3e50;
            &.router-link-exact-active {
                color: #42b983;
            }
        }
    }
</style>