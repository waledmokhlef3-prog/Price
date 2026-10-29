<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>عرض سعر — استديو وليد</title>
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Sans+Arabic:wght@200;300;400;500;600;700&display=swap" rel="stylesheet">
<style>
*, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }

:root {
  --bg: #0d1117;
  --surface: #161b22;
  --surface2: #1c2230;
  --border: rgba(255,255,255,0.07);
  --border2: rgba(255,255,255,0.13);
  --text: #e6edf3;
  --muted: rgba(230,237,243,0.45);
  --muted2: rgba(230,237,243,0.7);
  --accent: #7aa2d4;
  --accent-dim: rgba(122,162,212,0.1);
  --gold: #c9a227;
  --gold-dim: rgba(201,162,39,0.1);
  --green: #3fb950;
  --green-dim: rgba(63,185,80,0.1);
}

body {
  font-family: 'IBM Plex Sans Arabic', sans-serif;
  background: var(--bg);
  color: var(--text);
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 40px 20px;
}

/* Atmospheric background */
body::before {
  content: '';
  position: fixed; inset: 0;
  background:
    radial-gradient(ellipse 60% 50% at 20% 10%, rgba(30,50,90,0.25) 0%, transparent 65%),
    radial-gradient(ellipse 40% 40% at 80% 80%, rgba(20,40,70,0.2) 0%, transparent 60%);
  pointer-events: none;
}

.page {
  position: relative;
  z-index: 1;
  width: 100%;
  max-width: 720px;
}

/* ─── HEADER ─── */
.doc-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 32px 36px;
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 20px 20px 0 0;
  border-bottom: none;
}

.studio-brand {
  display: flex;
  align-items: center;
  gap: 14px;
}

.studio-logo {
  width: 52px;
  height: 52px;
  border-radius: 14px;
  object-fit: cover;
  border: 1px solid var(--border2);
}

.studio-name {
  font-size: 17px;
  font-weight: 700;
  letter-spacing: -0.02em;
  color: var(--text);
  line-height: 1.2;
}

.studio-sub {
  font-size: 11px;
  color: var(--muted);
  font-weight: 300;
  letter-spacing: 0.04em;
  margin-top: 2px;
}

.doc-meta {
  text-align: left;
}

.doc-badge {
  display: inline-block;
  padding: 5px 14px;
  background: var(--accent-dim);
  border: 1px solid rgba(122,162,212,0.2);
  border-radius: 100px;
  font-size: 11px;
  font-weight: 500;
  color: var(--accent);
  letter-spacing: 0.05em;
  text-transform: uppercase;
  margin-bottom: 8px;
}

.doc-date {
  font-size: 12px;
  color: var(--muted);
  font-weight: 300;
}

/* ─── DIVIDER ─── */
.hline {
  height: 1px;
  background: linear-gradient(90deg, transparent, rgba(122,162,212,0.3), transparent);
  margin: 0 36px;
}

/* ─── BODY ─── */
.doc-body {
  background: var(--surface);
  border-left: 1px solid var(--border);
  border-right: 1px solid var(--border);
  padding: 36px;
}

/* TO section */
.to-section {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  margin-bottom: 36px;
  gap: 20px;
}

.to-block {}
.to-label {
  font-size: 10px;
  letter-spacing: 0.1em;
  color: var(--muted);
  text-transform: uppercase;
  margin-bottom: 6px;
}

.client-name {
  font-size: 22px;
  font-weight: 700;
  letter-spacing: -0.03em;
  color: var(--text);
}

.doc-number {
  text-align: left;
}

.doc-num-label {
  font-size: 10px;
  letter-spacing: 0.08em;
  color: var(--muted);
  text-transform: uppercase;
  margin-bottom: 4px;
}

.doc-num-val {
  font-size: 15px;
  font-weight: 600;
  color: var(--muted2);
  letter-spacing: -0.01em;
}

