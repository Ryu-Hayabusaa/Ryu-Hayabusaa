correct_pin="mon"
def check_pin():
    user_pin=input("أدخل الرقم السري لفتح الباب: ")
    if user_pin==correct_pin:
        print("\n✅ تم فتح الباب! مرحبًا!\n")
    else:
        print("\n❌ الرقم السري خاطئ! الرجاء المحاولة مرة أخرى.\n")
while True:
    print("--- قائمة التحكم ---")
    print("1. فتح الباب")
    print("2. تغيير الرقم السري")
    print("3. خروج")
    choice=input("اختر الخيار: ")
    if choice=="1":
        check_pin()
    elif choice=="2":
        old_pin=input("أدخل الرقم السري الحالي لتغييره: ")
        if old_pin==correct_pin:
            new_pin=input("أدخل الرقم السري الجديد: ")
            confirm_pin=input("أعد إدخال الرقم السري الجديد للتأكيد: ")
            if new_pin==confirm_pin:
                correct_pin=new_pin
                print("\n✅ تم تغيير الرقم السري بنجاح!\n")
            else:
                print("\n❌ الرقم السري الجديد لا يطابق التأكيد.\n")
        else:
            print("\n❌ الرقم السري الحالي غير صحيح.\n")
    elif choice=="3":
        print("\n👋 وداعًا!\n")
        break
    else:
        print("\n❌ خيار غير صحيح. حاول مرة أخرى.\n")

