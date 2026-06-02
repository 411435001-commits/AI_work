# 洄山海

<style>
* { box-sizing: border-box; margin: 0; padding: 0; }
.wrap { font-family: var(--font-sans); padding: 2rem 1rem; max-width: 680px; margin: 0 auto; }
.hero { text-align: center; margin-bottom: 2rem; }
.cafe-name { font-size: 24px; font-weight: 500; color: var(--color-text-primary); letter-spacing: 0.05em; }
.cafe-en { font-size: 12px; color: var(--color-text-secondary); letter-spacing: 0.12em; margin-top: 3px; }
.tagline { font-size: 12px; color: var(--color-text-secondary); margin-top: 8px; }
.divider { width: 40px; height: 1px; background: var(--color-border-secondary); margin: 1rem auto; }
.tabs { display: flex; gap: 8px; justify-content: center; margin-bottom: 1.5rem; flex-wrap: wrap; }
.tab {
  font-size: 13px; padding: 5px 16px;
  border: 0.5px solid var(--color-border-secondary);
  border-radius: 99px; cursor: pointer;
  background: transparent; color: var(--color-text-secondary);
  transition: all 0.15s;
}
.tab.active {
  background: var(--color-text-primary);
  color: var(--color-background-primary);
  border-color: var(--color-text-primary);
}
.section { display: none; }
.section.show { display: block; }
.sec-label {
  font-size: 10px; font-weight: 500; letter-spacing: 0.15em;
  color: var(--color-text-secondary); margin-bottom: 0.75rem;
}
.grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(185px, 1fr)); gap: 10px; margin-bottom: 1.5rem; }
.card {
  background: var(--color-background-primary);
  border: 0.5px solid var(--color-border-tertiary);
  border-radius: var(--border-radius-lg);
  padding: 1rem 1.1rem;
  display: flex; flex-direction: column; gap: 5px;
  transition: border-color 0.15s;
}
.card:hover { border-color: var(--color-border-primary); }
.card-icon { font-size: 24px; color: var(--color-text-secondary); margin-bottom: 2px; }
.card-name { font-size: 14px; font-weight: 500; color: var(--color-text-primary); line-height: 1.4; }
.card-desc { font-size: 11px; color: var(--color-text-secondary); line-height: 1.5; }
.card-price { font-size: 14px; font-weight: 500; color: var(--color-text-primary); margin-top: auto; padding-top: 6px; }
.badge {
  display: inline-block; font-size: 10px; font-weight: 500;
  padding: 1px 7px; border-radius: var(--border-radius-md);
  background: var(--color-background-success); color: var(--color-text-success);
  margin-left: 5px; vertical-align: middle;
}
.footer { text-align: center; font-size: 11px; color: var(--color-text-secondary); margin-top: 1.5rem; line-height: 2; }
</style>