/* Hero title */
.project-title-block {
  background: linear-gradient(135deg, rgba(122,162,212,0.07) 0%, rgba(122,162,212,0.02) 100%);
  border: 1px solid rgba(122,162,212,0.15);
  border-radius: 16px;
  padding: 28px 30px;
  margin-bottom: 28px;
}

.project-eyebrow {
  font-size: 11px;
  color: var(--accent);
  letter-spacing: 0.08em;
  text-transform: uppercase;
  margin-bottom: 10px;
}

.project-name {
  font-size: 32px;
  font-weight: 700;
  letter-spacing: -0.04em;
  line-height: 1.1;
  margin-bottom: 12px;
}

.project-desc {
  font-size: 14px;
  color: var(--muted2);
  font-weight: 300;
  line-height: 1.75;
}

/* ─── DELIVERABLES ─── */
.section-title {
  font-size: 12px;
  font-weight: 600;
  color: var(--muted);
  letter-spacing: 0.07em;
  text-transform: uppercase;
  margin-bottom: 14px;
  display: flex;
  align-items: center;
  gap: 10px;
}

.section-title::after {
  content: '';
  flex: 1;
  height: 1px;
  background: var(--border);
}

.deliverables {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 10px;
  margin-bottom: 28px;
}

.deliv-card {
  background: var(--surface2);
  border: 1px solid var(--border);
  border-radius: 12px;
  padding: 16px 18px;
  display: flex;
  align-items: flex-start;
  gap: 12px;
  transition: border-color 0.2s;
}

.deliv-card:hover { border-color: var(--border2); }

.deliv-icon {
  font-size: 20px;
  line-height: 1;
  margin-top: 1px;
  flex-shrink: 0;
}

.deliv-text {}
.deliv-name {
  font-size: 13.5px;
  font-weight: 600;
  margin-bottom: 3px;
  letter-spacing: -0.01em;
}

.deliv-note {
  font-size: 11.5px;
  color: var(--muted);
  font-weight: 300;
  line-height: 1.5;
}

/* ─── PAYMENT ─── */
.payment-block {
  background: var(--surface2);
  border: 1px solid var(--border);
  border-radius: 16px;
  overflow: hidden;
  margin-bottom: 24px;
}

.payment-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 20px 24px;
  border-bottom: 1px solid var(--border);
}

.payment-header-label {
  font-size: 13px;
  font-weight: 600;
  color: var(--muted2);
}

.total-price {
  font-size: 28px;
  font-weight: 700;
  letter-spacing: -0.04em;
  color: var(--text);
}

.total-cur {
  font-size: 14px;
  color: var(--muted);
  font-weight: 400;
  margin-right: 4px;
}

.payment-rows {
  display: flex;
  flex-direction: column;
}

.payment-row {
  display: flex;
  align-items: center;
  padding: 18px 24px;
  border-bottom: 1px solid var(--border);
  gap: 16px;
}

.payment-row:last-child { border-bottom: none; }

.payment-step {
  width: 28px;
  height: 28px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 12px;
  font-weight: 700;
  flex-shrink: 0;
}

.step-1 {
  background: var(--green-dim);
  border: 1px solid rgba(63,185,80,0.25);
  color: var(--green);
}

.step-2 {
  background: rgba(122,162,212,0.1);
  border: 1px solid rgba(122,162,212,0.2);
  color: var(--accent);
}

.payment-info { flex: 1; }
.payment-phase {
  font-size: 14px;
  font-weight: 600;
  margin-bottom: 2px;
  letter-spacing: -0.01em;
}

.payment-when {
  font-size: 12px;
  color: var(--muted);
  font-weight: 300;
}

.payment-amount {
  font-size: 20px;
  font-weight: 700;
  letter-spacing: -0.03em;
}

.amount-1 { color: var(--green); }
.amount-2 { color: var(--accent); }

.amount-cur {
  font-size: 12px;
  color: var(--muted);
  font-weight: 400;
  margin-right: 3px;
}

/* ─── NOTE BOX ─── */
.note-box {
  background: rgba(201,162,39,0.06);
  border: 1px solid rgba(201,162,39,0.18);
  border-radius: 12px;
  padding: 18px 20px;
  display: flex;
  gap: 14px;
  align-items: flex-start;
  margin-bottom: 28px;
}

