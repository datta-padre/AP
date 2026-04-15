"# AP" 
### Activity लाइफसायकल

**1. Android Activity लाइफसायकलची विविध स्टेज कोणती आहेत?**
- उत्तर: onCreate(), onStart(), onResume(), onPause(), onStop(), onRestart(), onDestroy()

**2. onCreate() कधी कॉल होतो आणि का?**
- उत्तर: जेव्हा Activity प्रथम तयार होते तेव्हा कॉल होतो; इनिशियलाइজेशनसाठी वापरतात

**3. onPause() आणि onStop() मध्ये काय फरक आहे?**
- उत्तर: onPause() - Activity फोकस गमावते (आंशिक दृश्यमान), onStop() - Activity पूर्णपणे लपलेली असते

**4. onDestroy() ओव्हरराइड का करतो?**
- उत्तर: संसाधने मुक्त करण्यासाठी आणि Activity नष्ट होण्यापूर्वी क्लीनअप करण्यासाठी

**5. onStart() आणि onResume() मध्ये काय फरक आहे?**
- उत्तर: onStart() - Activity दृश्यमान होते; onResume() - Activity इंटरॅक्टिव होते

**6. Activity लाइफसायकल मध्ये कुठे डेटा सेव करतात?**
- उत्तर: onSaveInstanceState() मध्ये Bundle वापरून

### Intent आणि डेटा पास करणे

**7. Android मध्ये Intent म्हणजे काय?**
- उत्तर: एक मेसेजिंग ऑब्जेक्ट जो दुसरे component ला कार्य करण्यासाठी विनंती करतो

**8. Activity मध्ये डेटा कसे पास करतात?**
- उत्तर: Intent सह putExtra() वापरून आणि getStringExtra() सह retrieve करून

**9. putExtra() आणि putExtras() मध्ये काय फरक आहे?**
- उत्तर: putExtra() - एकल key-value जोडी; putExtras() - Bundle सह अनेक मूल्य

**10. Intent द्वारे objects पास करू शकतात का?**
- उत्तर: हो, जर ते Parcelable किंवा Serializable implement करत असतील

**11. Implicit Intent आणि Explicit Intent मध्ये काय फरक आहे?**
- उत्तर: Explicit - विशिष्ट component; Implicit - कोणत्याही उपयुक्त component

**12. Implicit Intent कसे काम करते?**
- उत्तर: Action आणि data यांच्या आधारे Android सर्वोत्तम component शोधतो

### Fragments

**13. Fragment म्हणजे काय?**
- उत्तर: Activity मध्ये embed करता येणारा पुनः वापरण्यायोग्य UI component

**14. Fragment मध्ये डेटा कसे पास करतात?**
- उत्तर: Bundle आणि setArguments() पद्धत वापरून

**15. Fragment आणि Activity मध्ये काय फरक आहे?**
- उत्तर: Fragment स्वतंत्रपणे अस्तित्वात असू शकत नाही; Activity host आवश्यक आहे

**16. FragmentTransaction म्हणजे काय?**
- उत्तर: Fragments जोडणे, काढणे, बदलणे यासाठी वापरला जातो

**17. Fragment लाइफसायकल कोणती आहे?**
- उत्तर: onAttach(), onCreate(), onCreateView(), onStart(), onResume(), onPause(), onStop(), onDestroyView(), onDestroy()

---

## **असाईनमेंट 2 - UI Layouts आणि Designs**

### ConstraintLayout

**18. ConstraintLayout चे मुख्य फायदे काय आहेत?**
- उत्तर: लवचिक पोजिशनिंग, चांगली कार्यक्षमता, responsive design, सपाट hierarchy

**19. ConstraintLayout मध्ये constraints कसे लागू करतात?**
- उत्तर: top, bottom, start, end constraints वापरून views पोजिशन करतात

**20. Responsive layouts कसे तयार करतात?**
- उत्तर: ConstraintLayout मध्ये constraints आणि weights वापरून

