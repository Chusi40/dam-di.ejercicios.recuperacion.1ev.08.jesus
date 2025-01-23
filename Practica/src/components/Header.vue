<template>
    <header>
        <div class="header-content">
            <img src="../../has.jpg" width="80px" alt="Foto de t1" />
            <h1>PRACTICA-DI</h1>
        </div>
    </header>
</template>

<style scoped>
body {
    background-color: #f7f9fc;
    color: #333333;
    font-family:Verdana, Geneva, Tahoma, sans-serif;
}

header {
    background-color: #ffffff;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
    margin-bottom: 20px;
}

.header-content {
    display: flex;
    align-items: center;
}

header img {
    margin-right: 20px;
    border-radius: 50%;
    border: 2px solid #592ef4;
}

header h1 {
    font-size: 28px;
    color: #647618;
    margin: 0;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 1.5px;
}
</style>