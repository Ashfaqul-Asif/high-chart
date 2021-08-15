<template>
  <div class="container px-4 mx-auto">
    <div
      class="Header w-full h-60 flex items-center justify-between bg-1b text-white rounded-md px-14"
    >
      <div class="text-xl">fat cap</div>
      <div style="text-xl text-left">
        <span class="text-56 font-gillSans">*Such & Co* Report</span>

        <br />
        <div class="grid place-items-center">
          <span class="text-3xl pl-6 font-gillSans">
            <i class="fas fa-calendar text-xl mr-2"></i>previous month
          </span>
        </div>
      </div>
      <div>
        <img
          class="inline object-cover w-20 h-20 mr-2 rounded-full"
          src="@/assets/avatarImage.svg"
          alt="Profile image"
        />
      </div>
    </div>
    <div class="flex">
      <div class="w-163 bg-no-repeat my-6 mr-4 text-center">
        <span class="font-gillSans text-xl font-bold">DATA JUMP</span>
        <div class="font-gillSans text-lg font-bold flex flex-col mt-4">
          <div class="rounded-100 w-8 h-8 grid place-items-center  mx-auto bg-1b text-white">
            <i class="far fa-chart-line text-xl"></i>
          </div>
          <span>CLV Metrices</span>
        </div>
        <div class="font-gillSans text-lg font-bold flex flex-col mt-4">
          <div class="rounded-100 w-8 h-8 grid place-items-center  mx-auto bg-1b text-white">
            <i class="fas fa-users-class "></i>
          </div>
          <span>CLV Table</span>
        </div>
        <div class="font-gillSans text-lg font-bold flex flex-col mt-4">
          <div class="rounded-100 w-8 h-8 grid place-items-center mx-auto bg-1b text-white">
           <i class="fas fa-user-circle text-2xl"></i>
          </div>
          <span>Customer Cohort Retention</span>
        </div>
        <div class="font-gillSans text-lg font-bold flex flex-col mt-4">
          <div class="grid place-items-center mx-auto ">
            <i class="fab fa-facebook text-3xl"></i>
          </div>
          <span>Facebook Base</span>
        </div>
      </div>
      <div class="flex-1 ml-14">
        <SalesConcentration class="mt-2" />
        <HelloWorld class="mt-2" />
        <CustomerLifetimeRevenue class="mt-2" />
        <CustomCohortSurvival class="mt-2" />
        <RevenueRetention class="mt-2" />
        <!-- <HistoricalRepeat class="mt-2" /> -->
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import CustomerLifetimeRevenue from '@/components/CustomerLifetimeRevenue.vue'
import SalesConcentration from '@/components/SalesConcentration.vue'
import CustomCohortSurvival from '@/components/CustomCohortSurvival.vue'
import RevenueRetention from '@/components/RevenueRetention.vue'
// import HistoricalRepeat from '@/components/HistoricalRepeat.vue'


export default {
  name: 'Home',
  components: {
    HelloWorld, CustomerLifetimeRevenue, SalesConcentration, CustomCohortSurvival,
    RevenueRetention
  }
}
</script>



