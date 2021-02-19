# NourGUI
GUI version of Nour 

![GPL3v](https://github.com/khalidt/NourGUI/blob/main/NourGUI.png)

# Description
 🐋 **Nour** is an Arabic Braille tool that converts Arabic words, letters, or sentences to and from  Braille notations.
Nour has used the unified braille standard for Arabic that was developed at a conference in Saudi Arabia in 2002. However, some other Arab countries in 2013 do not sign it up thus they use a different standard of braille notation which will be added in the next version of Nour. based on [the world Braille usage](https://unesdoc.unesco.org/ark:/48223/pf0000087242) we added the unified braille standard for Arabic and we will add other Arab countries standards.

# الوصف:
برنامج نور هو عبارة عن اداة لتحويل الحروف والجمل والنصوص العربية من والى لغة بريل العربية. تم استخدام الرموز الموحد القياسي من بريل العربية والتي تم تطويرها واعتمادها من قبل الموتمر المنعقد في المملكة العربية السعودية عام ٢٠٠٢. الا انه في عام ٢٠١٣ لم يتم اعتماد هذا الترميز من حروف بريل العربية عند بعض الدول العربية مثل الجزائر وغيرها فقد استخدموا ترميز مختلف لحروف بريل العربية.
يستخدم تطبيق في نسخة الاولى على الترميز الموحد والذي تم اعتمادة عام ٢٠٠٢ ، يمكنك مراجعة [ملف استخدام بريل العالمي](https://unesdoc.unesco.org/ark:/48223/pf0000087242) ، وسوف يتم إضافة بقية الترميز العربي المختلف في النسخ القادمة باذن الله
# Sample:

#### From inside python shell:
```python
>>> from Nour import nour
>>> nour.arabicToBraille('بسم الله الرحمن الرحيم')
⠃⠎⠍⠀⠁⠇⠇⠓⠀⠁⠇⠗⠱⠍⠝⠀⠁⠇⠗⠱⠊⠍
>>> nour.brailleToArabic('⠍⠗⠱⠃⠁')
مرحبا
>>> nour.util.brailles
['⠀', '\n', '⠁', '⠃', '⠞', '⠹', '⠚', '⠱', '⠭', '⠙', '⠮', '⠗', '⠵', '⠎', 
  '⠩', '⠯', '⠫', '⠾', '⠿', '⠷', '⠣', '⠋', '⠟', '⠅', '⠇', '⠍', '⠝', '⠓', 
  '⠡', '⠺', '⠊', '⠕', '⠉', '⠧', '⠴⠠', '⠌', '⠨', '⠜', '⠪', '⠳', '⠽', '⠄', 
  '⠥', '⠂', '⠆', '⠑', '⠔', '⠢', '⠒', '⠠', '⠐', '⠰', '⠐⠂', '⠶', '⠦…', '…⠴', 
  '⠠⠦', '⠐⠦', '⠴⠂', '⠲', '⠖', '⠦', '⠤', '⠼⠁', '⠼⠃', '⠼⠉',
  '⠼⠙', '⠼⠑', '⠼⠋', '⠼⠛', '⠼⠓', '⠼⠊', '⠼⠚', '⠒⠏']

>>> nour.util.arabic
[' ', '\n', 'ا', 'ب', 'ت', 'ث', 'ج', 'ح', 'خ', 'د', 'ذ', 'ر', 'ز', 'س', 
  'ش', 'ص', 'ض', 'ط', 'ظ', 'ع', 'غ', 'ف', 'ق', 'ك', 'ل', 'م', 'ن', 'ه', 'ة', 
  'و', 'ي', 'ى', 'ال', 'لا', ']', 'أ', 'إ', 'آ', 'أو', 'ؤ', 'ئ', 'ء', 'ُ', 
  'َ', 'ً', 'ِ', 'ٍ', 'ٌ', 'ْ', 'ّ', '،', '؛', ':', '"', '(', ')', '[', '{', 
  '}', '.', '!', '؟', '-', '١', '٢', '٣', '٤', '٥', '٦', '٧', '٨', '٩', '٠', 
  '٪']
```




#### From CLI:
```bash
python nour -br ⠞
```
output:
```
ت
```
#### From Virtualenv:
```bash
python -m Nour.nour -h
```

#  Requirements | المتطلبات
* Python3 >=3.6 


# Installation: التثبيت

* ### Install from pip: 
  Use the package manager [pip](https://pypi.org/project/Nour/) to install Nour.
 
  يمكن تثبيت البرنامج من خلال مدير الحزم عن طريق كتابة الامر التالي: 

```bash
pip install Nour
```

# Usage: الاستخدام
```bash
usage: Nour [-h] [-ar ARTEXT] [-br BRTEXT] [-arf ARFILE]           
            [-brf BRFILE] [-o] [-p] [-info]                        
                                                                   
optional arguments:                                                
  -h, --help            show this help message and exit            
  -ar ARTEXT, --artext ARTEXT                                      
                        The Arabic text to be converted to         
                        Braille.                                   
  -br BRTEXT, --brtext BRTEXT                                      
                        The Braille text to be converted to        
                        Arabic.                                    
  -arf ARFILE, --arfile ARFILE                                     
                        The Arabic text file to be converted to    
                        Braille.                                   
  -brf BRFILE, --brfile BRFILE                                     
                        The Braille text file to be converted to   
                        Arabic.                                    
  -o, --out             Write Conversion to file                   
  -p, --print           Print Standard Arabic Braille Code.        
  -info, --info         Print Information about Nour.              
                                                                   
Examples:                                                          
Nour -p                                                            
Nour -ar مرحبا                                                     
Nour -ar arabicTextFile.txt                                        
Nour -arf readFromtext.txt -o                                      
Nour -br ⠓                                                         
Nour -brf brailleTextFile.txt                                      
Nour -arf ArTextFile.txt -abf BrTextFile.txt        
```

# Notes:
* The character that is not in the standard of Arabic Braille code, will be ignored and replaced by space '  '. for **Example:** ~ , ^ , ' , & , /
* Arithmetic and Logic operators are not supported yet.
* Both the Arabic numerals (1,2,3 ...etc) and Eastern Arabic numerals (Hindi)  (١,٢,٣ ... etc) are used by the same Arabic Braille code.
* Underline is not tested but it's included! 
* When using the argument of output file ' **-o** ' it creates a file and writes the conversion to it, the generated file will be named by default as **'Nour %d-%m-%y %H-%M'.txt**. Ex: **Nour 02-10-2020 08-12.txt**.
* The only file that is supported for reading and writing is text **.txt**




# ملاحظات:
* الرموز والعلامات التي ليست مدرجة في الترميز القياسي  لحروف بريل العربية سوف يتم تجاهلها واستبدالها بمسافة فارغة. على سبيل المثال الرموز التالية: ~ , ^ , ' , & , /
* العلامات الرياضية والمنطقية ليست مدعمة
* يتم التعامل مع الارقام العربية والهندية سواء اي ان الرقم العربي او الهندي له نفس الترميز في بريل العربي
* تم ادراج ترميز الحرف العربي اذا كان تحته خط ولكن لم يتم اختبارة بعد.
* عندما يتم استخدام تطبيق نور من خلال شاشة الاوامر وليس الواجهة الرسومية يمكن استخدام المعامل استخراج عملية التحويل وحفظها في ملف يتم تسمية تلقائي باسم: 'Nour %d-%m-%y %H-%M'.txt. مثال: Nour 02-10-2020 08-12.txt.
* الملف الوحيد الذي يدعمة برنامج نور من نوع نص بامتداد txt

# Roadmap:
* Add other Arab countries braille standards  
* Import different files to read from and write to such as:
   - **.docx , .doc, .rtf, .pdf, .html, .odt, xml** and more.
* New feature will be added which is converting the Arabic alphabets in images and extract them to the document file.
* Add mechanism to deal with shapes, Maps ... etc.
* Add Math translation for **Nemeth** and more.

# خارطة الطريق :
* اضافة ودعم بقية ترميز بريل العربية لبقية الدول التي لها ترميز مختلف عن الترميز القياسي
* دعم ملفات مختلفة ليتم قراءة النص منها او الكتابة فيها مثل:
   - **.docx , .doc, .rtf, .pdf, .html, .odt, xml**
* اضافة خاصية استخراج النص من الصور او ملفات بي دي اف ثم تحويلها الى مستند بريل
* اضافة طرق للتعامل مع الاشكال والخرائط
* اضافة خاصية للتعامل مع الرموز الرياضية والمعادلات وترجمتها من خلال نظام Nemeth

# License


[![GPL3v](https://www.gnu.org/graphics/gplv3-127x51.png)](https://www.gnu.org/licenses/gpl-3.0.html)


    Nour is a tool which translates Arabic words, letters 
    or sentences to and from  Braille notations.
    Copyright (C) 2020  Khalid Alkhaldi

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, version 3.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.
