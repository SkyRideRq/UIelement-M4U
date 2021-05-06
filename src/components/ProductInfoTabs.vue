<template>
  <div class="container">
    <tabs
      :tabs="tabs"
      :currentTab="currentTab"
      :wrapper-class="'product-info-tabs'"
      :tab-class="'product-info-tabs__item'"
      :tab-active-class="'product-info-tabs__item_active'"
      :line-class="'product-info-tabs__active-line'"
      @onClick="handleClick"
    />
    <div class="content m-3 m-sm-5">
      <div v-if="currentTab === 'tab1'">
        Sed ut perspiciatis unde omnis iste natus error sit voluptatem
        accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab
        illo inventore veritatis et quasi architecto beatae vitae dicta sunt
        explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut
        odit aut fugit, sed quia consequuntur magni dolores eos qui ratione
        voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum
        quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam
        eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat
        voluptatem.
      </div>
      <div v-if="currentTab === 'tab2'">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
        velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
        occaecat cupidatat non proident, sunt in culpa qui officia deserunt
        mollit anim id est laborum.
      </div>
      <div v-if="currentTab === 'tab3'">
        At vero eos et accusamus et iusto odio dignissimos ducimus qui
        blanditiis praesentium voluptatum deleniti atque corrupti quos dolores
        et quas molestias excepturi sint occaecati cupiditate non provident,
        similique sunt in culpa qui officia deserunt mollitia animi, id est
        laborum et dolorum fuga.
      </div>
    </div>
  </div>
</template>

<script>
import Tabs from "vue-tabs-with-active-line";
const TABS = [
  {
    title: "Tab 1",
    value: "tab1",
  },
  {
    title: "Tab 2",
    value: "tab2",
  },
  {
    title: "Tab 3",
    value: "tab3",
  },
];
export default {
  name: "ProductInfoTabs",
  components: {
    Tabs,
  },
  data: () => ({
    tabs: TABS,
    currentTab: "tab1",
  }),
  methods: {
    handleClick(newTab) {
      this.currentTab = newTab;
    },
  },
};
</script>
