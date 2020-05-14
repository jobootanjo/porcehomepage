<template>
  <div>
    <!-- メニューバーの色など  -->
    <v-app-bar
      color="deep-purple accent-4"
      dense
      dark
    >
      
     
     
     <!-- ハンバーガーメニュー自体 -->
    <v-menu
        left
        bottom
      >

        <!-- 縦三点ボタン自体  -->
        <template v-slot:activator="{ on }">
        
        <!-- ボタンとしての機能を付加 -->
          <v-btn icon v-on="on">
            
            <!-- 縦三点ボタンのアイコン -->
            <v-icon>mdi-format-list-bulleted-square</v-icon>
          
          </v-btn>
        </template>

        <!--  クリックして出したウィンドウ -->
        <v-list>
          <v-list-item
            v-for="n in 5"
            :key="n"
            @click="() => {}"
          >
            <v-list-item-title>Option {{ n }}</v-list-item-title>
          </v-list-item>
        </v-list>
     
      </v-menu>

     
     
     
      <!-- ページのタイトル -->
      <v-toolbar-title>  Porc-épic T.C.</v-toolbar-title>

    <!-- 上に書いてあるメニューバーと下に書いてあるボタンの間隔をあけている  -->
      <v-spacer></v-spacer>

<!--  ハートのボタン -->
      <v-btn text href="https://www.instagram.com/tomoaki_bb6/" color="" >
        <v-icon>mdi-fruit-pineapple</v-icon>
      </v-btn>

<!--  虫眼鏡ボタン -->
  <!--    <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>  -->


<!--  縦三点ボタン  -->
    <!-- メニューを表示させるコンポーネント  -->  
      <v-menu
        left
        bottom
      > 
        <!-- 縦三点ボタン自体  -->
      <!--  <template v-slot:activator="{ on }"> -->
        
        <!-- ボタンとしての機能を付加 -->
         <!-- <v-btn icon v-on="on">  -->
            
            <!-- 縦三点ボタンのアイコン -->
          <!--  <v-icon>mdi-dots-vertical</v-icon>
          
          </v-btn>
        </template>  -->

        <!--  クリックして出したウィンドウ -->
        <v-list>
          <v-list-item
            
          >
           <!-- ここの中に表示したいものを書く  -->
            
            <v-list-item-title>
               
            </v-list-item-title> 
          
          
          
          </v-list-item>
        </v-list>
     
      </v-menu>  
    
    
    </v-app-bar>
  </div>
</template>


  
  
  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
