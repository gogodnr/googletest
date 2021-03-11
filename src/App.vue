<template>
  <v-app>
    <!--
    <v-navigation-drawer app>
   
    </v-navigation-drawer>
    -->
    <!--
    <v-app-bar app>

    </v-app-bar>
    -->
    <!-- Sizes your content based upon application components -->
    <v-main>

      <!-- Provides the application the proper gutter -->
      <v-container fluid>

        <v-sheet
          color="white"
          elevation="4"
          height="700"
          outlined
          width="800"
          style="margin-left:30%; margin-top:10%"
        >      
        <v-img
        height="250"
        src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAMgAAADICAMAAACahl6sAAAAeFBMVEX///8LOor09vlVda3k6fIOPIsmUJedsNBtibkeSZMWQo+0w9vM1ueFncX3+fvU3OpFaaYYRZBhgLOcr9ARP42PpcnF0OOsvNekttPu8fcjTZUvV5t7lMBefbJvirrn7PR+l8FGaqYsVZq8yd83Xp/c4u6MoshPcauqo4xJAAAE/ElEQVR4nO2a2ZqiOhRGlUnmeRZxLt//DU+pJARIGCy7qz3fv67aFOxkhQw70KsVAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAv4crSZL7QXEFtUX6TpblUN+8t06v0sPvuLs6fWtYMZK8fiJLb41rmc+w6uatYcVAZAKIvApEJoDIq0Bkgn9HZK807Pu3FNc0i5w7UZYqfX/pedOGiBwUGojNHdyCVtCj+K5hWLovJjpaJJJdtCcnp1O/ktVHLYjVZyvj4HSrLKVz4/O2QG3immUTSNueaRT7a+efNB7l5byS9HJQfvLlKvdGZAQiudEUx1XBaKT1Nl73MS8Hr70mUgcXrHujbF+VwouMDdOmHrG2y4uVAL4I48EUX0UNULUDfSpikThvuqMSXrI28pVY5BtTtpeI8D2sS9sA1TQMw2R++2Tc5KVxpx1aBkFrLrHLbi8wlHnTJrawq32y5otQj8BpC90NrT/e6oll27aV7DRai9b0d2E/SOhktynNsEjoParhh4dkQ4g2z5zfPW9YIucQ+gE12fKfCUek9UiYeZ7TUNtEIeXu1dFIcZmxcUeW3wPtEN0u5p2C3OK8M8ltIfeeoQjfIz2RXpS9ToDU53bViEhNbtCXbF2SQ5YZg/tIBiLUw2A9Cjr/jkovgn2hXcVOKLGITjrqPPjTGMWN1JPMEHET6pGzTzAjD7YcHl1zk9OyGSL8nhVD51Y9LeImZCYYOXuVG9LhMByg7WrJ1PAHREhI/iTpiIg8Vsq2KTd5ix/dOi7tdvUnRbhpISvSemhZ96qU/uHKiWGT4Vi268CPRSTFtvIoShxKGLdNHRVpPQabDp0iPi9FUMgSzEySn4lIqSNvDTPu74azRFyLeARZ/6qNOhZjzxl4PxI5y4E4i5l+Igr5Zycx6Yrc/oZI3s1hFousPLK3DUzoPLtwhxap+D1D60w91PIoy3qtP6hvo8Ois2oxJt0G86YzUzMZk2W7FLwu0q7mpeMVzOvj+asWY6LqHZM92b1j3snVITX7w+WXsw1PiNBOC7pbwCKRVUpa3DOp1uIge5ptOZxaq6UiGVllb71hvEhkZdNnErKH9ZSMWzMfhPgiNWvMuBupdUIkEmUiy0SY0SUz6aFLH8mpn2xZxFE9sOZ0Cx3Mqrki/WxooYjA5Npm6zkbp4jogeTG5sV0k1TrfrVzh9all0UsFRGY0NmzDsJz82bHVTKZnnf8TtdLO1Ieh2m34gkRj3ZB2H1rsliEMbkxjWtPUOvgon9t8qTabamGeuwNIZonfB9ob9U9V/q6zhJx6cFL1eTaeSHXYjqFtpnt5mtIm32vJWaziKDun7fcQ//FEdn3pzbE63E9znwRgYmU3Uxu5EC2OMcUp5dpkL1xMkXxZH41L4iwJmx1RaZve5Wo5lY/cw/fbqqf2KdC3mtNJ41FLpfDF4HjIm70zGT0qNun3pHcdumst9/z29n5mmGYZmCUmh86liJ8E+JeM+eRKdWPL7xNw7P7D1kOq/5oZJC83Kmf1w35WvQB+iqrXJN7+wrFsy3rbHvKzNc5j2/uUufHjE/wz+uGLPyQrohNPozWRPSa8lNoTTSY/CMwJsOs96NoTYz/j8mb///Q30Y5kH1IH9nAPgK6Ef12QwAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAPh9/gPOwUyJLtygpAAAAABJRU5ErkJggg=="
        ></v-img>
            <form>
                  <v-text-field v-model="name" :error-messages="nameErrors" :counter="10" label="Name" 
                  maxwidth="100" required @input="$v.name.$touch()" @blur="$v.name.$touch()">
                  </v-text-field>
                  <v-text-field v-model="email" :error-messages="emailErrors" label="E-mail" 
                  maxwidth="100" required @input="$v.email.$touch()" @blur="$v.email.$touch()">
                  </v-text-field>
                  <v-checkbox v-model="checkbox" :error-messages="checkboxErrors" label="Do you agree?" required @change="$v.checkbox.$touch()" @blur="$v.checkbox.$touch()">
                  </v-checkbox>
              
                  <v-btn
                    class="mr-4"
                    @click="submit"
                  >
                    submit
                  </v-btn>
                  <v-btn @click="clear">
                    clear
                  </v-btn>
                </form>
        </v-sheet>
      </v-container>
    </v-main>

    <v-footer app>
      <!-- -->
    </v-footer>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  components: {
  },

  data: () => ({
    //
  }),
};
</script>
