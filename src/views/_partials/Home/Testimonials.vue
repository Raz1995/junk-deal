<template>
    <div class="my-4 position-relative">
        <b-container>
            <i class="fas fa-quote-right quote"></i>
        </b-container>

        <carousel :per-page="1" :paginationEnabled="false">
            <slide :class="`p-4 bg-${key + 1}`" v-for="(testimonial, key) in testimonials" :key="`testimonials-${key}`">
                <b-container>
                    <div class="justify-content-between d-flex align-items-center">
                        <h2 class="ml-5 text-white jd-text-22 pl-5">{{ testimonial.name }}</h2>
                        <div class="align-self-start jd-text-21">
                            <i class="fas fa-star jd-theme-color" v-for="i in testimonial.feedback"></i>
                            <i class="fas fa-star" v-for="j in (5 - testimonial.feedback)"></i>
                        </div>
                    </div>
                    <p class="jd-text-dark jd-text-18 text-justify mt-4">
                        {{ testimonial.message }}
                    </p>
                </b-container>
            </slide>
        </carousel>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                testimonials: [
                    { name: "Anjeanette M.", message: " This company is amazing! I called them at 10am and they were here at 1pm .. I’m moving to another state I needed to throw some mattresses away.. and they were quick to come to help…", feedback: 5},
                    { name: "John Doe", message: " This company is amazing! I called them at 10am and they were here at 1pm .. I’m moving to another state I needed to throw some mattresses away.. and they were quick to come to help…", feedback: 3},
                    { name: "Emma Doe.", message: " This company is amazing! I called them at 10am and they were here at 1pm .. I’m moving to another state I needed to throw some mattresses away.. and they were quick to come to help…", feedback: 4},
                    { name: "Layla G.", message: " This company is amazing! I called them at 10am and they were here at 1pm .. I’m moving to another state I needed to throw some mattresses away.. and they were quick to come to help…", feedback: 1},
                    { name: "Jack B.", message: " This company is amazing! I called them at 10am and they were here at 1pm .. I’m moving to another state I needed to throw some mattresses away.. and they were quick to come to help…", feedback: 5}
                ]
            }
        }
    }
</script>

<style scoped lang="scss">
.quote{
    position: absolute;
    top: -10%;
    font-size: 60px;
    z-index: 1;
    color:#EF4E23;
}

.bg-1{
    background: rgba(53, 172, 163, 0.3)
}
.bg-2{
    background: rgba(53, 94, 172, 0.3);
}
.bg-3{
    background: rgba(145, 53, 172, 0.3);
}
.bg-4{
    background: rgba(172, 53, 53, 0.3);
}
.bg-5{
    background: rgba(158, 172, 53, 0.3);
}
</style>