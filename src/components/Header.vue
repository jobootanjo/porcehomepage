<template>
  <div>
    <v-app-bar color="deep-purple accent-4" dense dark>
    <v-avatar>
      <img src="@/assets/porce.jpg" alt="John">
    </v-avatar>
     
<v-spacer></v-spacer>
     
     <v-tabs right>
         <v-tab to="/">HOME</v-tab>
         <v-tab to="/about">ABOUT</v-tab>
         <v-tab to="/members">MEMBER</v-tab>
         <v-tab to="/place">PLACE</v-tab>
     </v-tabs>
    </v-app-bar>
  
  
  
  
  
  <v-card flat tile>
    <v-window v-model="onboarding" reverse>
      <v-window-item
      v-for="n in length"
        :key="`card-${n}`"
      >
        <v-card
          color="grey"
          height="200"
        >
          <v-row
            class="fill-height"
            align="center"
            justify="center"
            tag="v-card-text"
          >
           
          
          <h1 style="font-size: 5rem;" class="white--text">dasdas </h1>
          
          </v-row>
        </v-card>
      </v-window-item>
    </v-window>

   
   
   
   
   
   
   
   
   
   
   
   
   
   <!--  スライドの下の部分の間隔調整  -->
   
    <v-card-actions class="justify-space-between">
     <!-- 左のボタンを押すことでスライドが動くようにしている -->
      <v-btn
        text
        @click="prev"
      >
     
      <!--  左矢印  -->
        <v-icon>mdi-tennis</v-icon>
      </v-btn>
      <!--  左のボタンと真ん中のボタンが連動して動くようになる  -->
      <v-item-group
        v-model="onboarding"
        class="text-center"
        mandatory
      >
        
        <v-item
          v-for="n in length"
          :key="`btn-${n}`"
          v-slot:default="{ active, toggle }"
        >
          <v-btn
            :input-value="active"
            icon
            @click="toggle"
          >
          <!--  四つの丸  -->
            <v-icon>mdi-tennis-ball</v-icon>
          </v-btn>
        </v-item>
      
      </v-item-group>
      <v-btn
        text
        @click="next"
      >
      
      <!-- 右矢印  -->
        <v-icon>mdi-tennis</v-icon>
      </v-btn>
    </v-card-actions>


 
 
  </v-card>
  
  </div>
  </template>











<!-- スライドの枚数などの変更 -->
<script>
  export default {
    data: () => ({
      length: 3,
      onboarding: 0,
    }),

    methods: {
      next () {
        this.onboarding = this.onboarding + 1 === this.length
          ? 0
          : this.onboarding + 1
      },
      prev () {
        this.onboarding = this.onboarding - 1 < 0
          ? this.length - 1
          : this.onboarding - 1
      },
    },
  }
</script>


  
  
  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
