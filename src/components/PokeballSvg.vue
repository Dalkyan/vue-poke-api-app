<template>
  <svg
    class="min-w-min max-h-min move"
    width="40vw"
    viewBox="0 0 100.0 100.0"
    version="1.1"
    id="SVGRoot"
    xmlns="http://www.w3.org/2000/svg"
    xmlns:svg="http://www.w3.org/2000/svg"
    style="fill-opacity: 1"
  >
    <ellipse
      style="
        fill: #0f0f0f;
        fill-opacity: 0.292605;
        stroke: none;
        stroke-width: 0.341;
        stroke-miterlimit: 4;
        stroke-dasharray: none;
      "
      id="path4906"
      cx="46"
      cy="91"
      rx="31.468737"
      ry="8.8846416"
    />
    <defs id="defs824" />
    <g id="poke-svg">
      <g
        id="g2246"
        transform="matrix(0.96474871,0,0,0.96474871,1.7069776,1.7625638)"
      >
        <path
          id="path939"
          style="
            fill: #f2f2f2;
            stroke: #333333;
            stroke-width: 1;
            stroke-miterlimit: 4;
            stroke-dasharray: none;
          "
          d="M 99.820312,52.5 H 0.1796875 A 50,50 0 0 0 50,100 50,50 0 0 0 99.820312,52.5 Z"
        />
        <path
          id="path1848"
          style="
            fill: #333;
            stroke: #333333;
            stroke-width: 1;
            stroke-miterlimit: 4;
            stroke-dasharray: none;
          "
          d="M 98.581495,47.493775 H 1.5311173 A 48.643947,50.124501 0 0 0 1.3563026,50 48.643947,50.124501 0 0 0 1.5311173,52.506225 H 98.46938 A 48.643947,50.124501 0 0 0 98.644197,50 48.643947,50.124501 0 0 0 98.581543,47.493775 Z"
        />
        <path
          id="path1846"
          style="
            fill: #ff0000;
            stroke: #333333;
            stroke-width: 1;
            stroke-miterlimit: 4;
            stroke-dasharray: none;
          "
          d="M 50,0 A 50,50 0 0 0 0.1796875,47.5 H 99.935547 A 50,50 0 0 0 50,0 Z"
        />
        <circle
          style="
            fill: #e6e6e6;
            fill-opacity: 1;
            stroke: #333333;
            stroke-width: 2;
            stroke-miterlimit: 4;
            stroke-dasharray: none;
          "
          id="path1954"
          cx="50"
          cy="50"
          r="12.690478"
        />
        <RouterLink :to="`/pokemon/${index}`">
          <circle
            style="
              fill-opacity: 1;
              stroke: #333;
              stroke-width: 1;
              stroke-miterlimit: 4;
              stroke-dasharray: none;
            "
            id="poke-btn"
            cx="50"
            cy="50"
            r="10.364721"
          />
        </RouterLink>
      </g>
    </g>
    <path
      id="highlight"
      style="fill: #f2f2f2; fill-opacity: 0.292605"
      d="m 66.694266,11.25913 c 5.567938,0.126659 8.272559,1.830022 11.003762,6.703192 C 80.429229,22.835493 82.782046,30.155909 80,35 75.445671,32.363341 81.694266,11.25913 66.694266,11.25913 Z"
    />
  </svg>
</template>
<script setup lang="ts">
import { RouterLink } from "vue-router";
defineProps<{
  index: number;
}>();
</script>
