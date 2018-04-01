<template>
  <div id="app">
    <my-tree :treeData='treeData' />
  </div>
</template>

<script>
import Tree from "./components/my-tree/my-tree.vue";

export default {
  name: "app",
  data() {
    return {
      treeData: [
        {
          label: "1级菜单",
          children: [
            {
              label: "2级菜单"
            },
            {
              label: "2级菜单",
              children: [
                {
                  label: "3级菜单"
                },
                {
                  label: "3级菜单"
                }
              ]
            }
          ]
        },
        {
          label: "1级菜单",
          children: [
            {
              label: "2级菜单"
            },
            {
              label: "2级菜单"
            }
          ]
        }
      ]
    };
  },
  components: {
    "my-tree": Tree
  }
};
</script>

<style>

</style>
