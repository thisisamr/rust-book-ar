# The Rust Programming Language

[لغة البرمجة Rust](title-page.md)
[تمهيد](foreword.md)
[مقدمة](ch00-00-introduction.md)

## Getting started

- [البداية](ch01-00-getting-started.md)

  - [التنصيب](ch01-01-installation.md)
  - [اهلا بالعالم !](ch01-02-hello-world.md)
  - [اهلا cargo !](ch01-03-hello-cargo.md)

- [برمجة لعبة تخمين](ch02-00-guessing-game-tutorial.md)

- [مفاهيم برمجية مشتركة](ch03-00-common-programming-concepts.md)

  - [المتغيرات و التغيرية](ch03-01-variables-and-mutability.md)
  - [انواع البيانات](ch03-02-data-types.md)
  - [الدوال](ch03-03-how-functions-work.md)
  - [التعليقات](ch03-04-comments.md)
  - [تسلسل التنفيذ](ch03-05-control-flow.md)

- [فهم الملكية](ch04-00-understanding-ownership.md)

  - [ما هي الملكية ؟](ch04-01-what-is-ownership.md)
  - [المراجع و الاستعارة](ch04-02-references-and-borrowing.md)
  - [نوع الشريحة](ch04-03-slices.md)

- [استخدام التراكيب لتنظيم البيانات المترابطة](ch05-00-structs.md)

  - [تعريف وتهيئة التراكيب](ch05-01-defining-structs.md)
  - [مثال علي برنامج يستخدم التراكيب](ch05-02-example-structs.md)
  - [صياغة الدالة التابعة](ch05-03-method-syntax.md)

- [التعدادات و مطابقة الانماط](ch06-00-enums.md)
  - [تعريف التعداد](ch06-01-defining-an-enum.md)
  - [تسلسل التنفيذ باستخدام تعبير `match`](ch06-02-match.md)
  - [تسلسل تنفيذ مختصر باستخدام `if let`](ch06-03-if-let.md)

## Basic Rust Literacy

- [إدارة المشاريع الكبيرة باستخدام الحزم، والصناديق، والوحدات](ch07-00-managing-growing-projects-with-packages-crates-and-modules.md)

  - [الحزم والصناديق](ch07-01-packages-and-crates.md)
  - [تعريف الوحدات للتحكم في النطاق والخصوصية](ch07-02-defining-modules-to-control-scope-and-privacy.md)
  - [ المسارات للإشارة إلى عنصر في شجرة الوحدة](ch07-03-paths-for-referring-to-an-item-in-the-module-tree.md)
  - [إدخال المسارات في النطاق باستخدام الكلمة الرئيسية `use`](ch07-04-bringing-paths-into-scope-with-the-use-keyword.md)
  - [فصل الوحدات إلى ملفات مختلفة](ch07-05-separating-modules-into-different-files.md)

- [التجميعات الشائعة](ch08-00-common-collections.md)

  - [تخزين قوائم القيم باستخدام المتجهات](ch08-01-vectors.md)
  - [تخزين النصوص المشفرة بتنسيق UTF-8 باستخدام السلاسل النصية](ch08-02-strings.md)
  - [تخزين المفاتيح مع القيم المرتبطة في جداول التجزئة](ch08-03-hash-maps.md)

- [معالجة الاخطاء](ch09-00-error-handling.md)

  - [الاخطاء الغير قابلة للحل باستخدام الماكرو panic!](ch09-01-unrecoverable-errors-with-panic.md)
  - [الاخطاء القابلة للحل باستخدام `Result`](ch09-02-recoverable-errors-with-result.md)
  - [هل يجب استخدام panic! أم لا](ch09-03-to-panic-or-not-to-panic.md)

- [الانواع المعممة,السمات, ودورات الحياة](ch10-00-generics.md)

  - [الانواع المعممة](ch10-01-syntax.md)
  - [السمات:لتعريف سلوك مشترك](ch10-02-traits.md)
  - [التحقق من المراجع باستخدام دورات الحياة](ch10-03-lifetime-syntax.md)

- [كتابة الاختبارات اﻵلية](ch11-00-testing.md)

  - [كيفية كتابة الاختبارات](ch11-01-writing-tests.md)
  - [التحكم في كيفية تشغيل الاختبارات](ch11-02-running-tests.md)
  - [تنظيم الاختبارات](ch11-03-test-organization.md)

- [مشروع الإدخال/الإخراج: بناء برنامج سطر الأوامر](ch12-00-an-io-project.md)
  - [الحصول علي العوامل من سطر الاوامر](ch12-01-accepting-command-line-arguments.md)
  - [قراءة ملف](ch12-02-reading-a-file.md)
  - [اعادة هيكلة الكود لتحسين النمطية و معالجة اﻷخطاء](ch12-03-improving-error-handling-and-modularity.md)
  - [تطوير عمل المكتبة باستخدام التطوير المقتاد بالاختبار](ch12-04-testing-the-librarys-functionality.md)
  - [العمل مع متغيرات البيئة](ch12-05-working-with-environment-variables.md)
  - [كتابة رسائل الخطأ إلى الخطأ القياسي بدلاً من الإخراج القياسي](ch12-06-writing-to-stderr-instead-of-stdout.md)

