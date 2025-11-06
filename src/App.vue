<script setup>
import { CdxTab, CdxTabs } from '@wikimedia/codex'
import { Line } from 'vue-chartjs'
import {
  Chart as ChartJS,
  Tooltip,
  Legend,
  CategoryScale,
  LinearScale,
  PointElement,
  LineElement,
} from 'chart.js'

ChartJS.register(
  Tooltip,
  Legend,
  CategoryScale,
  LinearScale,
  PointElement,
  LineElement
)

const tabs = [
    {
      name: 'intro',
      label: 'Introduction',
    },
    {
      name: 'imf',
      label: 'IMF',
    },
    {
      name: 'wb',
      label: 'World Bank',
    },
    {
      name: 'un',
      label: 'United Nations',
    },
    {
      name: 'azstat',
      label: 'AzSTAT',
    },
  ],
  charts = [
    {
      labels: Array.from({ length: 16 }, (v, k) => k + 2010),
      datasets: [
        {
          label: 'Nominal GDP (billion US$)',
          data: [
            52.909, 65.952, 69.684, 74.164, 75.235, 52.997, 37.83, 41.375,
            47.113, 48.174, 42.693, 54.825, 78.807, 72.428, 74.316, 76.39,
          ],
          fill: false,
          borderColor: '#36c',
          tension: 0.1,
        },
        {
          label: 'Nominal GDP (billion AZN)',
          data: [
            42.465, 52.082, 54.744, 58.182, 59.014, 54.38, 60.425, 70.338,
            80.092, 81.896, 72.578, 93.203, 133.973, 123.128, 126.337, 129.863,
          ],
          fill: false,
          borderColor: '#1f7a39',
          tension: 0.1,
        },
        {
          label: 'Real GDP (billion AZN)',
          data: [
            26.748, 26.775, 27.365, 28.964, 29.765, 30.087, 29.165, 29.21,
            29.639, 30.374, 29.099, 30.733, 32.182, 32.618, 33.946, 34.97,
          ],
          fill: false,
          borderColor: '#886425',
          tension: 0.1,
        },
      ],
    },
    {
      labels: Array.from({ length: 15 }, (v, k) => k + 2010),
      datasets: [
        {
          label: 'Nominal GDP (billion US$)',
          data: [
            52.909, 65.953, 69.68, 74.161, 75.24, 53.076, 37.867, 40.867,
            47.112, 48.174, 42.693, 54.825, 78.807, 72.428, 74.316,
          ],
          fill: false,
          borderColor: '#36c',
          tension: 0.1,
        },
        {
          label: 'Nominal GDP (billion AZN)',
          data: [
            42.465, 52.082, 54.744, 58.182, 59.014, 54.38, 60.425, 70.338,
            80.092, 81.896, 72.578, 93.203, 133.973, 123.128, 126.337,
          ],
          fill: false,
          borderColor: '#1f7a39',
          tension: 0.1,
        },
        {
          label: 'Real GDP (billion 2015 US$)',
          data: [
            47.989, 47.234, 48.275, 51.096, 52.525, 53.076, 51.45, 51.529,
            52.302, 53.599, 51.349, 54.233, 56.79, 57.559, 59.902,
          ],
          fill: false,
          borderColor: '#9b527f',
          tension: 0.1,
        },
        {
          label: 'Real GDP (billion AZN)',
          data: [
            26.776, 26.355, 26.936, 28.51, 29.307, 29.615, 28.708, 28.752,
            29.183, 29.907, 28.651, 30.26, 31.687, 32.116, 33.424,
          ],
          fill: false,
          borderColor: '#886425',
          tension: 0.1,
        },
      ],
    },
    {
      labels: Array.from({ length: 14 }, (v, k) => k + 2010),
      datasets: [
        {
          label: 'Nominal GDP (billion US$)',
          data: [
            52.906, 65.953, 69.68, 74.161, 75.24, 53.076, 37.867, 40.867,
            47.112, 48.174, 42.693, 54.825, 78.807, 72.356,
          ],
          fill: false,
          borderColor: '#36c',
          tension: 0.1,
        },
        {
          label: 'Nominal GDP (billion AZN)',
          data: [
            42.465, 52.082, 54.744, 58.182, 59.014, 54.38, 60.425, 70.338,
            80.092, 81.896, 72.578, 93.203, 133.973, 123.005,
          ],
          fill: false,
          borderColor: '#1f7a39',
          tension: 0.1,
        },
        {
          label: 'Real GDP (billion 2015 US$)',
          data: [
            47.212, 47.245, 48.268, 51.072, 52.477, 53.076, 51.412, 51.454,
            52.251, 53.549, 51.277, 54.158, 56.685, 57.302,
          ],
          fill: false,
          borderColor: '#9b527f',
          tension: 0.1,
        },
        {
          label: 'Real GDP (billion 2015 AZN)',
          data: [
            48.371, 48.406, 49.454, 52.327, 53.766, 54.38, 52.675, 52.718,
            53.534, 54.864, 52.537, 55.488, 58.077, 58.709,
          ],
          fill: false,
          borderColor: '#886425',
          tension: 0.1,
        },
      ],
    },
    {
      labels: Array.from({ length: 15 }, (v, k) => k + 2010),
      datasets: [
        {
          label: 'Nominal GDP (billion US$)',
          data: [
            52.909, 65.952, 69.684, 74.164, 74.235, 52.997, 37.863, 40.868,
            47.113, 48.174, 42.693, 54.825, 78.808, 72.428, 74.316,
          ],
          fill: false,
          borderColor: '#36c',
          tension: 0.1,
        },
        {
          label: 'Nominal GDP (billion AZN)',
          data: [
            42.465, 52.082, 54.744, 58.182, 59.014, 54.38, 60.425, 70.338,
            80.092, 81.896, 72.578, 93.203, 133.973, 123.128, 126.337,
          ],
          fill: false,
          borderColor: '#1f7a39',
          tension: 0.1,
        },
      ],
    },
  ],
  sources = [
    [
      {
        href: 'https://data.imf.org/en/Data-Explorer?datasetUrn=IMF.RES:WEO(9.0.0)',
        label: 'IMF Data Explorer',
      },
    ],
    [
      {
        href: 'https://data.worldbank.org/indicator/NY.GDP.MKTP.CD?end=2024&locations=AZ&start=2010&view=chart',
        label: 'Nominal (US$)',
      },
      {
        href: 'https://data.worldbank.org/indicator/NY.GDP.MKTP.CN?end=2024&locations=AZ&start=2010&view=chart',
        label: 'Nominal (AZN)',
      },
      {
        href: 'https://data.worldbank.org/indicator/NY.GDP.MKTP.KD?end=2024&locations=AZ&start=2010&view=chart',
        label: 'Real (US$)',
      },
      {
        href: 'https://data.worldbank.org/indicator/NY.GDP.MKTP.KN?end=2024&locations=AZ&start=2010&view=chart',
        label: 'Real (AZN)',
      },
    ],
    [
      {
        href: 'https://unstats.un.org/unsd/amaapi/api/file/2',
        label: 'Nominal (US$)',
      },
      {
        href: 'https://unstats.un.org/unsd/amaapi/api/file/1',
        label: 'Nominal (AZN)',
      },
      {
        href: 'https://unstats.un.org/unsd/amaapi/api/file/6',
        label: 'Real (US$)',
      },
      {
        href: 'https://unstats.un.org/unsd/amaapi/api/file/5',
        label: 'Real (AZN)',
      },
    ],
    [
      {
        href: 'https://stat.gov.az/menu/6/statistical_yearbooks/source/system_nat_accounts_2025.pdf',
        label: 'National Accounts of Azerbaijan',
      },
    ],
  ]
