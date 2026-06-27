<!DOCTYPE html>
<html lang="zh-TW">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>游泳訓練與成績分析系統</title>

<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">

<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" rel="stylesheet">

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    background:#f4f7fb;
    font-family:
    "Microsoft JhengHei",
    sans-serif;
}

/* Sidebar */

.sidebar{

    position:fixed;
    left:0;
    top:0;

    width:250px;
    height:100vh;

    background:linear-gradient(
        180deg,
        #003c9e,
        #0057d8
    );

    color:white;

    display:flex;
    flex-direction:column;
}

.logo-area{

    text-align:center;
    padding:30px 20px;
}

.logo-area i{

    font-size:42px;
    margin-bottom:10px;
}

.logo-area h3{

    font-size:28px;
    margin-bottom:5px;
}

.logo-area small{

    opacity:.8;
}

/* Menu */

.menu{

    list-style:none;
    padding:0;
    margin-top:20px;
}

.menu li{

    margin:8px 12px;
}

.menu a{

    display:flex;
    align-items:center;

    gap:12px;

    color:white;
    text-decoration:none;

    padding:14px 18px;

    border-radius:12px;

    transition:.3s;
}

.menu a:hover{

    background:rgba(255,255,255,.15);
}

.menu i{

    width:20px;
}

/* User */

.user-card{

    margin-top:auto;

    padding:15px;

    display:flex;
    align-items:center;
    gap:12px;

    background:rgba(255,255,255,.1);
}

.user-card img{

    width:48px;
    height:48px;
    border-radius:50%;
}

.user-card h6{

    margin:0;
}

.user-card small{

    opacity:.8;
}

/* Content */

.content{

    margin-left:250px;
    padding:25px;
}

/* Top Bar */

.topbar{

    display:flex;
    justify-content:space-between;
    align-items:center;

    margin-bottom:20px;
}

.page-title{

    font-size:28px;
    font-weight:700;
}

.datetime{

    color:#666;
}

/* Instruction */

.instruction-box{

    background:#eef5ff;

    border:1px solid #cddfff;

    border-radius:12px;

    padding:18px 22px;

    margin-bottom:25px;
}

.instruction-box h5{

    color:#0d47a1;
    margin-bottom:10px;
}

.instruction-box p{

    margin:0;
    color:#555;
}

/* KPI */

.kpi-card{

    background:white;

    border-radius:18px;

    padding:22px;

    display:flex;
    align-items:center;
    gap:20px;

    box-shadow:
    0 2px 10px rgba(0,0,0,.08);

    height:130px;
}

.kpi-card h6{

    color:#666;
}

.kpi-card h2{

    margin:6px 0;
    font-weight:700;
}

.kpi-card span{

    color:#777;
    font-size:14px;
}

.icon{

    width:75px;
    height:75px;

    border-radius:50%;

    display:flex;
    align-items:center;
    justify-content:center;

    font-size:30px;
}

.swim{

    background:#e8f2ff;
    color:#1976d2;
}

.success{

    background:#e8fff0;
    color:#16a34a;
}

.trophy{

    background:#f5ebff;
    color:#7c3aed;
}

.target{

    background:#fff2e1;
    color:#ff8f00;
}

/* Card */

.content-card{

    background:white;

    border-radius:18px;

    padding:20px;

    margin-bottom:20px;

    box-shadow:
    0 2px 10px rgba(0,0,0,.08);
}

.card-title{

    font-size:22px;
    font-weight:600;

    margin-bottom:15px;

    color:#1a237e;
}

/* Goal */

.goal-info{

    display:flex;
    flex-direction:column;
    gap:20px;
}

.goal-info div{

    display:flex;
    justify-content:space-between;
}

.goal-info span{

    color:#666;
}

.goal-info strong{

    font-size:24px;
}

/* Progress */

.progress{

    height:26px;

    border-radius:50px;
}

/* Buttons */

.action-btn{

    width:100%;

    border:none;

    color:white;

    padding:15px;

    margin-bottom:12px;

    border-radius:12px;

    font-weight:600;

    cursor:pointer;

    transition:.3s;
}

.action-btn:hover{

    transform:translateY(-2px);
}

.blue{

    background:#1976d2;
}

.green{

    background:#16a34a;
}

.purple{

    background:#7c3aed;
}

/* Tables */

.table{

    margin-bottom:0;
}

.table thead{

    background:#f7f8fa;
}

.table th{

    color:#444;
    font-size:14px;
}

.table td{

    vertical-align:middle;
}

/* Chart */

#progressChart{

    height:320px !important;
}

/* Responsive */

@media(max-width:992px){

    .sidebar{

        width:100%;
        height:auto;

        position:relative;
    }

    .content{

        margin-left:0;
    }

    .topbar{

        flex-direction:column;
        align-items:flex-start;
        gap:10px;
    }

}

