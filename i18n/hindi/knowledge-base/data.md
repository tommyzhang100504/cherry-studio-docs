---
icon: database
---

{% hint style="warning" %}
यह दस्तावेज़ AI द्वारा चीनी से अनुवादित किया गया है और अभी तक इसकी समीक्षा नहीं की गई है।
{% endhint %}

# डेटा संग्रहण स्पष्टीकरण

Cherry Studio ज्ञान भंडार में जोड़ा गया डेटा पूरी तरह से स्थानीय रूप से संग्रहीत होता है। जोड़ने की प्रक्रिया में, एक दस्तावेज़ की प्रति Cherry Studio डेटा संग्रहण निर्देशिका में रखी जाती है।

<figure><img src="../.gitbook/assets/mermaid-diagram-1739241680067.png" alt=""><figcaption><p>ज्ञान भंडार प्रसंस्करण प्रवाह चार्ट</p></figcaption></figure>

वेक्टर डेटाबेस: [https://turso.tech/libsql](https://turso.tech/libsql)

जब कोई दस्तावेज़ Cherry Studio ज्ञान भंडार में जोड़ा जाता है, तो फ़ाइल को कई खंडों में विभाजित किया जाता है। फिर ये खंड एम्बेडिंग मॉडल को प्रसंस्करण के लिए सौंपे जाते हैं।

जब बड़े मॉडल का उपयोग करके प्रश्नोत्तर किया जाता है, तो प्रश्न से संबंधित पाठ खंडों को खोजा जाता है और एक बड़े भाषा मॉडल को प्रसंस्करण के लिए सौंपा जाता है।

यदि आपको डेटा गोपनीयता की आवश्यकता है, तो स्थानीय एम्बेडिंग डेटाबेस और स्थानीय बड़े भाषा मॉडल का उपयोग करने की सिफारिश की जाती है।