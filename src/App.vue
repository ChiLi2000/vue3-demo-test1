<template>
  <Button @click="open">hello</Button>
  <hr />
  <Switch v-model:value="switchValue" />
  <hr />
  <Tabs v-model:selected="tabSelected">
    <Tab title="tab1">内容1</Tab>
    <Tab title="tab2">内容2</Tab>
  </Tabs>
</template>

<script>
import { Button, Switch, Tabs, Tab, Dialog, openDialog } from "wheel-ui-chili";
import "wheel-ui-chili/dist/lib/wheel.css";
export default {
  name: "App",
  components: {
    Button,
    Switch,
    Tabs,
    Tab,
    Dialog,
  },
  data() {
    return {
      switchValue: false,
      tabSelected: "tab1",
    };
  },
  methods: {
    open() {
      openDialog({ title: "标题", content: "内容" });
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
