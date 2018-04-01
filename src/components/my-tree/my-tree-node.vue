<template>
  <li class='my-tree__node'>
    {{nodeData.label}}
    <ul v-if='nodeData.children && nodeData.children.length > 0' >
      <my-tree-node v-for='node of nodeData.children' :nodeData='node' :key='node.label'/>
    </ul>
  </li>
</template>

<script>
export default {
  name: "MyTreeNode",
  props: {
    nodeData: Object
  }
};
</script>

<style lang='less'>

</style>


