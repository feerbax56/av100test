<template>
    <div class="mainBlock">
        <div class="nameBlock">Прочие настройки</div>
        <div class="bodyBlock">
            <label class="multiselect__label caption">Часовой пояс</label>
            <input name="" type="text" autocomplete="off" spellcheck="false" placeholder="Москва">
            <div>
                <input id="input-125" type="checkbox" class="checkbox-label__input" value="true">
                <label for="input-125" class="checkbox-label__main">
                    Автоматически переходить к новым объявлениям
                </label>
                <img src="../assets/info-svgrepo-com.svg" class="infoImg">
                <!--                <span class="checkbox-label__main-tooltip"><svg-->
                <!--                        content="Лента будет автоматически обновляться 1 раз в 3 секунды"-->
                <!--                        xmlns="http://www.w3.org/2000/svg"-->
                <!--                        -->
                <!--                        class="checkbox-label__tooltip-icon icon sprite-icons" data-tippy-directive="" tabindex="0"><use-->
                <!--                        href="/_nuxt/8518bae7a68da9e9ae1000967ded07dc.svg#i-i-hint"-->
                <!--                        xlink:href="/_nuxt/8518bae7a68da9e9ae1000967ded07dc.svg#i-i-hint"></use></svg></span>-->

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
<!--                            <span class="checkbox-label__main-tooltip"><svg-->
                            <!--                                content="Включение зеленого/желтого цвета"-->
                            <!--                                xmlns="http://www.w3.org/2000/svg"-->
                            <!--                                class="checkbox-label__tooltip-icon icon sprite-icons"-->
                            <!--                                data-tippy-directive="" tabindex="0"><use-->
                            <!--                                href="/_nuxt/8518bae7a68da9e9ae1000967ded07dc.svg#i-i-hint"-->
                            <!--                                xlink:href="/_nuxt/8518bae7a68da9e9ae1000967ded07dc.svg#i-i-hint"></use></svg></span>-->
                        </div>
                    </div>
                </div>

            </div>

        </div>

    </div>

    <button>
        <span>Сохранить</span>
    </button>
</template>

<script>
export default {
    name: 'OtherSettings',
}

</script>

<style>

</style>