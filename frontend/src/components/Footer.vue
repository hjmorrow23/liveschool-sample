<template>
    <footer class="footer">
        <div class="footer-wrapper">
            <div class="footer-left">
                <a href="" class="footer-selections footer-select-all"></a>
                <a href="" class="footer-selections footer-select-none"></a>
            </div>
            <div class="footer-center">
                <a href="" class="footer-view-links footer-view-links-active footer-edit"></a>
                <a href="" class="footer-view-links footer-view"></a>
                <a href="" class="footer-view-links footer-graph"></a>
            </div>
            <div class="footer-right">
                <a href="" class="footer-continue">
                    <span class="footer-continue-text">Continue</span>
                    <span class="footer-continue-arrow">
                        <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
	                        width="20px" height="20px" viewBox="0 0 12 11.45" enable-background="new 0 0 12 11.45" xml:space="preserve">
                            <polygon fill-rule="evenodd" clip-rule="evenodd" fill="#3E71C5" points="0,4.9 0,6.54 8.86,6.54 4.91,10.35 6.05,11.45 10.86,6.83 
                                12,5.72 10.86,4.62 6.05,0 4.91,1.1 8.86,4.9 "/>
                        </svg>
                    </span>
                </a>
            </div>
        </div>
    </footer>
</template>

<script>
    export default {
        name: "Footer"
    }
</script>

<style lang="scss" scoped>
    .footer {
        background: #3B6FC8;
        height: 73px;
        position: fixed;
        bottom: 0;
        width: 100%;
        z-index: 101;

        &-wrapper {
            width: 100%;
            height: 100%;
            position: relative;
            text-align: center;
        }

        &-left,
        &-center,
        &-right {
            display: inline-block;
            height: 100%;
        }

        &-center {
            float: left;
        }

        &-left,
        &-right {
            position: absolute;
        }

        &-left {
            left: 0;
        }

        &-right {
            right: 0;
        }

        &-selections {
            
        }

        &-view-links {

        }

        &-select-all {
            background: url("../assets/select-all-icon.png") no-repeat;
        }

        &-select-none {
            background: url("../assets/select-none-icon.png") no-repeat;
        }
        &-edit {
            background: url("../assets/edit-icon.png") no-repeat;
        }

        &-view {
            background: url("../assets/view-icon.png") no-repeat;
        }

        &-graph {
            background: url("../assets/bar-chart-icon.png") no-repeat;
        }

        &-selections,
        &-view-links {
            background-position: center;
            height: 100%;
            display: inline-block;
            width: 75px;
            position: relative;
            opacity: 1;
            transition: opcaity .35s;

            &:hover {
                opacity: .8;
            }
        }

        &-selections {
            @media (max-width: 650px) {
                display: none;
            }
        }

        &-view-links-active {
            @media (max-width: 650px) {
                opacity: .8;
            }

            &::before {
                content: "";
                display: inline-block;
                position: absolute;
                top: -15px;
                width: 25px;
                height: 25px;
                background: #fff;
                transform: rotate(45deg);
                left: 25px;

                @media (max-width: 650px) {
                    background: transparent;
                }
            }
        }

        &-continue {
            display: inline-block;
            height: 100%;
            color: #3B6FC8;
            background: #28548A;
            text-decoration: none;
            width: 150px;
            text-transform: uppercase;
            font-size: 16px;

            @media (max-width: 650px) {
                width: 75px;
            }
        }

        &-continue-text,
        &-continue-arrow {
            display: inline-block;
            position: relative;
            
        }

        &-continue-text {
            margin-right: 10px;
            top: 24px;

            @media (max-width: 650px) {
                display: none;
            }
        }

        &-continue-arrow {
            top: 28px;
        }
    }
</style>