<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
<meta name="format-detection" content="telephone=no">
<title>减脂健身手册</title>
<style>
:root {
  --bg: #0d1117;
  --card: #161b22;
  --card2: #1c2333;
  --border: #30363d;
  --blue: #00c8f0;
  --orange: #ff7043;
  --purple: #b39ddb;
  --green: #4caf50;
  --red: #f44336;
  --yellow: #ffa726;
  --txt: #e6edf3;
  --txt2: #8b949e;
  --txt3: #6e7681;
}
*{margin:0;padding:0;box-sizing:border-box;-webkit-tap-highlight-color:transparent;-webkit-text-size-adjust:100%;}
body{background:var(--bg);color:var(--txt);font-family:-apple-system,sans-serif;font-size:14px;line-height:1.5;overflow-x:hidden;}

/* HEADER */
.hdr{background:linear-gradient(160deg,#0d1117,#1a1040,#0a1628);padding:36px 18px 24px;position:relative;overflow:hidden;}
.hdr:before{content:'';position:absolute;top:-50px;right:-50px;width:180px;height:180px;background:radial-gradient(circle,rgba(0,200,240,.18),transparent 70%);border-radius:50%;}
.hdr-badge{display:inline-block;background:rgba(0,200,240,.12);border:1px solid rgba(0,200,240,.3);border-radius:20px;padding:3px 12px;font-size:11px;color:var(--blue);letter-spacing:1px;margin-bottom:12px;}
.hdr h1{font-size:28px;font-weight:900;line-height:1.2;margin-bottom:6px;background:linear-gradient(135deg,#fff 20%,var(--blue));-webkit-background-clip:text;-webkit-text-fill-color:transparent;}
.hdr-sub{font-size:13px;color:var(--txt2);margin-bottom:20px;}
.stats{display:grid;grid-template-columns:repeat(3,1fr);gap:8px;}
.stat{background:rgba(255,255,255,.05);border:1px solid var(--border);border-radius:12px;padding:10px;text-align:center;}
.stat b{display:block;font-size:20px;font-weight:800;color:var(--blue);}
.stat s{display:block;font-size:11px;color:var(--txt3);margin-top:2px;text-decoration:none;}

/* NAV */
.nav-wrap{position:sticky;top:0;z-index:99;background:var(--bg);border-bottom:1px solid var(--border);overflow-x:auto;-webkit-overflow-scrolling:touch;}
.nav-wrap::-webkit-scrollbar{display:none;}
.nav{display:flex;white-space:nowrap;padding:0 8px;}
.nb{display:inline-flex;flex-direction:column;align-items:center;padding:9px 14px 7px;background:none;border:none;color:var(--txt3);font-size:11px;cursor:pointer;gap:2px;position:relative;font-family:-apple-system,sans-serif;}
.nb i{font-size:17px;font-style:normal;}
.nb.on{color:var(--blue);}
.nb.on:after{content:'';position:absolute;bottom:0;left:50%;transform:translateX(-50%);width:22px;height:2px;background:var(--blue);border-radius:2px;}

/* PAGES */
.pg{display:none;padding:14px;}
.pg.on{display:block;}

/* SECTION LABEL */
.slbl{font-size:11px;font-weight:700;color:var(--txt3);letter-spacing:2px;text-transform:uppercase;margin:18px 0 8px;}
.slbl:first-child{margin-top:4px;}

/* CARD */
.card{background:var(--card);border:1px solid var(--border);border-radius:14px;padding:14px;margin-bottom:10px;}

/* CALORIE SUMMARY */
.cal-wrap{text-align:center;padding:18px 0 12px;}
.cal-num{font-size:48px;font-weight:900;color:var(--blue);line-height:1;}
.cal-lbl{font-size:13px;color:var(--txt2);margin-top:4px;}
.macro-row{display:grid;grid-template-columns:repeat(3,1fr);gap:8px;margin-top:14px;}
.macro{background:var(--card2);border-radius:12px;padding:12px 8px;text-align:center;}
.macro b{display:block;font-size:20px;font-weight:800;}
.macro s{display:block;font-size:11px;color:var(--txt3);text-decoration:none;margin-top:2px;}

/* MEALS */
.meals{position:relative;padding-left:42px;}
.meals:before{content:'';position:absolute;left:15px;top:10px;bottom:10px;width:2px;background:linear-gradient(var(--blue),var(--purple));opacity:.3;}
.meal{position:relative;margin-bottom:14px;}
.mdot{position:absolute;left:-34px;top:3px;width:20px;height:20px;border-radius:50%;border:2px solid;background:var(--bg);display:flex;align-items:center;justify-content:center;font-size:10px;font-weight:700;}
.mdot.a{border-color:var(--yellow);color:var(--yellow);}
.mdot.b{border-color:var(--purple);color:var(--purple);}
.mdot.c{border-color:var(--green);color:var(--green);}
.mdot.d{border-color:var(--orange);color:var(--orange);}
.mdot.e{border-color:var(--blue);color:var(--blue);}
.mtime{font-size:11px;color:var(--txt3);}
.mname{font-size:14px;font-weight:700;margin:2px 0;}
.mcont{font-size:12px;color:var(--txt2);line-height:1.6;}
.mkcal{display:inline-block;background:rgba(0,200,240,.1);color:var(--blue);border-radius:6px;padding:1px 8px;font-size:11px;font-weight:600;margin-top:4px;}

/* FOOD GRID */
.fg{display:grid;grid-template-columns:repeat(2,1fr);gap:8px;}
.fi{background:var(--card2);border-radius:12px;padding:11px;display:flex;gap:8px;align-items:flex-start;}
.fe{font-size:22px;flex-shrink:0;}
.fn{font-size:13px;font-weight:600;}
.fnote{font-size:11px;color:var(--txt2);margin-top:2px;}
.avoid{display:flex;align-items:center;gap:8px;padding:9px 12px;background:rgba(244,67,54,.07);border:1px solid rgba(244,67,54,.2);border-radius:10px;margin-bottom:7px;font-size:13px;}
.ax{color:var(--red);font-size:15px;font-weight:800;flex-shrink:0;}

/* WEEK PLAN */
.drow{display:flex;align-items:center;gap:10px;padding:12px 13px;background:var(--card);border:1px solid var(--border);border-radius:12px;margin-bottom:8px;cursor:pointer;-webkit-user-select:none;}
.dbadge{width:40px;height:40px;border-radius:10px;display:flex;flex-direction:column;align-items:center;justify-content:center;flex-shrink:0;font-weight:700;}
.dbadge.str{background:rgba(0,200,240,.15);color:var(--blue);}
.dbadge.car{background:rgba(255,112,67,.15);color:var(--orange);}
.dbadge.rst{background:rgba(107,114,128,.15);color:var(--txt3);}
.dd{font-size:9px;opacity:.7;}
.dn{font-size:17px;}
.dinfo{flex:1;}
.dname{font-size:14px;font-weight:700;}
.ddesc{font-size:12px;color:var(--txt2);margin-top:2px;}
.dtag{font-size:11px;padding:3px 8px;border-radius:6px;font-weight:600;flex-shrink:0;}
.dtag.str{background:rgba(0,200,240,.15);color:var(--blue);}
.dtag.car{background:rgba(255,112,67,.15);color:var(--orange);}
.dtag.rst{background:rgba(107,114,128,.15);color:var(--txt3);}

/* MODAL */
.moverlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.75);z-index:200;-webkit-overflow-scrolling:touch;overflow-y:auto;}
.moverlay.on{display:block;}
.mbox{background:var(--card);border-radius:20px 20px 0 0;position:absolute;bottom:0;left:0;right:0;max-height:92vh;overflow-y:auto;-webkit-overflow-scrolling:touch;}
.mhandle{width:36px;height:4px;background:var(--border);border-radius:2px;margin:12px auto 0;}
.mhdr{padding:14px 16px 12px;border-bottom:1px solid var(--border);display:flex;justify-content:space-between;align-items:flex-start;}
.mtitle{font-size:20px;font-weight:800;}
.msub{font-size:12px;color:var(--txt2);margin-top:3px;}
.mclosebtn{width:30px;height:30px;background:var(--card2);border:none;border-radius:50%;color:var(--txt);font-size:16px;cursor:pointer;display:flex;align-items:center;justify-content:center;flex-shrink:0;font-family:-apple-system,sans-serif;}

/* PHASE */
.phase-hdr{display:flex;gap:10px;align-items:center;padding:11px 14px;background:rgba(0,200,240,.05);border-bottom:1px solid var(--border);}
.ph-icon{font-size:18px;}
.ph-title{font-size:13px;font-weight:700;color:var(--blue);}
.ph-sub{font-size:11px;color:var(--txt3);}
.ph-time{margin-left:auto;font-size:11px;color:var(--txt3);background:var(--card);padding:2px 8px;border-radius:6px;border:1px solid var(--border);}

/* EXERCISE */
.exlist{padding:10px 14px;}
.excard{background:var(--card2);border-radius:12px;margin-bottom:8px;overflow:hidden;border:1px solid var(--border);}
.exhdr{display:flex;align-items:center;gap:10px;padding:12px 12px 10px;cursor:pointer;-webkit-user-select:none;}
.exnum{width:26px;height:26px;border-radius:7px;background:rgba(0,200,240,.15);color:var(--blue);display:flex;align-items:center;justify-content:center;font-size:12px;font-weight:700;flex-shrink:0;}
.extitle{font-size:14px;font-weight:600;flex:1;}
.exsets{font-size:11px;color:var(--txt2);flex-shrink:0;text-align:right;max-width:80px;}
.exarrow{color:var(--txt3);font-size:11px;flex-shrink:0;transition:transform .2s;font-style:normal;}
.exarrow.open{transform:rotate(180deg);}
.exbody{display:none;padding:0 12px 12px;border-top:1px solid var(--border);}
.exbody.on{display:block;}
.extags{display:flex;flex-wrap:wrap;gap:6px;padding-top:10px;}
.extag{font-size:11px;padding:3px 8px;border-radius:6px;font-weight:600;}
.extag.s{background:rgba(0,200,240,.12);color:var(--blue);}
.extag.r{background:rgba(179,157,219,.12);color:var(--purple);}
.extag.m{background:rgba(76,175,80,.12);color:var(--green);}
.steps{margin-top:10px;display:flex;flex-direction:column;gap:7px;}
.step{display:flex;gap:8px;align-items:flex-start;}
.stepnum{width:18px;height:18px;border-radius:50%;background:var(--border);color:var(--txt3);font-size:10px;font-weight:700;display:flex;align-items:center;justify-content:center;flex-shrink:0;margin-top:2px;}
.steptxt{font-size:13px;color:var(--txt2);line-height:1.6;}
.extip{display:flex;gap:8px;padding:9px;background:rgba(255,167,38,.07);border-radius:9px;margin-top:9px;border-left:3px solid var(--yellow);}
.extip span{font-size:12px;color:var(--txt2);line-height:1.6;}

/* HR ZONES */
.hrz{display:flex;flex-direction:column;gap:7px;}
.hz{display:flex;align-items:center;gap:10px;padding:10px 13px;border-radius:11px;border:1px solid;}
.hz.z1{background:rgba(107,114,128,.08);border-color:rgba(107,114,128,.25);}
.hz.z2{background:rgba(76,175,80,.08);border-color:rgba(76,175,80,.25);}
.hz.z3{background:rgba(255,167,38,.08);border-color:rgba(255,167,38,.25);}
.hz.z4{background:rgba(244,67,54,.08);border-color:rgba(244,67,54,.25);}
.hzbpm{font-size:15px;font-weight:800;min-width:65px;}
.z1 .hzbpm{color:var(--txt3);}
.z2 .hzbpm{color:var(--green);}
.z3 .hzbpm{color:var(--yellow);}
.z4 .hzbpm{color:var(--red);}
.hzname{font-size:13px;font-weight:600;}
.hzdesc{font-size:11px;color:var(--txt2);margin-top:1px;}
.hzrec{font-size:11px;padding:2px 7px;border-radius:5px;background:rgba(76,175,80,.15);color:var(--green);margin-left:auto;flex-shrink:0;}

/* RUN PLAN */
.rweek{display:flex;gap:10px;align-items:flex-start;padding:13px 0;border-bottom:1px solid var(--border);}
.rweek:last-child{border-bottom:none;}
.rwnum{width:40px;height:40px;border-radius:10px;background:var(--card2);display:flex;flex-direction:column;align-items:center;justify-content:center;flex-shrink:0;font-size:10px;color:var(--txt3);}
.rwnum b{font-size:17px;color:var(--txt);display:block;}
.rwtitle{font-size:14px;font-weight:700;margin-bottom:3px;}
.rwmethod{font-size:13px;color:var(--orange);margin-bottom:3px;}
.rwnote{font-size:12px;color:var(--txt2);line-height:1.6;}
.rwdur{font-size:14px;font-weight:800;color:var(--blue);flex-shrink:0;}

/* STRETCH */
.sitem{background:var(--card);border:1px solid var(--border);border-radius:13px;padding:13px;display:flex;gap:10px;margin-bottom:8px;}
.sico{width:36px;height:36px;border-radius:9px;display:flex;align-items:center;justify-content:center;font-size:17px;flex-shrink:0;}
.sico.w{background:rgba(255,167,38,.15);}
.sico.c{background:rgba(179,157,219,.15);}
.sname{font-size:14px;font-weight:600;}
.starget{font-size:12px;color:var(--purple);margin-top:2px;}
.show{font-size:12px;color:var(--txt2);margin-top:5px;line-height:1.6;}
.sdur{font-size:12px;font-weight:700;color:var(--orange);flex-shrink:0;text-align:right;}

/* PROGRESS */
.inp-row{display:grid;grid-template-columns:repeat(2,1fr);gap:8px;margin-bottom:8px;}
.inp-f{background:var(--card2);border:1px solid var(--border);border-radius:11px;padding:11px;}
.inp-lbl{font-size:11px;color:var(--txt3);margin-bottom:4px;}
.inp-val{display:flex;align-items:baseline;gap:4px;}
.inp-val input{background:none;border:none;outline:none;font-size:22px;font-weight:700;color:var(--txt);width:90px;font-family:-apple-system,sans-serif;}
.inp-unit{font-size:12px;color:var(--txt3);}
.inp-val select{background:none;border:none;outline:none;font-size:14px;font-weight:600;color:var(--txt);width:100%;font-family:-apple-system,sans-serif;}
.sbtn{width:100%;padding:14px;background:linear-gradient(135deg,var(--blue),#0088aa);border:none;border-radius:12px;color:#fff;font-size:15px;font-weight:700;cursor:pointer;margin-top:4px;font-family:-apple-system,sans-serif;}
.sbtn:active{opacity:.8;}
.logitem{display:flex;justify-content:space-between;align-items:center;padding:11px 0;border-bottom:1px solid var(--border);}
.logitem:last-child{border-bottom:none;}
.logdate{font-size:12px;color:var(--txt3);}
.logw{font-size:18px;font-weight:800;}
.logchg{font-size:12px;padding:2px 7px;border-radius:6px;}
.logchg.d{background:rgba(76,175,80,.15);color:var(--green);}
.logchg.u{background:rgba(244,67,54,.15);color:var(--red);}
.logchg.s{background:rgba(107,114,128,.15);color:var(--txt3);}

/* TIPS */
.tcard{padding:13px;border-radius:13px;margin-bottom:9px;border-left:4px solid;}
.tcard.g{background:rgba(76,175,80,.07);border-color:var(--green);}
.tcard.b{background:rgba(0,200,240,.07);border-color:var(--blue);}
.tcard.p{background:rgba(179,157,219,.07);border-color:var(--purple);}
.tcard.o{background:rgba(255,112,67,.07);border-color:var(--orange);}
.tcard.y{background:rgba(255,167,38,.07);border-color:var(--yellow);}
.ttitle{font-size:14px;font-weight:700;margin-bottom:5px;}
.tbody{font-size:13px;color:var(--txt2);line-height:1.8;}
.faq-item{border-bottom:1px solid var(--border);}
.faq-item:last-child{border-bottom:none;}
.faq-q{display:flex;justify-content:space-between;align-items:center;padding:13px 0;font-size:14px;font-weight:600;cursor:pointer;-webkit-user-select:none;gap:8px;}
.faq-arrow{color:var(--txt3);font-size:13px;flex-shrink:0;transition:transform .2s;font-style:normal;}
.faq-a{display:none;font-size:13px;color:var(--txt2);padding-bottom:12px;line-height:1.7;}
.faq-a.on{display:block;}

/* EMPTY */
.empty{text-align:center;padding:36px 0;color:var(--txt3);}
.empty-icon{font-size:36px;margin-bottom:8px;}
</style>
</head>
<body>

<!-- HEADER -->
<div class="hdr">
  <div class="hdr-badge">🔥 专属减脂手册</div>
  <h1>科学减脂<br>精细训练</h1>
  <div class="hdr-sub">178cm · 164斤 · 目标3个月减14斤</div>
  <div class="stats">
    <div class="stat"><b>82kg</b><s>当前体重</s></div>
    <div class="stat"><b>25.9</b><s>BMI</s></div>
    <div class="stat"><b>1800</b><s>目标kcal</s></div>
  </div>
</div>

<!-- NAV -->
<div class="nav-wrap">
  <div class="nav">
    <button class="nb on" onclick="tab('diet',this)"><i>🥗</i>饮食</button>
    <button class="nb" onclick="tab('week',this)"><i>📅</i>计划</button>
    <button class="nb" onclick="tab('cardio',this)"><i>🏃</i>有氧</button>
    <button class="nb" onclick="tab('stretch',this)"><i>🧘</i>热身拉伸</button>
    <button class="nb" onclick="tab('prog',this)"><i>📊</i>记录</button>
    <button class="nb" onclick="tab('tips',this)"><i>💡</i>注意事项</button>
  </div>
</div>

<!-- ===== 饮食 ===== -->
<div class="pg on" id="pg-diet">
  <div class="slbl">每日热量分配</div>
  <div class="card">
    <div class="cal-wrap">
      <div class="cal-num">1800</div>
      <div class="cal-lbl">大卡 / 天（比维持热量少约500大卡）</div>
      <div class="macro-row">
        <div class="macro"><b style="color:var(--blue)">130g</b><s>蛋白质</s></div>
        <div class="macro"><b style="color:var(--purple)">170g</b><s>碳水</s></div>
        <div class="macro"><b style="color:var(--yellow)">50g</b><s>脂肪</s></div>
      </div>
    </div>
  </div>

  <div class="slbl">每日餐次安排</div>
  <div class="card">
    <div class="meals">
      <div class="meal">
        <div class="mdot a">早</div>
        <div class="mtime">07:00 — 08:00</div>
        <div class="mname">早餐</div>
        <div class="mcont">燕麦 50g + 鸡蛋 2个 + 脱脂牛奶 200ml + 水果（苹果或香蕉选一）</div>
        <span class="mkcal">≈ 420 kcal</span>
      </div>
      <div class="meal">
        <div class="mdot b">加</div>
        <div class="mtime">10:00（可选）</div>
        <div class="mname">上午加餐</div>
        <div class="mcont">无糖希腊酸奶 150g 或 水煮鸡胸肉 50g</div>
        <span class="mkcal">≈ 100 kcal</span>
      </div>
      <div class="meal">
        <div class="mdot c">午</div>
        <div class="mtime">12:00 — 13:00</div>
        <div class="mname">午餐（最大一餐）</div>
        <div class="mcont">糙米 100g（生重）+ 鸡胸/牛肉 150g + 绿叶蔬菜 200g + 少油炒或水煮</div>
        <span class="mkcal">≈ 520 kcal</span>
      </div>
      <div class="meal">
        <div class="mdot b">前</div>
        <div class="mtime">训练前 1 小时（训练日）</div>
        <div class="mname">训练前补给</div>
        <div class="mcont">香蕉 1根 + 鸡蛋 1个，提供训练能量</div>
        <span class="mkcal">≈ 150 kcal</span>
      </div>
      <div class="meal">
        <div class="mdot d">晚</div>
        <div class="mtime">18:00 — 19:00</div>
        <div class="mname">晚餐（清淡为主）</div>
        <div class="mcont">红薯 100g 或 蒸米饭 80g + 鱼/虾/豆腐 150g + 蔬菜 300g 水煮</div>
        <span class="mkcal">≈ 450 kcal</span>
      </div>
      <div class="meal">
        <div class="mdot e">后</div>
        <div class="mtime">训练后 30 分钟内（训练日）</div>
        <div class="mname">训练后补充</div>
        <div class="mcont">鸡蛋 2个 或 蛋白粉 1勺，帮助肌肉修复</div>
        <span class="mkcal">≈ 160 kcal</span>
      </div>
    </div>
  </div>

  <div class="slbl">推荐食物</div>
  <div class="fg">
    <div class="fi"><div class="fe">🍗</div><div><div class="fn">鸡胸肉</div><div class="fnote">每100g含31g蛋白</div></div></div>
    <div class="fi"><div class="fe">🥚</div><div><div class="fn">鸡蛋</div><div class="fnote">完整蛋白，每天2~3个</div></div></div>
    <div class="fi"><div class="fe">🐟</div><div><div class="fn">鱼肉 / 虾</div><div class="fnote">优质蛋白，低脂</div></div></div>
    <div class="fi"><div class="fe">🍚</div><div><div class="fn">糙米</div><div class="fnote">复合碳水，饱腹强</div></div></div>
    <div class="fi"><div class="fe">🍠</div><div><div class="fn">红薯</div><div class="fnote">低GI，富含膳食纤维</div></div></div>
    <div class="fi"><div class="fe">🥦</div><div><div class="fn">西兰花</div><div class="fnote">高纤维，几乎0热量</div></div></div>
    <div class="fi"><div class="fe">🥛</div><div><div class="fn">脱脂牛奶</div><div class="fnote">补钙+蛋白质</div></div></div>
    <div class="fi"><div class="fe">🌾</div><div><div class="fn">燕麦</div><div class="fnote">早餐首选，持久饱腹</div></div></div>
  </div>

  <div class="slbl" style="margin-top:18px">严格避免</div>
  <div class="avoid"><span class="ax">✕</span>奶茶、可乐、果汁 — 液体热量，难察觉</div>
  <div class="avoid"><span class="ax">✕</span>炸鸡、薯条、油条 — 一份顶一整餐热量</div>
  <div class="avoid"><span class="ax">✕</span>蛋糕、饼干、糖果 — 直接升血糖，促脂肪储存</div>
  <div class="avoid"><span class="ax">✕</span>宵夜 — 晚 8 点后不进食</div>
  <div class="avoid"><span class="ax">✕</span>过量精白米饭 — 换糙米或减半份量</div>
</div>

<!-- ===== 计划 ===== -->
<div class="pg" id="pg-week">
  <div class="slbl">本周训练计划 · 点击查看详情</div>
  <div class="drow" onclick="openM('A')">
    <div class="dbadge str"><div class="dd">MON</div><div class="dn">一</div></div>
    <div class="dinfo"><div class="dname">💪 力量训练 A</div><div class="ddesc">腿部 + 臀部 · 6个动作 · 55分钟</div></div>
    <span class="dtag str">力量</span>
  </div>
  <div class="drow" onclick="openM('CA')">
    <div class="dbadge car"><div class="dd">TUE</div><div class="dn">二</div></div>
    <div class="dinfo"><div class="dname">🏃 有氧训练</div><div class="ddesc">慢跑 / 跳绳 · 35~40分钟</div></div>
    <span class="dtag car">有氧</span>
  </div>
  <div class="drow" onclick="openM('B')">
    <div class="dbadge str"><div class="dd">WED</div><div class="dn">三</div></div>
    <div class="dinfo"><div class="dname">💪 力量训练 B</div><div class="ddesc">核心 + 上肢 · 7个动作 · 55分钟</div></div>
    <span class="dtag str">力量</span>
  </div>
  <div class="drow" onclick="openM('REST')">
    <div class="dbadge rst"><div class="dd">THU</div><div class="dn">四</div></div>
    <div class="dinfo"><div class="dname">🚶 主动休息</div><div class="ddesc">散步 + 全身拉伸 · 30分钟</div></div>
    <span class="dtag rst">休息</span>
  </div>
  <div class="drow" onclick="openM('C')">
    <div class="dbadge str"><div class="dd">FRI</div><div class="dn">五</div></div>
    <div class="dinfo"><div class="dname">💪 力量训练 C</div><div class="ddesc">腿部强化 + 核心 · 7个动作 · 60分钟</div></div>
    <span class="dtag str">力量</span>
  </div>
  <div class="drow" onclick="openM('CB')">
    <div class="dbadge car"><div class="dd">SAT</div><div class="dn">六</div></div>
    <div class="dinfo"><div class="dname">🚴 有氧训练</div><div class="ddesc">快走 / 骑车 · 40~50分钟</div></div>
    <span class="dtag car">有氧</span>
  </div>
  <div class="drow">
    <div class="dbadge rst"><div class="dd">SUN</div><div class="dn">日</div></div>
    <div class="dinfo"><div class="dname">😴 完全休息</div><div class="ddesc">充分恢复 — 肌肉在休息中生长</div></div>
    <span class="dtag rst">恢复</span>
  </div>
</div>

<!-- ===== 有氧 ===== -->
<div class="pg" id="pg-cardio">
  <div class="slbl">心率燃脂区间</div>
  <div class="card">
    <div class="hrz">
      <div class="hz z1"><div class="hzbpm">90~110</div><div><div class="hzname">热身区</div><div class="hzdesc">轻松，可正常说话</div></div></div>
      <div class="hz z2"><div class="hzbpm">115~135</div><div><div class="hzname">🔥 燃脂区（推荐）</div><div class="hzdesc">有点喘，能说短句</div></div><span class="hzrec">最佳</span></div>
      <div class="hz z3"><div class="hzbpm">135~155</div><div><div class="hzname">有氧区</div><div class="hzdesc">较喘，只能说单词</div></div></div>
      <div class="hz z4"><div class="hzbpm">155 +</div><div><div class="hzname">无氧区</div><div class="hzdesc">很喘，无法说话</div></div></div>
    </div>
    <div style="font-size:12px;color:var(--txt3);text-align:center;margin-top:10px">最大心率 ≈ 190 次/分（220 − 年龄）</div>
  </div>

  <div class="slbl">跑步分阶段计划</div>
  <div class="card">
    <div class="rweek">
      <div class="rwnum"><span>周</span><b>1~2</b></div>
      <div style="flex:1">
        <div class="rwtitle">适应期</div>
        <div class="rwmethod">快走 + 慢跑交替</div>
        <div class="rwnote">快走3分钟 → 慢跑2分钟，循环6次。不要强迫自己一直跑，先适应节奏。</div>
      </div>
      <div class="rwdur">30min</div>
    </div>
    <div class="rweek">
      <div class="rwnum"><span>周</span><b>3~4</b></div>
      <div style="flex:1">
        <div class="rwtitle">过渡期</div>
        <div class="rwmethod">慢跑为主</div>
        <div class="rwnote">热身慢走5分钟 → 慢跑25分钟 → 慢走冷却5分钟。配速约8~9分/公里。</div>
      </div>
      <div class="rwdur">35min</div>
    </div>
    <div class="rweek">
      <div class="rwnum"><span>周</span><b>5~8</b></div>
      <div style="flex:1">
        <div class="rwtitle">提升期</div>
        <div class="rwmethod">持续慢跑</div>
        <div class="rwnote">保持心率120~135次/分，配速约7~8分/公里。心率超过140时放慢脚步。</div>
      </div>
      <div class="rwdur">40min</div>
    </div>
    <div class="rweek">
      <div class="rwnum"><span>周</span><b>9+</b></div>
      <div style="flex:1">
        <div class="rwtitle">进阶期</div>
        <div class="rwmethod">变速跑 / 间歇跑</div>
        <div class="rwnote">慢跑5分钟 → 加速1分钟，循环进行。或选择坡道增加强度，燃脂效率提升约30%。</div>
      </div>
      <div class="rwdur">45min</div>
    </div>
  </div>

  <div class="slbl">跳绳方案（适合在家）</div>
  <div class="card" style="display:flex;flex-direction:column;gap:9px;">
    <div style="padding:11px;background:var(--card2);border-radius:11px;">
      <div style="font-weight:700;margin-bottom:4px;">🟢 间歇跳绳（新手推荐）</div>
      <div style="font-size:13px;color:var(--txt2);line-height:1.7;">跳1分钟 → 休息30秒，循环13组 = 20分钟<br>消耗约 150~180 kcal</div>
    </div>
    <div style="padding:11px;background:var(--card2);border-radius:11px;">
      <div style="font-weight:700;margin-bottom:4px;">🟡 节奏跳绳（中级）</div>
      <div style="font-size:13px;color:var(--txt2);line-height:1.7;">匀速跳30分钟，中间可休息2~3次<br>消耗约 200~250 kcal</div>
    </div>
    <div style="padding:11px;background:var(--card2);border-radius:11px;">
      <div style="font-weight:700;margin-bottom:4px;">🔴 高强度间歇（进阶）</div>
      <div style="font-size:13px;color:var(--txt2);line-height:1.7;">快跳45秒 → 休息15秒，循环15组 = 15分钟<br>消耗约 150 kcal，心肺强度更大</div>
    </div>
    <div class="extip" style="margin-top:4px;"><span>💡 脚掌先落地、膝盖微弯；穿有支撑的运动鞋；在软地垫或草地跳，保护膝盖。</span></div>
  </div>
</div>

<!-- ===== 热身拉伸 ===== -->
<div class="pg" id="pg-stretch">
  <div class="slbl">训练前热身（必做，约10分钟）</div>
  <div class="sitem"><div class="sico w">🏃</div><div style="flex:1"><div class="sname">慢跑 / 原地小跑</div><div class="starget">全身升温</div><div class="show">心率升至100次/分以上，身体微微出汗，是热身的基础。</div></div><div class="sdur">3~5分钟</div></div>
  <div class="sitem"><div class="sico w">💫</div><div style="flex:1"><div class="sname">肩关节 + 手腕绕环</div><div class="starget">肩部、腕部关节</div><div class="show">顺时针10次、逆时针10次，动作幅度尽量大，充分活动关节。</div></div><div class="sdur">各20次</div></div>
  <div class="sitem"><div class="sico w">🔄</div><div style="flex:1"><div class="sname">髋部绕环</div><div class="starget">髋关节、腰部</div><div class="show">双手叉腰，以髋部为中心做大圆圈绕转，像呼啦圈一样，顺逆各10次。</div></div><div class="sdur">各10次</div></div>
  <div class="sitem"><div class="sico w">⬇️</div><div style="flex:1"><div class="sname">空重深蹲热身</div><div class="starget">激活腿部肌群</div><div class="show">不加重量，慢速下蹲（3秒），底部停顿2秒，感受大腿和臀部充分拉伸。</div></div><div class="sdur">15次×2组</div></div>
  <div class="sitem"><div class="sico w">🦵</div><div style="flex:1"><div class="sname">弓步压腿</div><div class="starget">髋屈肌、大腿前侧</div><div class="show">向前迈一大步成弓步，膝盖不触地，感受后腿大腿前侧明显拉伸。</div></div><div class="sdur">每侧8次</div></div>
  <div class="sitem"><div class="sico w">🍑</div><div style="flex:1"><div class="sname">臀桥激活</div><div class="starget">臀大肌、核心</div><div class="show">平躺屈膝，臀部向上顶起，顶部停顿1秒挤压臀肌，缓慢下落，充分激活臀肌。</div></div><div class="sdur">15次×2组</div></div>

  <div class="slbl" style="margin-top:18px">训练后拉伸（必做，约15分钟）</div>
  <div class="sitem"><div class="sico c">🦵</div><div style="flex:1"><div class="sname">站姿大腿前侧拉伸</div><div class="starget">股四头肌</div><div class="show">单脚站立，另一腿屈膝，手抓脚踝向臀部拉近，保持上身直立，感受大腿前侧拉伸。</div></div><div class="sdur">每侧30秒×2</div></div>
  <div class="sitem"><div class="sico c">🪑</div><div style="flex:1"><div class="sname">坐姿大腿后侧拉伸</div><div class="starget">腘绳肌</div><div class="show">坐地，腿伸直，双手前伸尽量触碰脚尖，膝盖不弯，感受大腿后侧充分拉伸。</div></div><div class="sdur">每侧30秒×2</div></div>
  <div class="sitem"><div class="sico c">🦋</div><div style="flex:1"><div class="sname">蝴蝶式拉伸</div><div class="starget">大腿内侧</div><div class="show">坐地脚底对脚底，双手轻按膝盖向地面压，上身微前倾，感受大腿内侧拉伸。</div></div><div class="sdur">60秒</div></div>
  <div class="sitem"><div class="sico c">🙇</div><div style="flex:1"><div class="sname">跪姿髋屈肌拉伸</div><div class="starget">髋屈肌、腰大肌</div><div class="show">弓步跪姿，前腿90°，后膝着地，上身直立微前倾，感受后腿髋部深度拉伸。</div></div><div class="sdur">每侧30秒×2</div></div>
  <div class="sitem"><div class="sico c">🧸</div><div style="flex:1"><div class="sname">婴儿式</div><div class="starget">背部、腰部、肩部</div><div class="show">跪坐，臀部坐向脚跟，双手向前伸直趴下，额头贴地，深呼吸放松整个背部。</div></div><div class="sdur">60秒</div></div>
  <div class="sitem"><div class="sico c">🐈</div><div style="flex:1"><div class="sname">猫牛式</div><div class="starget">脊柱活动</div><div class="show">四肢跪地，吸气塌腰抬头（牛），呼气拱背低头（猫），缓慢交替，每次停顿2秒。</div></div><div class="sdur">各10次</div></div>
  <div class="sitem"><div class="sico c">🐍</div><div style="flex:1"><div class="sname">眼镜蛇式</div><div class="starget">腹部、腰椎伸展</div><div class="show">俯卧，双手撑地放胸侧，缓慢撑起上身，腿部放松贴地，感受腹部拉伸。</div></div><div class="sdur">30秒×2</div></div>
</div>

<!-- ===== 记录 ===== -->
<div class="pg" id="pg-prog">
  <div class="slbl">记录今天数据</div>
  <div class="card">
    <div class="inp-row">
      <div class="inp-f">
        <div class="inp-lbl">体重（晨起空腹）</div>
        <div class="inp-val"><input type="number" id="iw" placeholder="82" step="0.1"><span class="inp-unit">kg</span></div>
      </div>
      <div class="inp-f">
        <div class="inp-lbl">腰围</div>
        <div class="inp-val"><input type="number" id="iwa" placeholder="86" step="0.5"><span class="inp-unit">cm</span></div>
      </div>
      <div class="inp-f">
        <div class="inp-lbl">大腿围（左腿最粗处）</div>
        <div class="inp-val"><input type="number" id="it" placeholder="56" step="0.5"><span class="inp-unit">cm</span></div>
      </div>
      <div class="inp-f">
        <div class="inp-lbl">今日训练</div>
        <div class="inp-val">
          <select id="iwo">
            <option value="力量A">力量A</option>
            <option value="力量B">力量B</option>
            <option value="力量C">力量C</option>
            <option value="有氧">有氧</option>
            <option value="休息">休息</option>
          </select>
        </div>
      </div>
    </div>
    <button class="sbtn" onclick="saveLog()">💾 保存今日记录</button>
  </div>
  <div class="slbl">历史记录（本次打开有效）</div>
  <div class="card" id="loglist"><div class="empty"><div class="empty-icon">📝</div>填写上方数据后点击保存</div></div>
</div>

<!-- ===== 注意事项 ===== -->
<div class="pg" id="pg-tips">
  <div class="slbl">核心原则</div>
  <div class="tcard b"><div class="ttitle">🎯 不要追求太快</div><div class="tbody">健康减脂是每周0.5~1斤。1个月减5~8斤才可持续。减太快会掉肌肉、代谢变慢、反弹更严重。</div></div>
  <div class="tcard g"><div class="ttitle">🍖 蛋白质是关键</div><div class="tbody">每天至少120g蛋白质。蛋白质热效应高（消化时消耗更多热量），还能保住肌肉。减脂期掉肌肉等于失败。</div></div>
  <div class="tcard y"><div class="ttitle">🍞 不要断碳水</div><div class="tbody">断碳没力气训练，还会导致肌肉流失和代谢下降。换成糙米、红薯、燕麦等复合碳水，减量不断掉。</div></div>
  <div class="tcard p"><div class="ttitle">😴 睡眠比想象中重要</div><div class="tbody">睡眠不足7小时，皮质醇升高，身体倾向储存腹部脂肪。睡够后生长激素分泌更多，直接帮助减脂增肌。</div></div>
  <div class="tcard o"><div class="ttitle">⚖️ 体重不是唯一标准</div><div class="tbody">体重受水分、食物、时间等影响每天波动1~3kg。关注腰围和衣服是否松了更准确，看2~3周趋势。</div></div>
  <div class="tcard b"><div class="ttitle">🔥 遇到平台期怎么办</div><div class="tbody">减脂4~6周后可能停滞。应对：① 换训练种类；② 重查饮食热量；③ 增加1次有氧；④ 热量缺口不超过600大卡。</div></div>
  <div class="tcard g"><div class="ttitle">💧 每天喝够水</div><div class="tbody">每天2~2.5升白开水。饭前300ml水能减少食量。运动每20分钟补150~200ml。不用果汁或运动饮料代替。</div></div>
  <div class="tcard y"><div class="ttitle">🏥 避免受伤第一位</div><div class="tbody">深蹲、硬拉等动作先学姿势再加重。膝盖或腰部不适立即停止。新手前2周只用轻重量，动作质量比重量重要。</div></div>

  <div class="slbl" style="margin-top:4px">常见问题</div>
  <div class="card">
    <div class="faq-item">
      <div class="faq-q" onclick="faq(this)">做了腹肌训练肚子还是大？<i class="faq-arrow">▼</i></div>
      <div class="faq-a">局部减脂不存在。腹肌训练让腹肌更强，但脂肪只有全身有氧+饮食控制才能减掉。体脂降低后腹肌自然显现。</div>
    </div>
    <div class="faq-item">
      <div class="faq-q" onclick="faq(this)">训练后第二天全身酸痛正常吗？<i class="faq-arrow">▼</i></div>
      <div class="faq-a">正常，叫「延迟性肌肉酸痛（DOMS）」，是肌肉纤维撕裂后修复的表现，说明训练有效。轻微酸痛可换部位继续，严重就多休息一天。</div>
    </div>
    <div class="faq-item">
      <div class="faq-q" onclick="faq(this)">减肥必须吃蛋白粉吗？<i class="faq-arrow">▼</i></div>
      <div class="faq-a">不是必须的。蛋白粉只是方便补充蛋白质的食品，不是神药。食物能补够就不需要。训练后懒得做饭时，蛋白粉很方便。</div>
    </div>
    <div class="faq-item">
      <div class="faq-q" onclick="faq(this)">每天都可以做有氧吗？<i class="faq-arrow">▼</i></div>
      <div class="faq-a">轻度有氧（快走、骑车）每天都可以。高强度有氧（跑步、跳绳）建议每周3~4次。过多高强度有氧反而会导致肌肉流失。</div>
    </div>
    <div class="faq-item">
      <div class="faq-q" onclick="faq(this)">体重一直不降怎么办？<i class="faq-arrow">▼</i></div>
      <div class="faq-a">先排查：① 热量计算是否准确（容易低估）；② 是否睡眠不足；③ 压力是否过大。坚持2周后再评估，不要因为几天数据就放弃。</div>
    </div>
  </div>
</div>

<!-- MODAL -->
<div class="moverlay" id="modal" onclick="closeMO(event)">
  <div class="mbox" id="mbox">
    <div class="mhandle"></div>
    <div class="mhdr" id="mhdr"></div>
    <div id="mexlist"></div>
    <div style="height:20px"></div>
  </div>
</div>

<script>
// ── TAB ──
function tab(id,btn){
  document.querySelectorAll('.pg').forEach(function(p){p.classList.remove('on');});
  document.querySelectorAll('.nb').forEach(function(b){b.classList.remove('on');});
  document.getElementById('pg-'+id).classList.add('on');
  btn.classList.add('on');
  window.scrollTo(0,0);
}

// ── WORKOUT DATA ──
var WD = {
  A:{name:'力量训练 A',focus:'腿部 + 臀部',time:'55分钟',color:'#00c8f0',phases:[
    {icon:'🔥',title:'热身',sub:'激活腿部肌群',time:'10min',exs:[
      {n:'慢跑/原地跑',sets:'5分钟',rest:'—',muscles:'全身升温',steps:['慢速跑或原地小跑，不用快','直到身体微微出汗，心率达到100次/分以上'],tip:''},
      {n:'臀桥激活',sets:'15次×2组',rest:'30秒',muscles:'臀大肌',steps:['平躺，膝盖弯曲，双脚平放地面','臀部向上顶起，顶点停顿1秒挤压臀肌','缓慢下落，不要完全放松，再次向上'],tip:'顶部停顿是关键，感受臀肌收缩感。'},
      {n:'空重深蹲',sets:'15次×2组',rest:'30秒',muscles:'腿部全面激活',steps:['不加任何重量，双脚与肩同宽','3秒缓慢下蹲，底部停顿2秒','感受大腿和臀部充分拉伸后起立'],tip:''},
    ]},
    {icon:'💪',title:'主体训练',sub:'腿部+臀部强化',time:'35min',exs:[
      {n:'负重深蹲',sets:'4组 × 12次',rest:'90秒',muscles:'股四头肌、臀大肌、腘绳肌',steps:['双脚与肩同宽，脚尖微向外约15~30度','深吸气，收腹核心收紧，开始下蹲','膝盖沿脚尖方向外推，绝对不要内扣','下蹲至大腿平行地面或更低，背部挺直','脚跟发力蹬地，呼气起立，顶部挤压臀肌','重量从轻开始，先掌握动作再加重'],tip:'没有杠铃可用哑铃放肩上，或双手各持一个哑铃。'},
      {n:'罗马尼亚硬拉',sets:'3组 × 12次',rest:'90秒',muscles:'腘绳肌、臀大肌',steps:['站立，双手持哑铃放大腿前侧','双膝微弯，膝盖角度固定不变','臀部向后推，上身前倾，背部全程保持平直','哑铃沿大腿前侧缓慢下滑至小腿中段','感受大腿后侧（腘绳肌）充分拉伸','臀部前推起身，顶部挤压臀肌'],tip:'背部千万不要弓腰，宁可重量轻一些。'},
      {n:'保加利亚分腿蹲',sets:'3组 × 10次/腿',rest:'60秒',muscles:'股四头肌、臀大肌',steps:['后脚架在凳子或床沿上（高约45cm）','前脚向前迈出大步，成弓步姿势','上身保持直立，核心收紧','前腿膝盖不要超过脚尖太多','后膝缓慢向地面下落（不触地）','前脚跟发力站起，感受前腿臀部收缩'],tip:'初期可以不拿重量，只用体重练习平衡感。'},
      {n:'坐姿腿屈伸',sets:'3组 × 15次',rest:'60秒',muscles:'股四头肌（大腿前侧）',steps:['调整座椅，膝盖与机器转轴对齐','腿垫放在脚踝上方','呼气伸腿至几乎全伸，顶部停顿1秒','吸气控制2秒缓慢下落','不要用惯性甩腿'],tip:'专门针对大腿前侧，是深蹲的很好补充。'},
      {n:'腿举机 / 哑铃深蹲',sets:'3组 × 15次',rest:'60秒',muscles:'股四头肌、臀大肌',steps:['腿举机：双脚与肩同宽踩踏板','下放时大腿贴近胸口，感受充分拉伸','脚跟发力推起，不要锁死膝盖','无器械：双手各持哑铃做深蹲替代'],tip:''},
      {n:'站姿提踵',sets:'4组 × 20次',rest:'45秒',muscles:'小腿腓肠肌',steps:['站立，脚尖踩台阶边缘，脚跟悬空','踮起脚尖到最高点，停顿1秒','缓慢下落至脚跟低于台阶','可手持哑铃增加难度'],tip:''},
    ]},
    {icon:'🧘',title:'拉伸放松',sub:'腿部拉伸',time:'10min',exs:[
      {n:'大腿前侧拉伸',sets:'每侧30秒×2',rest:'—',muscles:'股四头肌',steps:['单腿站立，手抓另一侧脚踝向臀部拉','上身保持直立，感受大腿前侧拉伸'],tip:''},
      {n:'大腿后侧拉伸',sets:'每侧30秒×2',rest:'—',muscles:'腘绳肌',steps:['坐地腿伸直，身体前倾触碰脚尖','膝盖不弯，感受大腿后侧拉伸'],tip:''},
      {n:'蝴蝶式',sets:'60秒',rest:'—',muscles:'大腿内侧',steps:['坐地脚底对脚底，按膝盖向地面压'],tip:''},
    ]},
  ]},
  B:{name:'力量训练 B',focus:'核心 + 上肢',time:'55分钟',color:'#b39ddb',phases:[
    {icon:'🔥',title:'热身',sub:'激活核心肌群',time:'10min',exs:[
      {n:'慢跑/跳绳',sets:'5分钟',rest:'—',muscles:'全身升温',steps:['慢速跑或跳绳，直到身体微微出汗'],tip:''},
      {n:'猫牛式热身',sets:'各10次',rest:'30秒',muscles:'脊柱、核心',steps:['四肢跪地，吸气塌腰抬头（牛式）','呼气拱背低头（猫式），缓慢交替','感受脊柱逐节活动'],tip:''},
      {n:'平板支撑热身',sets:'30秒×2',rest:'30秒',muscles:'核心激活',steps:['肘撑地，身体成一直线','感受腹部收紧，正常呼吸'],tip:''},
    ]},
    {icon:'💪',title:'核心训练',sub:'腹部重点',time:'20min',exs:[
      {n:'平板支撑',sets:'4组 × 45~60秒',rest:'60秒',muscles:'腹横肌、核心稳定肌群',steps:['肘部着地，前臂平放地面','身体从头到脚成一直线','臀部不要翘起或下塌，收腹','想象肚脐向脊柱方向收缩','正常呼吸，不要憋气','快撑不住时，再坚持5秒才放'],tip:'姿势正确比时间长更重要。'},
      {n:'卷腹',sets:'4组 × 20次',rest:'60秒',muscles:'腹直肌上段',steps:['平躺屈膝，双手放耳侧，不要抱头','只抬起上背，不是完整坐起','呼气上卷，顶部停顿1秒挤压腹肌','吸气缓慢下落，不要完全放松腹肌','动作幅度小但收缩感强才是正确的'],tip:'感受腹肌收缩比次数更重要。'},
      {n:'俄罗斯转体',sets:'3组 × 20次（每侧10）',rest:'60秒',muscles:'腹斜肌',steps:['坐姿，膝盖弯曲，脚可以抬起（难）或放地（易）','上身后倾约45度，背部保持直','双手合十或持哑铃，左右交替旋转','触碰地面为一次，保持核心收紧'],tip:'腹斜肌是腰部线条的关键。'},
      {n:'反向卷腹',sets:'3组 × 15次',rest:'60秒',muscles:'腹直肌下段（下腹部）',steps:['平躺，双腿伸直抬起至垂直地面','用腹肌力量将臀部抬离地面','缓慢下落，腿不要完全落地','不要用惯性甩腿，全程腹肌控制'],tip:'针对下腹赘肉最有效的动作。'},
    ]},
    {icon:'💪',title:'上肢训练',sub:'背部+胸部+肩部',time:'20min',exs:[
      {n:'引体向上 / 高位下拉',sets:'3组 × 8~12次',rest:'90秒',muscles:'背阔肌、肱二头肌',steps:['引体：双手握杠，与肩同宽或略宽','用背阔肌发力将身体向上拉，不要耸肩','拉至下颌过杠，缓慢下落','不能做引体：高位下拉机器完全可替代','下拉时肘部向下贴肋骨，感受背部收缩'],tip:''},
      {n:'俯卧撑',sets:'3组 × 15次',rest:'60秒',muscles:'胸大肌、三角肌前束',steps:['双手与肩同宽，手指向前，身体成直线','胸部下落至距地面约5cm','呼气推起，顶部轻微夹胸','太难可以跪式俯卧撑','太简单可以双脚放在凳子上'],tip:''},
      {n:'哑铃肩推',sets:'3组 × 12次',rest:'60秒',muscles:'三角肌中束、前束',steps:['坐姿，背部靠椅，哑铃举至耳朵两侧','呼气向上推至头顶，两哑铃不要碰','下落至哑铃与耳朵同高','全程收腹，不要用腰部借力'],tip:''},
      {n:'哑铃俯身划船',sets:'3组 × 12次',rest:'60秒',muscles:'背阔肌、菱形肌',steps:['一手扶凳，另一手持哑铃，身体前倾45~60度','哑铃自然垂下，手臂伸直','肘部向上弯曲，将哑铃拉至腰侧','拉至最高点挤压背部1秒，缓慢下放'],tip:''},
    ]},
  ]},
  C:{name:'力量训练 C',focus:'腿部强化 + 核心',time:'60分钟',color:'#4caf50',phases:[
    {icon:'🔥',title:'热身',sub:'腿部动态热身',time:'10min',exs:[
      {n:'慢跑+高抬腿',sets:'5分钟',rest:'—',muscles:'全身升温',steps:['慢跑2分钟，然后高抬腿跑1分钟，循环'],tip:''},
      {n:'弓步行走',sets:'10步×2',rest:'30秒',muscles:'股四头肌、髋屈肌',steps:['向前迈大步成弓步','站起并步，再向前迈另一条腿','感受每步的拉伸感'],tip:''},
    ]},
    {icon:'💪',title:'腿部强化',sub:'变式深蹲为主',time:'30min',exs:[
      {n:'哑铃深蹲（控速）',sets:'4组 × 15次',rest:'90秒',muscles:'股四头肌、臀大肌',steps:['双手各持哑铃，动作同标准深蹲','重点：下蹲用3秒（离心控制），起立用1秒','这叫离心训练，肌肉刺激更深','重量比A训练稍轻，因为动作更慢'],tip:'慢速下蹲是精髓，不要图快。'},
      {n:'相扑深蹲',sets:'3组 × 12次',rest:'90秒',muscles:'大腿内侧、臀大肌',steps:['双脚比肩宽，脚尖大幅外八约45度','双手持哑铃放身体中间','膝盖沿脚尖方向推开，不要内扣','下蹲时上身保持直立','感受大腿内侧拉伸，起立时挤压臀部'],tip:'专门针对大腿内侧，减大腿的好动作。'},
      {n:'跨步弓步蹲',sets:'3组 × 10次/腿',rest:'60秒',muscles:'股四头肌、臀大肌',steps:['向前迈出大步成弓步','后腿膝盖不落地（距地约2cm）','前腿发力站起，双脚并拢','再向前迈另一条腿，在空地上行进'],tip:''},
      {n:'侧向弓步',sets:'3组 × 10次/腿',rest:'60秒',muscles:'大腿内侧、臀大肌',steps:['向侧面迈出大步，重心压向迈出的腿','另一腿保持伸直，脚尖朝前','迈出腿屈膝，大腿内侧有拉伸感','站起来并步，再向另一侧迈'],tip:'很好地针对大腿内侧脂肪。'},
    ]},
    {icon:'💪',title:'核心强化',sub:'进阶核心动作',time:'15min',exs:[
      {n:'悬挂举腿',sets:'3组 × 12次',rest:'60秒',muscles:'下腹部、髂腰肌',steps:['双手抓单杠悬挂（或用辅助带）','双腿伸直，用腹肌力量将腿抬至水平或以上','顶部停顿1秒，缓慢下落','不会可以屈膝举腿（更容易入门）','不要摇摆借力'],tip:'强化下腹部最有效的动作之一。'},
      {n:'侧平板支撑',sets:'3组 × 30秒/侧',rest:'45秒',muscles:'腹斜肌、腰方肌',steps:['侧身肘撑，身体侧面成一直线','腰部不要下塌，臀部不要翘起','可以上腿向前迈步增加难度'],tip:''},
      {n:'波比跳',sets:'3组 × 10次',rest:'90秒',muscles:'全身爆发力+燃脂',steps:['第1步：站立','第2步：下蹲，双手撑地','第3步：双脚向后跳成平板支撑','第4步：做一个俯卧撑','第5步：双脚向前跳回手旁','第6步：起立跳起，双手举过头顶','以上6步为1次，连续10次'],tip:'全身最燃脂的动作，做完心率会飙升，坚持！'},
    ]},
  ]},
  CA:{name:'有氧训练',focus:'跑步 / 跳绳',time:'35~40分钟',color:'#ff7043',phases:[
    {icon:'🏃',title:'有氧训练流程',sub:'燃脂区间训练',time:'35~40min',exs:[
      {n:'热身慢走',sets:'5分钟',rest:'—',muscles:'准备活动',steps:['以舒适步伐行走，逐渐加快步伐','深呼吸，感受身体状态'],tip:''},
      {n:'慢跑（第1~2周）',sets:'快走3min+慢跑2min，循环6次',rest:'—',muscles:'心肺+全身',steps:['快走3分钟（心率100~110）','慢跑2分钟（心率110~125）','循环6次，总计30分钟','配速不重要，保持能说话的强度'],tip:'不用追求速度，跑起来就对了。'},
      {n:'慢跑（第3~4周起）',sets:'持续25~30分钟',rest:'—',muscles:'心肺+全身',steps:['热身慢走5分钟','慢跑25分钟，心率120~135','配速约8~9分钟/公里','冷却慢走5分钟'],tip:''},
      {n:'冷却慢走+拉伸',sets:'5分钟',rest:'—',muscles:'冷却放松',steps:['慢走让心率降至100以下','做腿部静态拉伸'],tip:''},
    ]},
  ]},
  CB:{name:'有氧训练',focus:'快走 / 骑车',time:'40~50分钟',color:'#ff7043',phases:[
    {icon:'🚴',title:'低冲击有氧',sub:'轻松燃脂',time:'40~50min',exs:[
      {n:'快走',sets:'40~50分钟',rest:'—',muscles:'心肺+腿部',steps:['步速比散步快，双臂自然摆动','保持心率在110~130次/分','找有坡道的路线效果更好','每20分钟补水一次'],tip:'快走对膝盖压力小，适合周六轻松有氧。'},
      {n:'骑自行车',sets:'40~50分钟',rest:'—',muscles:'大腿+心肺',steps:['调整座椅：腿伸直时膝盖微弯','保持匀速踩踏，节奏稳定','有坡道时站起来踩增加强度','室内骑行机也可以'],tip:''},
    ]},
  ]},
  REST:{name:'主动休息日',focus:'低强度恢复',time:'30~40分钟',color:'#6e7681',phases:[
    {icon:'🚶',title:'散步+拉伸',sub:'促进恢复',time:'30~40min',exs:[
      {n:'轻松散步',sets:'20~30分钟',rest:'—',muscles:'促进血液循环',steps:['步速轻松舒适，不需要出汗','可以听音乐或播客','目的是让身体动起来，加速乳酸代谢'],tip:'休息日散步可以减轻肌肉酸痛。'},
      {n:'全身拉伸',sets:'15分钟',rest:'—',muscles:'全身肌肉放松',steps:['参考「热身拉伸」页面的训练后拉伸内容','在休息日做全身拉伸，恢复效果更好','可配合舒缓音乐，彻底放松'],tip:''},
    ]},
  ]},
};

function openM(id){
  var w = WD[id];
  if(!w) return;
  var mhdr = document.getElementById('mhdr');
  mhdr.innerHTML = '<div><div class="mtitle" style="color:'+w.color+'">'+w.name+'</div><div class="msub">'+w.focus+' · '+w.time+'</div></div><button class="mclosebtn" onclick="closeM()">✕</button>';
  var ml = document.getElementById('mexlist');
  ml.innerHTML = '';
  w.phases.forEach(function(ph){
    var phDiv = document.createElement('div');
    phDiv.innerHTML = '<div class="phase-hdr"><div class="ph-icon">'+ph.icon+'</div><div><div class="ph-title">'+ph.title+'</div><div class="ph-sub">'+ph.sub+'</div></div><div class="ph-time">'+ph.time+'</div></div>';
    ml.appendChild(phDiv);
    var exDiv = document.createElement('div');
    exDiv.className = 'exlist';
    ph.exs.forEach(function(ex,i){
      var stepsHtml = ex.steps.map(function(s,j){
        return '<div class="step"><div class="stepnum">'+(j+1)+'</div><div class="steptxt">'+s+'</div></div>';
      }).join('');
      var tipHtml = ex.tip ? '<div class="extip"><span>💡 '+ex.tip+'</span></div>' : '';
      var restTag = ex.rest !== '—' ? '<span class="extag r">⏱ 休息 '+ex.rest+'</span>' : '';
      var c = document.createElement('div');
      c.className = 'excard';
      c.innerHTML = '<div class="exhdr" onclick="toggleEx(this)"><div class="exnum">'+(i+1)+'</div><div class="extitle">'+ex.n+'</div><div class="exsets">'+ex.sets+'</div><i class="exarrow">▼</i></div><div class="exbody"><div class="extags"><span class="extag s">📊 '+ex.sets+'</span>'+restTag+'<span class="extag m">🎯 '+ex.muscles+'</span></div><div class="steps">'+stepsHtml+'</div>'+tipHtml+'</div>';
      exDiv.appendChild(c);
    });
    ml.appendChild(exDiv);
  });
  document.getElementById('modal').classList.add('on');
  document.body.style.overflow = 'hidden';
}

function toggleEx(hdr){
  var body = hdr.nextElementSibling;
  var arrow = hdr.querySelector('.exarrow');
  var isOpen = body.classList.contains('on');
  body.classList.toggle('on',!isOpen);
  arrow.classList.toggle('open',!isOpen);
}

function closeM(){
  document.getElementById('modal').classList.remove('on');
  document.body.style.overflow = '';
}

function closeMO(e){
  if(e.target === document.getElementById('modal')) closeM();
}

// ── FAQ ──
function faq(el){
  var ans = el.nextElementSibling;
  var arrow = el.querySelector('.faq-arrow');
  var isOpen = ans.classList.contains('on');
  ans.classList.toggle('on',!isOpen);
  arrow.style.transform = isOpen ? '' : 'rotate(180deg)';
}

// ── LOG (in-memory only, WeChat safe) ──
var logData = [];
function saveLog(){
  var w = document.getElementById('iw').value;
  var wa = document.getElementById('iwa').value;
  var t = document.getElementById('it').value;
  var wo = document.getElementById('iwo').value;
  if(!w){ alert('请填写体重'); return; }
  var now = new Date();
  var d = (now.getMonth()+1)+'月'+(now.getDate())+'日';
  logData.unshift({date:d,weight:parseFloat(w),waist:wa||'—',thigh:t||'—',wo:wo});
  document.getElementById('iw').value='';
  document.getElementById('iwa').value='';
  document.getElementById('it').value='';
  renderLog();
}
function renderLog(){
  var el = document.getElementById('loglist');
  if(!logData.length){
    el.innerHTML='<div class="empty"><div class="empty-icon">📝</div>填写上方数据后点击保存</div>';
    return;
  }
  el.innerHTML = logData.map(function(l,i){
    var prev = logData[i+1];
    var chgHtml = '';
    if(prev){
      var diff = (l.weight - prev.weight).toFixed(1);
      var cls = diff < 0 ? 'd' : diff > 0 ? 'u' : 's';
      var sym = diff < 0 ? '↓' : diff > 0 ? '↑' : '—';
      chgHtml = '<span class="logchg '+cls+'">'+sym+' '+Math.abs(diff)+'</span>';
    }
    return '<div class="logitem"><div><div class="logdate">'+l.date+' · '+l.wo+' · 腰'+l.waist+'cm</div></div><div style="display:flex;align-items:center;gap:8px"><div class="logw">'+l.weight+'<span style="font-size:12px;color:var(--txt3)">kg</span></div>'+chgHtml+'</div></div>';
  }).join('');
}
</script>
</body>
</html>
