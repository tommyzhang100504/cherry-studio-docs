---
hidden: True
icon: phone-arrow-up-right
---

{% hint style="warning" %}
تمت ترجمة هذا المستند من الصينية بواسطة الذكاء الاصطناعي ولم تتم مراجعته بعد.
{% endhint %}

```ar
# وظيفة الصوت

```
دليل استخدام وظيفة الصوت في Cherry Studio

## 1. نظرة عامة على وظيفة الصوت

يوفر Cherry Studio ثلاث وحدات صوتية رئيسية: TTS (تحويل النص إلى كلام)، ASR (التعرف على الكلام)، والمكالمات الصوتية. تتيح لك هذه الوظائف التفاعل مع الذكاء الاصطناعي بشكل طبيعي عبر الصوت، مما يعزز تجربة المستخدم.

- **TTS (تحويل النص إلى كلام)**: تحويل ردود الذكاء الاصطناعي النصية إلى ناتج صوتي
- **ASR (التعرف على الكلام)**: تحويل صوتك إلى نص مدخل
- **المكالمات الصوتية**: تجمع بين TTS و ASR لتوفير تجربة حوار صوتي مشابه لـ ChatGPT

## 2. وظيفة TTS (تحويل النص إلى كلام)

### 1. أنواع الخدمات المدعومة

يدعم Cherry Studio أربعة أنواع من خدمات TTS:

- **OpenAI**: استخدام واجهة برمجة التطبيقات (API) الخاصة بـ OpenAI، تتطلب مفتاح API
- **متصفح TTS**: استخدام وظيفة التوليف الصوتي المدمجة في المتصفح، مجاني ولا يتطلب تكوين
- **Siliconflow**: استخدام خدمة Siliconflow لتحويل النص إلى كلام، تتطلب مفتاح API
- **تحويل النص إلى كلام مجاني عبر الإنترنت**: استخدام خدمة TTS مجانية عبر الإنترنت، لا تتطلب مفتاح API

### 2. طريقة الإعداد

1) انتقل إلى صفحة الإعدادات، واختر علامة تبويب "وظيفة الصوت"
2) في علامة التبويب الفرعية "TTS":
   - تفعيل وظيفة TTS (تشغيل المفتاح)
   - اختيار نوع خدمة TTS
   - تكوين المعلمات بناءً على نوع الخدمة المحدد:
     - OpenAI: إدخال مفتاح API، عنوان API، اختيار نبرة الصوت والنموذج
     - متصفح TTS: اختيار نبرة الصوت
     - Siliconflow: إدخال مفتاح API، عنوان API، اختيار نبرة الصوت، النموذج، تنسيق الاستجابة وسرعة الكلام
     - التحويل المجاني عبر الإنترنت: اختيار نبرة الصوت وتنسيق الإخراج
3) تكوين خيارات تصفية TTS (اختياري):
   - تصفية عمليات التفكير
   - تصفية علامات Markdown
   - تصفية كتل الكود
4) تعيين إظهار شريط تقدم TTS أم لا
5) النقر على زر "اختبار TTS" للتحقق من صحة الإعدادات

### 3. طريقة الاستخدام

- عند تفعيل وظيفة TTS، سيتم تحويل ردود الذكاء الاصطناعي تلقائيًا إلى صوت
- في واجهة الدردشة، سيظهر زر تشغيل TTS أسفل كل رد من الذكاء الاصطناعي
- النقر على زر التشغيل لتشغيل/إيقاف الصوت مؤقتًا
- إذا تم تفعيل شريط تقدم TTS، سيعرض تقدم التشغيل أسفل النص
- سيقوم النص الطويل بالتقسيم التلقائي والتشغيل المتواصل

## 3. وظيفة ASR (التعرف على الكلام)

### 1. أنواع الخدمات المدعومة

يدعم Cherry Studio ثلاثة أنواع من خدمات ASR:

- **OpenAI**: استخدام نموذج Whisper من OpenAI، يتطلب مفتاح API
- **المتصفح**: استخدام وظيفة التعرف على الكلام المدمجة في المتصفح، مجانية ولا تتطلب تكوين
- **خادم محلي**: الاتصال بخادم WebSocket محلي للتعرف على الكلام

### 2. طريقة الإعداد

