<template>
    <div>
        <form>
            <div class="form-group">
                <label>Titre</label>
                <input type="text" class="form-control" placeholder="Votre Titre" v-model="title">
            </div>
            <div class="form-group">
                <label>Contenu</label>
                <textarea class="form-control" name="content" v-model="content"></textarea>
            </div>
            <span @click="newPost" class="btn btn-primary">Ajouter ce post</span>
        </form>
    </div>
</template>

<script>

    export default {
        name: 'addPost',
        data() {
            return {
                title: null,
                content: null
            }
        },
        methods: {
            newPost() {
                axios.post('/api/post/new', {
                    title: this.title,
                    content: this.content,

                }).then(res => {

                })
            },
        }
    }
</script>