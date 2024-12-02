<template lang="">
   
   <section class="banner text-[#ffffff] flex items-center  -mt-[85px] z-[2] min-h-screen  pb-[120px] relative bg-[#000000]">
        <canvas ref="globeCanvas" class="absolute top-0 left-1/2 -translate-x-1/2 w-[100%] h-[95%] mx-auto rounded-full"></canvas>
        <div class="mx-auto w-full max-w-7xl px-4 pt-[140px] relative z-10">
            <h2 class="md:text-[3rem] text-3xl leading-tight font-bold ">
                WELCOME TO <br />
                KAIN'CHI,THE FUTURE<br />OF WEB SHOPING
            </h2>
            <p class="text-[12px] pt-4">
                Lorem, ipsum dolor sit amet consectetur adipisicing elit. Iure eos molestiae<br />
                maxime consequatur. At voluptates non ex vel. Facilis architecto, natus praesentium!
            </p>

            <div
                class=" mt-10 text-white gap-2 transition-all duration-300 hover:bg-white hover:text-[#212121] flex items-center w-[200px] cursor-pointer justify-center rounded-full  border-white border py-[8px] ">
                <svg class="size-5" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="currentColor" fill-rule="evenodd" d="M5 19h14a1 1 0 0 1 0 2H5a1 1 0 0 1 0-2m8-5.825l3.243-3.242l1.414 1.414L12 17.004l-5.657-5.657l1.414-1.414L11 13.175V2h2z"/></svg>
                <p class="mt-[3px]">Download App</p>
            </div>
        </div>
    </section>

</template>
<script>
export default {
    data() {
        return {
            canvas: null,
            ctx: null,
            rotationX: 0,
            rotationY: 0,
            targetRotationX: 0,
            targetRotationY: 0,
            worldImage: null,
            centerX: 0,
            centerY: 0,
            lastMouseX: 0,
            lastMouseY: 0,
            stars: [],
            sphereRadius: 0,
            isMouseDragging: false,
            autoRotationSpeed: 0.015,
            mouseRotationSpeed: 0.5
        }
    },
    mounted() {
        this.loadWorldTexture()
        window.addEventListener('resize', this.handleResize)
        window.addEventListener('mousemove', this.handleMouseMove)
    },
    beforeUnmount() {
        window.removeEventListener('resize', this.handleResize)
        window.removeEventListener('mousemove', this.handleMouseMove)
    },
    methods: {
        loadWorldTexture() {
            this.worldImage = new Image()
            this.worldImage.src = 'https://raw.githubusercontent.com/mrdoob/three.js/master/examples/textures/planets/earth_atmos_2048.jpg'
            this.worldImage.onload = () => {
                this.initCanvas()
                this.animate()
            }
        },
        initCanvas() {
            this.canvas = this.$refs.globeCanvas
            this.ctx = this.canvas.getContext('2d')
            this.handleResize()
            
            this.stars = Array(100).fill().map(() => ({
                x: Math.random() * this.canvas.width,
                y: Math.random() * this.canvas.height,
                radius: Math.random() * 1.5,
                opacity: Math.random(),
                fadeDirection: Math.random() > 0.5 ? 1 : -1
            }))
        },
        handleResize() {
            this.canvas.width = window.innerWidth
            this.canvas.height = window.innerHeight
            this.centerX = this.canvas.width / 2
            this.centerY = this.canvas.height / 2
            this.sphereRadius = Math.min(this.canvas.width, this.canvas.height) * 0.3
        },
        handleMouseMove(e) {
            const rect = this.canvas.getBoundingClientRect()
            const mouseX = e.clientX - rect.left - this.centerX
            
            this.targetRotationX = (mouseX / this.centerX) * Math.PI * this.mouseRotationSpeed
        },
        drawGlobe() {
            this.ctx.clearRect(0, 0, this.canvas.width, this.canvas.height)

            this.updateAndDrawStars()

            this.targetRotationX += this.autoRotationSpeed

            this.rotationX += (this.targetRotationX - this.rotationX) * 0.2

            this.ctx.save()
            this.ctx.translate(this.centerX, this.centerY)
            
            this.ctx.beginPath()
            this.ctx.arc(0, 0, this.sphereRadius, 0, Math.PI * 2)
            this.ctx.clip()

            this.ctx.rotate(this.rotationX)
            
            this.ctx.drawImage(
                this.worldImage,
                -this.sphereRadius,
                -this.sphereRadius,
                this.sphereRadius * 2,
                this.sphereRadius * 2
            )

            const gradient = this.ctx.createRadialGradient(
                this.sphereRadius * 0.3, -this.sphereRadius * 0.3, 0,
                0, 0, this.sphereRadius
            )
            gradient.addColorStop(0, 'rgba(255,255,255,0.4)')
            gradient.addColorStop(0.5, 'rgba(0,0,0,0)')
            gradient.addColorStop(1, 'rgba(0,0,0,0.6)')
            this.ctx.fillStyle = gradient
            this.ctx.fillRect(-this.sphereRadius, -this.sphereRadius, this.sphereRadius * 2, this.sphereRadius * 2)

            this.ctx.restore()
        },
        updateAndDrawStars() {
            this.stars.forEach(star => {
                star.opacity += 0.005 * star.fadeDirection
                if (star.opacity > 1 || star.opacity < 0) {
                    star.fadeDirection *= -1
                }

                this.ctx.beginPath()
                this.ctx.arc(star.x, star.y, star.radius, 0, Math.PI * 2)
                this.ctx.fillStyle = `rgba(255, 255, 255, ${star.opacity})`
                this.ctx.fill()
            })
        },
        animate() {
            this.drawGlobe()
            requestAnimationFrame(this.animate)
        }
    }
}
</script>
<style lang="">
    
</style>