<script>
    export let 
        userName, 
        jobTitle, 
        description,
        imageName;
</script>

<style>
    .contact-card{
        box-shadow : 0 2px 8px rgba(0, 0, 0, 0.26);
        max-width : 30rem;
        border-radius : 5px;
        margin : 1rem 0;
    }

    header{
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .thumb{
        width : 33%;
        height : 100%;
    }

    .user-data{
        width : 67%;
        display : flex;
        flex-direction: column;
        justify-content: center;
        padding-left : 1rem;
    }

    h1{
        font-size : 1.25rem;
        font-family : "Roboto Slab", sans-serif;
    }

    h2{
        font-size : 1rem;
        font-weight : normal;
        color : #5a5a5a;
    }

    .description{
        border-top : 1px solid #ccc;
        padding : 1rem;
    }
    img{
        height: 100%;
        width: 100%;
        object-fit: cover;
    }
</style>

<div class="contact-card">
    <header>
        <div class="thumb">
            <img src={imageName} alt={userName}>    
        </div>
        <div class="user-data">
            <h1>{userName}</h1>
            <h2>{jobTitle}</h2>
        </div>
    </header>
    <div class="description">
        <p>{description}</p>
    </div>
</div>