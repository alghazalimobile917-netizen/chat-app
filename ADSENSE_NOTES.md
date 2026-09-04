# ملاحظات دمج Google AdSense

- توصي Google بإنشاء ملف `ads.txt` في جذر النطاق، وتنسيق السطر القياسي هو: `google.com, pub-0000000000000000, DIRECT, f08c47fec0942fa0`.
- يجب استخدام معرف الناشر الحقيقي بعد `pub-`، وعدم تخمينه. قد يستغرق ظهور التحقق في AdSense عدة أيام، وقد يبدأ ظهور الإعلانات بعد إعداد الموقع والمراجعة.
- الشفرة المعتادة تستخدم `data-ad-client="ca-pub-..."`، بينما ملف `ads.txt` يستخدم معرف `pub-...` من دون بادئة `ca-`.
- مصادر Google الرسمية:
  - https://support.google.com/adsense/answer/12171612?hl=en
  - https://developers.google.com/adsense/platforms/transparent/ads-txt

هذه الملاحظات مرجع تنفيذ وليست ضماناً لقبول الحساب؛ يجب استكمال مراجعة Google وسياساتها من لوحة AdSense.