.note-text {
  font-size: 13px;
  color: rgba(201,162,39,0.85);
  font-weight: 300;
  line-height: 1.7;
}

/* ─── TERMS ─── */
.terms-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 10px;
  margin-bottom: 32px;
}

.term-item {
  display: flex;
  align-items: flex-start;
  gap: 10px;
  padding: 14px 16px;
  background: var(--surface2);
  border: 1px solid var(--border);
  border-radius: 10px;
}

.term-check {
  font-size: 13px;
  color: var(--green);
  flex-shrink: 0;
  margin-top: 1px;
}

.term-text {
  font-size: 12.5px;
  color: var(--muted2);
  font-weight: 300;
  line-height: 1.55;
}

/* ─── CTA ─── */
.cta-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 16px;
}

.cta-msg {
  font-size: 13px;
  color: var(--muted);
  font-weight: 300;
  line-height: 1.6;
  max-width: 340px;
}

.cta-btn {
  flex-shrink: 0;
  padding: 13px 28px;
  background: var(--accent);
  color: #0d1117;
  border: none;
  border-radius: 100px;
  font-family: 'IBM Plex Sans Arabic', sans-serif;
  font-size: 14px;
  font-weight: 700;
  cursor: pointer;
  transition: all 0.2s;
  white-space: nowrap;
  box-shadow: 0 4px 20px rgba(122,162,212,0.3);
}

.cta-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 28px rgba(122,162,212,0.4);
}

/* ─── FOOTER ─── */
.doc-footer {
  background: var(--surface2);
  border: 1px solid var(--border);
  border-top: 1px solid var(--border);
  border-radius: 0 0 20px 20px;
  padding: 22px 36px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 12px;
}

.footer-brand {
  font-size: 13px;
  font-weight: 700;
  color: var(--muted2);
  letter-spacing: -0.01em;
}

.footer-note {
  font-size: 11.5px;
  color: var(--muted);
  font-weight: 300;
}

@media (max-width: 520px) {
  .doc-header, .doc-body { padding: 24px 20px; }
  .hline { margin: 0 20px; }
  .deliverables, .terms-grid { grid-template-columns: 1fr; }
  .to-section { flex-direction: column; }
  .cta-row { flex-direction: column; align-items: flex-start; }
  .doc-footer { padding: 18px 20px; }
}
</style>
</head>
<body>

