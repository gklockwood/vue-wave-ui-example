<template>
    <w-app>
        <div id="nav">
            <router-link to="/">Home</router-link> |
            <router-link to="/about">About</router-link>
          </div>
          <router-view/>
        <!-- All your app content goes here. -->
      
        <!-- Also try to add a button! -->
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