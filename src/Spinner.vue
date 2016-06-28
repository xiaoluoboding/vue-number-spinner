<script>
	export default {
		name: 'Spinner',
		data () {
			return {
				val: 0,
			}
		},

		props: {
			min: {
				type: Number,
				default: 0
			},
			max: {
				type: Number,
				default: 999
			},
			step: {
        type: Number,
        default: 1
      }
		},

		computed: {
			
		},

		ready () {

		},

		methods: {
			plus: function() {
				this.val += this.step;
			},
			minus: function() {
				this.val -= this.step;
			},
			onWheel: function(e) {
				e.deltaY < 0 ? this.plus() : this.minus()
			}
		},

		watch: {
			val: function(newVal, oldVal) {
				if(newVal < this.min) {
					this.val = this.min
				}
				if(newVal > this.max) {
					this.val = this.max
				}
			}
		}
	}
</script>

<template>
	<div class="input-group">
		<span class="input-group-btn">
			<button class="btn-minus" @click="minus()"><span>-</span></button>
		</span>
		<input type="text" class="spinner" v-model="val" @keydown.up="plus" @keydown.down="minus" @wheel="onWheel">
		<div class="input-group-btn">
			<button class="btn-plus" @click="plus()"><span>+</span></button>
		</div>
	</div>
</template>

<style>

.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}

.input-group-btn {
  position: relative;
	display: table-cell;
  font-size: 0;
  white-space: nowrap;
}

.btn-plus {
  display: table-cell;
  font-family: 'Roboto Mono', Monaco, courier, monospace;
  font-weight: 700;
  color: #fff;
  height: 32px;
  background-color: #4fc08d;
  border-bottom: 2px solid #3aa373;
  border: none;
  transition: all 0.15s ease;
}

.btn-plus:hover {
  background-color: #5dc596;
  /*-webkit-transform: translate(0, -2px);
          transform: translate(0, -2px);*/
}

.btn-minus {
  display: table-cell;
  font-family: 'Roboto Mono', Monaco, courier, monospace;
  font-weight: 700;
  color: #fff;
  height: 32px;
  background-color: #f66;
  border: none;
  /*padding: 2px;*/
  /*transition: all 0.15s ease;*/
}

.btn-minus:hover {
  background-color: #f56;
  /*-webkit-transform: translate(0, -2px);
          transform: translate(0, -2px);*/
}

.spinner {
  height: 32px;
  line-height: 32px;
  box-sizing: border-box;
  padding: 6px 10px;
  border: 1px solid #e3e3e3;
  outline: none;
  transition: border-color 0.2s ease;
}

.spinner:focus {
	border: 1px solid #4fc08d;
}
</style>