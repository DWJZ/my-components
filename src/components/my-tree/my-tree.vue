<template>
  <ul class="my-tree__warpper">
    <my-tree-node v-for='node of treeData' :nodeData='node' :key='node.label'/>
	</ul>
</template>

<script>
import MyTreeNode from "./my-tree-node.vue";

export default {
  name: "MyTree",
  components: {
    "my-tree-node": MyTreeNode
  },
  props: {
    treeData: Array
  }
};
</script>

<style lang='less'>
@left: -0.7em;

ul.my-tree__warpper,
ul.my-tree__warpper ul {
  margin: 0;
  padding: 0 0 0 2em;
}

ul.my-tree__warpper .my-tree__node {
  list-style: none;
  position: relative;
}

ul.my-tree__warpper > .my-tree__node:first-child:before {
  border-style: none none solid none;
}

ul.my-tree__warpper .my-tree__node:before {
  position: absolute;
  content: "";
  top: -0.01em;
  left: @left;
  width: 0.5em;
  height: 0.615em;
  border-style: none none solid solid;
  border-width: 0.05em;
  border-color: #aaa;
}

ul.my-tree__warpper .my-tree__node:not(:last-child):after {
  position: absolute;
  content: "";
  top: 0.7em;
  left: @left;
  bottom: 0;
  border-style: none none none solid;
  border-width: 0.05em;
  border-color: #aaa;
}
</style>


