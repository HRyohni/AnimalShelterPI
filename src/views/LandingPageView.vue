<template>
  <v-container  class="">
    <div class="naslov">
        <div class="naslovText" style="padding: 6vw;">
            <v-row>
                <v-col>

                    <h1 style="color: white; text-shadow: 2px 2px #000000;">Animal Shelter</h1>
                
                </v-col>
                <v-col> 
                    <v-img
                    style="-webkit-filter: drop-shadow(10 10px 10px #222);
                    filter: drop-shadow(5px 5px 5px #222);"
                    src="../assets/goodBoys/dog3.png">

                    
                    </v-img>
                    </v-col>
                
            </v-row>
            
        </div>
        
    </div>
    <div style="height: 500px;" class="pa-12">
        <h1 style="font-size: 5vw;" class="">Meet Ben,</h1>
        <h2 class="">He is looking for a loyal companion</h2>
    </div>
   <div class="gallery" style="margin-top: auto;">
    <v-row>
       <v-col>
        <GoodBoyCard name = "Max"></GoodBoyCard>
       </v-col>
       <v-col>
        <GoodBoyCard name = "Ben"></GoodBoyCard>
       </v-col>
       <v-col>
        <GoodBoyCard name = "Rex"></GoodBoyCard>
       </v-col>
       <v-col>
        <GoodBoyCard name = "Leo"></GoodBoyCard>
       </v-col>
    </v-row>
</div>
<v-divider></v-divider>
    <h1 style="font-size: 6vw;" class="d-flex justify-center mb-6 bg-surface-variant">How to get a Pet!</h1>
    <div class="steps">
        <v-row class="ma-16">
            <v-col>
                <v-card class="pa-3"
                color="yellow"
                
                elevation="2">
                <v-card-title style="font-size: 2vh;">Choose a Friend</v-card-title>
                <v-img  src="../assets/icons/search.png" 
                max-height="8vw"
                max-width="8vw"  class="pa-12 -flex justify-center mb-6 bg-surface-variant" style="margin-left: auto; margin-right: auto;"></v-img>
                <p>You can chose online pet from now on, no need to come </p> 
               
                </v-card>
            </v-col>
            <v-col>
                <v-card>
                   <v-card class="pa-3"
                color="yellow"
                
                elevation="2">
                <v-card-title style="font-size: 2vh;">Meet us</v-card-title>
                <v-img src="../assets/icons/house.png" 
                max-height="8vw"
                max-width="8vw"  class="pa-12 -flex justify-center mb-6 bg-surface-variant" style="margin-left: auto; margin-right: auto;"></v-img>
                <p>You can chose online pet from now on, no need to come </p> 
               
                </v-card>
                </v-card>
            </v-col>
            <v-col>
                <v-card>
                   <v-card class="pa-3"
                color="yellow "
                
                elevation="2">
                <v-card-title style="font-size: 2vh;">Fill the adoption form</v-card-title>
                <v-img src="../assets/icons/note.png" 
                max-height="8vw"
                max-width="8vw"  class="pa-12 -flex justify-center mb-6 bg-surface-variant" style="margin-left: auto; margin-right: auto;"></v-img>
                <p>You can chose online pet from now on, no need to come </p> 
               
                </v-card>
                </v-card>
            </v-col>
            <v-col>
                <v-card style="">
                   <v-card class="pa-3"
                color="yellow"
                
                elevation="2">
                <v-card-title style="font-size: 2vh;">Take your friend home!</v-card-title>
                <v-img src="../assets/icons/doggo.png" 
                max-height="8vw"
                max-width="8vw"  class="pa-12 -flex justify-center mb-6 bg-surface-variant" style="margin-left: auto; margin-right: auto;"></v-img>
                <p>You can chose online pet from now on, no need to come </p> 
               
                </v-card>
                </v-card>
            </v-col>
        </v-row>
       
    </div>
  
    <div class="pomoc" style="margin-top: 0px;">
        <v-row style="margin-top: 0px;" >

            <v-col style="margin-top: 0px;">
                
                <v-card class="pa-12">
                    <v-card-title><h1>sudjeluj i ti pomozi zivotinjama</h1></v-card-title>
                 
                    
                    <h2>pridruzi nam se u spasavanju nekih zivotinja neznam ni ja kakvih vise samo pisem da ima teksta</h2>
                    <v-btn
                    dark>Sudjeluj!</v-btn>
                </v-card>
            </v-col>
            <v-col>
                <v-img src="../assets/goodBoys/fakeDoctor.png"
                 max-height="auto"
                 max-width="500"
                 style="margin-top: 0px;"
             
                ></v-img>
            </v-col>
        </v-row>
    </div>
    
    <template>
        <div class="comments">
            <div class="text-center">
                <v-avatar style="margin-top:-50px    ;"
                color="primary"
                size="100"
              >LM</v-avatar>
              <h3 class="pa-9">omg you change THEIR the world</h3>
              <h5 style="font-size: 30px;">...</h5>
              <p>Marta Butorac</p>
             
           
              <v-rating
                v-model="rating"
                background-color="orange lighten-3"
                color="orange"
                large
              ></v-rating>
              
            </div>
        </div>
        
      </template>
  </v-container>
</template>

<script>
import GoodBoyCard from '@/components/GoodBoysCards.vue';

export default{
    
    components:
    {
        GoodBoyCard
    },

}
</script>

<style>
* 
{margin: 0px;
padding: 0px;}
.naslov
{
background-color: #FFF44F;
width: 100%;
background-size: cover;
height: 600px;


}

.steps
{
margin: 10%;
text-align: center;

margin: 0px;

}
.naslovText
{
    font-size: 2vw;
    color: rgb(30, 30, 30);
    
}

.comments
{
    color: white;
    background-color: #424e5e;
}
.gallery
{  
    
    margin: 4%;
}
.container{
    max-width: 100vw;
    padding:0px;
 }

 .pomoc
 {
    background-color: #56acc3;
    
    color: white;   
 }
 .rating
 {
    
    width: 100%;
    height: 250px;
    background-color: rgb(14, 25, 81);
    padding: 20px;
 }
</style>