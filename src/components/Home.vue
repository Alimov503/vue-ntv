<template>
  <Page>
    <ActionBar class="action-bar" title="Home"/>

    <StackLayout>
    
    <AbsoluteLayout class="column" >
       <FlexboxLayout class="img" @tap="toNews" left="10" top="10" width="100" height="100" >
        <Image src="~/images/newspaper.png"  width="76" height="76" 
         row="0" col="0"/>
      </FlexboxLayout>
       <FlexboxLayout class="img" @tap="toOrders" left="120" top="10" width="100" height="100">
        <Image src="~/images/sss.png" width="76" height="76" 
         row="0" col="0"/>    
      </FlexboxLayout>

      <FlexboxLayout class="img" @tap="toAcceptedOrders" left="230" top="10" width="100" height="100">
        <Image src="~/images/list.png" width="76" height="76" 
         row="0" col="0"/>  
      </FlexboxLayout>

      <Label text="Новости" left="30" top="120" width="100" height="50"/>
      <HtmlView left="130" top="120" width="190" 
      height="50" html="<div><label> Посмотреть <br/> заявки</label></div>"/>
      <HtmlView left="250" top="120" width="190" height="50" 
      html="<div><label> Принятые <br/> заявки</label></div>"/>

      <FlexboxLayout class="img" @tap="toTracking" left="10" top="190" width="100" height="100">
        <Image src="~/images/calculator.png" alt="Hola" width="76" height="76" 
         row="0" col="0"/>
      </FlexboxLayout>
      <FlexboxLayout class="img" @tap="toDataBase" left="120" top="190" width="100" height="100">
        <Image src="~/images/cloud.png" alt="Hola" width="76" height="76" 
         row="0" col="0"/>
      </FlexboxLayout>
       <FlexboxLayout class="img" @tap="toGift" left="230" top="190" width="100" height="100">
        <Image src="~/images/gift.png" alt="Hola" width="76" height="76" 
         row="0" col="0"/>
      </FlexboxLayout>
      <Label text="Отслеживание" left="10" top="300" width="110" height="50"/>
      <Label text="База данных" left="130" top="300" width="100" height="50"/>
      <Label text="Розыгрыш" left="240" top="300" width="100" height="50"/>

    </AbsoluteLayout>
  </StackLayout>
  
      <GridLayout class="footer">
        <Label col="0"  backgroundColor="yellow" text="footer"/>
        <!-- <Label col="1" text="rest of the content"/> -->
      </GridLayout>

  </Page>
</template>

<script>
import login from './Login'
import userPage from './UserPage'


export default {
  data(){
    return{
     
    }
  },
   methods:{
    toNews(){
      this.$navigateTo(login)
    },
    toOrders(){
      this.$navigateTo(userPage)
    },
    toAcceptedOrders(){
      this.$navigateTo(login)
    },
    toTracking(){
      this.$navigateTo(login)
    },
    toDataBase(){
      this.$navigateTo(login)
    },
    toGift(){
      this.$navigateTo(login)
    },
  },
}
</script>

<style scoped>
.img{
  background-color: #FFE600;
  border-radius: 150px;
  justify-content:center
  }
.column{
  height: 900px;
  /* align-items: top; */
  /* padding: 200px */
  margin: 70px
}
.footer{
  height: 100px;
  margin-top: 750px;
  justify-content: end
  /* justify-content:  */
}

</style>
