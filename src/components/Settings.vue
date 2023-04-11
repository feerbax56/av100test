<template>
    <h1>test</h1>
    <other-settings/>
    <go-to-card/>
    <new-collection-alerts/>
</template>

<script>

import OtherSettings from "@/components/OtherSettings.vue";
import GoToCard from "@/components/GoToCard.vue";
import NewCollectionAlerts from "@/components/NewCollectionAlerts.vue";

export default {
    name: 'SettingsBlock',
    components: {
        OtherSettings,
        GoToCard,
        NewCollectionAlerts,
    }
}


</script>