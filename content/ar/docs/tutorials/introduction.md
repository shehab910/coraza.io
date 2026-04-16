---
title: "مقدمة"
description: "مقدمة عن جدار حماية تطبيقات الويب Coraza. ابدأ بحماية تطبيقات الويب الخاصة بك في خطوات قليلة."
lead: "مرحبًا بك في جدار حماية تطبيقات الويب Coraza، هذا المشروع هو نسخة مبنية بلغة Go من ModSecurity بهدف أن يصبح أول جدار حماية تطبيقات ويب مفتوح المصدر بمستوى المؤسسات، مرن وقوي بما يكفي ليكون الأساس للعديد من المشاريع."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
weight: 100
toc: true
---

<div dir="rtl">

<h1>
  <img src="https://coraza.io/images/logo_shield_only.png" align="left" height="46px" alt=""/>&nbsp;
  <span>Coraza - جدار حماية تطبيقات الويب</span>
</h1>

<a href="https://github.com/corazawaf/coraza/actions/workflows/regression.yml"><img src="https://github.com/corazawaf/coraza/actions/workflows/regression.yml/badge.svg" alt="Regression Tests"></a>
<a href="#"><img src="https://img.shields.io/badge/Coreruleset%20Compatibility-100%25-brightgreen" alt="Coreruleset Compatibility"></a>
<a href="https://github.com/corazawaf/coraza/actions/workflows/codeql-analysis.yml"><img src="https://github.com/corazawaf/coraza/actions/workflows/codeql-analysis.yml/badge.svg" alt="CodeQL"></a>
<a href="https://codecov.io/gh/corazawaf/coraza"><img src="https://codecov.io/gh/corazawaf/coraza/branch/v3/dev/graph/badge.svg?token=6570804ZC7" alt="codecov"></a>
<a href="https://www.repostatus.org/#active"><img src="https://www.repostatus.org/badges/latest/active.svg" alt="Project Status: Active"></a>
<a href="https://owasp.org/www-project-coraza-web-application-firewall"><img src="https://img.shields.io/badge/owasp-lab%20project-brightgreen" alt="OWASP Lab Project"></a>
<a href="https://godoc.org/github.com/corazawaf/coraza/v3"><img src="https://godoc.org/github.com/corazawaf/coraza?status.svg" alt="GoDoc"></a>

Coraza هو جدار حماية تطبيقات ويب (WAF) مفتوح المصدر، بمستوى المؤسسات وعالي الأداء، جاهز لحماية تطبيقاتك. مكتوب بلغة Go، ويدعم مجموعات قواعد ModSecurity SecLang ومتوافق بنسبة 100% مع OWASP Core Rule Set.

