<template>
  
  <div class="tabs">
      <div class="tab">
        <input type="checkbox" id="chck1" class="tab-input">
        <label class="tab-label" for="chck1">How the heck did I get here?</label>
        <div class="tab-content">
           <div class="timeline">
            <div v-for="item in timeline" :key="item.name" class="timeline-item frosted">
              <div class="timeline-content">
              <h3 class="year">{{item.year}}</h3>
              <h2 class="timeline-item-title">{{item.title}}</h2>
              <p>{{item.description}}</p>
              </div>
            </div>

          </div>
        </div>
      </div>

      </div>
</template>

<script>

import data from "../../data/data.json";

export default {
  name: "Timeline",
  props: {},

 data() {
    return {
    timeline: data.about.timeline,
    }
}
}

</script>

<style lang="scss"></style>
