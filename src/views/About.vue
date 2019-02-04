<template>
  <div class="about">
    <h1>This is an about page about scoped slots</h1>
    <!--Shapes-->
    <my-list :items="shapes" title="Shapes">
      <template scope="shape">
        <div>{{ shape.name }} <small>({{ shape.sides }} sides)</small></div>
      </template>
    </my-list>

    <!--Colors-->
    <my-list :items="colors" title="Colors">
      <template scope="color">
        <div>
          <div class="swatch" :style="{ background: color.hex }"></div>
          {{ color.name }}
        </div>
      </template>
    </my-list>
    <!--Colors-->
    <my-list :items="dimensions" title="Dimensions">
      <h5 slot="subtitle">this is a super reusable template</h5>
      <template scope="thisIsARandomNameForTheScopedVariable">
        <div>
          {{ thisIsARandomNameForTheScopedVariable.denomination }}
          <strong>dimensions ({{ thisIsARandomNameForTheScopedVariable.randomProperty }})</strong>
        </div>
        <img style="background-color: white; width:60px;max-width: 60px;height: 60px"
             :src="thisIsARandomNameForTheScopedVariable.image">
      </template>
    </my-list>
  </div>
</template>
<script>
  import MyList from '@/components/MyList'
  export default {
    name: "about",
    components:{
      MyList,
    },
    data(){
      return{
        shapes: [
          { name: 'Square', sides: 4 },
          { name: 'Hexagon', sides: 6 },
          { name: 'Triangle', sides: 3 }
        ],
        colors: [
          { name: 'Yellow', hex: '#F4D03F', },
          { name: 'Green', hex: '#229954' },
          { name: 'Purple', hex: '#9B59B6' }
        ],
        dimensions: [
          { denomination: 'Emptiness', image: '', randomProperty: 'null' },
          { denomination: 'Dot', image: '../../dot.png', randomProperty: '1'  },
          { denomination: 'Line', image: '../../line.png', randomProperty: '2' },
          { denomination: 'Cube', image: '../../cube.png', randomProperty: '3' }
        ]
      }
    }
  }
</script>

<style scoped>
  .swatch {
    display: inline-block;
    width: 15px;
    height: 10px;
    margin-right: 8px;
  }
</style>
<style>
  .about{
    height: auto;
    background: linear-gradient(270deg, #002e9d, #29b3b4)
  }

</style>
