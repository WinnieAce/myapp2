<template>
  <head>
    <title>Logs Sheet</title>
  </head>
  <body>
    <div id="app">
      <h1>Logs Sheet</h1>
      <div>
      <table>
        <thead>
          <tr>
            <th class="branch">Branch</th>
            <th class="itemName">Item Name</th>
            <th class="loanPurpose">Purpose of Loan</th>
            <th class="timeAndDate">Time and Date of Loan</th>
            <th class="issuerRankName">Issuer Rank and Name</th>
            <th class="issuerNRIC">Issuer Masked NRIC</th>
            <th></th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="log in logs" :key="log.id">
            <td class="branch">{{ log.branchItem }}</td>
            <td class="itemName">{{ log.itemName }}</td>
            <td class="loanPurpose">{{ log.loanPurpose }}</td>
            <td class="timeAndDate">{{ log.timeAndDate }}</td>
            <td class="issuerRankName">{{ log.issuerRankName }}</td>
            <td class="issuerNRIC">{{ log.issuerNRIC }}</td>
            <td class="button">
              <a href="https://example.com"><img src="./assets/3515498.png"/></a>
            </td>
          </tr>
        </tbody>
      </table>
      </div>
    </div>
  </body>
</template>

<script setup>
import {ref} from 'vue';


let logs= ref([
  { id: 1, branchItem: 'Branch 1', itemName: 'Test 1', loanPurpose: 'Activity 1', timeAndDate: '1200 090823', issuerRankName: 'Pte Winston', issuerNRIC: '123A'},
  { id: 2, branchItem: 'Branch 2', itemName: 'Test 2', loanPurpose: 'Activity 2', timeAndDate: '1430 090823', issuerRankName: 'Pte Winston', issuerNRIC: '123A'},
  { id: 3, branchItem: 'Branch 3', itemName: 'Test 3', loanPurpose: 'Activity 3', timeAndDate: '1200 100823', issuerRankName: 'Pte Winston', issuerNRIC: '123A'},
  { id: 4, branchItem: 'Branch 4', itemName: 'Test 4', loanPurpose: 'Activity 4', timeAndDate: '1430 100823', issuerRankName: 'Pte Winston', issuerNRIC: '123A'}, 
])


// let peopleList = {
//       {
//           "id": 1,
//           "name": "Winston",
//           "age": 19,
//           "unit": "SBN"
//       },
//       "2":
//       {
//           "name": "Ryan",
//           "age": 21,
//           "unit": "SBN"
//       },

//   }

</script>

<style>
@font-face {
  font-family: "Hussar Bold";
  src: local("Hussar Bold"), url(fonts/HussarBoldWebEdition-xq5O.otf)
}

* {
  font-family: Arial, Helvetica, sans-serif;
}

body {
  margin: 0;
  width: 100%;
  background-color: #010145;
}

tr, td {
  /* display: flex */
}

tr {
  margin: auto
}

h1 {
  font-weight: 900;
  font-family: "Hussar Bold";
  font-size: 40px;
  text-decoration: underline;
  display: block;
  text-align: center;
  margin:auto;
  color: #ffffff;
  background-color:rgb(3, 0, 31);
  height: 70px;
  line-height: 70px;
  border-radius: 10px;
  
}

table {
  width: calc(100% - 2px);
  /* border: white dotted 2px; */
  border-radius: 10px;
  /* display: block; */
  margin: 0 auto;
  padding-top: 30px
  
}

thead, tbody {
  width: 100%;
  /* display: inline-block; */
  margin: 0 auto
}

th, td, button {
  /* display: inline-flex; */
  /* border-left: #379683 solid 1px; */
  /* flex-shrink: 0;
  justify-content: center */
}

th {
  font-family: "Hussar bold";
  font-weight: 100;
  font-size: 15px;
  padding: 10px 10px;
  color: white;
  text-align: center;
  overflow: hidden;
  flex-wrap: nowrap;
  text-decoration: underline;
  justify-content: center
}

td {
  padding: 10px 10px;
  color: white;
  font-family: Hussar Bold;
  font-size: 14px;
  text-align: center;
}

th, td {
  border: white dotted 1px
}

img {
  width:20px;
  height: 20px;
  padding: 7.333px 0;
  /* fill: white; */
  filter: invert(18%) sepia(99%) saturate(7294%) hue-rotate(0deg) brightness(97%) contrast(110%);
}
/*
.branch {
  width: 10%;
}

.itemName {
  width: 10%;
}

.loanPurpose {
  width: 15%;
}

.timeAndDate {
  width: 20%;
}

.issuerRankName {
  width: calc(20% - 20px);
}

.issuerNRIC {
  width: 15%;
}
*/

td.button {
  margin:0;
  padding: 0;
  /* background-color: rgb(255, 255, 255); */
  /* border-color: black */
}

.button:hover {
  background-color: white;
}
</style>