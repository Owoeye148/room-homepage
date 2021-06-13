<template>
    <div class="about-cont">
        <div id="mot"><!--<img id="img-dark" src="../assets/img/image-about-dark.jpg" alt="">--></div>
        <div id="about-fur-cont">
            <div class="about-fur">
                <h5>ABOUT OUR FURNITURE</h5>
                <P>
                    Our multifunctional collection blends design and function to suit your individual taste.
                     Make each room unique, or pick a cohesive theme that best express your interests and what inspires you.
                     Find the furniture pieces you need, from traditional to contemporary styles or anything in between. 
                     Product specialists are available to help you create your dream space.
                </P>
            </div>
        </div>
        <div id="wch"><!--<img id="img-light" src="../assets/img/image-about-light.jpg" alt="">--></div>
    </div>
</template>

<script>
export default {
    name: "AboutCo"
}
</script>

<style scoped>
.about-cont {
    display: grid;
    grid-template-columns: 30% 40% 30%;
}
#mot {
    height: 35vh;
    background-image: url("../assets/img/image-about-dark.jpg");
    background-repeat: no-repeat;
}
#about-fur-cont {
    display: flex;
    align-items: center;
    justify-content: center;
}
.about-fur {
    margin-left: 10%;
    margin-right: 10%;

}
p {
    font-size: 12px;
    line-height: 20px;
    color: rgb(106, 99, 99);
}
#wch {
    background-image: url("../assets/img/image-about-light.jpg");
    background-repeat: no-repeat;
}
h5 {
    line-height: 5px;
    font-weight: 800;
    letter-spacing: 2px;
}
@media (max-width: 500px) {
    .about-cont {
        display: block;
        width: 100%;
        height: auto;
    }
    #mot {
        width: 100%;
        height: 30vh;
    }
    #wch {
        height: 30vh;
        width: 100%;
    }
    #about-fur-cont {
        display: block;
        height: auto;
    }
    #img-light {
        overflow: hidden;
    }
}
</style>