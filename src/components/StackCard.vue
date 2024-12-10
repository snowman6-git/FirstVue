<script>
export default {
  name: 'SildePage',
};
</script>

<template>

<div class="fan-container">
        <div class="card">
        <table border="0" id="">
            <tr>
                <td>Setting/설정</td>
            </tr>
            <tr>
                <td>icon</td>
            </tr>
        </table>
        </div>


        <div class="card">
        <table border="0" id="">
            <tr>
                <td>App/앱</td>
            </tr>
            <tr>
                <td>icon</td>
            </tr>
        </table>
        </div>



        <div class="card">
        <table border="0" id="">
            <tr>
                <td>Frontend/프론트앤드</td>
            </tr>
            <tr>
                <td>icon</td>
            </tr>
        </table>
        </div>

        <div class="card">
        <table border="0" id="">
            <tr>
                <td>Backend/백앤드</td>
            </tr>
            <tr>
                <td>icon</td>
            </tr>
        </table>
        </div>

        <div class="card">
            <!-- td옆으로 상승 2개면 가로 정렬-->
            <table border="0" id="">
                <tr>
                    <!-- <td rowspan="1"> -->
                    <!-- </td> -->
                    <td>AboutMe/내 소개</td>
                </tr>
                <tr>
                    <td>icon</td>
                </tr>
            </table>

        </div>
    </div>

</template>

<style>
.fan-container {
    /* transform: rotate(-90deg); */
    bottom: 7rem;
    position: fixed;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
}

.card {
    color: #DAA520;
    background-color: black;
    position: absolute;
    height: 15rem; width: 10rem;
    border-radius: 0.5rem;
    transition: transform 0.3s ease; /* 부드러운 변환 효과 */
    border: 0.1rem solid #DAA520;
}

/* 카드 위치 설정 */
.card:nth-child(1) {
    transform: rotate(-30deg) translateX(-100px);
}
.card:nth-child(2) {
    transform: rotate(-15deg) translateX(-60px);
}
.card:nth-child(3) {
    transform: rotate(0deg);
}
.card:nth-child(4) {
    transform: rotate(15deg) translateX(60px);
}
.card:nth-child(5) {
    transform: rotate(30deg) translateX(100px);
}

/* 카드 호버 효과 */
.card:hover {
    border: 0.25rem solid rgba(255, 255, 255, 1);
    /* z-index: 1; */
    transform: translateY(-10px); /* 위로 10px 이동 */
}

/* .card:not(:hover){
  filter: blur(1px);
  opacity: 0.5;
} */

/* 회전/기운각도로/위로 */
.card:nth-child(1):hover {
  transform: rotate(-30deg) translateX(-100px) translateY(-3.5rem);
}
.card:nth-child(2):hover {
    transform: rotate(-15deg) translateX(-60px) translateY(-3.5rem);
}
.card:nth-child(3):hover {
    transform: rotate(0deg) translateY(-3.5rem);
}
.card:nth-child(4):hover {
    transform: rotate(15deg) translateX(60px) translateY(-3.5rem);
}
.card:nth-child(5):hover {
    transform: rotate(30deg) translateX(100px) translateY(-3.5rem);
}

</style>
