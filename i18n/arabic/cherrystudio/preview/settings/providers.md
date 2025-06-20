---
icon: cloud-check
---

{% hint style="warning" %}
تمت ترجمة هذا المستند من الصينية بواسطة الذكاء الاصطناعي ولم تتم مراجعته بعد.
{% endhint %}

# إعدادات موفري الخدمة

تقدم هذه الصفحة فقط وصفًا لوظائف الواجهة. للإرشادات التفصيلية حول التكوين، يمكنك الرجوع إلى برنامج [إعدادات المورد](../../../pre-basic/providers/) في الدروس الأساسية.

{% hint style="info" %}
* عند استخدام موفري الخدمة المدمجين، ما عليك سوى ملء المفتاح المقابل.
* قد تختلف تسميات المفاتيح باختلاف موفري الخدمة، لكن "المفتاح السري"، "Key"، "API Key"، "الرمز" كلها تشير إلى نفس الشيء.
{% endhint %}



### مفتاح API

في Cherry Studio، يدعم كل موفر خدمة استخدام مفاتيح متعددة بالتناوب، حيث يتم التناوب بشكل دوري عبر القائمة من البداية إلى النهاية.

* تتم إضافة المفاتيح المتعددة مفصولة بفواصل إنجليزية. كما في المثال التالي:

<pre><code><strong>sk-xxxx1,sk-xxxx2,sk-xxxx3,sk-xxxx4
</strong></code></pre>

{% hint style="warning" %}
يجب استخدام **فاصلة إنجليزية** فقط.
{% endhint %}

### عنوان API

عند استخدام موفري الخدمة المدمجين، لا تحتاج عادةً إلى ملء عنوان API. إذا احتجت إلى تعديله، اتبع بدقة العنوان المقدم في الوثائق الرسمية المقابلة.

> إذا كان العنوان المقدم من المزود بالشكل <mark style="background-color:red;">https://xxx.xxx.com</mark><mark style="background-color:green;">/v1/chat/completions</mark>، يكفي ملء جزء العنوان الأساسي (<mark style="background-color:red;">https://xxx.xxx.com</mark>) فقط.
>
> سيقوم Cherry Studio تلقائيًا بتوصيل المسار المتبقي (<mark style="background-color:green;">/v1/chat/completions</mark>). عدم الالتزام بهذا قد يؤدي إلى مشاكل في التشغيل.

{% hint style="info" %}
ملاحظة: يكون توجيه نماذج اللغة الكبيرة موحدًا لدى معظم المزودين، لذا لا تحتاج عادةً للإجراءات التالية. إذا كان مسار API للمزود هو v2، v3/chat/completions أو إصدار آخر، يمكنك إدخال الإصدار يدويًا في حقل العنوان مع إنهائه ب `\`. عند اختلاف مسار طلب المزود عن المعيار <mark style="background-color:green;">/v1/chat/completions</mark>، استخدم العنوان الكامل المقدم من المزود مع إنهائه بـ `#`.

بشكل أكثر وضوحًا:

* عند انتهاء عنوان API بـ `/`، يتم فقط توصيل "<mark style="background-color:green;">chat/completions</mark>"
* عند انتهاء عنوان API بـ `#`، لا يتم إجراء أي توصيل، ويُستخدم العنوان المدخل كما هو.

![](<../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png>)![](<../../../.gitbook/assets/image (15).png>)
{% endhint %}



### إضافة النماذج

بشكل عام، يؤدي النقر على زر `إدارة` في الزاوية السفلية اليسرى لصفحة إعدادات المزود إلى جلب جميع النماذج المدعومة تلقائيًا. انقر على رمز `+` بجوار النموذج المطلوب لإضافته إلى قائمة النماذج.

{% hint style="info" %}
لن تتم إضافة جميع النماذج من القائمة المنبثقة تلقائيًا عند النقر على زر الإدارة. يجب النقر على `+` بجوار كل نموذج لإضافته إلى قائمة نماذج المزود حتى يظهر في قائمة اختيار النماذج.
{% endhint %}


### فحص الاتصال

انقر على زر الفحص بجانب حقل مفتاح API لاختبار نجاح التكوين.

{% hint style="info" %}
يستخدم الفحص افتراضيًا آخر نموذج محادثة مضاف إلى القائمة. إذا فشل الفحص، تحقق من وجود نماذج غير صحيحة أو غير مدعومة في القائمة.
{% endhint %}

{% hint style="danger" %}
بعد التكوين الناجح، تأكد من تفعيل المفتاح في الزاوية العلوية اليمنى، وإلا سيظل المزود غير نشط ولن تظهر نماذجه في القائمة.
{% endhint %}