<template>
  <v-container>
    <v-row>
      <v-col v-for="repo in orderRepos" v-bind:key="repo.id">
        <v-card min-width="300px" height="100%" :title="repo.name" :text="repo.description">
          <v-card-actions>
            <v-btn :href="repo.html_url"><v-icon>fab fa-github</v-icon></v-btn>
            <v-spacer />
            <v-icon v-if="repo.language">fas fa-code</v-icon>
            <span class="px-2" v-html="repo.language"></span>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import axios from 'axios'
import _ from 'lodash'

type DataType = {
  repos: Repos[]
}
type Repos = {
  id: number
  name: string
  description: string
  html_url: string
  language: string | null
}

const URL = 'https://api.github.com/users/reiyuchan/repos'

export default defineComponent({
  data(): DataType {
    return {
      repos: []
    }
  },
  created() {
    axios.get(URL).then(response => this.repos = response.data)
  },
  computed: {
    orderRepos() {
      return _.orderBy(this.repos, 'created_at', 'desc')
    }
  }
})
</script>