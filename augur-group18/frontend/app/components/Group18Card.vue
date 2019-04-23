<template>
  <section>
    <h1>Group 18 Features</h1>
    <div style="display: inline-block;">
      <h2 style="display: inline-block; color: black !important">{{ $store.state.baseRepo }}</h2>
      <h2 style="display: inline-block;" class="repolisting" v-if="$store.state.comparedRepos.length > 0"> compared to: </h2>
      <h2 style="display: inline-block;" v-for="(repo, index) in $store.state.comparedRepos">
        <span v-bind:style="{ 'color': colors[index] }" class="repolisting"> {{ repo }} </span>
      </h2>
    </div>
    <div class="row">
      <div class="col col-6">
        <dynamic-line-chart source="codeCommits"
                    title="Top Authors By Commit"
                    cite-url=""
                    cite-text="Authors by Commit">
        </dynamic-line-chart>
      </div>

      <div class="col col-6">
        <dynamic-line-chart source="totalCommitters"
                    title="Repo Openness"
                    cite-url=""
                    cite-text="Repo Openness"
                    >
        </dynamic-line-chart>
      </div>
      <div class="col col-12">
        <h3>Days until this Repo is considered inactive:  100</h3>
      </div>
    </div>
  </section>
</template>
<script>

import DynamicLineChart from './charts/DynamicLineChart'
import BubbleChart from './charts/BubbleChart'
import StackedBarChart from './charts/StackedBarChart'
import DualAxisContributions from './charts/DualAxisContributions'

module.exports = {
  data() {
    return {
      colors: ["#FF3647", "#4736FF","#3cb44b","#ffe119","#f58231","#911eb4","#42d4f4","#f032e6"]
    }
  },
  components: {
    DynamicLineChart,
    BubbleChart,
    StackedBarChart,
    DualAxisContributions
  }
}
</script>
