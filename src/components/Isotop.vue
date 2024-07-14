<template>
    <div class="isotop-area">
        <div class="button-group">
            <button :class="{ active: activeButton === 1 }" @click="filter('.category-a', 1)">Commercial</button>
            <button :class="{ active: activeButton === 2 }" @click="filter('.category-b', 2)">Residential</button>
        </div>
        <div class="row isotope" ref="grid">
            <div class="col-sm-12 col-md-6 col-lg-4 element-item category-a" v-if="itemsToShow >= 1">
                <div class="element-item-inner">
                    <img src="../assets/images/image-group-1.png" alt="">
                    <div class="element-box">
                        <h6>Pavilion Hilltop</h6>
                        <p>Medium Bedroom</p>
                    </div>
                </div>
            </div>
            <div class="col-sm-12 col-md-6 col-lg-4 element-item category-a" v-if="itemsToShow >= 2">
                <div class="element-item-inner">
                    <img src="../assets/images/image-group-2.png" alt="">
                    <div class="element-box">
                        <h6>Pavilion Hilltop</h6>
                        <p>Medium Bedroom</p>
                    </div>
                </div>
                
            </div>
            <div class="col-sm-12 col-md-6 col-lg-4 element-item category-a" v-if="itemsToShow >= 3">
                <div class="element-item-inner">
                    <img src="../assets/images/Mask group (1).png" alt="">
                    <div class="element-box">
                        <h6>Pavilion Hilltop</h6>
                        <p>Medium Bedroom</p>
                    </div>
                </div>
                
            </div>
            <div class="col-sm-12 col-md-6 col-lg-4 element-item category-a" v-if="itemsToShow >= 4">
                <div class="element-item-inner">
                    <img src="../assets/images/Mask group (2).png" alt="">
                    <div class="element-box">
                        <h6>Pavilion Hilltop</h6>
                        <p>Medium Bedroom</p>
                    </div>
                </div>
                
            </div>
            <div class="col-sm-12 col-md-6 col-lg-4 element-item category-a" v-if="itemsToShow >= 5">
                <div class="element-item-inner">
                    <img src="../assets/images/image-group-5.png" alt="">
                    <div class="element-box">
                        <h6>Pavilion Hilltop</h6>
                        <p>Medium Bedroom</p>
                    </div>
                </div>
                
            </div>
            <div class="col-sm-12 col-md-6 col-lg-4 element-item category-a" v-if="itemsToShow >= 6">
                <div class="element-item-inner">
                    <img src="../assets/images/Mask group (3).png" alt="">
                    <div class="element-box">
                        <h6>Pavilion Hilltop</h6>
                        <p>Medium Bedroom</p>
                    </div>
                </div>
                
            </div>

            <div class="col-sm-12 col-md-6 col-lg-4 element-item category-b" v-if="itemsToShow >= 6">
                <div class="element-item-inner">
                    <img src="../assets/images/Mask group (3).png" alt="">
                    <div class="element-box">
                        <h6>Pavilion Hilltop</h6>
                        <p>Medium Bedroom</p>
                    </div>
                </div>
                
            </div>
        </div>

        <a class="viewMore" v-if="itemsToShow > 1" @click="viewMore">View More</a>

    </div>

</template>

<script>
import { ref, onMounted, watch } from 'vue';

export default {
    name: 'IsotopeGrid',
    setup() {
        const grid = ref(null);
        const activeButton = ref(1); // Default active button is 1 (Category A)
        const itemsToShow = ref(6);
        let iso = null;

        onMounted(() => {
            iso = new Isotope(grid.value, {
                itemSelector: '.element-item',
                layoutMode: 'fitRows',
            });
            console.log('Initial grid height:', grid.value.clientHeight); 
            iso.arrange({ filter: '.category-a' }); // Apply default filter for Category A
        });

        watch(itemsToShow, () => {
            iso.layout(); // Refresh the layout whenever itemsToShow changes
            console.log('Updated grid height:', grid.value.clientHeight); // Check updated height
        });

        const filter = (selector, buttonNumber) => {
            iso.arrange({ filter: selector });
            activeButton.value = buttonNumber; // Update active button
            if (buttonNumber === 1) {
                itemsToShow.value = 6; // Reset itemsToShow for Category A
            }
            console.log('Updated grid height:', grid.value.clientHeight); // Check updated height

        };

        const viewMore = () => {
            itemsToShow.value = 9;
        };

        return {
            grid,
            filter,
            activeButton,
            itemsToShow,
            viewMore,
        };
    },
};
</script>

<style scoped>
.isotope-area {
    padding: 20px;
}

.isotope {
    height: auto;
    /* overflow: hidden; */
    gap: 20px !important;
    padding: 20px 0 !important;
    /* height: 831.969px !important; */
}

.element-item {
    background: #f3f3f3;
    border-radius: 10px;
    padding: 0;
    position: absolute !important;
    /* top: 404.188px !important; */
}

.element-item-inner {
    margin: 20px;
    /* border: 1px solid red; */
    border-radius: 15px;
    overflow: hidden;
    text-align: left !important;
}

.element-item-inner img {
    width: 100%;
}

.element-box {
    padding: 20px;
}

.element-box h6 {
    font-weight: 600;
    font-size: 16px;
    color: #000;
}

.element-box p {
    margin-bottom: 0;
    font-size: 16px;
    color: #000;
}
.viewMore{
    text-decoration: none;
    color: #131839 !important;
    font-size: 24px;
    font-weight: 600;
}

.button-group {
    display: flex;
    justify-items: center;
    justify-content: center;
    gap: 30px;
    margin-bottom: 20px;
}

.button-group button {
    width: 230px;
    padding: 10px;
    color: #131839;
    font-size: 24px;
    line-height: 24px;
    background-color: #fff;
    border: 1px solid #000;
    border-radius: 5px;
}

.button-group button.active {
    background-color: #FBF4DF;
    color: #0E2442;
}
</style>