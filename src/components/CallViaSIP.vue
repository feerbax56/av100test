<template>
    <div class="mainBlock">
        <div class="nameBlock">Звонок через SIP
            <v-switch
                    v-model="model"
                    hide-details
                    inset
            ></v-switch>
        </div>

        <div class="switcher-label settings-section__switcher switcher-label--thin">
            <div class="bodyBlock">
                <p>Включите эту функцию чтобы Авито и другие площадки не блокировали ваш аккаунт. Будет выглядеть так,
                    будто
                    звонки совершаются с разных номеров.</p>
            </div>

        </div>
    </div>


</template>

<script>
export default {
    name: 'CallViaSIP',
    data() {
        return {
            model: true,
        }
    },
}

</script>

<style>

</style>