@media(max-width:768px){

    .kpi-card{

        flex-direction:column;
        text-align:center;

        height:auto;
    }

    .goal-info strong{

        font-size:18px;
    }

}

</style>

</head>

<body>

<!-- Sidebar -->

<div class="sidebar">

    <div class="logo-area">
        <i class="fa-solid fa-person-swimming"></i>
        <h3>游泳分析系統</h3>
        <small>PROTOTYPE</small>
    </div>

    <ul class="menu">

        <li>
            <a href="#dashboard">
                <i class="fa-solid fa-house"></i>
                首頁 Dashboard
            </a>
        </li>

        <li>
            <a href="#training">
                <i class="fa-solid fa-person-swimming"></i>
                訓練紀錄
            </a>
        </li>

        <li>
            <a href="#goal">
                <i class="fa-solid fa-bullseye"></i>
                目標管理
            </a>
        </li>

        <li>
            <a href="#competition">
                <i class="fa-solid fa-trophy"></i>
                比賽成績
            </a>
        </li>

        <li>
            <a href="#help">
                <i class="fa-solid fa-circle-info"></i>
                系統說明
            </a>
        </li>

    </ul>

    <div class="user-card">

        <img src="https://cdn-icons-png.flaticon.com/512/149/149071.png">

        <div>
            <h6>王小明</h6>
            <small>選手</small>
        </div>

    </div>

</div>

<!-- Main Content -->

<div class="content">

    <!-- Top Bar -->

    <div class="topbar">

        <div class="page-title">
            游泳訓練與成績分析系統
        </div>

        <div class="datetime">
            <i class="fa-regular fa-calendar"></i>
            2025/06/21 14:30
        </div>

    </div>

    <!-- 操作說明 -->

    <div class="instruction-box">

        <h5>
            <i class="fa-solid fa-circle-info"></i>
            操作說明
        </h5>

        <p>
            歡迎使用游泳訓練與成績分析系統！
            您可以在各個頁面新增紀錄、
            設定目標並追蹤進度，
            系統將自動分析您的表現並以圖表呈現。
        </p>

    </div>

    <!-- KPI -->

    <section id="dashboard">

        <div class="row">

            <div class="col-lg-3 mb-3">

                <div class="kpi-card">

                    <div class="icon swim">
                        <i class="fa-solid fa-person-swimming"></i>
                    </div>

                    <div>
                        <h6>訓練次數</h6>
                        <h2>58</h2>
                        <span>較上月 +12</span>
                    </div>

                </div>

            </div>

            <div class="col-lg-3 mb-3">

                <div class="kpi-card">

                    <div class="icon success">
                        <i class="fa-solid fa-chart-line"></i>
                    </div>

                    <div>
                        <h6>最佳訓練成績</h6>
                        <h2>1:11</h2>
                        <span>100m 自由式</span>
                    </div>

                </div>

            </div>

            <div class="col-lg-3 mb-3">

                <div class="kpi-card">

                    <div class="icon trophy">
                        <i class="fa-solid fa-trophy"></i>
                    </div>

                    <div>
                        <h6>最佳比賽成績</h6>
                        <h2>1:12</h2>
                        <span>100m 自由式</span>
                    </div>

                </div>

            </div>

            <div class="col-lg-3 mb-3">

                <div class="kpi-card">

                    <div class="icon target">
                        <i class="fa-solid fa-bullseye"></i>
                    </div>

                    <div>
                        <h6>目標達成率</h6>
                        <h2>95%</h2>
                        <span>持續進步中！</span>
                    </div>

                </div>

            </div>

        </div>

    </section>

    <!-- 圖表區 -->

    <div class="row">

        <div class="col-lg-7">

            <div class="content-card">

                <div class="card-title">
                    100m 自由式進步趨勢
                </div>

                <canvas id="progressChart"></canvas>

            </div>

        </div>

        <div class="col-lg-3">

            <div class="content-card">

                <div class="card-title">
                    目標追蹤
                </div>

                <div class="goal-info">

                    <div>
                        <span>目標成績</span>
                        <strong>1:10</strong>
                    </div>

                    <div>
                        <span>目前最佳</span>
                        <strong>1:11</strong>
                    </div>

                    <div>
                        <span>差距</span>
                        <strong>1秒</strong>
                    </div>

                </div>

                <div class="progress mt-4">

                    <div
                        class="progress-bar bg-success"
                        style="width:95%">
                        95%
                    </div>

                </div>

            </div>

        </div>

        <div class="col-lg-2">

            <div class="content-card">

                <div class="card-title">
                    快速操作
                </div>

                <button class="action-btn blue">
                    <i class="fa-solid fa-plus"></i>
                    新增訓練紀錄
                </button>

                <button class="action-btn green">
                    <i class="fa-solid fa-bullseye"></i>
                    新增目標
                </button>

                <button class="action-btn purple">
                    <i class="fa-solid fa-trophy"></i>
                    新增比賽成績
                </button>

            </div>

        </div>

    </div>

    <!-- 三個資料表 -->

    <div class="row mt-4">

        <div class="col-lg-4">

            <div class="content-card">

                <div class="card-title">
                    最新訓練紀錄
                </div>

                <table class="table">

                    <thead>
                    <tr>
                        <th>日期</th>
                        <th>項目</th>
                        <th>成績</th>
                    </tr>
                    </thead>

                    <tbody>

                    <tr>
                        <td>06/20</td>
                        <td>100m自由式</td>
                        <td class="text-danger">1:11</td>
                    </tr>

                    <tr>
                        <td>06/18</td>
                        <td>100m自由式</td>
                        <td>1:14</td>
                    </tr>

                    <tr>
                        <td>06/15</td>
                        <td>100m自由式</td>
                        <td>1:15</td>
                    </tr>

                    </tbody>

                </table>

            </div>

        </div>

        <div class="col-lg-4">

            <div class="content-card">

                <div class="card-title">
                    目標管理
                </div>

                <table class="table">

                    <thead>
                    <tr>
                        <th>項目</th>
                        <th>目標</th>
                        <th>完成率</th>
                    </tr>
                    </thead>

                    <tbody>

                    <tr>
                        <td>100m自由式</td>
                        <td>1:10</td>
                        <td>95%</td>
                    </tr>

                    <tr>
                        <td>200m自由式</td>
                        <td>2:40</td>
                        <td>92%</td>
                    </tr>

                    </tbody>

                </table>

            </div>

        </div>

        <div class="col-lg-4">

            <div class="content-card">

                <div class="card-title">
                    最新比賽成績
                </div>

                <table class="table">

                    <thead>
                    <tr>
                        <th>比賽</th>
                        <th>成績</th>
                        <th>名次</th>
                    </tr>
                    </thead>

                    <tbody>

                    <tr>
                        <td>市長盃</td>
                        <td>1:12</td>
                        <td>第3名</td>
                    </tr>

                    <tr>
                        <td>全國春季賽</td>
                        <td>1:13</td>
                        <td>第5名</td>
                    </tr>

                    </tbody>

                </table>

            </div>

        </div>

    </div>

