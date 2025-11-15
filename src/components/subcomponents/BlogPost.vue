<script>
    export default {
        // Add code if/as necessary
        // Hint: Add properties subject, entry and mood
        props:{
            blog: Object
        },
        computed:{
            moodImage() {
            if (this.blog.mood === 'Happy') {
                return '../../public/assets/happy.png'
            } 
            else if (this.blog.mood === 'Sad') {
                return '../../public/assets/sad.png'
            } 
            else if (this.blog.mood === 'Angry') {
                return '../../public/assets/angry.png'
            }
        }
        }
    }
</script>


<template>
    <!-- TODO: add your template code here. Use boostrap card --> 
    <div class="card" style="width: 18rem;">
    <img :src="moodImage" class="card-img-top">
    <div class="card-body">
        <h5 class="card-title">{{ blog.subject }}</h5>
        <p class="card-text"> {{ blog.entry }}</p>
    </div>
    </div>
</template>