<div class="wrap">
  <h2 class="sr-only">洄山海咖啡菜單</h2>
  <div class="hero">
    <div class="cafe-name">洄山海咖啡</div>
    <div class="cafe-en">Hualien Tide &amp; Ridge Café</div>
    <div class="tagline">山嵐・海鹽・蜜香・鮮奶　花蓮在地好味道</div>
    <div class="divider"></div>
  </div>

  <div class="tabs">
    <button class="tab active" onclick="show('all',this)">全部</button>
    <button class="tab" onclick="show('hot',this)">熱飲</button>
    <button class="tab" onclick="show('cold',this)">冷飲</button>
    <button class="tab" onclick="show('food',this)">輕食</button>
  </div>

  <div id="all" class="section show">
    <div class="sec-label">熱飲 HOT DRINKS</div>
    <div class="grid">
      <div class="card">
        <i class="ti ti-tea card-icon" aria-hidden="true"></i>
        <div class="card-name">花蓮蜜香紅茶拿鐵</div>
        <div class="card-desc">舞鶴蜜香紅茶融合瑞穗鮮奶，香甜圓潤</div>
        <div class="card-price">NT$ 140</div>
      </div>
      <div class="card">
        <i class="ti ti-mug card-icon" aria-hidden="true"></i>
        <div class="card-name">瑞穗鮮奶熱可可</div>
        <div class="card-desc">比利時可可搭瑞穗牧場鮮奶，暖心厚實</div>
        <div class="card-price">NT$ 150</div>
      </div>
      <div class="card">
        <i class="ti ti-leaf card-icon" aria-hidden="true"></i>
        <div class="card-name">舞鶴蜜香紅茶<span class="badge">招牌</span></div>
        <div class="card-desc">舞鶴茶園直送，蜜香自然甘甜，無需加糖</div>
        <div class="card-price">NT$ 120</div>
      </div>
      <div class="card">
        <i class="ti ti-coffee card-icon" aria-hidden="true"></i>
        <div class="card-name">太魯閣山嵐手沖</div>
        <div class="card-desc">花蓮高山豆，雲霧孕育，果香清亮尾韻甜</div>
        <div class="card-price">NT$ 170</div>
      </div>
    </div>

    <div class="sec-label">冷飲 COLD DRINKS</div>
    <div class="grid">
      <div class="card">
        <i class="ti ti-glass-full card-icon" aria-hidden="true"></i>
        <div class="card-name">七星潭海鹽冰拿鐵<span class="badge">招牌</span></div>
        <div class="card-desc">海鹽奶蓋點睛，提升咖啡層次感，鹹甜平衡</div>
        <div class="card-price">NT$ 160</div>
      </div>
      <div class="card">
        <i class="ti ti-lemon card-icon" aria-hidden="true"></i>
        <div class="card-name">花蓮柚香氣泡飲</div>
        <div class="card-desc">富里文旦柚鮮榨，加入天然氣泡，清爽解渴</div>
        <div class="card-price">NT$ 140</div>
      </div>
      <div class="card">
        <i class="ti ti-droplet card-icon" aria-hidden="true"></i>
        <div class="card-name">鳳林檸檬冷萃咖啡</div>
        <div class="card-desc">18 小時冷萃，加入鳳林檸檬，酸香清爽</div>
        <div class="card-price">NT$ 160</div>
      </div>
      <div class="card">
        <i class="ti ti-milk card-icon" aria-hidden="true"></i>
        <div class="card-name">瑞穗鮮奶黑糖冰茶</div>
        <div class="card-desc">手工黑糖搭瑞穗鮮奶，濃醇甜蜜，消暑首選</div>
        <div class="card-price">NT$ 150</div>
      </div>
    </div>

    <div class="sec-label">輕食 LIGHT MEALS</div>
    <div class="grid">
      <div class="card">
        <i class="ti ti-bread card-icon" aria-hidden="true"></i>
        <div class="card-name">剝皮辣椒雞肉可頌</div>
        <div class="card-desc">花蓮特產剝皮辣椒，鹹香微辣，搭奶油可頌</div>
        <div class="card-price">NT$ 180</div>
      </div>
      <div class="card">
        <i class="ti ti-slice card-icon" aria-hidden="true"></i>
        <div class="card-name">花蓮地瓜乳酪吐司</div>
        <div class="card-desc">花蓮地瓜泥抹厚，搭奶油乳酪，香甜綿密</div>
        <div class="card-price">NT$ 160</div>
      </div>
      <div class="card">
        <i class="ti ti-bowl card-icon" aria-hidden="true"></i>
        <div class="card-name">洄瀾小米鹹派<span class="badge">招牌</span></div>
        <div class="card-desc">原住民小米入派皮，蔬菜鹹餡，在地風味獨特</div>
        <div class="card-price">NT$ 170</div>
      </div>
      <div class="card">
        <i class="ti ti-cookie card-icon" aria-hidden="true"></i>
        <div class="card-name">瑞穗鮮奶布丁佐茶凍</div>
        <div class="card-desc">鮮奶布丁搭蜜香茶凍，滑嫩清香，甜點首選</div>
        <div class="card-price">NT$ 150</div>
      </div>
    </div>
  </div>

  <div id="hot" class="section">
    <div class="sec-label">熱飲 HOT DRINKS</div>
    <div class="grid">
      <div class="card"><i class="ti ti-tea card-icon" aria-hidden="true"></i><div class="card-name">花蓮蜜香紅茶拿鐵</div><div class="card-desc">舞鶴蜜香紅茶融合瑞穗鮮奶，香甜圓潤</div><div class="card-price">NT$ 140</div></div>
      <div class="card"><i class="ti ti-mug card-icon" aria-hidden="true"></i><div class="card-name">瑞穗鮮奶熱可可</div><div class="card-desc">比利時可可搭瑞穗牧場鮮奶，暖心厚實</div><div class="card-price">NT$ 150</div></div>
      <div class="card"><i class="ti ti-leaf card-icon" aria-hidden="true"></i><div class="card-name">舞鶴蜜香紅茶<span class="badge">招牌</span></div><div class="card-desc">舞鶴茶園直送，蜜香自然甘甜，無需加糖</div><div class="card-price">NT$ 120</div></div>
      <div class="card"><i class="ti ti-coffee card-icon" aria-hidden="true"></i><div class="card-name">太魯閣山嵐手沖</div><div class="card-desc">花蓮高山豆，雲霧孕育，果香清亮尾韻甜</div><div class="card-price">NT$ 170</div></div>
    </div>
  </div>

  <div id="cold" class="section">
    <div class="sec-label">冷飲 COLD DRINKS</div>
    <div class="grid">
      <div class="card"><i class="ti ti-glass-full card-icon" aria-hidden="true"></i><div class="card-name">七星潭海鹽冰拿鐵<span class="badge">招牌</span></div><div class="card-desc">海鹽奶蓋點睛，提升咖啡層次感，鹹甜平衡</div><div class="card-price">NT$ 160</div></div>
      <div class="card"><i class="ti ti-lemon card-icon" aria-hidden="true"></i><div class="card-name">花蓮柚香氣泡飲</div><div class="card-desc">富里文旦柚鮮榨，加入天然氣泡，清爽解渴</div><div class="card-price">NT$ 140</div></div>
      <div class="card"><i class="ti ti-droplet card-icon" aria-hidden="true"></i><div class="card-name">鳳林檸檬冷萃咖啡</div><div class="card-desc">18 小時冷萃，加入鳳林檸檬，酸香清爽</div><div class="card-price">NT$ 160</div></div>
      <div class="card"><i class="ti ti-milk card-icon" aria-hidden="true"></i><div class="card-name">瑞穗鮮奶黑糖冰茶</div><div class="card-desc">手工黑糖搭瑞穗鮮奶，濃醇甜蜜，消暑首選</div><div class="card-price">NT$ 150</div></div>
    </div>
  </div>

  <div id="food" class="section">
    <div class="sec-label">輕食 LIGHT MEALS</div>
    <div class="grid">
      <div class="card"><i class="ti ti-bread card-icon" aria-hidden="true"></i><div class="card-name">剝皮辣椒雞肉可頌</div><div class="card-desc">花蓮特產剝皮辣椒，鹹香微辣，搭奶油可頌</div><div class="card-price">NT$ 180</div></div>
      <div class="card"><i class="ti ti-slice card-icon" aria-hidden="true"></i><div class="card-name">花蓮地瓜乳酪吐司</div><div class="card-desc">花蓮地瓜泥抹厚，搭奶油乳酪，香甜綿密</div><div class="card-price">NT$ 160</div></div>
      <div class="card"><i class="ti ti-bowl card-icon" aria-hidden="true"></i><div class="card-name">洄瀾小米鹹派<span class="badge">招牌</span></div><div class="card-desc">原住民小米入派皮，蔬菜鹹餡，在地風味獨特</div><div class="card-price">NT$ 170</div></div>
      <div class="card"><i class="ti ti-cookie card-icon" aria-hidden="true"></i><div class="card-name">瑞穗鮮奶布丁佐茶凍</div><div class="card-desc">鮮奶布丁搭蜜香茶凍，滑嫩清香，甜點首選</div><div class="card-price">NT$ 150</div></div>
    </div>
  </div>

  <div class="footer">
    <i class="ti ti-map-pin" style="font-size:12px;vertical-align:-1px;margin-right:3px;" aria-hidden="true"></i>花蓮市
    &nbsp;·&nbsp;
    <i class="ti ti-clock" style="font-size:12px;vertical-align:-1px;margin-right:3px;" aria-hidden="true"></i>週二至週日 08:00–18:00
    &nbsp;·&nbsp;
    <i class="ti ti-leaf" style="font-size:12px;vertical-align:-1px;margin-right:3px;" aria-hidden="true"></i>食材來自花蓮在地小農
  </div>
</div>

<script>
function show(id, btn) {
  document.querySelectorAll('.section').forEach(s => s.classList.remove('show'));
  document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
  document.getElementById(id).classList.add('show');
  btn.classList.add('active');
}
</script>