## التفكير بلغة Rust

- [ميزات لغة البرمجة الوظيفية: الإغلاقات والمكررات](ch13-00-functional-features.md)

  - [الإغلاقات: الدوال المجهولة التي تلتقط بيئتها](ch13-01-closures.md)
  - [معالجة سلسلة من العناصر باستخدام المكررات](ch13-02-iterators.md)
  - [تحسين مشروع الإدخال/الإخراج الخاص بنا](ch13-03-improving-our-io-project.md)
  - [مقارنة الأداء: الحلقات مقابل المكررات](ch13-04-performance.md)

- [المزيد حول Cargo و Crates.io](ch14-00-more-about-cargo.md)

  - [تخصيص البُنيات باستخدام ملفات الإصدار في Rust](ch14-01-release-profiles.md)
  - [نشر صندوق إلى Crates.io](ch14-02-publishing-to-crates-io.md)
  - [مساحة عمل Cargo](ch14-03-cargo-workspaces.md)
  - [تثبيت الملفات التنفيذية الثنائية من Crates.io باستخدام `cargo install`](ch14-04-installing-binaries.md)
  - [توسيع استخدامات Cargo عن طريق اوامر مخصصة](ch14-05-extending-cargo.md)

- [المؤشرات الذكية](ch15-00-smart-pointers.md)

  - [استخدام`Box<T>&lrm;` للإشارة إلى البيانات في الكومة](ch15-01-box.md)
  - [معاملة المؤشرات الذكية مثل المراجع العادية باستخدام خاصية `Deref`](ch15-02-deref.md)
  - [تنفيذ كود عند تحرير الذاكرة cleanup باستخدام السمة `Drop`](ch15-03-drop.md)
  - [ المؤشر `Rc<T>&lrm;` الذكي واستخدامه للاشارة إلي عدد المراجع](ch15-04-rc.md)
  - [`RefCell<T>&lrm;` و نمط التغيير الداخلي](ch15-05-interior-mutability.md)
  - [حلقات المراجع قد تؤدي الي تسريب الذاكرة](ch15-06-reference-cycles.md)

- [التواقت بلا خوف](ch16-00-concurrency.md)

  - [استخدام الخيوط لتشغيل الكود بطريقة متزامنة](ch16-01-threads.md)
  - [استخدام تمرير الرسائل لنقل البيانات بين الخيوط](ch16-02-message-passing.md)
  - [تواقت الحالة المشتركة](ch16-03-shared-state.md)
  - [التواقت القابل للتوسعة باستخدام خصائص `Sync` و `Send`](ch16-04-extensible-concurrency-sync-and-send.md)

- [ميزات البرمجة الكائنية في Rust](ch17-00-oop.md)
  - [خصائص اللغات الكائنية](ch17-01-what-is-oo.md)
  - [استخدام كائنات السمات التي تسمح بقيم من أنواع مختلفة](ch17-02-trait-objects.md)
  - [تنفيذ نمط تصميمي كائن التوجه](ch17-03-oo-design-patterns.md)

## مواضيع متقدمة

- [الأنماط والمطابقة](ch18-00-patterns.md)

  - [جميع الأماكن التي يمكن استخدام الأنماط فيها](ch18-01-all-the-places-for-patterns.md)
  - [إمكانية الفشل في المطابقة: ما إذا كان النمط قد يفشل في المطابقة](ch18-02-refutability.md)
  - [بنية الأنماط](ch18-03-pattern-syntax.md)

- [ميزات متقدمة](ch19-00-advanced-features.md)
  Macros

  - [Rust غير اﻵمنة](ch19-01-unsafe-rust.md)
  - [السمات المتقدمة](ch19-03-advanced-traits.md)
  - [انواع متقدمة](ch19-04-advanced-types.md)
  - [الدوال و المغلفات المتقدمة](ch19-05-advanced-functions-and-closures.md)
  - [الماكروز](ch19-06-macros.md)

- [المشروع الخير: بناء خادم ويب متعددالخيوط](ch20-00-final-project-a-web-server.md)

  - [بناء خادم ويب احادي الخيط](ch20-01-single-threaded.md)
  - [تحويل الخادم الاحادي الي خادم متعدد الخيوط](ch20-02-multithreaded.md)
  - [الاغلاق الناعم والتنظيف](ch20-03-graceful-shutdown-and-cleanup.md)

- [الملحق](appendix-00.md)
  - [أ - الكلمات المحجوزة](appendix-01-keywords.md)
  - [ب - المعاملات و الرموز](appendix-02-operators.md)
  - [ج - السمات القبلة للاشتقاق](appendix-03-derivable-traits.md)
  - [د - بعض ادوات التطوير المفيدة](appendix-04-useful-development-tools.md)
  - [هـ - الاصدارات](appendix-05-editions.md)
  - [و - ترجمات للكتاب](appendix-06-translation.md)
  - [كيف يتم تطوير Rust و Rust "Nightly"&lrm;](appendix-07-nightly-rust.md)
