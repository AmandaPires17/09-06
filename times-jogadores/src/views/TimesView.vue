<script>
import {v4 as uuid} from "uuid";
export default {
  data() {
    return {
      novo_time: "",
      times: [
        {id: "935d917f-9612-4473-80f5-ebf77eaba923", name: "Time 1"},
        {id: "3aa79f04-9cf6-4248-b772-b831c1ea6c8e", name: "Time 2"},
        {id: "72f44dc5-f276-46c2-9463-ed058a8ef667", name: "Time 3"},
        {id: "b667a3b3-3fb7-40af-ad89-96ff020f955c", name: "Time 4"},
      ],
    };
  },
  methods: {
    salvar() {
      const novo_id=uuid();
      this.times.push({
        id: novo_id,
        name: this.novo_time,
      });
    },
  },
};
</script>

<template>
<div class="container">
  <div class="title">
    <h2>Gerenciamento de times</h2>
  </div>
  <div class="form-input">
    <input type="text" v-model="novo_time" />
    <button @click="salvar">salvar</button>
  </div>
  <div class="list-itens">
    
    <table>
      <thead>
        <tr>
          <th>ID</th>
          <th>Nome</th>
          <th>Ações</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="time in times" :key="time.id">
          <td>{{ time.id }}</td>
          <td>{{ time.name }}</td>
          <td>???</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>
</template>

<style></style>
