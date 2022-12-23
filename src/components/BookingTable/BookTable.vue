<template>
    <section class="book-table">
        <div class="container">
            <div class="row gy-5">
                <div class="col-lg-6 col-md-12 col-sm-12">

                    <Head Title="book table" subTitle="Reservation" />
                    <div class="row">
                        <div class="col-lg-6 col-md-6 col-sm-12">
                            <label for="exampleInputEmail1" class="form-label text-capitalize">date</label>
                            <div class="mb-3 date">
                                <input class="form-control p-2" id="exampleInputEmail1" name="daterange"
                                    aria-describedby="emailHelp">
                                <i class="fa-regular fa-calendar-days"></i>
                            </div>
                        </div>
                        <div class="col-lg-6 col-md-6 col-sm-12">
                            <label class="form-label text-capitalize">name</label>
                            <input class="form-control p-2" placeholder="Name">
                        </div>
                        <div class="col-lg-6 col-md-6 col-sm-12">
                            <label class="form-label text-capitalize">time</label>
                            <select class="form-select p-2" aria-label="Default select example">
                                <option selected>9:00</option>
                                <option value="1">9:30</option>
                                <option value="2">10:00</option>
                                <option value="3">10:30</option>
                                <option value="4">11:00</option>
                                <option value="5">11:30</option>
                                <option value="6">12:00</option>
                                <option value="7">12:30</option>
                                <option value="8">13:00</option>
                                <option value="9">13:30</option>
                                <option value="10">14:00</option>
                                <option value="11">14:30</option>
                                <option value="12">15:00</option>
                                <option value="13">15:30</option>
                                <option value="14">16:00</option>
                                <option value="15">16:30</option>
                                <option value="16">17:00</option>
                                <option value="17">17:30</option>
                                <option value="18">18:00</option>
                                <option value="19">18:30</option>
                            </select>
                        </div>
                        <div class="col-lg-6 col-md-6 col-sm-12">
                            <label class="form-label text-capitalize">phone</label>
                            <input class="form-control p-2" placeholder="Phone">
                        </div>
                        <div class="col-lg-6 col-md-6 col-sm-12">
                            <label class="form-label text-capitalize mt-3">pepole</label>
                            <select class="form-select p-2" aria-label="Default select example">
                                <option selected>persone 1</option>
                                <option value="1">persone 2</option>
                                <option value="2">persone 3</option>
                                <option value="3">persone 4</option>
                                <option value="4">persone 5</option>
                                <option value="5">persone 6</option>
                                <option value="6">persone 7</option>
                                <option value="7">persone 8</option>
                                <option value="8">persone 9</option>
                                <option value="9">persone 10</option>
                                <option value="10">persone 11</option>
                                <option value="11">persone 12</option>

                            </select>
                        </div>
                        <div class="col-lg-6 col-md-6 col-sm-12">
                            <label class="form-label text-capitalize mt-3">email</label>
                            <input class="form-control p-2" placeholder="Email">
                        </div>
                        <div class="col-12 text-center py-4">
                            <a href="#" class="btn text-uppercase">book table</a>
                        </div>
                    </div>
                </div>
                <div class="col-lg-6 col-md-12 col-sm-12 d-flex justify-content-center align-items-center ">
                    <div class="content-img">
                        <img src="../../Imgs/booking-01.jpg.webp">
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<script>
import Head from '../HeadSections/Head.vue';

export default {
    name: "BookTable",
    components: { Head }
}
$().ready(function () {
    $('input[name="daterange"]').daterangepicker({
        singleDatePicker: true,
    })
})
</script>
<style lang="scss" scoped>
@import '../../Scss/Main.scss';

.book-table {
    background-image: url('../../Imgs/pattern1.png.webp');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    clear: both;
    padding: 100px 0px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;

    .date {
        position: relative;

        i,
        svg {
            position: absolute;
            z-index: 1;
            top: 18px;
            right: 13px;
            color: gray;
        }
    }

    .btn {
        background-color: $Copyright-Color;
        color: white;
        transition: all .3s ease-in-out;
        font-size: 13px;
        padding: 10px 35px;
        border-radius: 10px;
        font-weight: 200;
        margin-top: 10px;
    }

    .btn:hover {
        background-color: $Main-Color;
        transition: all .3s ease-in-out;
    }

    input,
    select {
        border: 2px solid rgb(200, 199, 199);
        padding: 12px !important;
        border-radius: 13px;
        transition: all .2s ease-in-out;


    }

    ::placeholder {
        color: rgb(188, 184, 184);
        font-size: 15px;
    }

    input:focus-visible,
    select:focus-visible {
        border-color: $Main-Color;
        outline: none;
        box-shadow: none;
        transition: all .2s ease-in-out;
    }

    input:focus::placeholder {
        color: transparent;
        transition: all .2s ease-in-out;
    }

    .content-img {
        overflow: hidden;
        border-radius: 10px;
        position: relative;
        perspective: 600px;

        img {
            width: 390px;
            height: 390px;
            transition: all .5s ease;

        }
    }

    .content-img:hover {
        img {
            transform: translateZ(40px);
            transition: all .5s ease;
        }
    }
}
</style>