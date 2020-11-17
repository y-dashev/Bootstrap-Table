<template>
<div>
<div class="table-responsive-sm">
<table class="table ">
  <thead>
    <tr  >
      <th scope="col"   v-for="header in columnHeads" :key="header.id">
         {{ header }} 
      </th>
    </tr>
  </thead>
  <tbody>
    <tr v-for="(element, index) in elements" :key="element.id">
      <td scope="row">{{index + 1}}</td>
      <td @dblclick="element.editable=false"
          @mouseleave="element.editable=true"
          >  
          <textarea :disabled="element.editable" v-model="element.name" cols="15" rows="1"></textarea>
      </td>
      <td id="elementSymbol"> 
          <span> {{ element.symbol }} </span> 
      </td>
      <td @dblclick="element.editableWeight=false"
          @mouseleave="element.editableWeight=true"
          > 
           <textarea :disabled="element.editableWeight" v-model="element.weight" cols="12" rows="1"></textarea>
      </td>
      <td>
          <b-progress :value="element.abundance" :height="progressBarHeight" class="w-70"> </b-progress> 
      </td>
      <td> 
          <b-button :id="element.name" :style="infoButtonStyles" >
              <b-icon id="infoIcon" icon="info-circle-fill" aria-hidden="true" ></b-icon>
          </b-button>
          <b-popover  triggers="focus" 
                      placement="right" 
                      :target="element.name" 
                      title="Origin of name">
              {{element.infoText}}
          </b-popover>
      </td>
    </tr>
  </tbody>
</table> 
</div>
      
</div>
</template>
<script>
export default {
  name: 'ElementsTable',
  props: {
    columnHeads: Array,
    elements: Array,
  },
  data(){
    return{
      progressBarHeight: '1.3rem',
      infoButtonStyles:{
        background: 'none',
        border: 'none',
        outline: 'none',
        cursor: 'pointer',
        boxShadow:'none'
      }
    }
  },
}
</script>
