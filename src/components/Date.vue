<template>
	<div class="Date">
		<h4>{{ date }}</h4>
		<DatePicker
			is-dark
			color="red"
			:value="null"
			title-position="left"
			mode="single"
			:max-date="new Date()"
			v-model="date"
			:popover="{ placement: 'bottom', visibility: 'click' }"
		>
			<button>
				<svg
					width="22px"
					height="35px"
					viewBox="0 0 27 30"
					version="1.1"
					xmlns="http://www.w3.org/2000/svg"
					xmlns:xlink="http://www.w3.org/1999/xlink"
				>
					<g
						id="Welcome"
						stroke="none"
						stroke-width="1"
						fill="none"
						fill-rule="evenodd"
					>
						<g
							id="Desktop-HD"
							transform="translate(-1179.000000, -101.000000)"
							fill-rule="nonzero"
						>
							<g id="Group-2" transform="translate(251.000000, 79.000000)">
								<g
									id="iconfinder_date_1118214"
									transform="translate(928.000000, 22.000000)"
								>
									<path
										d="M0,30 L27,30 L27,9 L0,9 L0,30 Z M0.9,24.96 L4.95,24.96 L4.95,29.16 L0.9,29.16 L0.9,24.96 Z M15.75,19.92 L15.75,24.12 L11.25,24.12 L11.25,19.92 L15.75,19.92 Z M11.25,19.08 L11.25,14.88 L15.75,14.88 L15.75,19.08 L11.25,19.08 Z M10.35,24.12 L5.85,24.12 L5.85,19.92 L10.35,19.92 L10.35,24.12 Z M10.35,24.96 L10.35,29.16 L5.85,29.16 L5.85,24.96 L10.35,24.96 Z M11.25,24.96 L15.75,24.96 L15.75,29.16 L11.25,29.16 L11.25,24.96 Z M16.65,24.96 L21.15,24.96 L21.15,29.16 L16.65,29.16 L16.65,24.96 Z M16.65,24.12 L16.65,19.92 L21.15,19.92 L21.15,24.12 L16.65,24.12 Z M22.05,19.92 L26.1,19.92 L26.1,24.12 L22.05,24.12 L22.05,19.92 Z M22.05,19.08 L22.05,14.88 L26.1,14.88 L26.1,19.08 L22.05,19.08 Z M21.15,19.08 L16.65,19.08 L16.65,14.88 L21.15,14.88 L21.15,19.08 Z M16.65,14.04 L16.65,9.84 L21.15,9.84 L21.15,14.04 L16.65,14.04 Z M15.75,14.04 L11.25,14.04 L11.25,9.84 L15.75,9.84 L15.75,14.04 Z M10.35,14.04 L5.85,14.04 L5.85,9.84 L10.35,9.84 L10.35,14.04 Z M10.35,14.88 L10.35,19.08 L5.85,19.08 L5.85,14.88 L10.35,14.88 Z M4.95,19.08 L0.9,19.08 L0.9,14.88 L4.95,14.88 L4.95,19.08 Z M4.95,19.92 L4.95,24.12 L0.9,24.12 L0.9,19.92 L4.95,19.92 Z M22.05,29.16 L22.05,24.96 L26.1,24.96 L26.1,29.16 L22.05,29.16 Z M26.1,14.04 L22.05,14.04 L22.05,9.84 L26.1,9.84 L26.1,14.04 Z M4.95,9.84 L4.95,14.04 L0.9,14.04 L0.9,9.84 L4.95,9.84 Z"
										id="Shape"
										fill="#fff"
									/>
									<path
										d="M23.4,3.31707317 L22.5,3.31707317 L22.5,0.780487805 C22.5,0.349658537 22.0968,0 21.6,0 C21.1032,0 20.7,0.349658537 20.7,0.780487805 L20.7,3.31707317 L6.3,3.31707317 L6.3,0.780487805 C6.3,0.349658537 5.8968,0 5.4,0 C4.9032,0 4.5,0.349658537 4.5,0.780487805 L4.5,3.31707317 L3.6,3.31707317 C1.6119,3.31707317 0,4.51980488 0,6.24390244 L0,8 L27,8 L27,6.24390244 C27,4.51980488 25.3881,3.31707317 23.4,3.31707317 Z M5.3991,7.02439024 C4.4046,7.02439024 3.5991,6.32585366 3.5991,5.46341463 C3.5991,4.8862439 3.96405,4.38868293 4.5,4.1182439 L4.5,5.46341463 C4.5,5.8942439 4.9032,6.24390244 5.4,6.24390244 C5.8968,6.24390244 6.3,5.8942439 6.3,5.46341463 L6.3,4.11941463 C6.83505,4.38985366 7.1991,4.88741463 7.1991,5.46341463 C7.1991,6.32585366 6.3936,7.02439024 5.3991,7.02439024 Z M21.5991,7.02439024 C20.6046,7.02439024 19.7991,6.32585366 19.7991,5.46341463 C19.7991,4.8862439 20.16405,4.38868293 20.7,4.1182439 L20.7,5.46341463 C20.7,5.8942439 21.1032,6.24390244 21.6,6.24390244 C22.0968,6.24390244 22.5,5.8942439 22.5,5.46341463 L22.5,4.11941463 C23.03505,4.38985366 23.3991,4.88741463 23.3991,5.46341463 C23.3991,6.32585366 22.5936,7.02439024 21.5991,7.02439024 Z"
										id="Shape"
										fill="#C73D28"
									/>
									<rect
										id="Rectangle"
										fill="#231F20"
										x="8"
										y="11"
										width="2"
										height="3"
									/>
									<rect
										id="Rectangle"
										fill="#231F20"
										x="18"
										y="21"
										width="2"
										height="3"
									/>
									<rect
										id="Rectangle"
										fill="#231F20"
										x="13"
										y="21"
										width="2"
										height="3"
									/>
								</g>
							</g>
						</g>
					</g>
				</svg>
			</button>
		</DatePicker>
	</div>
