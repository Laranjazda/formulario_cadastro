<template>
  <q-page padding class="flex flex-center bg-primary">
    <q-card class="my-card">
      <q-card-section class="q-pt-none full-width">
            <q-input class="q-mt-sm"
                    outlined
                    v-model="login.email"
                    label="Email" />
      </q-card-section>

      <q-card-actions class="full-width" >
          <q-btn class="full-width q-mx-sm" color="primary" label="Redefinir Senha" />
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
