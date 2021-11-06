<script>
    import Carousel from 'svelte-carousel';

    let imgTab = [
        {
            name: 'name1',
            url: 'img_01_xl.jpg'
        },
        {
            name: 'name2',
            url: 'img_03_xl.jpg'
        },
        {
            name: 'name3',
            url: 'img_06_xl.jpg'
        }
    ];

</script>


<div class="content">
    <Carousel
        autoplay
        autoplayDuration={5000}
        autoplayProgress
        pauseOnFocus
    >
    {#each imgTab as { name, url }}
    <div class="box">
        <img class="box-img" src="{url}" alt="{name}"/>
        <h2 class="box-title">{name}</h2>
    </div>   
    {/each}

    </Carousel>

</div>



<style lang='scss'>

.content {
    width: 70%;
    margin: auto;
}

.box {
    position: relative;
}
.box-img {
    width: 100%;
    
}

.box-title {
    background-color: #fff;
    position: absolute;
    bottom: 10%;
    right: 50%;
}
</style>