<template>

</template>

<style scoped>
.page {
  max-width: 1200px;
  margin: 0 auto;
  padding: 28px 20px 80px;
}

.content {
  display: flex;
  flex-direction: column;
  gap: 96px;
}

.topbar {
  position: sticky;
  top: 0;
  z-index: 10;
  display: flex;
  align-items: center;
  gap: 18px;
  padding: 16px 18px;
  margin: 0 -4px 28px;
  border: 1px solid rgba(255, 255, 255, 0.6);
  border-radius: 16px;
  background: rgba(255, 255, 255, 0.75);
  backdrop-filter: blur(8px);
  box-shadow: 0 12px 40px rgba(16, 24, 40, 0.08);
}

.brand {
  display: grid;
  grid-auto-flow: column;
  grid-template-columns: auto 1fr;
  align-items: center;
  gap: 12px;
}

.brand__mark {
  width: 42px;
  height: 42px;
  border-radius: 14px;
  background: linear-gradient(145deg, var(--brand-primary), #ff7a8b);
  display: grid;
  place-items: center;
  color: #fff;
  font-weight: 700;
  letter-spacing: -0.01em;
}

.brand__eyebrow {
  font-size: 12px;
  text-transform: uppercase;
  color: var(--text-muted);
  letter-spacing: 0.12em;
}

.brand__name {
  font-size: 18px;
  font-weight: 700;
  color: var(--text-main);
}

.nav {
  display: flex;
  gap: 16px;
  margin-left: auto;
  margin-right: 16px;
  align-items: center;
}

.nav a {
  color: var(--text-main);
  text-decoration: none;
  font-weight: 600;
  padding: 8px 12px;
  border-radius: 10px;
  transition: all 0.2s ease;
}

.nav a:hover {
  color: var(--brand-primary);
  background: rgba(241, 92, 109, 0.08);
}

.topbar__cta {
  display: flex;
  gap: 8px;
  align-items: center;
}

.hero {
  display: grid;
  gap: 32px;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  align-items: center;
}

.pill {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: rgba(27, 154, 170, 0.14);
  color: var(--brand-secondary);
  padding: 8px 12px;
  border-radius: 999px;
  font-weight: 600;
  font-size: 13px;
}

h1 {
  font-size: clamp(32px, 5vw, 48px);
  margin: 12px 0 12px;
}

h2 {
  font-size: clamp(26px, 4vw, 36px);
  margin-bottom: 10px;
}

.lede {
  font-size: 18px;
  color: var(--text-muted);
  max-width: 640px;
}

.hero__actions,
.volunteer__actions {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin: 20px 0 12px;
}

.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  border-radius: 14px;
  padding: 12px 16px;
  font-weight: 700;
  text-decoration: none;
  border: 1px solid transparent;
  transition: all 0.2s ease;
}

.btn--primary {
  background: linear-gradient(135deg, var(--brand-primary), #ff7586);
  color: #fff;
  box-shadow: 0 14px 34px rgba(241, 92, 109, 0.25);
}

.btn--primary:hover {
  transform: translateY(-1px);
}

.btn--secondary {
  background: #ffffff;
  color: var(--brand-secondary);
  border-color: rgba(27, 154, 170, 0.3);
}

.btn--ghost {
  background: rgba(27, 154, 170, 0.08);
  color: var(--brand-secondary);
  border-color: rgba(27, 154, 170, 0.18);
}

.metrics {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(130px, 1fr));
  gap: 14px;
  margin-top: 24px;
}

.metric {
  padding: 14px 16px;
  border: 1px solid var(--border-subtle);
  border-radius: 14px;
  background: rgba(255, 255, 255, 0.92);
  box-shadow: 0 8px 24px rgba(15, 23, 42, 0.05);
}

.metric dt {
  color: var(--text-muted);
  font-size: 13px;
}

.metric dd {
  font-weight: 800;
  font-size: 24px;
  color: var(--text-main);
  margin: 4px 0 0;
}

.hero__visual {
  display: grid;
  gap: 16px;
}

.hero__photo {
  position: relative;
  overflow: hidden;
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-soft);
  border: 1px solid var(--border-subtle);
  background: linear-gradient(145deg, #ffffff, #f7fbff);
  min-height: 220px;
}

.hero__photo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.photo__badge {
  position: absolute;
  left: 14px;
  bottom: 14px;
  padding: 8px 12px;
  background: rgba(15, 23, 42, 0.78);
  color: #fff;
  border-radius: 999px;
  font-weight: 700;
  letter-spacing: 0.04em;
  font-size: 12px;
  backdrop-filter: blur(2px);
}

.card {
  background: linear-gradient(145deg, #ffffff, #f8fbff);
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-soft);
  padding: 18px 20px;
}

.card--floating {
  position: relative;
  overflow: hidden;
}

.card--floating::after {
  content: '';
  position: absolute;
  inset: -40% auto auto 60%;
  width: 160px;
  height: 160px;
  background: radial-gradient(circle, rgba(255, 209, 102, 0.6), rgba(255, 209, 102, 0));
  filter: blur(12px);
}