</div>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

<script>

// ===== 100m自由式進步趨勢 =====

const ctx = document.getElementById("progressChart");

new Chart(ctx, {

    type: "line",

    data: {

        labels: [
            "1月",
            "2月",
            "3月",
            "4月",
            "5月",
            "6月"
        ],

        datasets: [

            {
                label: "100m自由式(秒)",

                data: [
                    80,
                    78,
                    77,
                    75,
                    74,
                    73
                ],

                borderColor: "#1976d2",

                backgroundColor:
                "rgba(25,118,210,0.15)",

                borderWidth: 4,

                tension: 0.4,

                fill: true,

                pointRadius: 6,

                pointHoverRadius: 8,

                pointBackgroundColor:
                "#1976d2"
            }

        ]

    },

    options: {

        responsive: true,

        maintainAspectRatio: false,

        animation: {

            duration: 1800,

            easing: "easeOutQuart"
        },

        plugins: {

            legend: {

                display: true,

                position: "top"
            }

        },

        scales: {

            y: {

                beginAtZero: false,

                reverse: true,

                title: {

                    display: true,

                    text: "成績（秒）"
                }

            },

            x: {

                title: {

                    display: true,

                    text: "月份"
                }

            }

        }

    }

});


// ===== Dashboard 載入動畫 =====

window.addEventListener("load", () => {

    const cards =
        document.querySelectorAll(
            ".kpi-card,.content-card"
        );

    cards.forEach((card, index) => {

        card.style.opacity = "0";
        card.style.transform =
            "translateY(20px)";

        setTimeout(() => {

            card.style.transition =
                "all .6s ease";

            card.style.opacity = "1";
            card.style.transform =
                "translateY(0)";

        }, index * 120);

    });

});


// ===== Quick Action Demo =====

const buttons =
    document.querySelectorAll(".action-btn");

buttons.forEach(btn => {

    btn.addEventListener("click", () => {

        alert(
            "Prototype展示版\n\n此功能將於正式版實作。"
        );

    });

});


// ===== 系統啟動訊息 =====

console.log(
    "🏊 游泳訓練與成績分析系統 Prototype 啟動成功"
);

</script>

</body>
</html>
