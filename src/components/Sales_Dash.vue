<template>
  <div class="main">
    <br />
    <!-- Sales block  Row -->
    <div id="filter">
      
      <b-dropdown id="dropdown-1"  class="m-md-2">
        <template #button-content>
          <b-icon icon="filter" aria-hidden="true"></b-icon> Filter
        </template>
        <b-dropdown-item>This Month</b-dropdown-item>
        <b-dropdown-item>This Quarter</b-dropdown-item>
        <b-dropdown-item active>This Year</b-dropdown-item>
        <b-dropdown-item  >Past 2 Year</b-dropdown-item>
        <b-dropdown-item  >Past 3 Year</b-dropdown-item>
        <!-- <b-dropdown-divider></b-dropdown-divider> -->
        <!-- <b-dropdown-item active>Active action</b-dropdown-item>
        <b-dropdown-item disabled>Disabled action</b-dropdown-item> -->
      </b-dropdown>
    </div>
 
    <div class="heading">
      <h5>Sales</h5>
    </div>
    <div class="salse">
      <!-- Col -->
      <div class="box" v-for="values in sales" :key="values.icon">
        <div class="graph">
          <b-icon :icon="values.icon" font-scale="3"></b-icon>
        </div>
        <div class="text">
          <h5>{{ values.text1 }}</h5>
          <h4>{{ values.text2 }}</h4>
        </div>
      </div>
    </div>
    <!-- <div id="graph">
          <apexchart width="500" type="bar" :options="options" :series="series"></apexchart>

    </div> -->
    <!-- <br><br><br><br><br><br><br><br><br><br><br><br><br><br> -->
    <hr />
    <div class="heading">
      <h5>Membership Status</h5>
    </div>
    <div class="salse">
      <!-- Col -->
      <div class="box" v-for="values in membership" :key="values.icon">
        <div class="graph">
          <b-icon :icon="values.icon" font-scale="3"></b-icon>
        </div>
        <div class="text">
          <h5>{{ values.text1 }}</h5>
          <h4>{{ values.text2 }}</h4>
        </div>
      </div>
    </div>
    <hr />
    <div class="heading">
      <h5>PT (Personal Training)</h5>
    </div>
    <div class="salse">
      <!-- Col -->
      <div class="box" v-for="values in pt" :key="values.icon">
        <div class="graph">
          <b-icon :icon="values.icon" font-scale="3"></b-icon>
        </div>
        <div class="text">
          <h5>{{ values.text1 }}</h5>
          <h4>{{ values.text2 }}</h4>
        </div>
      </div>
    </div>
    <hr />
    <div class="heading">
      <h5>INQ (Enquiries Status)</h5>
    </div>
    <div class="salse">
      <!-- Col -->
      <div class="box" v-for="values in inq" :key="values.icon">
        <div class="graph">
          <b-icon :icon="values.icon" font-scale="3"></b-icon>
        </div>
        <div class="text">
          <h5>{{ values.text1 }}</h5>
          <h4>{{ values.text2 }}</h4>
        </div>
      </div>
    </div>
    <hr />
    <div id="graphs">
      <div id="sales">
      <h5> Sales Graph</h5>
      <br>
      <apexchart type="line" height="350"  width="650" :options="chartOptions" :series="series"></apexchart>
      </div>
      <div id="membership">
      <h5> Membership Graph</h5>
      <br>
            <Donat_chart/>
      </div>

    </div>
 
 

    <br /><br /><br />
  </div>
</template>

