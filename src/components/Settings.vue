<template>
    <other-settings :timezonestring="userInfo.timezonestring"/>
    <go-to-card/>
    <new-collection-alerts :telegramChat="userInfo.telegramChat"
                           :emailPlas="userInfo.email"
                           @sendEmail="sendEmail"
    />
    <me-account :companyname="userInfo.companyname"
                :login="userInfo.login"
                :phone="userInfo.phone"
                :fname="userInfo.fname"
                :lname="userInfo.lname"/>
    <CallViaSIP/>

    <button class="btnSave" @click="updateEmail">
        Сохранить
    </button>
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
    methods: {
        sendEmail(email) {
            this.userInfo.email = email
        },
        async updateEmail() {
            console.log('старт ')
            let userTocen = localStorage.getItem('X-User-Token').substring(1, 37)
            console.log(userTocen)
            let userId = localStorage.getItem('userId')
            const sucsses = await axios.put(`https://api.av100.ru/v3/user/${userId}`, {
                    email: this.userInfo.email
                },
                {
                    headers: {
                        'X-Api-Key': '8bcfb6e1-4fa8-4fae-872c-a435bbdbe8d9',
                        'X-User-Token': `${userTocen}`,
                        // 'X-User-Token': '8a11b936-0a42-48bc-93d9-92330ebbc531',
                        'X-Device-OS': 'chromeOS'
                    }
                })
            if (sucsses.status === 200) {
                console.log('111111')
            }
        },
    },
    data() {
        return {
            userInfo: {
                id: 0,
                login: '',
                clicks: 0,
                expire: 0,
                autoru: 0,
                phone: '',
                email: '',
                sendMethod: 0,
                lname: '',
                fname: '',
                timezone: '',
                timezonestring: '',
                notifytype: '',
                notifytypestring: '',
                companyid: 0,
                companyname: '',
                calltype: '',
                enableaudio: false,
                locklentaupdate: true,
                erased: 0,
                sipid: '',
                updatePeriod: 0,
                filterMaxCount: 0,
                telegramChat: '',
                turbosip: '',
                turbosip5accessto: '',
                turbosip20accessto: '',
                colorlenta: true,
                ignoreavg: false,
                redirecttarget: 0,
                lentacolortype: 0
            }
        }
    },


    mounted() {
        this.$nextTick(async function () {
            // первый запрос для получения токена
            let result = await axios.post('https://api.av100.ru/v3/login', {
                login: "89878420298",
                password: "8072712643"
            }, {
                headers: {
                    'X-Api-Key': '8bcfb6e1-4fa8-4fae-872c-a435bbdbe8d9',
                    'X-Device-OS': 'chromeOS'
                }
            })
            if (result.status === 200) {
                // токен и userID в localStorage
                localStorage.setItem('userId', JSON.stringify(result.data.user.id))
                localStorage.setItem('X-User-Token', JSON.stringify(result.data.token))
                // и делаем запрос за остальной инфой на сервер для заполнения страницы настроек данными
                let getInfo = await axios.get(`https://api.av100.ru/v3/user/${result.data.user.id}`, {
                    headers: {
                        'X-Api-Key': '8bcfb6e1-4fa8-4fae-872c-a435bbdbe8d9',
                        'X-User-Token': `${result.data.token}`,
                        'X-Device-OS': 'chromeOS'
                    }
                })
                if (getInfo.status === 200) {
                    // заносим данные в data для дальнейшего использования
                    let user = getInfo.data
                    this.userInfo = user
                }
            }
        })

    }
}


</script>

<style>

.btnSave {
    background-color: rgb(45, 197, 116);
    display: block;
    width: 392px;
    height: 44px;
    padding: 13px 20px;
    font-size: 13px;
    color: white;
    border-radius: 5px;
    margin-left: 200px;
    margin-bottom: 20px;
}

.btnSave:active {
    background: #26a763;
}
</style>