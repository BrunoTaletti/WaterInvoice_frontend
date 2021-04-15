<template>
        <div class="botoes">
            <button type="button" class="btn btn-primary">Html</button>
            <button type="button" class="btn btn-success">Excel</button>
        </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
    .botoes{
        display: flex;
        float: right;
        margin: 0 10%;
    }

    button{
        font-weight: bold;
        padding: 5% 10%;
        margin: 0 5%;
        border: 2px solid #12130F;
        
        border-radius: 50px 50px 50px 50px;
    }

    button:hover{
        border: 2px solid #12130F;
    }

    .btn-success{
        color: #12130F;
        background-color: #81F499;
    }
    
    .btn-primary{
        color: #FCF7FF;
        background-color: #F61067;
    }

    .btn-success:hover{
        background-color: #65db7e;
    }

    .btn-primary:hover{
        background-color: #fa3c84;
    }
</style>