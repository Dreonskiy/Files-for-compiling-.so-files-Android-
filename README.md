[Russian Version: ]

[Инструкция]

1) Создайте в любом диске папку jni.

2) Когда скачали 2 файла, обязательно перекидывайте в папку JNI.

3) Чтобы изменить название компилируемово файла. Например: libname.so. 

Заходим сначало в Android.mk а потом находим строчку LOCAL_MODULE. Где будет слово name изменяйте на своё. Заходим в Applicatio.mk. Внутри этого файла будет строчка APP_MODULES. В нём будет слово name. Вы должны заменить на своё название. 

[Диалог]

A: А как сделать так, чтобы компилятор мог скомпилировать те файлы, который я вставил в свой проект.
B: Заходим в Android.mk. Ищем раздел FILE_LIST. Если непонятно то вот оригинальная строчка:  FILE_LIST := $(wildcard $(LOCAL_PATH)/*.cpp).

Если хотите, чтобы он скомпилировал файлы, которые находятся в папке, то делайте следующее. Заходите в Android.mk и ищите строчку:

FILE_LIST := $(wildcard $(LOCAL_PATH)/test/*.cpp)

Где test - это название папки!

Команды для компиляции своего проекта в папке JNI

1) win + r (Пишите cmd)
2) cd C:\ndk
3) ndk-build -C C:\jni

[English Version: ]

[Instructions]

1) Create a jni folder on any disk.

2) When you have downloaded 2 files, be sure to transfer them to the JNI folder.

3) To change the name of the compiled file. For example: libname.so . 

We go first to Android.mk and then we find the line LOCAL_MODULE. Where the word name will be, change it to your own. We go to Applicatio.mk . Inside this file there will be a line APP_MODULES. It will contain the word name. You should replace it with your name. 

[Dialog]

A: And how to make it so that the compiler can compile the files that I inserted into my project.
B: We go to Android.mk . Looking for the FILE_LIST section. If it is not clear, then here is the original line: FILE_LIST := $(wildcard $(LOCAL_PATH)/*.cpp).

If you want it to compile the files that are in the folder, then do the following. Go to Android.mk and look for the line:

FILE_LIST := $(wildcard $(LOCAL_PATH)/test/*.cpp)

Where test is the folder name!

Commands to compile your project in the JNI folder

1) win + r (Write cmd)
2) cd C:\ndk
3) ndk-build -C C:\jni