<script scoped>
import Donat_chart from "@/components/Donat_chart.vue";
export default {
  components: {
    Donat_chart,
  },
  data() {
    return {
      show: "aka",
      sales: [
        { icon: "graph-up", text1: "Sales", text2: "$1,500" },
        { icon: "wallet", text1: "Payment Received", text2: "$25,900" },
        { icon: "hourglass-split", text1: "Payment Pending", text2: "$1,500" },
      ],
      membership: [
        {
          icon: "file-earmark-person",
          text1: "New Memberships",
          text2: "$1,500",
        },
        { icon: "person-check", text1: "Active Member", text2: "$25,900" },
        { icon: "person-dash", text1: "Inactive member", text2: "$1,500" },
        { icon: "bootstrap-reboot", text1: "Renewals", text2: "$1,500" },
      ],
      pt: [
        { icon: "person-square", text1: "New PT", text2: "$1,500" },
        { icon: "person-check", text1: "Active PT", text2: "$25,900" },
      ],
      inq: [
        { icon: "patch-question", text1: "Total INQ", text2: "$1,500" },
        { icon: "chat-square-text", text1: "Open", text2: "$25,900" },
        { icon: "check2-square", text1: "Closed", text2: "$25,900" },
        { icon: "check-all", text1: "Archive", text2: "$25,900" },
      ],
      // options: {
      //   chart: {
      //     id: "Salse-vuechart",
      //   },
      //   xaxis: {
      //     categories: [1991, 1992, 1993, 1994, 1995, 1996, 1997, 1998],
      //   },
      // },
      // series: [
      //   {
      //     name: "series-1",
      //     data: [30, 40, 45, 50, 49, 60, 70, 91],
      //   },
      // ],

      // series: [44, 55, 13, 43, 22],
      //     chartOptions: {
      //       chart: {
      //         width: 380,
      //         type: 'pie',
      //       },
      //       labels: ['Team A', 'Team B', 'Team C', 'Team D', 'Team E'],
      //       responsive: [{
      //         breakpoint: 480,
      //         options: {
      //           chart: {
      //             width: 200
      //           },
      //           legend: {
      //             position: 'bottom'
      //           }
      //         }
      //       }]
      //     },
       series: [{
            name: 'Income',
            type: 'column',
            data: [1.4, 2, 2.5, 1.5, 2.5, 2.8, 3.8, 4.6]
          }, {
            name: 'Cashflow',
            type: 'column',
            data: [1.1, 3, 3.1, 4, 4.1, 4.9, 6.5, 8.5]
          }, {
            name: 'Revenue',
            type: 'line',
            data: [20, 29, 37, 36, 44, 45, 50, 58]
          }],
          chartOptions: {
            chart: {
              height: 350,
              type: 'line',
              stacked: false
            },
            dataLabels: {
              enabled: false
            },
            stroke: {
              width: [1, 1, 4]
            },
            title: {
              text: 'XYZ - Stock Analysis (2009 - 2016)',
              align: 'left',
              offsetX: 110
            },
            xaxis: {
              categories: [2009, 2010, 2011, 2012, 2013, 2014, 2015, 2016],
            },
            yaxis: [
              {
                axisTicks: {
                  show: true,
                },
                axisBorder: {
                  show: true,
                  color: '#008FFB'
                },
                labels: {
                  style: {
                    colors: '#008FFB',
                  }
                },
                title: {
                  text: "Income (thousand crores)",
                  style: {
                    color: '#008FFB',
                  }
                },
                tooltip: {
                  enabled: true
                }
              },
              {
                seriesName: 'Income',
                opposite: true,
                axisTicks: {
                  show: true,
                },
                axisBorder: {
                  show: true,
                  color: '#00E396'
                },
                labels: {
                  style: {
                    colors: '#00E396',
                  }
                },
                title: {
                  text: "Operating Cashflow (thousand crores)",
                  style: {
                    color: '#00E396',
                  }
                },
              },
              {
                seriesName: 'Revenue',
                opposite: true,
                axisTicks: {
                  show: true,
                },
                axisBorder: {
                  show: true,
                  color: '#FEB019'
                },
                labels: {
                  style: {
                    colors: '#FEB019',
                  },
                },
                title: {
                  text: "Revenue (thousand crores)",
                  style: {
                    color: '#FEB019',
                  }
                }
              },
            ],
            tooltip: {
              fixed: {
                enabled: true,
                position: 'topLeft', // topRight, topLeft, bottomRight, bottomLeft
                offsetY: 30,
                offsetX: 60
              },
            },
            legend: {
              horizontalAlign: 'left',
              offsetX: 40
            }
          },
          
          
        
    }; //return ending
  },
};
</script>

<style>
h5 {
  font-family: "Oswald", sans-serif;
}
h3 {
  font-family: "Oswald", sans-serif;
}
.main {
  background-color: rgb(244, 243, 239);
  height: 100%;
}
 
.salse {
  display: flex;
}
.salse > div {
  background-color: rgb(255, 255, 255);
  /* background-color: brown; */
  /* margin: 10px;*/
  margin-left: 2%;
  padding: 1%;
  width: 20%;
  border-radius: 5px;
  /* box-shadow: 5px 2px darkblue; */
}
.box {
  display: flex;
  /* background-color: violet; */
  align-items: center;
}
.text {
  margin-right: auto;
  height: 100%;
  /* background-color: yellow; */
}
.graph {
  margin: auto;
}

.heading{
  margin-left: 2%;
}
#graphs{
  display: flex;
}
#graphs > div{
  margin-left:3%;
  padding:1%;
}
/* #graph{
  margin-left: 6%;
} */
#filter{margin-right:5%;
float: right;}
</style>