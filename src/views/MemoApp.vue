<template>
  <h1>Vue メモ</h1>
  <button v-on:click="deleteAll" class="memo__delete_all">全て削除</button>
  <div id="app" class="memo-list">
    <h1>Vue メモアプリ</h1>
    <li v-for="(memo, index) in memos" v-bind:key="index" class="memo">
      {{ index }}:{{ memo.text }}
      <button v-on:click="deleteMemo(index)" class="memo__delete">削除</button>
    </li>
    <div class="add-memo-field">
      <input class="add-memo-field__input" type="text" v-model="inputMemo" />
      <button class="add-memo-field__button" v-on:click="addMemo">追加</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputMemo: "",
      memos: [],
    }
  },
  methods: {
    addMemo() {
      if (this.inputMemo !== "") {
        const memo = { text: this.inputMemo }
        this.memos.push(memo)
        this.inputMemo = ""
      }
    },
    deleteMemo(index) {
      this.memos.splice(index, 1)
    },
    deleteAll() {
      this.memos = ""
    },
  },
}
</script>

<style scoped>
.memo-list {
  padding-left: 5rem;
  padding-right: 5rem;
  display: flex;
  flex-direction: column;
  align-items: stretch;
  max-width: 512px;
  margin-left: auto;
  margin-right: auto;
}

.memo-list__container {
  padding: 0;
}

.memo {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.5rem;
  border-radius: 5px;
}

.memo:hover {
  color: white;
  background-color: #b23b61;
}

.memo__text {
  margin-left: 2rem;
  text-align: left;
}

.memo__text--done {
  text-decoration-line: line-through;
}

.memo__delete {
  margin-left: 1rem;
  padding: 0.5rem 0.5rem;
  border: solid 1px black;
  border-radius: 5px;
  background-color: white;
}

.memo__delete:hover {
  background-color: #b2ae3b;
  border-radius: 5px;
}

.add-memo-field {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.add-memo-field__input {
  padding: 10px;
}
.add-memo-field__button {
  padding: 0.5rem 0.5rem;
  border: solid 1px black;
  border-radius: 5px;
  background-color: white;
}

.add-memo-field__button:hover {
  background-color: #b2ae3b;
  border-radius: 5px;
}
</style>
