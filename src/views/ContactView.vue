<template>
<MessageContact/>
<DetailContact/>
<MappingContact/>


</template>

<script>
import MessageContact from "@/components/contact/MessageContact";
import DetailContact from "@/components/contact/DetailContact";
import MappingContact from "@/components/contact/MappingContact";
export default {
  name: "ContactView",
  components:{MessageContact,DetailContact,MappingContact}
}
</script>

<style scoped>




</style>