<template>
    <section class="realworld">
        <div class="container">
            <div class="explore">
                <div class="explore-content">
                    <SectionTitle :subtitle="subtitle" :title="title" :isCentered="false" />
                    <div class="explore-button-wrap">
                        <Button
                            link="#"
                            text="Explore Textures"
                            type="primary"
                            color="green"
                        />
                        <Button
                            link="#"
                            text="Explore Models"
                            type="primary"
                            color="blue"
                        />
                    </div>
                </div>
                <div class="explore-texture">
                    <img :src="texture_current" class="explore-texture-current" alt="">
                    <img :src="texture_prev" class="explore-texture-prev" alt="">
                    <img :src="texture_next" class="explore-texture-next" alt="">
                </div>
                <div class="explore-control">
                    <div><a href class="explore-control-prev"><img src="@/assets/img/icon-arrow.png" alt=""></a></div>
                    <p class="explore-texture-number">{{ texture_number }}</p>
                    <p class="explore-texture-title">{{ texture_title }}</p>
                    <div><Button
                        link="#"
                        text="See in gallery"
                        type="secondary"
                        color=""
                    /></div>
                    <div><a href class="explore-control-next"><img src="@/assets/img/icon-arrow.png" alt=""></a></div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import SectionTitle from "@/components/SectionParts/SectionTitle";
import Button from "@/components/Button";

export default {
    name: "SectionRealworld",
    components: {
        SectionTitle,
        Button
    },
    data() {
        return {
            subtitle: "Real World Textures",
            title: "PBR materials and models from the real worldwide manufacturers",
            texture_number: "0059",
            texture_title: "WOODVEENER OAK COPPER2",
            texture_current: "_nuxt/assets/img/spheres/sphere-4-1.png",
            texture_prev: "_nuxt/assets/img/spheres/sphere-5.png",
            texture_next: "_nuxt/assets/img/spheres/sphere-6.png"
        }
    }
}
</script>