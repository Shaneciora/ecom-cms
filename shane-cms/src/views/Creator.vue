<template>
    <div class='main_content'>
        <creatorSideBar></creatorSideBar>
        <div class='creator_content'>
            <creatorContent></creatorContent>    
        </div>
    </div>
    
    
</template>

<style scoped>
    .main_content{
        display: flex;
    }
    .creator_content{
        flex-grow: 1;
    }
</style>

<script>
import creatorSideBar from '@/components/creatorSideBar.vue'
import creatorContent from '@/components/creatorContent.vue'

export default {


  components: {
      creatorSideBar,
      creatorContent
  }

    
}
</script>


