<template>
    <div class="mainBlock">
        <div class="nameBlock">Переход в карточку</div>
        <div class="bodyBlock">
            <div>
                <p>
                    Выберите, каким образом будет открываться детальное представление выбранного вами транспорта.
                </p>
            </div>
            <div class="settings-section__fields">
                <div class="settings-section__notifications block-2">
                    <div class="settings-section__field is-flex">
                        <div class="radio-label settings-section__radio">
                            <input id="is-notification-card" value="0"
                                   type="radio" checked="checked"
                                   name="redirecttarget"
                                   class="radio-label__input">
                            <label
                                    for="is-notification-card" class="radio-label__main">В карточку в текущем
                                окне</label>
                        </div>
                    </div>
                    <div class="settings-section__field is-flex">
                        <div class="radio-label settings-section__radio">
                            <input id="is-notification-page" value="1"
                                   type="radio" checked="checked"
                                   name="redirecttarget"
                                   class="radio-label__input">
                            <label
                                    for="is-notification-page" class="radio-label__main">В карточку в отдельном
                                окне</label>
                        </div>
                    </div>
                    <div class="settings-section__field is-flex">
                        <div class="radio-label settings-section__radio">
                            <input id="is-notification-source" value="2"
                                   type="radio" checked="checked"
                                   name="redirecttarget"
                                   class="radio-label__input">
                            <label
                                    for="is-notification-source" class="radio-label__main">На источник </label>
                        </div>
                        <img src="../assets/info-svgrepo-com.svg" class="infoImg">


                    </div>
                </div>
            </div>
        </div>


    </div>


</template>

<script>
export default {
    name: 'GoToCard',
}

</script>

<style>

</style>