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
			<nav class="sidebar">
				<ul class="side-nav">
					<li
						class="side-nav__item"
						:class="{ 'side-nav__item--active': active === 0 }"
						@click="toggleActive(0)"
					>
						<a href="#" class="side-nav__link">
							<svg class="side-nav__icon">
								<use xlink:href="@/assets/images/sprite.svg#icon-home"></use>
							</svg>
							<span>Hotel</span>
						</a>
					</li>
					<li
						class="side-nav__item"
						:class="{ 'side-nav__item--active': active === 1 }"
						@click="toggleActive(1)"
					>
						<a href="#" class="side-nav__link">
							<svg class="side-nav__icon">
								<use
									xlink:href="@/assets/images/sprite.svg#icon-aircraft-take-off"
								></use>
							</svg>
							<span>Flight</span>
						</a>
					</li>
					<li
						class="side-nav__item"
						:class="{ 'side-nav__item--active': active === 2 }"
						@click="toggleActive(2)"
					>
						<a href="#" class="side-nav__link">
							<svg class="side-nav__icon">
								<use xlink:href="@/assets/images/sprite.svg#icon-key"></use>
							</svg>
							<span>Car Rental</span>
						</a>
					</li>
					<li
						class="side-nav__item"
						:class="{ 'side-nav__item--active': active === 3 }"
						@click="toggleActive(3)"
					>
						<a href="#" class="side-nav__link">
							<svg class="side-nav__icon">
								<use xlink:href="@/assets/images/sprite.svg#icon-map"></use>
							</svg>
							<span>Tours</span>
						</a>
					</li>
				</ul>
				<div class="legal">&copy; 2017 by trillo. All rights reserved</div>
			</nav>
			<!-- HOTEL VIEW SECTION -->
			<main class="hotel-view">
				<div class="gallery">
					<figure class="gallery__item">
						<img
							class="gallery__photo"
							src="@/assets/images/hotel-1.jpg"
							alt="hotel image"
						/>
					</figure>
					<figure class="gallery__item">
						<img
							class="gallery__photo"
							src="@/assets/images/hotel-2.jpg"
							alt="hotel image"
						/>
					</figure>
					<figure class="gallery__item">
						<img
							class="gallery__photo"
							src="@/assets/images/hotel-3.jpg"
							alt="hotel image"
						/>
					</figure>
				</div>
				<div class="overview">
					<h1 class="overview__heading">
						Hotel Las Palmas
					</h1>
					<div class="overview__stars">
						<svg class="overview__icon-star" v-for="(star, i) in 5" :key="i">
							<use xlink:href="@/assets/images/sprite.svg#icon-star"></use>
						</svg>
					</div>
					<div class="overview__location">
						<svg class="overview__icon-location">
							<use
								xlink:href="@/assets/images/sprite.svg#icon-location-pin"
							></use>
						</svg>
						<button class="btn-inline">Albufeira, Portugal</button>
						<div class="overview__rating">
							<div class="overview__rating-average">8.6</div>
							<div class="overview__rating-count">429 votes</div>
						</div>
					</div>
				</div>
			</main>
		</div>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				active: 0
			};
		},
		methods: {
			toggleActive(activeItem) {
				this.active = activeItem;
			}
		}
	};
</script>
