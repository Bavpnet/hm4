<script lang="ts">

    interface Inpt {
        url: string;
    }

    let getData = async () => {
        let response = await fetch("https://random.dog/woof.json");
        let myInpt: Inpt = await response.json();
        console.log(myInpt.url);
        return myInpt.url;
    }



    async function call() {
        event.preventDefault();
        let img = document.getElementById('image') as HTMLImageElement;

       img.src   = await getData();

    }



</script>

<main>
    <div class="flexbox-container">
        <div class="flexbox1">
            THIS is API about random dogs 🐶
        </div>
        <div class="flexbox2">
            <button id="generate1" on:click = {call}>
                тык
            </button>
        </div>

        <div class="image-container">

            <img id = "image" src="">
        </div>


    </div>
</main>

<style>
    .flexbox-container{

        display: flex;
        flex-direction: column;
        align-items: center;

    }

    .flexbox1{
        display: flow-root;
        text-align: center;
        margin-top: 20px;
        font-size: 30px;
    }





    .flexbox-container{
        color: #FFFFFF;
    }

    button {
        margin-bottom: 10px;
        border: #FFFFFF 1px solid;
    }


</style>