</script>

<template>
  <cdx-tabs style="margin: auto; width: min(100%, 1280px)">
    <cdx-tab v-for="(tab, i) in tabs" :key="tab.name" v-bind="tab">
      <template v-if="i > 0">
        <Line
          :data="charts[i - 1]"
          :options="{
            plugins: {
              legend: {
                labels: {
                  font: {
                    family: `'Stack Sans Text', sans-serif`,
                  },
                },
              },
            },
            scales: {
              y: {
                beginAtZero: true,
              },
            },
          }"
        />
        <br />
        <span>
          Source<template v-if="sources[i - 1].length > 1">s</template>:

          <template v-for="(source, j) in sources[i - 1]">
            <a :href="source.href">{{ source.label }}</a>
            <template v-if="j < sources[i - 1].length - 1">, </template>
          </template>
        </span>
      </template>
      <template v-else>
        <h1>GDP of Azerbaijan over years (2010–today)</h1>
        <p>
          Made by
          <a
            href="https://ekrem.vercel.app"
            style="
              padding: 4px 6px;
              background-color: black;
              color: white;
              font-weight: bold;
              text-decoration: none;
            "
            >əkrəm<span style="color: #ababab">.</span></a
          >
          <br />
          See individual graphs for links to the primary sources.
        </p>
      </template>
      <br />
      <span>Tip: You can click on its legend label to hide a line.</span>
    </cdx-tab>
  </cdx-tabs>
</template>

<style scoped></style>
