<template>
    <section class="content">
        <div class="info-bar">
            <div class="info-bar-left">
                <a href="" class="info-bar-link">
                    <span class="info-bar-expand"></span>
                    <span class="info-bar-grade-level">Kindergarten</span>
                    <span class="info-bar-student-count">2 students</span>
                </a>
                
            </div>
            <div class="info-bar-center">
                <a href="" class="info-bar-button">Today's Points</a>
            </div>
            <div class="info-bar-right">
                <a href="" class="info-bar-button">Options</a>
            </div>
        </div>
        <div class="student-grid">
            <a href="" class="student" v-for="student in students" v-bind:key="student.id">
                <span class="student-first">{{student.firstName}}</span>
                <span class="student-last">{{student.lastName}}</span>
            </a>
        </div>
    </section>
</template>

<script>
    export default {
        name: "Content",
        data() {
            return {
                students: [
                    {
                        id: 1,
                        firstName: "Jane",
                        lastName: "Doe"
                    },
                    {
                        id: 2,
                        firstName: "John",
                        lastName: "Doe"
                    },
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    a {
        text-decoration: none;
    }

    .content {
        padding: 14px 20px;
        position: relative;
        z-index: 100;
    }

    .info-bar {
        text-align: center;
        position: relative;
        margin-bottom: 50px;

        &-left,
        &-center,
        &-right {
            display: inline-block;

            @media (max-width: 650px) {
                display: block;
            }
        }

        &-left,
        &-right {
            position: absolute;
            @media (max-width: 650px) {
                position: relative;
            }
        }

        &-center {
            @media (max-width: 650px) {
                margin: 20px 0 40px;
            }
        }

        &-left {
            left: 0;
        }

        &-right {
            right: 0;

        }

        &-link {
            display: inline-block;
        }

        &-expand {
            display: inline-block;
            width: 24px;
            height: 24px;
            background: url("../assets/info-bar-icon-expand.png") no-repeat;
            background-size: 24px;
            background-position: center;
            padding: 4px;
        }

        &-grade-level {
            font-size: 26px;
            vertical-align: top;
            color: #000;
        }

        &-student-count {
            display: block;
            position: relative;
            right: 20px;
            color: #ccc;
            font-size: 12px;
        }

        &-button {
            color: #3B6FC8;
            border: 1px solid #3B6FC8;
            border-radius: 13px;
            padding: 10px 30px;
            width: 160px;
            position: relative;
            top: 15px;

            @media (max-width: 650px) {
                padding: 10px;
            }
        }

    }

    .student-grid {
        text-align: center;

        .student {
            display: inline-block;
            border: 1px solid #000;
            margin: 5px;
            padding: 10px;
            width: 155px;
            text-align: left;

            &-first,
            &-last {
                display: block;
                color: #000;
            }

            &-first {
                font-size: 28px;
            }

            &-last {
                font-size: 18px;
            }
        }
    }
</style>