**21. Chain constraints म्हणजे काय?**
- उत्तर: Views च्या समूहाचे एकसंध वितरण करण्यासाठी

### LinearLayout

**22. LinearLayout कसे काम करतो?**
- उत्तर: Views ला क्रमाने एका पंक्तीत किंवा स्तंभात व्यवस्थित करतो

**23. LinearLayout मध्ये weight कसे वापरतात?**
- उत्तर: layout_weight सह उपलब्ध जागेचे अनुपात निर्धारित करतात

### RelativeLayout

**24. RelativeLayout कसे views पोजिशन करतो?**
- उत्तर: इतर views च्या सापेक्ष पोजिशनवर आधारित (layout_above, layout_below, इ.)

**25. RelativeLayout आणि LinearLayout मध्ये काय फरक आहे?**
- उत्तर: RelativeLayout - सापेक्ष पोजिशनिंग; LinearLayout - क्रमिक एकक पंक्तीत/स्तंभात

### Portrait आणि Landscape

**26. Portrait आणि Landscape यासाठी वेगवेगळे layouts कसे बनवतात?**
- उत्तर: res/layout आणि res/layout-land directory मध्ये वेगवेगळी XML files बनवतात

**27. Device rotate झाल्यावर Activity शी काय होते?**
- उत्तर: Activity नष्ट आणि पुनः तयार होते; डेटा हरला जाते जर onSaveInstanceState() मध्ये सेव न केला

**28. Rotation यांत्रिकता कसे हाताळतात?**
- उत्तर: onSaveInstanceState() आणि onRestoreInstanceState() वापरून

### Spinners

**29. Spinner मध्ये डेटा कसे भरतात?**
- उत्तर: ArrayAdapter वापरून आणि setAdapter() कॉल करून

**30. Spinner selection हाताळणे कसे करतात?**
- उत्तर: OnItemSelectedListener interface implement करून

**31. Custom Spinner items कसे बनवतात?**
- उत्तर: Custom ArrayAdapter बनवून आणि getView() override करून

---

## **असाईनमेंट 3 - Widgets आणि Components**

### RadioButton आणि CheckBox

**32. RadioButton आणि CheckBox मध्ये काय फरक आहे?**
- उत्तर: RadioButton - एक निवड; CheckBox - अनेक निवड

**33. RadioGroup मधून selected RadioButton कसे मिळवतात?**
- उत्तर: getCheckedRadioButtonId() वापरून

**34. RadioGroup मध्ये एकाच वेळी एकच RadioButton का निवडलेला असतो?**
- उत्तर: RadioGroup मध्ये mutual exclusion logic आहे

### DatePicker आणि TimePicker

**35. DatePickerDialog कसे दाखवतात?**
- उत्तर: DatePickerDialog तयार करून आणि show() कॉल करून

**36. Date selection कसे हाताळतात?**
- उत्तर: DatePickerDialog.OnDateSetListener callback implement करून

**37. TimePicker वापरून time कसे मिळवतात?**
- उत्तर: TimePickerDialog.OnTimeSetListener callback implementation द्वारे

**38. Calendar class कसे वापरतात?**
- उत्तर: getInstance() सह current date/time मिळवतात

### ToggleButton

**39. ToggleButton आणि Switch मध्ये काय फरक आहे?**
- उत्तर: ToggleButton - ON/OFF text दाखवते; Switch - modern Material Design

**40. ToggleButton selection check कसे करतात?**
- उत्तर: isChecked() method वापरून

### HorizontalScrollView

**41. HorizontalScrollView आणि ScrollView मध्ये काय फरक आहे?**
- उत्तर: HorizontalScrollView - क्षैतिज स्क्रोलिंग; ScrollView - उर्ध्व स्क्रोलिंग

**42. HorizontalScrollView कधी वापरतात?**
- उत्तर: जेव्हा content पक्ष पुरेसे width ओव्हरफ्लो करते तेव्हा

