<nav>

    <div class="container">
    <h1>Firma XxX</h1>
	<ul>
		<li>
			<a href="/">Home</a>
		</li>
		<li>
			<a href="/about">O nas</a>
		</li>
		<li>
			<a href="/produkty">Produkty</a>
		</li>
		<li>
			<a href="/blog">Blog</a>
		</li>
		<li>
			<a href="/login">Logowanie</a>
		</li>
	</ul>
</div>
</nav>
<div class="container">
    <slot />
</div>
<style>
    nav {
        padding:  0.5em;
        background-color: #24170f;
        color: white;
    }

    .container{
        display: flex;
    }
	ul{
		display: flex;
        margin: 0;
        margin-left: auto;
		list-style: none;
        font-size: 1.5em;
	}
	
	li{
		margin-right: 20px;
	}
    h1{
        margin: 0;
        font-size: 2em;
        
    }
    a{
        text-decoration: none;
        color: white;
    }

</style>