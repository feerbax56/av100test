<template>
    <other-settings/>
    <go-to-card/>
    <new-collection-alerts/>
    <me-account/>
    <CallViaSIP/>
</template>

<script>

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
    }
}


</script>