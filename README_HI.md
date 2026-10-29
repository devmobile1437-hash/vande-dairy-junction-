# Vande Dairy Junction — Flutter Android Starter

यह Flutter source project है, तैयार APK नहीं। इसमें local demo screens और sample data हैं।

## शामिल स्क्रीन
- Demo login: Admin / Salesman / Retailer role selector
- Dashboard और expiry watch
- Product & batch stock entry (batch number + expiry date)
- Order booking और demo stock deduction
- Retailer master
- Cash / UPI demo collection ledger

## चलाने के लिए
1. Computer पर Flutter SDK और Android Studio install करें।
2. इस project folder को extract करें।
3. Terminal में project folder खोलकर चलाएँ:
   ```bash
   flutter pub get
   flutter run
   ```
4. APK build करने के लिए:
   ```bash
   flutter build apk --release
   ```
   APK सामान्यतः `build/app/outputs/flutter-apk/app-release.apk` में बनेगा।

## जरूरी सीमाएँ
- अभी कोई वास्तविक login/authentication नहीं है; role selector केवल demo है।
- डेटा app बंद करने या app reinstall करने पर सुरक्षित नहीं रहता।
- Firebase/Supabase connection अभी configure नहीं है।
- Cash/UPI entry सिर्फ demo record है; payment process नहीं होता।
- Production में उपयोग से पहले role-aware database security, trusted server-side order/stock transactions, invoice numbering, backups, audit log और tests जोड़ना जरूरी है।
- SQL starter schema `supabase/vande_dairy_junction_mvp_schema.sql` में है। उसे नई Supabase project में लागू करने से पहले policies की समीक्षा करें।
- Android ऐप में कभी भी Supabase service-role key शामिल न करें।
