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
                <div class="col-lg-4 col-md-6 col-sm-12 my-3">
                    <div class="lastest-twitter">
                        <h5 class="text-light text-uppercase mb-4">lastest twitter</h5>
                        <a href="#">
                            <span class="text-light d-inline-block">
                                <i class="fa-brands fa-twitter"></i>
                            </span>
                            @colorlib
                        </a>
                        <p class="m-0">
                            Activello is a good option. It has a slider built into that displays the featured image in
                            the slider.
                        </p>
                        <p>
                            <a href="#">https://buff.ly/2zaSfAQ</a>
                        </p>
                        <div class="date my-3">21 Dec 2017</div>
                        <a href="#">
                            <span class="text-light d-inline-block">
                                <i class="fa-brands fa-twitter"></i>
                            </span>
                            @colorlib
                        </a>
                        <p class="m-0">
                            Activello is a good option. It has a slider built into that displays
                            the featured
                            <a href="#">https://buff.ly/2zaSfAQ</a>

                        </p>
                        <div class="date mt-3">21 Dec 2017</div>
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
<style lang="scss" scoped>
@import '@/Scss/Main.scss';

a {
    text-decoration: none !important;
    color: $Main-Color !important;
}

a,
p {
    font-size: 13px;
}

footer {
    background-color: $Footer-Color;

    .contact-us {
        p {
            color: #999;
        }
    }

    .lastest-twitter {



        p {
            color: #999;
        }

        .date {
            color: rgb(79, 78, 78);
            font-size: 13px;
        }
    }
}
</style>