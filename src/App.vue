<script setup>
import { ref, onMounted } from 'vue';

// Define theme
const theme = ref('fantasy');

// Toggle theme function
const toggleTheme = () => {
  theme.value = theme.value === 'fantasy' ? 'dark' : 'fantasy';
  document.documentElement.setAttribute('data-theme', theme.value);
};

// Set initial theme on component mount
onMounted(() => {
  document.documentElement.setAttribute('data-theme', theme.value);
});
</script>

<template>
  <div class="min-h-screen bg-base-100">
    <!-- Navbar with vibrant colors -->
    <div class="navbar bg-primary text-primary-content shadow-xl">
      <div class="flex-1">
        <a class="btn btn-ghost text-xl font-bold">RE-THINK X 童軍總會</a>
      </div>
      <div class="flex-none">
        <button @click="toggleTheme" class="btn btn-circle btn-ghost">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z" />
          </svg>
        </button>
      </div>
    </div>

    <!-- Hero Section with vibrant gradient background -->
    <div class="hero gradient-primary py-10 text-white">
      <div class="hero-content text-center">
        <div>
          <h1 class="text-4xl md:text-5xl font-bold leading-tight">RE-THINK X 童軍總會</h1>
          <h2 class="text-2xl md:text-3xl font-semibold mt-2">全國海岸線海廢調查</h2>
          <div class="mt-6 flex justify-center">
            <div class="badge badge-secondary badge-lg mx-1">環保行動</div>
            <div class="badge badge-accent badge-lg mx-1">海洋保育</div>
            <div class="badge badge-info badge-lg mx-1">童軍活動</div>
          </div>
        </div>
      </div>
    </div>

    <!-- Project Information Sections -->
    <div class="container mx-auto px-4 py-10">
      <!-- Introduction Section -->
      <div class="card bg-base-100 shadow-xl mb-10">
        <div class="card-body">
          <h2 class="card-title text-3xl font-bold mb-6 text-center">號召全國童軍團， 一起守望台灣海岸線</h2>
          
          <!-- Execution Method -->
          <div class="mb-6">
            <h3 class="text-2xl font-bold bg-primary text-white px-4 py-2 inline-block mb-4"># 執行方式</h3>
            <ul class="list-disc list-inside space-y-2 text-lg ml-4">
              <li>全國146個點位， 每月調查一次， 延續一年</li>
              <li>調查海岸現況， 拍照、 填寫、 上傳調查紀錄表</li>
            </ul>
          </div>
          
          <!-- Expected Impact -->
          <div class="mb-6">
            <h3 class="text-2xl font-bold bg-primary text-white px-4 py-2 inline-block mb-4"># 預期影響力</h3>
            <ul class="list-disc list-inside space-y-2 text-lg ml-4">
              <li>得集全台灣 146 個海灘、 12個月的調查數據</li>
              <li>發布1份台灣海廢品牌審計調查</li>
            </ul>
          </div>
        </div>
      </div>

      <!-- Motivation and Purpose Section -->
      <div class="card bg-base-100 shadow-xl mb-10">
        <div class="card-body">
          <h2 class="card-title text-3xl font-bold mb-6 text-center">全國海岸線海廢調查</h2>
          
          <!-- Motivation -->
          <div>
            <h3 class="text-2xl font-bold bg-accent text-white px-4 py-2 inline-block mb-4"># 動機</h3>
            <p class="text-lg">身在四面環海的島嶼， 我們被 940,000 公斤的垃圾圍繞</p>
            <p class="text-lg">政府現有的海廢快篩僅一季一次，無法反映海灘狀況即時性，希望能將人力與資源放在最需要被清理的海灘。</p>
          </div>
          
          <!-- Purpose -->
          <div class="mt-8">
            <h3 class="text-2xl font-bold bg-secondary text-white px-4 py-2 inline-block mb-4"># 目的</h3>
            <ul class="list-disc list-inside space-y-4 text-lg ml-4">
              <li>
                <span class="font-bold">公開海岸線調查資訊：</span> 透過完成全國海岸線垃圾調查，即時更新全國海岸線年度髒亂狀況，供淨灘團體/民眾參考使用
              </li>
              <li>
                <span class="font-bold">年度影響力報告：</span> 透過深入調查的海廢數據，成為呼籲省思企業的包裝政策、民眾的丟棄行為可以如何改善的重要資料
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>

    <!-- Banner Image Section -->
    <div class="container mx-auto px-4 py-6 flex justify-center">
      <img src="/images/home-banner.jpg" alt="童軍與海廢調查活動" class="w-full md:w-1/2 h-auto rounded-lg shadow-lg">
    </div>

    <!-- Main Content with Three Cards for File Downloads (Vertical Layout) -->
    <div class="container mx-auto px-4 py-12">
      <h2 class="text-3xl font-bold text-center mb-10">活動資料下載</h2>
      <div class="flex flex-col gap-12">
        <!-- 說明 Card -->
        <div class="card bg-base-100 border-4 border-secondary shadow-xl hover:shadow-2xl hover-lift">
          <div class="card-body">
            <h2 class="card-title text-3xl text-secondary text-center mb-4 font-bold">說明資料</h2>
            <div class="divider divider-secondary"></div>
            <ul class="menu bg-transparent rounded-box w-full text-lg">
              <li>
                <a href="https://docs.google.com/presentation/d/19gE0pfixlM3L-GSkKcPZb40NMDduhHAK/edit?usp=drive_link&ouid=115104828132103303227&rtpof=true&sd=true" class="flex items-center gap-2">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
                  </svg>
                  說明會簡報-全國海岸線海廢調查.pptx
                </a>
              </li>
              <li>
                <a href="https://drive.google.com/file/d/1IFx2F5rsMRiPkcPVIzCprcFrq52Rhb1T/view" class="flex items-center gap-2">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
                  </svg>
                  說明會影片
                </a>
              </li>
              <li>
                <a href="https://drive.google.com/file/d/13nuPtiz-Ixb48231xKAtu6iCX6sfQa3U/view?usp=drive_link" class="flex items-center gap-2">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
                  </svg>
                  實施計畫-全國海岸線海廢調查.pdf
                </a>
              </li>
              <li>
                <a href="https://drive.google.com/file/d/1GpOyoF2UcDoYj9pZ8qiTVgxl80KZUVHY/view?usp=drive_link" class="flex items-center gap-2">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
                  </svg>
                  地球部落 EarthTribe 申請說明.pdf
                </a>
              </li>
              <li>
                <a href="https://docs.google.com/forms/d/1GFpf5eVZBJB40fVW1uunOT25EoHRX8l8LvQihBUk2JY/viewform?edit_requested=true" class="flex items-center gap-2">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
                  </svg>
                  2025全國海岸線海廢調查計畫-各群團認養報名
                </a>
              </li>
            </ul>
          </div>
        </div>

        <!-- 進度 Card -->
        <div class="card bg-base-100 border-4 border-accent shadow-xl hover:shadow-2xl hover-lift">
          <div class="card-body">
            <h2 class="card-title text-3xl text-accent text-center mb-4 font-bold">進度資料</h2>
            <div class="divider divider-accent"></div>
            <ul class="menu bg-transparent rounded-box w-full text-lg">
              <li>
                <a href="https://docs.google.com/spreadsheets/d/15KkdM-YP5OcOAXz17-xKLGkHhDpL-SNCFAGgj71V7ZE/edit?usp=drive_link" class="flex items-center gap-2">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
                  </svg>
                  全國海岸線海廢調查計畫-童軍團進度追蹤表.xlsx
                </a>
              </li>
              <li>
                <a href="https://docs.google.com/spreadsheets/d/1Z8ZoNXDJzvWovQZ4OR2g0Asf3k2HMYur/edit?usp=drive_link&ouid=115104828132103303227&rtpof=true&sd=true" class="flex items-center gap-2">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
                  </svg>
                  146點位認養表單-全國海岸線海廢調查.xlsx
                </a>
              </li>
            </ul>
          </div>
        </div>

        <!-- 表單 Card -->
        <div class="card bg-base-100 border-4 border-primary shadow-xl hover:shadow-2xl hover-lift">
          <div class="card-body">
            <h2 class="card-title text-3xl text-primary text-center mb-4 font-bold">表單</h2>
            <div class="divider divider-primary"></div>
            <ul class="menu bg-transparent rounded-box w-full text-lg">
              <li>
                <a href="https://drive.google.com/file/d/1HurpjQ0XiLCkJ1hXXyAbdBFSpNpSx4PP/view?usp=drive_link" class="flex items-center gap-2">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
                  </svg>
                  BA紙本紀錄表.pdf
                </a>
              </li>
              <li>
                <a href="https://drive.google.com/file/d/1rnjXA5JcSCl4ebrgltq4GumsLPgs5zEX/view?usp=drive_link" class="flex items-center gap-2">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
                  </svg>
                  紙本表單-首次調查.pdf
                </a>
              </li>
              <li>
                <a href="https://drive.google.com/file/d/1oUTP3jEoidJLQ67jG3RzMWEGKyo3IA_y/view?usp=drive_link" class="flex items-center gap-2">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
                  </svg>
                  紙本表單-非首次調查.pdf
                </a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>

    <!-- Call to Action Section -->
    <div class="gradient-secondary text-primary-content py-10 px-4 mt-8">
      <div class="container mx-auto text-center">
        <h2 class="text-3xl font-bold mb-4">加入我們的行動</h2>
        <p class="max-w-2xl mx-auto mb-6">一起為台灣的海岸線環境盡一份心力，參與全國海岸線海廢調查，為環境永續發展貢獻力量。</p>
        <a href="https://docs.google.com/forms/d/1GFpf5eVZBJB40fVW1uunOT25EoHRX8l8LvQihBUk2JY/viewform?edit_requested=true" target="_blank" rel="noopener noreferrer" class="btn btn-secondary btn-lg">立即報名</a>
      </div>
    </div>

    <!-- Full-width Image Section -->
    <div class="w-full">
      <img src="/images/home-footer.jpg" alt="海岸線海廢調查" class="w-full object-cover h-auto max-h-[400px]">
    </div>

    <!-- Footer -->
    <footer class="footer footer-center p-10 gradient-accent text-neutral-content">
      <div>
        <p class="font-bold text-xl">RE-THINK X 童軍總會</p> 
        <p>全國海岸線海廢調查 © 2025</p>
        <div class="flex flex-col mt-4 space-y-3">
          <a href="https://rethinktw.org/" target="_blank" rel="noopener noreferrer" class="btn btn-outline btn-block">
            <span class="font-bold">RETHINK 官方網站</span>
          </a>
          <a href="https://www.scout.org.tw/" target="_blank" rel="noopener noreferrer" class="btn btn-outline btn-block">
            <span class="font-bold">中華民國童軍總會</span>
          </a>
        </div>
      </div>
    </footer>
  </div>
</template>

<style scoped>
/* Additional custom styles can be added here */
</style>
