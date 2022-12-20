<template>
    <nav>
        <h1>CAMPANHA</h1>
        <div class="opt">
            <a href="" class="icons"><img src="/Imgs/Search.png" alt="Search"></a>
            <a href="" class="icons"><img src="/Imgs/Bell.png" alt="Bell"></a>
            <a href="" class="icons"><img src="/Imgs/chat.png" alt="Chat"></a>
            <a href="" class="icons"><img src="/Imgs/share.png" alt="Share"></a>
            <div id="user">
                <a href="" class="icons">
                    <img src="/Imgs/user.png" alt="User">
                Admin
                </a>
            </div>

        </div>
    </nav>
</template>
<script>
export default {
    name:"Nav"
}
</script>
<style scoped>
    *{
        font-family: helvetica;
    }
    img{
        max-width: 20px;
        height: 25px;
    }
    nav{
        height: 150px;
        display: flex;
        justify-content: space-between;
        padding: 10px 20px;
    }
    nav .opt{
        padding: 15px;
        margin: 0 5px;
        display: flex;
        
    }
    nav .opt .icons{
        margin: 0 10px;
        text-decoration: none;
        color: rgb(118, 118, 118);
        height: 30px;
        display: flex;
        justify-content: center;
        align-items: center;
        align-content: center;
    }
    nav .opt #user{
        background-color: rgb(238, 238, 238);
        border-radius: 5px;
        height: 30px;
        padding: 0 4px;
        display: flex;
        justify-content: center;
        align-items: center;
        align-content: center;
        
    }
    nav .opt #user img{
        height: 20px; width: 15px;
        margin-right: 8px;
    }
</style>