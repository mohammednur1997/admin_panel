<template>
  <data-page
    v-if="$can('brand', 'create') || $can('brand', 'view')"
    ref="dataPage"
    set-api="setBrand"
    get-api="getBrand"
    empty-store-variable="allBrands"
    route-name="brands"
    :name="$t('prod.brand')"
    gate="brand"
    :validation-keys="['title', 'slug']"
    :result="result"
    @result="result = $event"
  >

    <template v-slot:form="{hasError}">

      <div class="input-wrapper">
        <label>{{ $t('index.image') }}</label>
        <upload-files @updateInput="saveAttachment" :max-files="1"></upload-files>
        <span
          class="error"
          v-if="!!!result.title && hasError"
        >
          {{ $t('category.req', {type: $t('index.image')}) }}
        </span>
      </div>


      <div class="input-wrapper">
        <label>{{ $t('index.title') }}</label>
<!--        <input-->
<!--          type="text"-->
<!--          :placeholder="$t('index.title')"-->
<!--          name="title"-->
<!--          v-model="result.title"-->
<!--          ref="title"-->
<!--          @change="slugChange"-->
<!--          :class="{invalid: !!!result.title && hasError}"-->
<!--        >-->

        <lang-input :hasError="hasError" type="text" :title="$t('index.title')" :valuesOfLang="result.title"
                    @updateInput="updateInput"></lang-input>


        <span
          class="error"
          v-if="!!!result.title && hasError"
        >
          {{ $t('category.req', {type: $t('index.title')}) }}
        </span>
      </div>


      <div class="input-wrapper">
        <label>{{ $t('category.slug') }}</label>
        <input
          type="text"
          :placeholder="$t('category.slug')"
          name="slug"
          v-model="result.slug"
          ref="slug"
          :class="{invalid: !!!result.slug && hasError}"
        >
        <span
          class="error"
          v-if="!!!result.slug && hasError"
        >
          {{ $t('category.req', {type: $t('category.slug')}) }}
        </span>
      </div>

      <div class="input-wrapper">
        <div class="dply-felx j-left mb-20 mb-sm-15">
          <span class="mr-15">
            {{ $t('category.featured') }}
          </span>

          <dropdown
            :selectedKey="`${result.featured}`"
            :options="featuredObj"
            @clicked="featuredSelected"
          />
        </div>
      </div>


      <div class="input-wrapper">
        <div class="dply-felx j-left mb-20 mb-sm-15">
          <span class="mr-15">
            {{ $t('category.status') }}
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

import Dropdown from "~/components/Dropdown"
import DataPage from "~/components/partials/DataPage"
import util from "~/mixin/util"
import {mapGetters} from 'vuex'
import UploadFiles from "../../components/UploadFiles.vue";
import LangInput from "../../components/langInput.vue";

export default {
  name: "brands",
  middleware: ['common-middleware', 'auth'],
  data() {
    return {
      result: {
        id: '',
        // title: '',
        title: {'ar': '', 'en': ''},
        slug: '',
        featured: 2,
        status: 2,
        image: '',
        file: '',
      }
    }
  },
  mixins: [util],
  components: {
    LangInput,
    UploadFiles,
    DataPage,
    Dropdown
  },
  computed: {
    ...mapGetters('language', ['currentLanguage']),
  },
  methods: {
    updateInput(input, language, value) {

      this.$set(input, language, value);
    },
    featuredSelected(data) {
      this.result.featured = data.key
    },
    dropdownSelected(data) {
      this.result.status = data.key
    },
    saveAttachment(image) {
      console.log(image)
      // this.result.rfq_attachments = rfq_attachments
      this.result.file = image
    },

  },

  async mounted() {
  }
}
</script>

<style scoped>

</style>