1) انتقل إلى صفحة الإعدادات، واختر علامة تبويب "وظيفة الصوت"
2) في علامة التبويب الفرعية "ASR":
   - تفعيل وظيفة ASR (تشغيل المفتاح)
   - اختيار نوع خدمة ASR
   - تكوين المعلمات بناءً على نوع الخدمة المحدد:
     - OpenAI: إدخال مفتاح API، عنوان API، اختيار النموذج
     - المتصفح: لا يتطلب تكوين إضافي
     - الخادم المحلي: تعيين ما إذا كان سيتم بدء تشغيل خادم ASR تلقائيًا عند بدء التطبيق
   - اختيار لغة التعرف على الكلام (الافتراضي: الصينية)
3) النقر على زر "اختبار ASR" للتحقق من صحة الإعدادات

### 3. طريقة الاستخدام

- عند تفعيل وظيفة ASR، سيعرض زر التعرف على الكلام بجانب حقل الإدخال
- النقر على زر التعرف على الكلام لبدء التسجيل
- بعد التحدث، سيتم تحويل الصوت إلى نص وإدخاله في الحقل
- النقر على الزر مرة أخرى لإنهاء التسجيل
- يدعم التعرف على الكلام تسجيل جمل متعددة بشكل متواصل بالوضع التراكمي

## 4. وظيفة المكالمات الصوتية

### 1. الميزات الرئيسية

- تجمع بين TTS و ASR لتوفير تجربة حوار صوتي مشابه لـ ChatGPT
- استخدام واجهة نافذة عائمة قابلة للسحب
- دعم وضع الضغط الطويل للتحدث
- دعم اختصارات لوحة المفاتيح المخصصة
- دعم طي النافذة
- إمكانية اختيار نموذج خاص بالمكالمات الصوتية
- دعم تخصيص التلميحات

### 2. طريقة الإعداد

1) انتقل إلى صفحة الإعدادات، واختر علامة تبويب "وظيفة الصوت"
2) في علامة التبويب الفرعية "وظيفة المكالمات":
   - تفعيل وظيفة المكالمات الصوتية (تشغيل المفتاح)
   - النقر على زر "اختيار نموذج"، واختيار نموذج الذكاء الاصطناعي للمكالمات الصوتية
   - تخصيص تلميحات المكالمات الصوتية في مربع النص (اختياري)
   - النقر على زر "حفظ" لحفظ التلميحات، أو "إعادة تعيين" لاستعادة التلميحات الافتراضية

### 3. طريقة الاستخدام

1) في واجهة الدردشة، انقر على زر المكالمة الصوتية (أيقونة الهاتف) على يمين حقل الإدخال
2) ستفتح نافذة المكالمة الصوتية وتشغيل رسالة الترحيب الصوتية
3) اضغط باستمرار على زر "اضغط للتحدث" لبدء التسجيل (أو استخدام اختصار لوحة المفاتيح المعد)
4) اترك الزر لإنهاء التسجيل وإرسال النص إلى الذكاء الاصطناعي
5) يقوم الذكاء الاصطناعي بإنشاء الرد وتشغيله عبر TTS
6) استخدام أزرار التحكم في النافذة:
   - زر كتم/إلغاء الكتم: التحكم في ناتج TTS
   - زر إيقاف مؤقت/متابعة: إيقاف أو استئناف المحادثة
   - زر الإعدادات: تكوين اختصارات لوحة المفاتيح
   - زر الطي: طي النافذة، مع الاحتفاظ فقط بصف الضغط للتحدث
7) انقر على زر الإغلاق لإنهاء المكالمة

### 4. إعداد اختصارات لوحة المفاتيح

1) في نافذة المكالمة الصوتية، انقر على زر الإعدادات
2) في لوحة الإعدادات المنبثقة، انقر على زر اختصارات لوحة المفاتيح
3) اضغط على المفتاح الذي تريد تعيينه (مثل مفتاح المسافة، مفتاح Shift، إلخ)
4) انقر على زر "حفظ" لحفظ الإعدادات
5) عند الاستخدام، اضغط باستمرار على المفتاح المعد لبدء التسجيل، ثم اتركه لإنهاء التسجيل والإرسال

## 5. المشاكل الشائعة والحلول

### 1. مشاكل متعلقة بـ TTS

- **المشكلة**: TTS لا يصدر صوتًا  
  **الحل**: تحقق من تفعيل وظيفة TTS، وتأكد من اختيار نوع الخدمة الصحيح وتكوين المعلمات الضرورية

- **المشكلة**: جودة صوت TTS منخفضة  
  **الحل**: جرب تبديل نوع خدمة TTS أو نبرة الصوت

