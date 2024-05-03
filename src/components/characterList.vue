<script setup>
const character = defineProps(["name", "image", "status", "species", "gender", "location", "episodes"])
</script>

<template>
    <div class="card" style="width: 18rem; padding: 0; margin: 1rem auto; box-shadow: rgba(0, 0, 0, 0.35) 0px 3px 8px; border: 2px solid #52d1ff;">
        <div class="ImgCard">
            <img :src="character.image" class="card-img-top" alt="...">
        </div>
        <div class="card-body">
            <h3 class="card-title">{{ character.name}}</h3>
            <p class="card-text"><span>Status:</span> {{ character.status}} 
                <i id="alive" class="bi bi-check-circle-fill" style="color: green;"></i>
                <i id="dead" class="bi bi-x-circle-fill" style="color: red;" hidden></i>
                <i id="unknown" class="bi bi-question-circle-fill" style="color: grey;" hidden></i>
            </p>
            <p class="card-text"><span>Espécie:</span> {{ character.species}}</p>
            <p class="card-text"><span>Gênero:</span> {{ character.gender}}</p>
            <p class="card-text"><span>Localização atual:</span> {{ character.location.name}}</p>
            <p class="card-text"><span>Episódios:</span> {{ character.episodes.length }}</p>
        </div>
    </div>
</template>

<style>

i{
    padding-top: 4px;
    display: flex;
    float: right;
}

p, span{
    font-size: 16px;
}

h3, p{
    font-family: 'Oswald';
    font-weight: 300;
}

span{
    font-weight: 500;
}

.card{
    overflow: hidden
}

.ImgCard{
    width: 100%;
    display: block;
    object-fit: cover;
    filter: grayscale(1);
}

.ImgCard:hover{
    cursor: pointer;
    filter: none;
}

</style>