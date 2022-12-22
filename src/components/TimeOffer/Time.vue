<template>
    <div id="timer">
        <div class="row">
            <div class="col">
                <h1 data-days class="d-block"></h1>
                <p class="text-uppercase">days</p>
            </div>
            <div class="col">
                <h1 data-hours class="d-block"></h1>
                <p class="text-uppercase">hours</p>
            </div>
            <div class="col">
                <h1 data-minutes class="d-block"></h1>
                <p class="text-uppercase">minutes</p>
            </div>
            <div class="col">
                <h1 data-seconds class="d-block"></h1>
                <p class="text-uppercase">seconds</p>
            </div>
        </div>
    </div>
</template>
<script>
import timezz from "timezz";
import { onMounted } from "vue";
export default {
    name: 'Time',
    setup() {
        onMounted(() => {
            timezz(document.getElementById("timer"), {
                date: "march 01, 2023 00:00:00",
                update(event) {
                    if (document.getElementById("seconds") !== null) {
                        document.getElementById("seconds").innerHTML =
                            event.seconds === 1 ? "" : "";
                    }
                },
            });
        });
    },
}
</script>
<style lang="scss" scoped>
@import '../../Scss/Main.scss';
</style>