.card--stacked {
  display: flex;
  flex-direction: column;
  gap: 14px;
}

.card__text {
  color: var(--text-muted);
}

.tag {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 6px 10px;
  border-radius: 999px;
  background: rgba(241, 92, 109, 0.12);
  color: var(--brand-primary);
  font-weight: 700;
  font-size: 13px;
}

.tag--ghost {
  background: rgba(27, 154, 170, 0.1);
  color: var(--brand-secondary);
}

.progress {
  background: #f1f5f9;
  border-radius: 999px;
  overflow: hidden;
  height: 10px;
  margin: 16px 0 8px;
}

.progress.small {
  height: 8px;
  margin-top: 12px;
}

.progress__bar {
  height: 100%;
  background: linear-gradient(135deg, var(--brand-primary), #ff9aa8);
  border-radius: 999px;
}

.progress__label {
  font-size: 14px;
  color: var(--text-muted);
}

.chips {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}

.chip {
  padding: 8px 12px;
  border-radius: 999px;
  background: #f7fbff;
  border: 1px solid var(--border-subtle);
  color: var(--text-main);
  font-weight: 600;
}

.section {
  display: flex;
  flex-direction: column;
  gap: 32px;
}

.section--alt {
  background: #ffffff;
  border: 1px solid var(--border-subtle);
  border-radius: var(--radius-lg);
  padding: 28px;
  box-shadow: var(--shadow-soft);
}

.section__header {
  max-width: 800px;
}

.eyebrow {
  text-transform: uppercase;
  letter-spacing: 0.14em;
  color: var(--brand-secondary);
  font-weight: 700;
  font-size: 12px;
}

.description {
  color: var(--text-muted);
}

.grid {
  display: grid;
  gap: 18px;
}

.grid--cards {
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
}

.card--program {
  display: grid;
  gap: 12px;
}

.icon {
  width: 48px;
  height: 48px;
  display: grid;
  place-items: center;
  border-radius: 14px;
  background: rgba(27, 154, 170, 0.12);
  font-size: 22px;
}

.bullet-list {
  list-style: none;
  padding: 0;
  margin: 0;
  display: grid;
  gap: 8px;
}

.bullet-list li {
  position: relative;
  padding-left: 18px;
  color: var(--text-muted);
}

.bullet-list li::before {
  content: '•';
  position: absolute;
  left: 0;
  color: var(--brand-primary);
}

.timeline {
  display: grid;
  gap: 14px;
}

.timeline__item {
  display: grid;
  grid-template-columns: auto 1fr;
  align-items: start;
  gap: 12px;
  padding: 16px;
  border-radius: 18px;
  border: 1px solid var(--border-subtle);
  background: linear-gradient(180deg, #fdfefe 0%, #f7fbff 100%);
}

.badge {
  width: 38px;
  height: 38px;
  border-radius: 12px;
  background: var(--brand-deep);
  color: #fff;
  display: grid;
  place-items: center;
  font-weight: 700;
}

.donation {
  display: grid;
  gap: 20px;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  align-items: center;
  background: linear-gradient(145deg, rgba(241, 92, 109, 0.08), rgba(27, 154, 170, 0.08));
  border: 1px solid rgba(241, 92, 109, 0.16);
  border-radius: var(--radius-lg);
  padding: 28px;
}

.donation__copy {
  display: grid;
  gap: 16px;
}

.options {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 12px;
}

.option {
  padding: 14px;
  border-radius: 14px;
  border: 1px dashed rgba(27, 154, 170, 0.25);
  background: #fff;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.04);
}

.muted {
  color: var(--text-muted);
}

.donation__card {
  background: #0f172a;
  color: #fff;
  border-radius: var(--radius-lg);
  padding: 22px;
  box-shadow: 0 16px 40px rgba(12, 33, 56, 0.25);
  border: 1px solid rgba(255, 255, 255, 0.06);
}

.donation__card .bullet-list li {
  color: rgba(255, 255, 255, 0.86);
}

.card--volunteer {
  display: grid;
  gap: 12px;
  border: 1px solid var(--border-subtle);
  background: linear-gradient(180deg, #ffffff 0%, #fff6eb 100%);
}

.footer {
  margin-top: 64px;
  padding-top: 24px;
  border-top: 1px solid var(--border-subtle);
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  gap: 12px;
}

.footer__links {
  display: flex;
  gap: 16px;
  align-items: center;
}

.footer a {
  color: var(--text-main);
  text-decoration: none;
  font-weight: 600;
}

@media (max-width: 960px) {
  .topbar {
    position: static;
    flex-wrap: wrap;
    justify-content: space-between;
  }

  .nav {
    width: 100%;
    order: 3;
    justify-content: center;
    flex-wrap: wrap;
    margin: 0;
  }

  .topbar__cta {
    margin-left: auto;
  }

  .page {
    padding: 20px 16px 64px;
  }
}

@media (max-width: 640px) {
  .metrics {
    grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  }

  .topbar__cta {
    width: 100%;
    justify-content: space-between;
  }

  .btn {
    width: 100%;
  }
}
</style>