* الموقع الإلكتروني: https://coraza.io
* المنتدى: [مناقشات Github](https://github.com/corazawaf/coraza/discussions)
* مجتمع OWASP على Slack (قناة #coraza): https://owasp.org/slack/invite
* اختبار القواعد: [Coraza Playground](https://playground.coraza.io)

<br/>

الميزات الرئيسية:

* ⇲ **بديل جاهز** - Coraza هو محرك بديل يتمتع بتوافق جزئي مع ~Trustwave~[محرك OWASP ModSecurity](https://github.com/owasp-modsecurity/modsecurity/) ويدعم مجموعات قواعد SecLang المعتمدة كمعيار في المجال.

* 🔥 **الأمان** - يُشغّل Coraza مجموعة قواعد [OWASP CRS](https://coreruleset.org) لحماية تطبيقات الويب الخاصة بك من مجموعة واسعة من الهجمات، بما في ذلك OWASP Top Ten، مع الحد الأدنى من التنبيهات الخاطئة. تحمي CRS من العديد من فئات الهجمات الشائعة بما في ذلك حقن SQL (SQLi)، والبرمجة عبر المواقع (XSS)، وحقن أكواد PHP و Java، وHTTPoxy، وShellshock، واكتشاف البرامج النصية/الماسحات/الروبوتات، وتسريب البيانات الوصفية والأخطاء.

* 🔌 **قابل للتوسعة** - Coraza في جوهره مكتبة برمجية، مع العديد من التكاملات لنشر نسخ جدار حماية تطبيقات الويب محليًا. مسجّلات التدقيق، ومحركات التخزين الدائم، والمعاملات، والإجراءات — أنشئ وظائفك الخاصة لتوسيع Coraza بقدر ما تريد.

* 🚀 **الأداء** - من المواقع الضخمة إلى المدونات الصغيرة، يستطيع Coraza التعامل مع الحِمل بأقل تأثير على الأداء. اطّلع على [اختبارات الأداء](https://coraza.io/docs/reference/benchmarks) الخاصة بنا.

* ﹡ **البساطة** - يمكن لأي شخص فهم وتعديل الكود المصدري لـ Coraza. من السهل توسيع Coraza بوظائف جديدة.

* 💬 **المجتمع** - Coraza مشروع مجتمعي، المساهمات مرحّب بها وجميع الأفكار ستؤخذ بعين الاعتبار. تجد إرشادات المساهمة في وثيقة [CONTRIBUTION](https://github.com/corazawaf/coraza/blob/main/CONTRIBUTING.md).

<br/>

## التكاملات

يحتفظ مشروع Coraza بتطبيقات وإضافات للخوادم التالية:

* [إضافة Caddy كخادم وكيل عكسي وخادم ويب](https://github.com/corazawaf/coraza-caddy) - مستقر، يحتاج إلى مشرف
* [إضافة Proxy WASM](https://github.com/corazawaf/coraza-proxy-wasm) للخوادم الوكيلة التي تدعم proxy-wasm (مثل Envoy) - مستقر، لا يزال قيد التطوير
* [إضافة HAProxy SPOE](https://github.com/corazawaf/coraza-spoa) - معاينة
* [إضافة Traefik Proxy](https://github.com/jptosso/coraza-traefik) - معاينة، يحتاج إلى مشرف
* [وسيط إطار عمل Gin للويب](https://github.com/jptosso/coraza-gin) - معاينة، يحتاج إلى مشرف
* [Apache HTTP Server](https://github.com/corazawaf/coraza-apache) - تجريبي
* [Nginx](https://github.com/corazawaf/coraza-nginx) - تجريبي
* [مكتبة Coraza بلغة C](https://github.com/corazawaf/libcoraza) - تجريبي

## الإضافات

* [Coraza GeoIP](https://github.com/corazawaf/coraza-geoip) (معاينة)

## المتطلبات الأساسية

* مُصرّف Go الإصدار 1.18 أو أحدث
* توزيعة Linux (يُنصح بـ Debian أو CentOS) أو Mac. نظام Windows غير مدعوم حاليًا.


## استخدام نواة Coraza

يمكن استخدام Coraza كمكتبة برمجية في برنامج Go الخاص بك لتنفيذ وسيط أمان أو دمجه مع التطبيقات وخوادم الويب الحالية.

```go
package main

import (
	"fmt"
	"github.com/corazawaf/coraza/v3"
)

func main() {
	// First we initialize our waf and our seclang parser
	waf, err := coraza.NewWAF(coraza.NewWAFConfig().
		WithDirectives(`SecRule REMOTE_ADDR "@rx .*" "id:1,phase:1,deny,status:403"`))
	// Now we parse our rules
	if err != nil {
		fmt.Println(err)
	}

	// Then we create a transaction and assign some variables
    tx := waf.NewTransaction()
	defer func() {
		tx.ProcessLogging()
		tx.Close()
	}()
	tx.ProcessConnection("127.0.0.1", 8080, "127.0.0.1", 12345)

	// Finally we process the request headers phase, which may return an interruption
	if it := tx.ProcessRequestHeaders(); it != nil {
		fmt.Printf("Transaction was interrupted with status %d\n", it.Status)
	}
}
```
يوفر [Examples/http-server](./examples/http-server/) مثالًا للتدريب العملي مع Coraza.

### علامات البناء

يمكن لعلامات البناء في Go تعديل وظائف معينة في وقت التصريف. هذه مخصصة لحالات الاستخدام المتقدمة فقط ولا تتضمن
ضمانات توافق عبر الإصدارات الفرعية — استخدمها بحذر.

- coraza.disabled_operators.* - تستثني المعامل المحدد من التصريف. مفيد بشكل خاص عند استبدال
المعامل باستخدام `operators.Register` لتقليل حجم الملف التنفيذي / عبء بدء التشغيل.
- `coraza.rule.multiphase_valuation` - تُمكّن تقييم متغيرات القاعدة في المراحل التي تكون جاهزة فيها، وليس
فقط في المرحلة التي تم تعريف القاعدة لها.

## الأدوات

* [Go FTW](https://github.com/coreruleset/go-ftw): محرك اختبار القواعد
* [Coraza Playground](https://playground.coraza.io/): واجهة ويب لاختبار القواعد في بيئة معزولة
* [OWASP Core Ruleset](https://github.com/coreruleset/coreruleset/): مجموعة قواعد متميزة، متوافقة مع Coraza

## التطوير

يتطلب Coraza فقط Go للتطوير. يمكنك تشغيل `mage.go` لتنفيذ أوامر التطوير.

عرض قائمة الأوامر

```shell
go run mage.go -l
```

على سبيل المثال، لتنسيق الكود قبل الإرسال، نفّذ

```shell
go run mage.go format
```

## المساهمة

المساهمات مرحّب بها! يُرجى الرجوع إلى [CONTRIBUTING.md](./CONTRIBUTING.md) للاطلاع على الإرشادات.

## شكر وتقدير

* فريق ModSecurity لإنشاء ModSecurity
* فريق OWASP Core Ruleset لمجموعة CRS ومساعدتهم

### الشركات والمنتجات التي تستخدم Coraza

* [Traefik](https://owasp.org/blog/2024/03/19/traefik_owasp)
* [United Security Providers AG](https://www.united-security-providers.ch/)
* [Ambassador Labs](https://www.getambassador.io/docs/edge-stack/latest/howtos/web-application-firewalls)
* [Apache APISIX](https://apisix.apache.org/blog/2023/09/08/APISIX-integrates-with-Coraza/)
* [Wallarm API Firewall](https://github.com/wallarm/api-firewall)

### Coraza على X/Twitter

- [@corazaio](https://twitter.com/corazaio)

## التبرعات

للتبرعات، راجع [صفحة التبرعات](https://owasp.org/donate/?reponame=www-project-coraza-web-application-firewall&title=OWASP+Coraza+Web+Application+Firewall)

## شكر لجميع الأشخاص الذين ساهموا

لم نكن لنتمكن من تحقيق هذا بدونكم!

<a href="https://github.com/corazawaf/coraza/graphs/contributors">
<img src="https://contrib.rocks/image?repo=corazawaf/coraza" />
</a>

صُنع باستخدام [contrib.rocks](https://contrib.rocks).

</div>
