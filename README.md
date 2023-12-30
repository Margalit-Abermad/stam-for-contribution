# stam-for-contribution
For him to inform me of a donation

# first day
# second day
# third day
# more mjkjkjre 😎😎😎😎
😎😎😎
# the summer vication is here djnjdnjdddddsfkfkddddbnbfkffmfksmdjhjhjmffmfmhyy
# ff 👈💪💪🎤😊😵🤪 kfhdjrdfdfdh
- [ ] \(Optional) Open a followup issue













## תוכנה לזיהוי פנים ופתיחת דלת במצלמת אינטרקום Hikvision

<br/>
#### התכנה מתחברת למצלמת אינטרקום DS-KD8003 של Hikvision.
## מהלך התוכנה-
## פרוט קובץ sql_adapter:
##### קובץ sql_adapter אחראי על הלוגיקה של sql, פונקציות CRUD בסיסיות ונוסםות.
##### החלוקה בקובץ מתבצעת  

1. לפי טבלאות- לכל טבלה של sql קיים region שבו יש 4 פונקציות בסיסיות (CREATE,READ,UPDATE,DALETE).
2. פונקציות שליפה / עדכון נוספות שנצרכות קיימות גם כן לכל טבלה לפי הצורך.
3. לכל פונקציה חתימת פונקציה מתאימה + פרוט פעילות הפונקציה.
   <br/>
## פרוט קובץ encoding_folder_images
#### הקובץ מבצע בפועל את פעולת הקידוד לתמונות חדשות למאגר התמונות המורשות.
##### בקובץ מוקצה משתנה קבוע בשם faces_folder_path, המשתנה מכיל את ניתוב תיקיית התמונות במחשב,
##### פונקציה encoding_authorized_faces מקבלת את ניתוב תיקיית התמונות, עוברת על התמונות שבתיקיה ויוצרת קידוד לפנים
##### שם התמונה צריך להיות שם פרטי_שם משפחה - הפונקציה חותכת את שם התמונה ומחלקת אותו לשם פרטי ושם משפחה לפי המקף התחתון, ומתאימה את השם לקידוד של התמונה הנוכחית.

 <br/>
 
        person_name_parts = os.path.splitext(file_name)[0].split('_')
        if len(person_name_parts) == 2:
            first_name, last_name = person_name_parts
        else:
            first_name, last_name = '', ''
 <br/>
 
###### כרגע- במידה ואין שם לתמונה יכנס שם פרטי ומשפחה ריק. 
##### משתנה PERSON_FACE_ENCODING ב- SQL הוא מסוג nvarchar כי הוא מספרי אבל לא מספר שלם אלא קבוצות של מספרים, לכן גם בפיתון עשיתי convert לפורמט של סטרינג-
 <br/>

       face_encoding_str = ' '.join(map(str, face_encoding))



