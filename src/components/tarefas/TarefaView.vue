<template>
  <div>
    <v-list-item
      @click="salvarClique"
      :input-value="tarefa.concluido"
      :class="tarefa.concluido ? 'teal lighten-4' : 'white'"
    >
      <template v-slot:default="{}">
        <v-list-item-action>
          <v-checkbox :input-value="tarefa.concluido"></v-checkbox>
        </v-list-item-action>

        <v-list-item-content>
          <v-list-item-title>{{ tarefa.titulo }}</v-list-item-title>
          <v-list-item-subtitle>{{ tarefa.descricao }}</v-list-item-subtitle>
        </v-list-item-content>
      </template>
    </v-list-item>
  </div>
</template>

<script>
export default {
  props: ["tarefa"],
  methods: {
    salvarClique() {
      this.$emit("salvarClick");
    },
  },
};
</script>
