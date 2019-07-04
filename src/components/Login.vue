<template>
  <Page>
    <ActionBar title="My App">
  <NavigationButton text="Go back" android.systemIcon="ic_menu_back" @tap="goBack" />
</ActionBar>

       <FlexboxLayout flexDirection="column" justifyContent="center" class="full-height">   

      <StackLayout class="container">

        <FlexboxLayout alignItems="center" class="border-bottom">
          <Image src="~/images/zzz.png" width="16" height="16" class="icon-margin" />
          <TextField  v-model="userNameInput" hint="Email adress" class="form-input"/>
        </FlexboxLayout>

        <FlexboxLayout alignItems="center" class="border-bottom">
          <Image src="~/images/aaa.png" width="16" height="16" class="icon-margin" />
          <TextField  v-model="userNameInput" hint="Password" secure="true" class="form-input"/>
        </FlexboxLayout>
        
      <Button text="Login" @tap="onButtonTap" class="log-btn"/>

      <FlexboxLayout alignItems="center" justifyContent="space-between"  class="auth-buttons">
    
        <Label horizontalAlignment="left" text="Forgot Password" class="" />
        
      </FlexboxLayout>
      
      </StackLayout>
        
        <Button  verticalAlignment="bottom"  text="Create Account" class="reg-btn" /> 

      </FlexboxLayout>

       
  </Page>
</template>

<script>
export default {
  data(){
    return{
      userNameInput: '',
      userNameInput: ''
    }
  },
  methods:{
    onButtonTap(){
      console.log('Hola')
    },
    goBack(){
      this.$navigateBack()
    }
  },
}
</script>

<style lang="scss" scoped>
.border-bottom {
  border-bottom-width: 1;
  border-bottom-color: #FFE600;
  margin-bottom: 40;
  padding-bottom: 8
}

.form-input{
  color: black;
  placeholder-color: black;
}

.icon-margin {
  margin-right: 10
}

.log-btn {
  background-color: #FFE600 ;
  color: black;
  font-weight: bold;
  // border-radius: 25;
  padding-bottom: 14;
  text-transform: uppercase;
  letter-spacing: 0.1; 
  margin-bottom: 20;
    margin-bottom: 10;
}

.auth-buttons{
  color: black;
  font-size: 14
}

.full-height {
  height: 100%;
}
.logo-container{
  width: 150;
  margin-bottom: 60;
}
.container{
  margin-left: 35;
  margin-right: 35;
}
.reg-btn {
  background-color: black ;
  color: #FFE600;
  font-weight: bold;
  padding-bottom: 14;
  text-transform: uppercase;
  letter-spacing: 0.1; 
  width: 100%; 
}
</style>
