<swimming html>
<html lang="zh-TW">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">

<title>游泳訓練與成績分析系統</title>

<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" rel="stylesheet">

<style>

body{
    background:#f4f7fc;
}

.sidebar{
    height:100vh;
    background:#0d47a1;
    color:white;
    position:fixed;
    width:250px;
}

.sidebar h3{
    padding:20px;
    text-align:center;
}

.sidebar a{
    color:white;
    text-decoration:none;
    display:block;
    padding:15px 25px;
}

.sidebar a:hover{
    background:#1565c0;
}

.content{
    margin-left:250px;
    padding:20px;
}

.kpi-card{
    border:none;
    border-radius:15px;
    box-shadow:0 3px 10px rgba(0,0,0,.1);
}

.section-card{
    border:none;
    border-radius:15px;
    box-shadow:0 3px 10px rgba(0,0,0,.1);
}

.table{
    font-size:14px;
}

.progress{
    height:25px;
}

@media(max-width:768px){

.sidebar{
    width:100%;
    height:auto;
    position:relative;
}

.content{
    margin-left:0;
}

}

</style>

</head>
<body>

<div class="sidebar">

<h3>🏊 游泳分析系統</h3>

<a href="#dashboard">
<i class="fa-solid fa-chart-line"></i>
Dashboard
</a>

<a href="#training">
<i class="fa-solid fa-person-swimming"></i>
訓練紀錄
</a>

<a href="#goal">
<i class="fa-solid fa-bullseye"></i>
目標管理
</a>

<a href="#competition">
<i class="fa-solid fa-trophy"></i>
比賽成績
</a>

</div>

<div class="content">

<!-- Header -->

<div class="d-flex justify-content-between align-items-center mb-4">
    <h2>游泳訓練與成績分析系統</h2>
    <span class="badge bg-primary p-2">王小明</span>
</div>

<!-- KPI -->

<section id="dashboard">

<div class="row g-3 mb-4">

<div class="col-md-3">
<div class="card kpi-card">
<div class="card-body text-center">
<h1>58</h1>
<p>訓練次數</p>
</div>
</div>
</div>

<div class="col-md-3">
<div class="card kpi-card">
<div class="card-body text-center">
<h1>1:13</h1>
<p>最佳訓練成績</p>
</div>
</div>
</div>

<div class="col-md-3">
<div class="card kpi-card">
<div class="card-body text-center">
<h1>1:12</h1>
<p>最佳比賽成績</p>
</div>
</div>
</div>

<div class="col-md-3">
<div class="card kpi-card">
<div class="card-body text-center">
<h1>95%</h1>
<p>目標達成率</p>
</div>
</div>
</div>

</div>

<!-- Charts -->

<div class="row">

<div class="col-md-8">

<div class="card section-card">
<div class="card-header">
100m自由式進步趨勢
</div>

<div class="card-body">
<canvas id="progressChart"></canvas>
</div>

</div>

</div>

<div class="col-md-4">

<div class="card section-card">
<div class="card-header">
目標追蹤
</div>

<div class="card-body">

<p>目標：1:10</p>
<p>目前最佳：1:13</p>
<p>差距：3秒</p>

<div class="progress">
<div class="progress-bar bg-success"
style="width:95%">
95%
</div>
</div>

</div>
</div>

</div>

</div>

</section>

<!-- Training -->

<section id="training" class="mt-5">

<div class="card section-card">

<div class="card-header">
訓練紀錄
</div>

<div class="card-body">

<table class="table table-striped">

<thead>

<tr>
<th>日期</th>
<th>項目</th>
<th>距離</th>
<th>成績</th>
<th>備註</th>
</tr>

</thead>

<tbody>

<tr>
<td>2025-06-20</td>
<td>100m自由式</td>
<td>100m</td>
<td>1:15</td>
<td>狀況佳</td>
</tr>

<tr>
<td>2025-06-18</td>
<td>100m自由式</td>
<td>100m</td>
<td>1:16</td>
<td>普通</td>
</tr>

<tr>
<td>2025-06-15</td>
<td>100m自由式</td>
<td>100m</td>
<td>1:14</td>
<td>PB</td>
</tr>

</tbody>

</table>

</div>

</div>

</section>

<!-- Goal -->

<section id="goal" class="mt-5">

<div class="card section-card">

<div class="card-header">
目標管理
</div>

<div class="card-body">

<table class="table">

<thead>

<tr>
<th>項目</th>
<th>目標成績</th>
<th>目前最佳</th>
<th>完成率</th>
<th>狀態</th>
</tr>

</thead>

<tbody>

<tr>
<td>100m自由式</td>
<td>1:10</td>
<td>1:13</td>
<td>95%</td>
<td>
<span class="badge bg-warning">
進行中
</span>
</td>
</tr>

<tr>
<td>200m自由式</td>
<td>2:40</td>
<td>2:48</td>
<td>92%</td>
<td>
<span class="badge bg-warning">
進行中
</span>
</td>
</tr>

</tbody>

</table>

</div>

</div>

</section>

<!-- Competition -->

<section id="competition" class="mt-5">

<div class="card section-card">

<div class="card-header">
比賽成績
</div>

<div class="card-body">

<table class="table table-hover">

<thead>

<tr>
<th>比賽名稱</th>
<th>項目</th>
<th>成績</th>
<th>名次</th>
<th>日期</th>
</tr>

</thead>

<tbody>

<tr>
<td>台北市長盃</td>
<td>100m自由式</td>
<td>1:12</td>
<td>第3名</td>
<td>2025-05-24</td>
</tr>

<tr>
<td>全國春季賽</td>
<td>100m自由式</td>
<td>1:13</td>
<td>第5名</td>
<td>2025-03-15</td>
</tr>

<tr>
<td>分齡賽</td>
<td>100m自由式</td>
<td>1:14</td>
<td>第6名</td>
<td>2025-01-18</td>
</tr>

</tbody>

</table>

</div>

</div>

</section>

</div>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

<script>

new Chart(
document.getElementById('progressChart'),
{
type:'line',
data:{
labels:[
'Jan',
'Feb',
'Mar',
'Apr',
'May',
'Jun'
],
datasets:[
{
label:'100m自由式',
data:[
80,
78,
77,
75,
74,
73
],
borderWidth:3,
fill:false
}
]
},
options:{
responsive:true
}
}
);

</script>

</body>
</html>
</body>
</html>
