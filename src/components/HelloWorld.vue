<template>
  <Page class="page">
    <ActionBar class="action-bar" title="Hello world">
      <NavigationButton text="Go Back" android.systemIcon="ic_menu_back" @tap="$router.push('/home')"/>
    </ActionBar>

    <StackLayout class="hello-world">
      <Label class="body" textWrap=true text="This is a hello world component, tap the button if you dare"/>

      <Button class="btn btn-primary" @tap="surprise = !surprise" text="Tap me!"/>
      <Image v-if="surprise" src="~/images/NativeScript-Vue.png"/>

    </StackLayout>

  </Page>
</template>

<script>
  export default {
    data () {
      return {
        surprise: false,
      };
    },
  };
</script>

<style scoped>
  .hello-world {
    margin: 20;
  }

  Label {
    color: red;
  }
</style>
