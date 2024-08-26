<script>
import { ref } from 'vue'

const toggle = ref(false)

const toggleClick = () => {
  toggle.value = !toggle.value
}

export default {
  data() {
    return {
      message: 'Hello Vue.js!',
      toggleClick,
      toggle
    }
  },
  beforeCreate() {
    console.log('beforeCreate: Component instance is being initialized.')
  },
  created() {
    console.log('created: Component instance has been created.')
  },
  beforeMount() {
    console.log('beforeMount: Component is about to mount to DOM.')
  },
  mounted() {
    console.log('mounted: Component has been mounted to DOM.')
  },
  beforeUpdate() {
    console.log('beforeUpdate: Data is about to change.')
  },
  updated() {
    console.log('updated: DOM has been updated.')
  },
  beforeUnmount() {
    console.log('beforeUnmount: Component is about to be unmounted.')
  },
  unmounted() {
    console.log('unmounted: Component has been unmounted.')
  }
}
// import { onMounted } from 'vue'

// onMounted sẽ được chạy sau khi component được mount vào DOM
// onMounted(() => {
//   alert(`the component is now mounted.`)
// })

// onMounted không hoạt động trong hàm setTimeout
// setTimeout(() => {
//   onMounted(() => {
//     // this won't work.
//   })
// }, 100)
</script>

<template>
  <h1>- Lifecycle Hook</h1>
  <span>+ onMounted sẽ được chạy sau khi component được mount vào DOM</span>
  <br />
  <span>+ onMounted không hoạt động trong hàm setTimeout</span>
  <br />
  <h3>Lifecycle in Vue</h3>
  <button @click="toggleClick">Bật/tắt nội dung</button>
  <br />
  <div v-show="toggle">
    <div style="font-weight: bold">beforeCreate</div>
    <br />
    <p>
      Được gọi ngay sau khi một instance của Vue được khởi tạo, nhưng trước khi các reactive data và
      methods được khởi tạo.
    </p>
    <p>
      Ứng dụng: Sử dụng để kiểm tra dữ liệu hoặc thực hiện các thao tác cần thiết trước khi
      component bắt đầu khởi tạo.
    </p>
    <div style="font-weight: bold; margin-top: 20px">created</div>
    <br />
    <p>
      Được gọi sau khi instance đã được khởi tạo và reactive data, computed properties, watchers đã
      được thiết lập, nhưng trước khi DOM được render.
    </p>
    <p>
      Ứng dụng: Thường dùng để khởi tạo dữ liệu từ API hoặc thực hiện các thao tác không phụ thuộc
      vào DOM.
    </p>
    <div style="font-weight: bold; margin-top: 20px">beforeMount</div>
    <br />
    <p>Được gọi ngay trước khi DOM được render.</p>
    <p>
      Ứng dụng: Có thể sử dụng để thực hiện các công việc cuối cùng trước khi DOM bắt đầu render.
    </p>
    <div style="font-weight: bold; margin-top: 20px">mounted</div>
    <br />
    <p>Được gọi ngay sau khi component đã được render vào DOM.</p>
    <p>
      Ứng dụng: Thường dùng để làm việc với các thư viện liên quan đến DOM hoặc thực hiện các tác vụ
      phụ thuộc vào việc component đã được render.
    </p>
    <div style="font-weight: bold; margin-top: 20px">beforeUpdate</div>
    <br />
    <p>Được gọi khi data thay đổi nhưng trước khi DOM được cập nhật.</p>
    <p>
      Ứng dụng: Sử dụng để thực hiện các thay đổi hoặc tính toán trước khi DOM phản ánh sự thay đổi.
    </p>
    <div style="font-weight: bold; margin-top: 20px">updated</div>
    <br />
    <p>Được gọi sau khi DOM đã được cập nhật để phản ánh những thay đổi của data.</p>
    <p>Ứng dụng: Thực hiện các hành động phụ thuộc vào việc DOM đã được cập nhật.</p>
    <div style="font-weight: bold; margin-top: 20px">beforeUnmount</div>
    <br />
    <p>Được gọi ngay trước khi component bị hủy và DOM bị loại bỏ.</p>
    <p>Ứng dụng: Sử dụng để dọn dẹp tài nguyên, hủy sự kiện hoặc ngừng các listeners.</p>
    <div style="font-weight: bold; margin-top: 20px">unmounted</div>
    <br />
    <p>Được gọi sau khi component đã bị hủy và DOM bị loại bỏ.</p>
    <p>
      Ứng dụng: Dọn dẹp các tài nguyên cuối cùng hoặc thực hiện các tác vụ sau khi component đã hoàn
      toàn bị hủy.
    </p>
  </div>
</template>
