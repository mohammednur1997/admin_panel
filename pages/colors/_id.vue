<template>
  <data-page
    ref="dataPage"
    set-api="setColor"
    get-api="getColor"
    set-image-api="setCategoryImage"
    route-name="colors"
    :name="$t('color.color')"
    gate="brand"
    :validation-keys="['code','name.ar','name.en']"
    :result="result"
    @result="resultData"
  >
    <template v-slot:form="{hasError}">
      <lang-input :hasError="hasError" type="text" :title="$t('global.name')" :valuesOfLang="result.name"
                  @updateInput="updateInput"></lang-input>

      <div class="input-wrapper">
        <label>{{ $t('color.select_color') }}</label>
        <input
          type="color"
          v-model="result.code"
          ref="name"
          :class="{invalid: !!!result.code && hasError}"
        >
        <span
          class="error"
          v-if="!!!result.code && hasError"
        >
          {{ $t('global.req', { type: $t('color.select_color')}) }}
        </span>
      </div>

      <div class="input-wrapper">
        <div class="dply-felx j-left mb-20 mb-sm-15">
            <span class="mr-15">
              {{ $t('global.status') }}
            </span>

          <dropdown
            :selectedKey="`${result.status}`"
            :options="statusObj"
            @clicked="dropdownSelected"
          />
        </div>
      </div>


    </template>
  </data-page>
</template>

<script>

  import DataPage from "~/components/partials/DataPage";
  import util from "~/mixin/util"
  import Dropdown from '~/components/Dropdown'
  import {mapGetters, mapActions } from 'vuex'

  export default {
    name: "colors",
    middleware: ['common-middleware', 'auth'],
    data() {
      return {
        result: {
          id: '',
          name:{'ar':'','en':''},
          code:''

        }
      }
    },
    mixins: [util],
    components: {
      DataPage,
      Dropdown
    },
    computed: {
      ...mapGetters('language', ['currentLanguage']),
      ...mapGetters('common', ['allCategories'])
    },
    methods: {
      updateInput(input, language, value) {
        this.$set(input, language, value);
      },
      resultData(evt){
        if(this.$route?.params?.id === 'add'){
          this.emptyAllList('allCategories')
        }
        this.result = evt
      },

      dropdownSelected(data) {
        this.result.status = data.key
      },

      ...mapActions('common', ['getAllList', 'emptyAllList'])
    },
    async mounted() {
      if (!this.allCategories) {
        try {
          await this.getAllList({api: 'getAllCategories', mutation: 'SET_ALL_CATEGORIES'})
        } catch (e) {
          return this.$nuxt.error(e)
        }
      }
    }
  }
</script>

<style scoped>

</style>