---

## **असाईनमेंट 4 - Database आणि SQLite**

### Database मूलभूत गोष्टी

**43. SQLite म्हणजे काय आणि Android मध्ये का वापरतात?**
- उत्तर: हल्का relational database; Android मध्ये built-in; सर्व्हर आवश्यक नाही

**44. SQLiteOpenHelper म्हणजे काय?**
- उत्तर: Database access आणि management साठी abstract class

**45. onCreate() आणि onUpgrade() मध्ये काय फरक आहे?**
- उत्तर: onCreate() - tables तयार करतो; onUpgrade() - schema बदल हाताळतो

**46. getReadableDatabase() आणि getWritableDatabase() मध्ये काय फरक आहे?**
- उत्तर: getReadableDatabase() - read operations साठी; getWritableDatabase() - write साठी

### CRUD Operations

**47. Database मध्ये डेटा कसे insert करतात?**
- उत्तर: ContentValues वापरून आणि insert() method कॉल करून

**48. Database मधून डेटा कसे query करतात?**
- उत्तर: rawQuery() किंवा query() method वापरून, Cursor return होते

**49. डेटा update कसे करतात?**
- उत्तर: update() method आणि WHERE clause वापरून

**50. रेकॉर्ड delete कसे करतात?**
- उत्तर: delete() method आणि WHERE clause वापरून

**51. Cursor म्हणजे काय?**
- उत्तर: Query result set ला represent करणारा इंटरफेस

**52. Cursor iterate करण्याचे सही तरीका कोणता आहे?**
- उत्तर: moveToFirst() असा करून आणि moveToNext() सह loop लागवून

### Relationships

**53. Foreign Keys म्हणजे काय?**
- उत्तर: Tables मध्ये referential integrity maintain करणे

**54. One-to-Many relationship कसे define करतात?**
- उत्तर: Parent table ची primary key, Child table ची foreign key होते

**55. Many-to-Many relationship कसे implement करतात?**
- उत्तर: Junction table बनवून दोन्ही tables ली foreign keys add करून

**56. Foreign Key constraint enable कसे करतात?**
- उत्तर: setForeignKeyConstraintsEnabled(true) कॉल करून

### Queries

**57. SQLite मध्ये JOIN कसे करतात?**
- उत्तर: INNER JOIN, LEFT JOIN, इत्यादी वापरून

**58. Multiple tables मधून डेटा कसे fetch करतात?**
- उत्तर: rawQuery() मध्ये JOIN statement लिहून

**59. WHERE clause कसे लिहितात?**
- उत्तर: Parameterized queries वापरून (?), SQL injection टाळण्यासाठी

**60. ORDER BY आणि GROUP BY कसे वापरतात?**
- उत्तर: Sorting आणि grouping साठी

---

## **Advanced Concepts**

### Input Validation

**61. Form inputs validate कसे करतात?**
- उत्तर: isEmpty check, email format, length requirements

**62. Validation errors कसे दाखवतात?**
- उत्तर: EditText वर setError() किंवा Toast message वापरून

**63. TextUtils.isEmpty() काय करते?**
- उत्तर: Text null किंवा empty आहे का हे check करतो

**64. Email validation कसे करतात?**
- उत्तर: Patterns.EMAIL_ADDRESS.matcher() वापरून

### Dialogs आणि Fragments

**65. AlertDialog कसे create करतात?**
- उत्तर: AlertDialog.Builder वापरून setTitle(), setMessage(), buttons add करून

**66. DialogFragment म्हणजे काय?**
- उत्तर: Dialog साठी Fragment subclass

**67. Dialog वर buttons कसे add करतात?**
- उत्तर: setPositiveButton(), setNegativeButton(), setNeutralButton() वापरून

### SharedPreferences

**68. SharedPreferences कधी वापरतात?**
- उत्तर: छोटी key-value data स्थायीपणे store करण्यासाठी

