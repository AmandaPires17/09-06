<script>
import {v4 as uuid} from "uuid";
export default {
  data() {
    return {
      novo_jogador: "",
      jogadores: [
        {id: "d6aa0cb0-4232-49a3-8698-5131e28d94b6", name: "Jogador 1", idade: "X", timeid: "1", acoes:"?"  },
        {id: "54413720-559a-44c2-8019-06d360482c7d", name: "Jogador 2", idade: "X", timeid: "1", acoes:"?"  },
        {id: "2d66ac28-a63c-471c-b301-abacff8dd2fb", name: "Jogador 3", idade: "X", timeid: "2", acoes:"?"  },
        {id: "29da6b76-21f1-4df6-898c-e4705fd819df", name: "Jogador 4", idade: "X", timeid: "4", acoes:"?"  },
      ],
    };
  },
  methods: {
    salvar() {
      const novo_id=uuid();
      this.jogadores.push({
        id: novo_id,
        name: this.novo_jogadores,
      });
    },
  },
}
</script>
<template>
 <div class="container">
  <div class="title">
    <h2>Gerenciamento de jogadores</h2>
  </div>
  <div class="form-input">
    <input type="text" placeholder="Nome" v-model="novo_jogador" /> 
    <input type="text" placeholder="Time" v-model="">
    <button>salvar</button>
  </div>
  <div class="list-itens">
    <table>
      <thead>
        <tr>
          <th>ID</th>
          <th>Nome</th>
          <th>Idade</th>
          <th>Time ID</th>
          <th>Ações</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="jogador in jogadores" :key="jogador.id">
          <td>1</td>
          <td>Jogador 1</td>
          <td>X</td>
          <td>1</td>
          <td>???</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>
</template>
<style scoped>

</style>