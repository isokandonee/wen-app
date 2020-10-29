<template>
<v-container class="grey lighten-5">
    <v-row class="mb-6" no-gutters>
        <v-col xs="6" offset-xs="3">
            <v-card class="pa-2" outlined tile>
                <v-title title>Add a New Blog Post</v-title>
            </v-card>
        </v-col>
    </v-row>
    <v-row class="mb-6" no-gutters>
        <v-col xs="6" offset-xs="3">
            <v-card class="pa-2" outlined tile><template>
                    <v-form ref="form" v-model="valid" lazy-validation>
                        <v-text-field v-model="title" :rules="titleRules" label="Title" required></v-text-field>

                        <v-text-field v-model="content" :rules="contentRules" label="Content" required></v-text-field>

                        <v-checkbox v-model="checkbox" :rules="[v => !!v || 'You must agree to continue!']" label="Are you sure?" required></v-checkbox>

                        <v-btn :disabled="!valid" color="deep-purple white--text" class="mr-4" @click="validate">
                            Post
                        </v-btn>
                    </v-form>
                </template>
            </v-card>
        </v-col>
    </v-row>
    <v-row class="mb-6" no-gutters>
        <v-col xs="6" offset-xs="3">
            <v-card class="pa-2" outlined tile>
                <v-title title>New Blog Post Preview</v-title>
            </v-card>
        </v-col>
    </v-row>
    <v-row class="" no-gutters>
        <v-col xs="6" offset-xs="3">
            <v-card class="pa-2" outlined tile>
                <template>
                    <v-title title>
                        <v-label>Title</v-label>
                        <div value="" label="Title">{{title}}</div>
                    </v-title>
                    <v-divider></v-divider>
                    <v-text>
                        <v-label>Content</v-label>
                        <div value="" label="">{{content}}</div>
                    </v-text>
                </template>
            </v-card>
        </v-col>
    </v-row>
</v-container>
</template>

<script>
export default {
    name: 'AddBlog',
    data: () => ({
        valid: true,
        title: '',
        titleRules: [
            v => !!v || 'Title is required',
        ],
        content: '',
        contentRules: [
            v => !!v || 'Content is required',
        ],
        checkbox: false,
    }),

    methods: {
        validate() {
            this.$refs.form.validate()
        }
    },
}
</script>
