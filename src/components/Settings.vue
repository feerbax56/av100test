<template>
    <other-settings/>
    <go-to-card/>
    <new-collection-alerts/>
    <me-account/>
    <CallViaSIP/>
    <button @click="check"> проверка</button>
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
        check() {
            console.log(this.id)
        }
    },
    data() {
        return {
            id: 0,
            login: '',
            clicks: 0,
            expire: 0,
            autoru: 0,
            phone: '',
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
            turbosip: '',
            turbosip5accessto: '',
            turbosip20accessto: '',
            colorlenta: true,
            ignoreavg: false,
            redirecttarget: 0,
            lentacolortype: 0
        }
    },

    mounted() {
        this.$nextTick(async function () {
            let result = await axios.post('https://api.av100.ru/v3/login', {
                login: "89878420298",
                password: "8072712643"
            }, {
                headers: {
                    'X-Api-Key': '8bcfb6e1-4fa8-4fae-872c-a435bbdbe8d9',
                    'X-Device-OS': 'chromeOS'
                }
            })
            if (result.status === 200 && result.data.length > 0) {
                localStorage.setItem('userId', JSON.stringify(result.data.user.id))
                localStorage.setItem('X-User-Token', JSON.stringify(result.data.token))
                let getInfo = await axios.get('https://api.av100.ru/v3/' + `${result.data.user.id}`)
                if (getInfo.status === 200 && getInfo.data.length > 0) {
                    let user = getInfo.data.user
                    this.id = user.id;
                    this.login = user.login;
                    this.clicks = user.clicks;
                    this.expire = user.expire;
                    this.autoru = user.autoru;
                    this.phone = user.phone;
                    this.sendMethod = user.sendMethod;
                    this.lname = user.lname;
                    this.fname = user.fname;
                    this.timezone = user.timezone;
                    this.timezonestring = user.timezonestring;
                    this.notifytype = user.notifytype;
                    this.notifytypestring = user.notifytypestring;
                    this.companyid = user.companyid;
                    this.companyname = user.companyname;
                    this.calltype = user.calltype;
                    this.enableaudio = user.enableaudio;
                    this.locklentaupdate = user.locklentaupdate;
                    this.erased = user.erased;
                    this.sipid = user.sipid;
                    this.updatePeriod = user.updatePeriod;
                    this.filterMaxCount = user.filterMaxCount;
                    this.turbosip = user.turbosip;
                    this.turbosip5accessto = user.turbosip5accessto;
                    this.turbosip20accessto = user.turbosip20accessto;
                    this.colorlenta = user.colorlenta;
                    this.ignoreavg = user.ignoreavg;
                    this.redirecttarget = user.redirecttarget;
                    this.lentacolortype = user.lentacolortype;
                }
            }
        })

    }
}


</script>