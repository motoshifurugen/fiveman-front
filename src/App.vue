<template>
    <v-app>
        <v-app-bar color="teal" dark app clipped-left>
            <v-toolbar-title>ヘッダー</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-toolbar-items>
                <v-menu offset-y>
                    <template v-slot:activator="{on}">
                    <v-app-bar-nav-icon v-on="on"></v-app-bar-nav-icon>
                    </template>
                    <v-list>
                        <v-list-item v-for="page in menu" :key="page">
                            <v-list-item-content>
                                <v-list-item-title>{{ page }}</v-list-item-title>
                            </v-list-item-content>
                        </v-list-item>
                    </v-list>
                </v-menu>
                </v-toolbar-items>
        </v-app-bar>
        <v-footer color="teal" dark app>
            footer
        </v-footer>
    </v-app>
</template>

<script>
export default {
    data(){
    return{
        menu:[
            {name: 'やっほー隊', icon: 'mdi-rocket-launch'},
            {name: 'メンバー', icon: 'mdi-account-group'},
            {name: 'お問い合わせ', icon: 'mdi-email'}
        ]
    }
  }
};
</script>