- **المشكلة**: ظهور رسائل خطأ أثناء تشغيل TTS  
  **الحل**: تحقق من صحة مفتاح API، وتأكد من اتصال الشبكة

### 2. مشاكل متعلقة بـ ASR

- **المشكلة**: ASR لا يتعرف على الصوت  
  **الحل**: تحقق من تفعيل وظيفة ASR، وتأكد من اختيار نوع الخدمة الصحيح وتكوين المعلمات الضرورية

- **المشكلة**: دقة التعرف على الكلام منخفضة  
  **الحل**: جرب تبديل نوع خدمة ASR، أو اضبط موقع الميكروفون ومستوى الصوت

- **المشكلة**: فشل الاتصال بخادم ASR  
  **الحل**: تحقق من تشغيل الخادم المحلي بشكل صحيح، أو حاول إعادة تشغيل التطبيق

### 3. مشاكل متعلقة بالمكالمات الصوتية

- **المشكلة**: نافذة المكالمة الصوتية لا تفتح  
  **الحل**: تحقق من تفعيل وظيفة المكالمات الصوتية، وتأكد من تكوين وظائف TTS و ASR بشكل صحيح

- **المشكلة**: لا يستجيب زر الضغط للتحدث  
  **الحل**: تحقق من منح إذن الميكروفون، أو حاول إعادة تشغيل المكالمة الصوتية

- **المشكلة**: الردود الصوتية من الذكاء الاصطناعي لا تعمل  
  **الحل**: تحقق من تفعيل وظيفة TTS، وتأكد من عدم تفعيل وضع الكتم

## 6. الإعدادات المتقدمة وخيارات التخصيص

### 1. إعدادات TTS المتقدمة

- خيارات التصفية: تصفية عمليات التفكير، علامات Markdown وكتل الكود للحصول على تشغيل TTS أكثر سلاسة
- إظهار شريط التقدم: اختيار إظهار شريط تقدم TTS أم لا
- تخصيص نبرة الصوت والنموذج: إضافة خيارات مخصصة لنبرة الصوت والنماذج

### 2. إعدادات ASR المتقدمة

- بدء تشغيل الخادم تلقائيًا: تعيين ما إذا كان سيتم بدء تشغيل خادم ASR تلقائيًا عند بدء التطبيق
- اختيار اللغة: اختيار لغات مختلفة للتعرف على الكلام

### 3. إعدادات المكالمات الصوتية المتقدمة

- تخصيص التلميحات: تخصيص تلميحات المكالمات الصوتية لتوجيه ردود الذكاء الاصطناعي أثناء المكالمات
- اختيار نموذج مخصص: اختيار نموذج ذكاء اصطناعي خاص بالمكالمات الصوتية بشكل منفصل عن نموذج المحادثة الحالي
- تخصيص اختصارات لوحة المفاتيح: تعيين اختصارات مخصصة للتحكم في التسجيل

## 7. نصائح الاستخدام

1. **اختيار خدمة TTS المناسبة**:
   - لصوت عالي الجودة: أوصي باستخدام OpenAI أو Siliconflow
   - لتجنب تكوين API: استخدم متصفح TTS أو خدمة TTS المجانية عبر الإنترنت

2. **اختيار خدمة ASR المناسبة**:
   - لدقة عالية: أوصي باستخدام OpenAI
   - لتجنب تكوين API: استخدم وظيفة التعرف على الكلام المدمجة في المتصفح

3. **تحسين تجربة المكالمات الصوتية**:
   - استخدام سماعات الأذن لتجنب التقاط صوت TTS مجددًا بواسطة ASR
   - استخدام بيئة هادئة لتحسين دقة التعرف على الكلام
   - استخدام تلميحات مخصصة لجعل ردود الذكاء الاصطناعي أكثر ملاءمة للتشغيل الصوتي

4. **تعديل الإعدادات حسب الاحتياجات**:
   - للتواصل النصي بشكل رئيسي: قم بتفعيل وظيفة TTS فقط
   - للإدخال الصوتي بشكل رئيسي: قم بتفعيل وظيفة ASR فقط
   - لتجربة حوار صوتي كاملة: قم بتفعيل وظيفة المكالمات الصوتية

نأمل أن يساعدك هذا الدليل في الاستفادة الكاملة من وظائف الصوت في Cherry Studio، والتمتع بتجربة تفاعل طبيعية ومريحة مع الذكاء الاصطناعي!
```