</template>

<script>
import DatePicker from 'v-calendar/lib/components/date-picker.umd';

export default {
	name: 'Date',
	components: {
		DatePicker
	},
	data() {
		return {
			date: new Date().toString().slice(4, 15),
			newDate: null,
			months: [
				{
					text: 'Jan',
					digit: '01'
				},
				{
					text: 'Feb',
					digit: '02'
				},
				{
					text: 'Mar',
					digit: '03'
				},
				{
					text: 'Apr',
					digit: '04'
				},
				{
					text: 'May',
					digit: '05'
				},
				{
					text: 'Jun',
					digit: '06'
				},
				{
					text: 'Jul',
					digit: '07'
				},
				{
					text: 'Aug',
					digit: '08'
				},
				{
					text: 'Sep',
					digit: '09'
				},
				{
					text: 'Oct',
					digit: '10'
				},
				{
					text: 'Nov',
					digit: '11'
				},
				{
					text: 'Dec',
					digit: '12'
				}
			]
		};
	},
	watch: {
		date: function() {
			const textMonth = this.date.toString().slice(4, 7);
			const day = this.date.toString().slice(8, 10);
			const year = this.date.toString().slice(11, 15);
			const month = this.months.find(month => month.text === textMonth).digit;
			this.newDate = `${year}-${month}-${day}`;
			this.$emit('getDate', this.newDate);
			this.date = this.date.toString().slice(4, 15);
		}
	}
};
</script>

<style scoped>
h4 {
	color: rgb(235, 235, 235);
	margin-right: 12px;
	cursor: default;
}

button {
	background: #093172;
	border: none;
	width: 40px;
	height: 42px;
	margin-bottom: 6px;
	border-radius: 4px;
	cursor: pointer;
	transition: 0.15s;
}

button:focus {
	outline: none;
}

button:hover {
	background: #163f81;
}
</style>
