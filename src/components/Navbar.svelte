<script>
    let isMenuOpen = false;

    function toggleMenu(){

        isMenuOpen = !isMenuOpen;
    }

    let current = 0;
</script>

<div class="navbar">
    <a href="/" class="logo"><h1>Firma XxX</h1></a>
    <nav class:open={isMenuOpen}>
        <ul>
            <li on:click = {()=>(isMenuOpen = false)}>
                <a class:current={current === 0} on:click = {()=>(current = 0)} href="/">Home</a>
            </li>
            <li on:click = {()=>(isMenuOpen = false)}>
                <a class:current={current === 1} on:click = {()=>(current = 1)} href="/about">O nas</a>
            </li>
            <li on:click = {()=>(isMenuOpen = false)}>
                <a class:current={current === 2} on:click = {()=>(current = 2)} href="/products">Produkty</a>
            </li>
            <li on:click = {()=>(isMenuOpen = false)}>
                <a class:current={current === 3} on:click = {()=>(current = 3)} href="/blog">Blog</a>
            </li>
            <li on:click = {()=>(isMenuOpen = false)} class="sign-in-btn">
                <a on:click={()=>(current = 4)} href="/login">Logowanie</a>
            </li>
        </ul>
    </nav>
    <button class="burger" on:click={toggleMenu}>
        <div class="bar-1"/>
        <div class="bar-2"/>
        <div class="bar-3"/>
    </button>

    <style>
        .navbar {
            background-color: var(--dark);
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: relative;
            height: 4rem;
        }
        .logo {
            margin-left: 6vw;
        }
        nav{
           display: none;
        }
        nav.open {
            display: block;
            position: absolute;
            top: 100%;
            left: 0;
            background-color: var(--dark);
            width: 100%;
        }
        ul{
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            gap: 5vh;
            margin-top: 2vh;
            margin-bottom: 4vh;
            list-style: none;
            font-size: 1.1rem; 
        }

        .current{
            position:relative;
        }
        .current::after{
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 2px;
            background-color: var(--secondary);
        }

        
        .sign-in-btn{

            background-color: var(--primary);
            padding: 0.4rem 1rem;
            border-radius: 10px;
            font-weight: 500;
        }
        .burger{
            height: 28px;
            aspect-ratio: 1;
            border: 2px solid var(--light);
            background-color: transparent;
            border-radius: 5px;
            margin-right: 6vw;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .burger > div {
            height: 2px;
            width: 14px;
            background-color: var(--light);
            position: absolute;
        }
        .bar-1{
            transform: translateY(-5px);
        }
        .bar-3{
            transform: translateY(5px);
        }
    </style>
</div>