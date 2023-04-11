<template>
    <other-settings/>
    <go-to-card/>
    <new-collection-alerts/>
    <me-account/>
    <CallViaSIP/>
    <button v-on:click="signUp">проверка API</button>
</template>

<script>
import axios from 'axios'
import OtherSettings from "@/components/OtherSettings.vue";
import GoToCard from "@/components/GoToCard.vue";
import NewCollectionAlerts from "@/components/NewCollectionAlerts.vue";
import MeAccount from "@/components/Account.vue";
import CallViaSIP from "@/components/CallViaSIP.vue";

export default {
    name: 'SettingsBlock',
    components: {
        OtherSettings,
        GoToCard,
        NewCollectionAlerts,
        MeAccount,
        CallViaSIP,
    },
    data() {
        return {
            name: '',
            email: '',
            password: '',
        }
    },
    methods: {
        async signUp() {
            // let body = {
            //     "login": "89878420298",
            //     "password": "8072712643",
            // }
            let result = await axios.post('https://api.av100.ru/v3/login', {
                login: "89878420298",
                password: "8072712643"
            }, {
                headers: {
                    'X-Api-Key': '8bcfb6e1-4fa8-4fae-872c-a435bbdbe8d9',
                    // 'X-User-Token':'8a11b936-0a42-48bc-93d9-92330ebbc531',
                    'X-Device-OS': 'chromeOS'
                }
            })
            // 'userId': 2011307,
            // body,
            console.log(result.data)
        }
    },
}


</script>