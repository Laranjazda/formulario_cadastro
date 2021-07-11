<template>
  <q-page class="flex flex-center bg-primary">
    <q-card class="my-card">
      <img src="../assets/cidade-verde.jpg">

      <q-card-section class="q-pt-none full-width">
            <q-input class="q-mt-sm"
                    outlined
                    v-model="login.email"
                    label="Email" />

            <q-input class="q-mt-sm"
                    v-model="login.password"
                    label="Password"
                    filled
                    :type="login.isPwd ? 'password' : 'text'"
                    >
              <template v-slot:append>
                <q-icon
                  :name="login.isPwd ? 'visibility_off' : 'visibility'"
                  class="cursor-pointer"
                  @click="login.isPwd = !login.isPwd"
                />
              </template>
            </q-input>
      </q-card-section>

      <q-card-actions class="full-width" >
          <q-btn class="full-width q-mx-sm" color="primary" label="Login" />
      </q-card-actions>
      <q-card-actions class="full-width" >
          <q-btn
          flat
          class="full-width q-mx-sm"
          color="primary"
          label="Recuperar Senha"
          @click="$router.push({name:'recoveryPassword'})"
          />
      </q-card-actions>

    </q-card>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  setup () {
    return {
      login: {
        email: '',
        password: '',
        isPwd: true

      }

    }
  }
}
</script>

<style lang="sass" scoped>
.my-card
  width: 450px
  height: auto
  display: flex
  flex-direction: column
  align-items: center
  background-color: #C1FFC1

.my-card.img
  width: 250px
  height: auto

</style>