<div class="page">

  <!-- HEADER -->
  <div class="doc-header">
    <div class="studio-brand">
      <img class="studio-logo" src="data:image/jpeg;base64,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" alt="شعار استديو وليد">
      <div>
        <div class="studio-name">استديو وليد</div>
        <div class="studio-sub">تصميم جرافيكي احترافي</div>
      </div>
    </div>
    <div class="doc-meta">
      <div class="doc-badge">عرض سعر</div>
      <div class="doc-date">الخميس، ٢٩ أكتوبر ٢٠٢٦</div>
    </div>
  </div>

  <div class="hline"></div>

  <!-- BODY -->
  <div class="doc-body">

    <!-- TO -->
    <div class="to-section">
      <div class="to-block">
        <div class="to-label">مُقدَّم إلى</div>
        <div class="client-name" dir="ltr" style="text-align:right">0500200188</div>
      </div>
      <div class="doc-number">
        <div class="doc-num-label">رقم العرض</div>
        <div class="doc-num-val">#WS-2026-002</div>
      </div>
    </div>

    <!-- PROJECT TITLE -->
    <div class="project-title-block">
      <div class="project-eyebrow">نوع الخدمة</div>
      <div class="project-name">هوية بصرية متكاملة</div>
      <div class="project-desc">
        نبدأ بشعار يعبّر عنك بدقة وذوق، ثم نبني عليه مطبوعاتك الرسمية — بطاقة العمل والأوراق الرسمية — بنفس الروح والألوان، لتظهر أمام عملائك بصورة واحدة متناسقة واحترافية من أول لقاء.
      </div>
    </div>

    <!-- DELIVERABLES -->
    <div class="section-title">ما تحصل عليه</div>

    <div class="deliverables">
      <div class="deliv-card">
        <div class="deliv-text">
          <div class="deliv-name">تصميم الشعار</div>
          <div class="deliv-note">نموذج واحد مدروس مع جولة تعديل واحدة شاملة</div>
        </div>
      </div>
      <div class="deliv-card">
        <div class="deliv-text">
          <div class="deliv-name">بطاقة العمل (Business Card)</div>
          <div class="deliv-note">تصميم أمامي وخلفي جاهز للطباعة</div>
        </div>
      </div>
      <div class="deliv-card">
        <div class="deliv-text">
          <div class="deliv-name">الأوراق الرسمية</div>
          <div class="deliv-note">ورق رسمي (Letterhead) وما يلزمه من قوالب مطبوعة</div>
        </div>
      </div>
      <div class="deliv-card">
        <div class="deliv-text">
          <div class="deliv-name">جميع الملفات</div>
          <div class="deliv-note">PNG شفاف · PDF · SVG · AI · ملفات الطباعة بدقة عالية</div>
        </div>
      </div>
    </div>

    <!-- PAYMENT -->
    <div class="section-title">هيكل الدفع</div>

    <div class="payment-block">
      <div class="payment-header">
        <div class="payment-header-label">إجمالي المشروع</div>
        <div class="total-price"><span class="total-cur">ر.س</span>300</div>
      </div>
      <div class="payment-rows">
        <div class="payment-row">
          <div class="payment-step step-1">١</div>
          <div class="payment-info">
            <div class="payment-phase">العربون</div>
            <div class="payment-when">عربون نصف القيمة — قبل البدء لتأكيد الطلب وحجز موعدك</div>
          </div>
          <div class="payment-amount amount-1"><span class="amount-cur">ر.س</span>150</div>
        </div>
        <div class="payment-row">
          <div class="payment-step step-2">٢</div>
          <div class="payment-info">
            <div class="payment-phase">دفعة الإكمال</div>
            <div class="payment-when">بعد إكمال التصاميم وقبل استلام الملفات النهائية</div>
          </div>
          <div class="payment-amount amount-2"><span class="amount-cur">ر.س</span>150</div>
        </div>
      </div>
    </div>

    <!-- NOTE -->
    <div class="note-box">
      <div class="note-text">
        العربون يؤكد الطلب وتضمن إبداعيتنا الكاملة من اليوم الأول — والدفعة الثانية تُسدَّد عند استلام الملفات النهائية.
      </div>
    </div>

    <!-- TERMS -->
    <div class="section-title">شروط العرض</div>

    <div class="terms-grid">
      <div class="term-item">
        <span class="term-check">—</span>
        <span class="term-text">مدة التسليم من يومين إلى أسبوع</span>
      </div>
      <div class="term-item">
        <span class="term-check">—</span>
        <span class="term-text">تسليم جميع الملفات فور اكتمال الدفع</span>
      </div>
      <div class="term-item">
        <span class="term-check">—</span>
        <span class="term-text">جولة تعديل واحدة شاملة للشعار</span>
      </div>
      <div class="term-item">
        <span class="term-check">—</span>
        <span class="term-text">العرض صالح لمدة ١٤ يوماً من تاريخه</span>
      </div>
    </div>

    <!-- CTA -->
    <div class="cta-row">
      <div class="cta-msg">للتأكيد وبدء المشروع، تواصل على واتساب: <strong style="color:var(--accent)">0537441043</strong></div>
      <button class="cta-btn">تواصل الآن</button>
    </div>

  </div>

  <!-- FOOTER -->
  <div class="doc-footer">
    <div class="footer-brand">استديو وليد</div>
    <div class="footer-note">هذا عرض سعر رسمي · مُعدّ خصيصاً للعميل الكريم</div>
  </div>

</div>

</body>
</html>
