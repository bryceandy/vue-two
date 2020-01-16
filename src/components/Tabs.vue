<template>
  <div>
    <div class="tabs">
      <ul>
        <li :key="tab.index" v-for="tab in tabs" :class="{'is-selected': tab.isActive}">
          <a :href="tab.href" @click="selectTab(tab)">{{ tab.name }}</a>
        </li>
      </ul>
    </div>
    <hr>
    <div class="tab-details">
      <slot />
    </div>
  </div>
</template>

<script>
    export default {
        name: "Tabs",
        data() {
            return {
                tabs: []
            }
        },
        created() {
            this.tabs = this.$children
        },
        methods: {
            selectTab(currentTab) {
                this.tabs.forEach((tab) => tab.isActive = (currentTab.name === tab.name))
            }
        }
    }
</script>

<style scoped>
  .tabs {
    text-align: right
  }
  ul {
    padding-inline-start: 0
  }
  ul li {
    display: inline-block
  }
  ul li a {
    text-decoration: none;
    color: darkgray;
    padding-right: 1em;
    font-weight: bolder
  }
  .is-selected a {
    color: darkblue
  }
</style>