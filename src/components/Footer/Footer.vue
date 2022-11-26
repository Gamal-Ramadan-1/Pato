<template>
    <footer>
        <div class="container">
            <div class="row py-5">
                <div class="col-lg-4 col-md-6 col-sm-12 my-3">
                    <div class="contact-us">
                        <h5 class="text-light text-uppercase mb-4">conatct us</h5>
                        <p>
                            <i class="fa-solid fa-location-dot me-2"></i>
                            8th floor, 379 Hudson St, New York, NY 10018
                        </p>
                        <p>
                            <i class="fa-solid fa-phone me-2"></i>
                            (+1) 96 716 6879
                        </p>
                        <p class="mb-5">
                            <i class="fa-solid fa-envelope me-2"></i>
                            contact@site.com
                        </p>
                        <h5 class="text-light text-uppercase mb-4">opining times</h5>
                        <p>
                            09:30 AM – 11:00 PM
                            <span class="d-block">Every Day</span>
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>
<script>
export default {
    name: 'Footer'
}
</script>
<style lang="scss">
@import '@/Scss/Main.scss';

footer {
    background-color: $Footer-Color;

    .contact-us {
        p {
            color: #999;
            font-size: 13px;
        }
    }
}
</style>