**69. SharedPreferences मध्ये डेटा कसे store करतात?**
- उत्तर: getSharedPreferences().edit().putString().apply()

**70. SharedPreferences मधून डेटा कसे retrieve करतात?**
- उत्तर: getSharedPreferences().getString(key, defaultValue)

---

## **Practical Scenario Questions**

**71. Activity rotation यांत्रिकता काय आहे?**
- उत्तर: Configuration change - Activity destroy आणि recreate होते

**72. Activity rotation मध्ये डेटा loss कसे रोखतात?**
- उत्तर: onSaveInstanceState() override करून Bundle मध्ये save करून

**73. Database operations main thread मध्ये का करू नये?**
- उत्तर: UI freeze होते; background thread वापरावा

**74. Permissions Android मध्ये कसे हाताळतात?**
- उत्तर: Runtime permissions request करावे (API 23+)

**75. Fragment onCreateView() मध्ये काय करतात?**
- उत्तर: UI create करतात आणि View return करतात

**76. Database performance कसे optimize करतात?**
- उत्तर: Indexes, proper queries, cursor close, batch operations

**77. rawQuery() आणि query() मध्ये काय फरक आहे?**
- उत्तर: rawQuery() - direct SQL; query() - parameterized (safer)

**78. Cursor leak मुळे काय समस्या होते?**
- उत्तर: Memory leak; हमेशा cursor close करावा

**79. Database transactions कधी वापरतात?**
- उत्तर: एकाधिक operations एकसाथी atomic करायचे असतील तेव्हा

**80. App मधील database file कुठे store होते?**
- उत्तर: /data/data/package_name/databases/ directory मध्ये

---

## **Layout आणि UI Related**

**81. Padding आणि Margin मध्ये काय फरक आहे?**
- उत्तर: Padding - content आणि border मध्ये; Margin - border आणि बाहेर

**82. dp, sp, px मध्ये काय फरक आहे?**
- उत्तर: dp - density-independent; sp - scale-independent; px - pixels

**83. layout_weight कसे काम करते?**
- उत्तर: उपलब्ध space हे weight अनुपातात विभाजित करतो

**84. Gravity आणि layout_gravity मध्ये काय फरक आहे?**
- उत्तर: gravity - content inside view; layout_gravity - view inside parent

**85. View visibility states कोणती आहेत?**
- उत्तर: VISIBLE, INVISIBLE, GONE

---

## **Program Related**

**86. Simple Calculator कसे काम करते?**
- उत्तर: Button clicks वर input store करता आणि evaluate() method evaluate करते

**87. Expression evaluate कसे करतात?**
- उत्तर: Operator precedence - multiplication/division पहिले, नंतर addition/subtraction

**88. Implicit evaluation कोण करतो?**
- उत्तर: Parser - parseExpression(), parseTerm(), parseFactor()

**89. Student information application मध्ये कोणते operations आहेत?**
- उत्तर: Add student, Delete student, Display all students

**90. Gallery application कसे बनवतात?**
- उत्तर: GridView वापरून, ImageAdapter बनवून, external storage permissions घेऊन

---

## **Best Practices**

**91. Android development मधील best practices कोणती आहेत?**
- उत्तर: Proper lifecycle handling, background threads, memory management, security

**92. Code organization कसे करावो?**
- उत्तर: Packages द्वारा - models, views, activities, database, utils

**93. Error handling कसे करावो?**
- उत्तर: Try-catch blocks, proper logging, user-friendly messages

**94. Memory leaks कसे रोखतात?**
- उत्तर: Resources properly close करून, listeners unregister करून

**95. Security related काय सावधानी घेतल्या पाहिजेत?**
- उत्तर: SQL injection रोखण्यासाठी parameterized queries, sensitive data encrypt करणे

---

**Note:** प्रत्येक प्रश्नाचे उत्तर comprehensive आहे आणि परीक्षकाला समाधानकारक असावे.