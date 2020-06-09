<template>
  <v-layout
    column
    justify-center
    align-center
  >
    <v-flex
      xs12
      sm8
      md6
    >
      <board-list />
    </v-flex>
  </v-layout>
</template>

<script>
import BoardList from '~/components/board/BoardList'

export default {
  components: {
    BoardList
  }
}
</script>
