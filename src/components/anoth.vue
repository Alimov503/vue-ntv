<template>
    <Page>
            <StackLayout>
        <Label>
            Salam
        </Label>
        <Image :src="this.imageSrc" />
        <Button class="buttn" text="Back" @tap="tapped"/>
            </StackLayout>
    </Page>
</template>

<script>
export default {

methods:{
    tapped(){
        console.log('hola')
        this.$navigateBack()
    }
},
props: {
    imageSrc: {
        type: String,
        required: true
    },
}

}
</script>

<style>


.buttn{
    background-color: lime;
}
</style>
