<template>
  <v-card class="mx-auto" max-width="344">
    <v-img :src= tempUrl   cover></v-img>

    <v-card-title> Meet {{ name }} </v-card-title>

 

    <v-card-actions>
      <v-btn color="orange-lighten-2" variant="text" dark> Adopt </v-btn>

      <v-spacer></v-spacer>

      <v-btn
        
        @click="show = !show"
      >
      <div
      v-show="!show"
      >more</div>
    
      <div
      v-show="show"
      >less</div>
    </v-btn>
      
    </v-card-actions>

    <v-expand-transition>
      
      <div v-show="show">
        
        <v-divider> </v-divider>

        <v-card-text>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Placeat nemo cumque earum! Eum impedit sit ut, iusto eius magni sunt enim ipsa vitae animi sapiente error voluptatibus eaque quas officia.
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>
export default {
  props:  ["name","filename"],
  methods:
  {
    setData ()
    {
        this.Dogname = this.name;
        this.Typefilename = this.filename;

    },
    setUrl ()
    {
      let url = "../assets/goodBoys/" + this.filename + ".jpg";
      this.url = url;
      console.log(this.url)
      return url;
    },
    mounted ()
    {
      this.setData();
    }

  },
  data() {

    return {
      Dogname : null,
      Typefilename : null,
      show: null,
      url : null,
      icon : true,
      tempUrl: this.filename,
    
    }
  }
}
</script>

<style></style>
