<!-- MultilingualInput.vue -->
<template>
  <div>
    <!-- Tab navigation -->
    <ul class="flex mb-0 list-none flex-wrap  w-50 shadow mt-10 flex-row">
      <li  v-for="(language, lindex) in languages" key="index" @click="currentTab = lindex" class="-mb-px mr-2 last:mr-0 cursor-pointer  flex-auto text-center">
        <a class="text-xs font-bold uppercase px-5 py-3  block leading-normal"  v-bind:class="{'bg-white border-white border-b-2': currentTab !== lindex, 'border-b-2 border-primary':currentTab === lindex}">
          {{ language }}
        </a>
      </li>
    </ul>

    <!-- Input fields for each language -->

    <div v-for="(language, key) in languages" :key="key" v-show="currentTab === key">
      <label>{{ $t('prod.key_features') }} ({{ language }})</label>
      <template v-for="(row,index) in  valuesOfLang">
        <div class="flex append-input pt-1">
<!--          <input class="form-control" :placeholder="title"-->
<!--                 :value="valuesOfLang[index][language]"-->
<!--                 @input="updateInputValue(language, $event.target.value)"-->
<!--                 :class="{ invalid: !!!valuesOfLang[index][language] && hasError }"-->
<!--          >-->
          <input class="form-control" :placeholder="$t('prod.features_placeholder')"
                 v-model="valuesOfLang[index][language]"
                 @input="updateInputValue(language, $event.target.value)"
                 :class="{ invalid: !!!valuesOfLang[index][language] && hasError }"
          >
          <button type="button" class="btn ml-2 mr-2 btn-danger" v-if="index !== 0" @click.prevent="removeRow(index)">
            <svg class="w-6 h-6 text-gray-800 " aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                 fill="none" viewBox="0 0 18 2">
              <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M1 1h16"/>
            </svg>
          </button>

          <button v-if="index+1===valuesOfLang.length" type="button" class="btn ml-2 mr-2  btn-primary" @click.prevent="addRow()">
            <svg class="w-4 h-4" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none"
                 viewBox="0 0 18 18">
              <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M9 1v16M1 9h16"/>
            </svg>
          </button>
        </div>
      </template>
    </div>


  </div>
</template>

<script>
export default {
  props: {
    valuesOfLang: {
      type: Array,
      required: true,
    },
    hasError: {
      type: Boolean,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    type: {
      type: String,
      required: true,
      default: "text"
    },
  },
  data() {
    return {
      languages: ['ar', 'en'], // Add your desired languages here
      currentTab: 0,
    };
  },
  methods: {
    addRow() {
      localStorage.setItem('formValues', JSON.stringify(this.valuesOfLang));
      this.valuesOfLang.push({"ar": "", "en": ""})
    },
    removeRow(index) {
      if (index != 0){
        this.valuesOfLang.splice(index, 1);
      }
    },
    updateInputValue(language, value) {
      console.log(0)
      this.$emit('updateInput', this.valuesOfLang, language, value);
    },
  },
};
</script>
