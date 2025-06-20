---
description: 数据设置→Obsidian配置
icon: gem
---

{% hint style="warning" %}
এই নথিটি এআই দ্বারা চীনা থেকে অনুবাদ করা হয়েছে এবং এখনও পর্যালোচনা করা হয়নি।
{% endhint %}

# Obsidian কনফিগারেশন টিউটোরিয়াল

Cherry Studio Obsidian-এর সাথে সংযোগ সমর্থন করে, সম্পূর্ণ কথোপকথন বা একক বার্তাকে Obsidian লাইব্রেরিতে রপ্তানি করতে।

{% hint style="warning" %}
এই প্রক্রিয়ার জন্য কোনো অতিরিক্ত Obsidian প্লাগইন ইনস্টল করার প্রয়োজন নেই। তবে যেহেতু Cherry Studio থেকে Obsidian-এ আমদানির প্রক্রিয়া Obsidian Web Clipper-এর অনুরূপ, তাই ব্যবহারকারীদের Obsidian-কে সর্বশেষ সংস্করণে আপগ্রেড করার পরামর্শ দেওয়া হয় (বর্তমান Obsidian সংস্করণ **1.7.2**-এর চেয়ে বেশি হওয়া উচিত)। এটি না করলে [দীর্ঘ কথোপকথনের ক্ষেত্রে আমদানি ব্যর্থ হতে পারে](https://github.com/obsidianmd/obsidian-clipper/releases/tag/0.7.0)।
{% endhint %}

## সর্বশেষ টিউটোরিয়াল

{% hint style="info" %}
Obsidian-এ রপ্তানির পুরনো সংস্করণের তুলনায়, নতুন সংস্করণ স্বয়ংক্রিয়ভাবে লাইব্রেরি পথ নির্বাচন করতে পারে, আর ম্যানুয়ালি লাইব্রেরি নাম বা ফোল্ডার নাম লিখতে হবে না।
{% endhint %}

### প্রথম ধাপ: Cherry Studio কনফিগার করুন

Cherry Studio-এর _সেটিংস_ → _ডেটা সেটিংস_ → _Obsidian কনফিগারেশন_ মেনু খুলুন। ড্রপডাউন তালিকায় স্বয়ংক্রিয়ভাবে আপনার ডিভাইসে খোলা Obsidian লাইব্রেরিগুলো প্রদর্শিত হবে। আপনার টার্গেট Obsidian লাইব্রেরি নির্বাচন করুন:

<figure><img src="../.gitbook/assets/image (142).png" alt=""><figcaption></figcaption></figure>

### দ্বিতীয় ধাপ: কথোপকথন রপ্তানি করুন

#### সম্পূর্ণ কথোপকথন রপ্তানি করুন

Cherry Studio-এর কথোপকথন ইন্টারফেসে ফিরে যান, কথোপকথনে রাইট-ক্লিক করুন, _রপ্তানি করুন_ নির্বাচন করুন, তারপর _Obsidian-এ রপ্তানি করুন_-এ ক্লিক করুন:

<figure><img src="../.gitbook/assets/image (143).png" alt=""><figcaption></figcaption></figure>

একটি উইন্ডো পপ আপ হবে যা Obsidian-এ রপ্তানি করা নোটের **প্রোপার্টিজ (Properties)**, Obsidian-এ **ফোল্ডার অবস্থান** এবং রপ্তানির **প্রক্রিয়াকরণ পদ্ধতি** সামঞ্জস্য করতে সাহায্য করবে:

* **ভল্ট (Vault)**: ড্রপডাউন মেনু থেকে অন্য Obsidian লাইব্রেরি নির্বাচন করুন
* **পথ (Path)**: রপ্তানি করা নোট সংরক্ষণের ফোল্ডার নির্বাচন করতে ড্রপডাউন মেনু ক্লিক করুন
* Obsidian নোট প্রোপার্টিজ (Properties) হিসেবে:
  * ট্যাগস (tags)
  * তৈরি করা সময় (created)
  * উৎস (source)
* Obsidian-এ রপ্তানির জন্য নিম্নোক্ত তিনটি **প্রক্রিয়াকরণ পদ্ধতি** উপলব্ধ:
  * **নতুন তৈরি করুন (যদি বিদ্যমান থাকে, তবে প্রতিস্থাপন করুন)**: **পথ**-এ উল্লেখিত `ফোল্ডার`-এ একটি নতুন কথোপকথন নোট তৈরি করুন। যদি একই নামের নোট বিদ্যমান থাকে, তবে তা পুরনো নোট প্রতিস্থাপন করবে
  * **প্রিফিক্স (Prepend)**: বিদ্যমান একই নামের নোট থাকলে, নির্বাচিত কথোপকথন সামগ্রী নোটের শুরুতে যোগ করুন
  * **অ্যাপেন্ড (Append)**: বিদ্যমান একই নামের নোট থাকলে, নির্বাচিত কথোপকথন সামগ্রী নোটের শেষে যোগ করুন

{% hint style="info" %}
শুধুমাত্র প্রথম পদ্ধতিতে প্রোপার্টিজ (Properties) সংযুক্ত থাকে, পরবর্তী দুটি পদ্ধতিতে প্রোপার্টিজ থাকে না।
{% endhint %}

<figure><img src="../.gitbook/assets/image (144).png" alt=""><figcaption><p>নোট প্রোপার্টিজ কনফিগার করুন</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (145).png" alt=""><figcaption><p>পথ নির্বাচন করুন</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (146).png" alt=""><figcaption><p>প্রক্রিয়াকরণ পদ্ধতি নির্বাচন করুন</p></figcaption></figure>

সমস্ত বিকল্প নির্বাচন করার পর, সঠিক Obsidian লাইব্রেরির সংশ্লিষ্ট ফোল্ডারে সম্পূর্ণ কথোপকথন রপ্তানি করতে নিশ্চিত করুন ক্লিক করুন।

#### একক বার্তা রপ্তানি করুন

একক বার্তা রপ্তানি করতে, বার্তার নিচের _থ্রি-লাইন মেনু_ ক্লিক করুন, _রপ্তানি করুন_ নির্বাচন করুন, তারপর _Obsidian-এ রপ্তানি করুন_-এ ক্লিক করুন:

<figure><img src="../.gitbook/assets/image (147).png" alt=""><figcaption><p>একক বার্তা রপ্তানি করুন</p></figcaption></figure>

এরপর সম্পূর্ণ কথোপকথন রপ্তানির মতো একই উইন্ডো পপ আপ হবে, যেখানে আপনাকে **নোট প্রোপার্টিজ** এবং **নোট প্রক্রিয়াকরণ পদ্ধতি** কনফিগার করতে হবে। [উপরের টিউটোরিয়ালে](obsidian.md#dao-chu-wan-zheng-dui-hua) উল্লেখিত ধাপগুলি অনুসরণ করে সম্পূর্ণ করুন।

### সফলভাবে রপ্তানি সম্পন্ন

🎉 এই পর্যায়ে, আপনি Cherry Studio-কে Obsidian-এর সাথে সংযুক্ত করার সমস্ত কনফিগারেশন সম্পূর্ণ করেছেন এবং সম্পূর্ণ রপ্তানি প্রক্রিয়া সফলভাবে সম্পন্ন করেছেন, উপভোগ করুন!

<figure><img src="../.gitbook/assets/image (140).png" alt=""><figcaption><p>Obsidian-এ রপ্তানি করুন</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (139).png" alt=""><figcaption><p>রপ্তানি ফলাফল পরীক্ষা করুন</p></figcaption></figure>

***

## পুরনো টিউটোরিয়াল (Cherry Studio <v1.1.13 সংস্করণের জন্য প্রযোজ্য)

### প্রথম ধাপ: Obsidian প্রস্তুত করুন

Obsidian লাইব্রেরি খুলুন, রপ্তানি করা কথোপকথন সংরক্ষণের জন্য একটি `ফোল্ডার` তৈরি করুন (উদাহরণ হিসেবে চিত্রে Cherry Studio ফোল্ডার দেখানো হয়েছে):

<figure><img src="../.gitbook/assets/image (127).png" alt=""><figcaption></figcaption></figure>

নিচের বাম দিকে হাইলাইট করা লেখাটি মনে রাখুন, এটি আপনার `ভল্ট` নাম।

### দ্বিতীয় ধাপ: Cherry Studio কনফিগার করুন

Cherry Studio-এর _সেটিংস_ → _ডেটা সেটিংস_ → _Obsidian কনফিগারেশন_ মেনুতে, [প্রথম ধাপে](obsidian.md#di-yi-bu) পাওয়া `ভল্ট` নাম এবং `ফোল্ডার` নাম লিখুন:

<figure><img src="../.gitbook/assets/image (129).png" alt=""><figcaption></figcaption></figure>

`গ্লোবাল ট্যাগস` ঐচ্ছিক, Obsidian-এ সমস্ত রপ্তানি করা কথোপকথনের জন্য ট্যাগ সেট করতে ব্যবহার করা যেতে পারে, প্রয়োজনে পূরণ করুন।

### তৃতীয় ধাপ: কথোপকথন রপ্তানি করুন

#### সম্পূর্ণ কথোপকথন রপ্তানি করুন

Cherry Studio-এর কথোপকথন ইন্টারফেসে ফিরে যান, কথোপকথনে রাইট-ক্লিক করুন, _রপ্তানি করুন_ নির্বাচন করুন, তারপর _Obsidian-এ রপ্তানি করুন_-এ ক্লিক করুন।

<figure><img src="../.gitbook/assets/image (138).png" alt=""><figcaption><p>সম্পূর্ণ কথোপকথন রপ্তানি করুন</p></figcaption></figure>

একটি উইন্ডো পপ আপ হবে যা Obsidian-এ রপ্তানি করা নোটের **প্রোপার্টিজ (Properties)** এবং রপ্তানির **প্রক্রিয়াকরণ পদ্ধতি** সামঞ্জস্য করতে সাহায্য করবে। নিম্নোক্ত তিনটি **প্রক্রিয়াকরণ পদ্ধতি** উপলব্ধ:

* **নতুন তৈরি করুন (যদি বিদ্যমান থাকে, তবে প্রতিস্থাপন করুন)**: [দ্বিতীয় ধাপে](obsidian.md#di-er-bu) উল্লেখিত `ফোল্ডার`-এ একটি নতুন কথোপকথন নোট তৈরি করুন
* **প্রিফিক্স (Prepend)**: বিদ্যমান একই নামের নোট থাকলে, নির্বাচিত কথোপকথন সামগ্রী নোটের শুরুতে যোগ করুন
* **অ্যাপেন্ড (Append)**: বিদ্যমান একই নামের নোট থাকলে, নির্বাচিত কথোপকথন সামগ্রী নোটের শেষে যোগ করুন

<figure><img src="../.gitbook/assets/image (137).png" alt=""><figcaption><p>নোট প্রোপার্টিজ কনফিগার করুন</p></figcaption></figure>

{% hint style="info" %}
শুধুমাত্র প্রথম পদ্ধতিতে প্রোপার্টিজ (Properties) সংযুক্ত থাকে, পরবর্তী দুটি পদ্ধতিতে প্রোপার্টিজ থাকে না।
{% endhint %}

#### একক বার্তা রপ্তানি করুন

একক বার্তা রপ্তানি করতে, বার্তার নিচের _থ্রি-লাইন মেনু_ ক্লিক করুন, _রপ্তানি করুন_ নির্বাচন করুন, তারপর _Obsidian-এ রপ্তানি করুন_-এ ক্লিক করুন।

<figure><img src="../.gitbook/assets/image (141).png" alt=""><figcaption><p>একক বার্তা রপ্তানি করুন</p></figcaption></figure>

এরপর সম্পূর্ণ কথোপকথন রপ্তানির মতো একই উইন্ডো পপ আপ হবে, যেখানে আপনাকে **নোট প্রোপার্টিজ** এবং **নোট প্রক্রিয়াকরণ পদ্ধতি** কনফিগার করতে হবে। [উপরের টিউটোরিয়ালে](obsidian.md#dao-chu-wan-zheng-dui-hua) উল্লেখিত ধাপগুলি অনুসরণ করে সম্পূর্ণ করুন।

### সফলভাবে রপ্তানি সম্পন্ন

🎉 এই পর্যায়ে, আপনি Cherry Studio-কে Obsidian-এর সাথে সংযুক্ত করার সমস্ত কনফিগারেশন সম্পূর্ণ করেছেন এবং সম্পূর্ণ রপ্তানি প্রক্রিয়া সফলভাবে সম্পন্ন করেছেন, উপভোগ করুন!

<figure><img src="../.gitbook/assets/image (140).png" alt=""><figcaption><p>Obsidian-এ রপ্তানি করুন</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (139).png" alt=""><figcaption><p>রপ্তানি ফলাফল পরীক্ষা করুন</p></figcaption></figure>