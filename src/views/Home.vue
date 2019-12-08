<template>
	<div class="container">
		<!-- header section -->
		<header class="header">
			<!-- logo -->
			<img class="logo" src="@/assets/images/logo.png" alt="logo image" />

			<!-- search bar -->
			<form action="#" class="search">
				<input type="text" class="search__input" placeholder="search hotels" />
				<button class="search__button">
					<svg class="search__icon">
						<use
							xlink:href="@/assets/images/sprite.svg#icon-magnifying-glass"
						></use>
					</svg>
				</button>
			</form>

			<!-- right hand side navigation -->
			<nav class="user-nav">
				<div class="user-nav__icon-box">
					<svg class="user-nav__icon">
						<use xlink:href="@/assets/images/sprite.svg#icon-bookmark"></use>
					</svg>
					<span class="user-nav__notification">7</span>
				</div>
				<div class="user-nav__icon-box">
					<svg class="user-nav__icon">
						<use xlink:href="@/assets/images/sprite.svg#icon-chat"></use>
					</svg>
					<span class="user-nav__notification">14</span>
				</div>
				<div class="user-nav__user">
					<img
						src="@/assets/images/user.jpg"
						alt="user photo"
						class="user-nav__user-photo"
					/>
					<span class="user-nav__user-name"></span>
				</div>
			</nav>
		</header>

		<!-- main content section -->
		<div class="content">
			<nav class="sidebar">sidebar navigation</nav>
			<main class="hotel-view">hotel view</main>
		</div>
	</div>
</template>

<script>
	export default {};
</script>
