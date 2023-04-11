<template>
    <div class="mainBlock">
        <div class="nameBlock">Прочие настройки</div>
        <div class="bodyBlock">
            <div class="labelBlock">
                <label class="multiselectCaption">Часовой пояс</label>
                <v-select class="inputSity"
                          clearable
                          :items="['Калининград', 'Москва', 'Самара', 'Екатеринбург', 'Омск', 'Красноярск','Иркутск', 'Якутск', 'Владивасток', 'Магадан', 'Камчатка' ]"
                ></v-select>
            </div>

            <div class="labelBlock">
                <v-container fluid>
                    <v-checkbox
                        v-model="checkbox1"
                        :label="`Автоматически переходить к новым объявлениям`"
                    ></v-checkbox>
                    <v-checkbox
                        v-model="checkbox2"
                        :label="`Включить цвета в ленте`"
                    ></v-checkbox>
                </v-container>

                     <img src="../assets/info-svgrepo-com.svg" class="infoImg">
            </div>

            <div>
                <div class="settings-section__field" style="display: block;">
                    <div class="checkbox-label has-tooltip">
                        <div style="display: flex;"><input id="input-126" type="checkbox" class="checkbox-label__input"
                                                           value="false"> <label for="input-126"
                                                                                 class="checkbox-label__main">
                            Включить цвета в ленте
                        </label>
                            <img src="../assets/info-svgrepo-com.svg" class="infoImg">
                        </div>
                    </div>
                </div>

            </div>
            <button>
                <span>Сохранить</span>
            </button>
        </div>

    </div>


</template>

<script>
export default {
    name: 'OtherSettings',

}

</script>

<style>
.multiselectCaption {
    margin: 4px 25px 0 0;
    font-size: 14px;
}

.inputSity {
    width: 214px;
    height: 28px;
    margin: 0;
}

.labelBlock {
    display: flex;
    align-content: center;
}
</style>