<template>
  <div id="app" class="mt-4">
    <elements-table class="col-10 col-lg-10 col-md-10 col-sm-10 mx-auto" :elements="elements" :columnHeads="columnHeads">
    </elements-table>
  </div>
</template>

<script>
import ElementsTable from './components/ElementsTable.vue'

export default {
  name: 'App',
  components: {
    ElementsTable
  },
  data() {
    return {
      columnHeads: ['No', 'Name', 'Symbol', 'Weight', 'Abundance', ''],
      elements: [
        {
          name: 'Hydrogen',
          editable: true,
          symbol: 'H',
          weight: 1.008,
          editableWeight: true,
          abundance: 30,
          infoText: 'Greek words hydro for "water" and genes for "forming'
        },
        {
          name: 'Helium',
          editable: true,
          symbol: 'He',
          weight: 4.002602,
          editableWeight: true,
          abundance: 0,
          infoText: "From Greek: ἥλιος, romanized: Helios, lit. 'Sun' is a chemical element with the symbol He and atomic number 2."
        },
        {
          name: 'Lithium',
          editable: true,
          symbol: 'Li',
          weight: 6.94,
          editableWeight: true,
          abundance: 20,
          infoText: "From Greek: λίθος, romanized: lithos, lit. 'stone'."
        },
        {
          name: 'Beryllium',
          editable: true,
          symbol: 'Be',
          weight: 9.0121831,
          editableWeight: true,
          abundance: 10,
          infoText: 'The origin of the name comes from the Greek word beryllos meaning mineral beryl; also called glucinium from the Greek word glykys meaning sweet.'
        },
        {
          name: 'Boron',
          editable: true,
          symbol: 'B',
          weight: 10.81,
          editableWeight: true,
          abundance: 20,
          infoText: "The name is derived from the Arabic 'buraq', which was the name for borax."
        },
        {
          name: 'Carbon',
          editable: true,
          symbol: 'C',
          weight: 12.011,
          editableWeight: true,
          abundance: 40,
          infoText: "Carbon gets its name from the Latin word carbo, which means 'coal'."
        },
        {
          name: 'Nitrogen',
          editable: true,
          symbol: 'N',
          weight: 14.007,
          editableWeight: true,
          abundance: 30,
          infoText: "The name is derived from the Greek 'nitron' and 'genes' meaning nitre forming."
        },
        {
          name: 'Oxygen',
          editable: true,
          symbol: 'O',
          weight: 15.999,
          editableWeight: true,
          abundance: 90,
          infoText: "From the Greek words 'oxy genes' meaning 'acid' (sharp) and 'forming' (acid former)."
        },
        {
          name: 'Fluorine',
          editable: true,
          symbol: 'F',
          weight: 18.998403163,
          editableWeight: true,
          abundance: 45,
          infoText: "The name fluorine is derived from the mineral fluorite which comes from the Latin word 'fluere' meaning 'to flow'."
        },
        {
          name: 'Neon',
          editable: true,
          symbol: 'Ne',
          weight: 20.1797,
          editableWeight: true,
          abundance: 0,
          infoText: "The name comes from the Greek 'neos', meaning new."
        },
      ]
    }
  },
}
</script>
