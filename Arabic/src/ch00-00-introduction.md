# مقدمة

> ملاحظة: هذه النسخة من الكتاب هي نفس نسخة [The Rust Programming
> Language][nsprust] المتاحة في الشكل المطبوع والكتاب الإلكتروني من [No Starch
> Press][nsp].

[nsprust]: https://nostarch.com/rust-programming-language-2nd-edition
[nsp]: https://nostarch.com/

مرحبًا بكم في _لغة البرمجة Rust_، وهو كتاب تمهيدي عن Rust.
تساعدك Rust على كتابة برامج أسرع وأكثر موثوقية.

غالبًا ما تكون سهولة الاستخدام والتحكم المنخفض المستوى في تصميم لغات البرمجة على خلاف،ولكن Rust تتحدي هذا الخلاف من خلال تحقيق توازن بين القدرة التقنية القوية وتجربة المطور الرائعة.كما ان Rust تمنحك الخيار للتحكم في التفاصيل المنخفضة المستوى (مثل استخدام الذاكرة) دون كل المتاعب التقليدية المرتبطة بهذا النوع من التحكم المنخفض.

## لمن Rust :

تعتبر Rust مثالية للعديد من الأشخاص لأسباب متنوعة. دعونا نلقي نظرة على بعض أهم الفئات:

### فرق المطورين

تثبت Rust أنها أداة مثمرة للتعاون بين فرق كبيرة من المطورين الذين لديهم مستويات متفاوتة من المعرفة ببرمجة الأنظمة. الكود منخفض المستوى غالبا ما يكون عرضة لمختلف الأخطاء الدقيقة، والتي في معظم اللغات الأخرى يمكن اكتشافها فقط من خلال اختبار شامل ومراجعة دقيقة للكود من قبل المطورين ذوي الخبرة. في Rust، يلعب المترجم دور حارس البوابة برفضه تجميع الكود الذي يحتوي على هذه الأخطاء الدقيقة، بما في ذلك أخطاء التواقت. فمن خلال العمل مع المترجم، يمكن للفريق التركيز على منطق البرنامج بدلاً من مطاردة الأخطاء.

كما تجلب Rust أدوات تطوير حديثة إلى عالم برمجة الأنظمة:

- Cargo، مدير الاعتمادات وأداة البناء، التي تجعل إضافة وتجميع وإدارة الاعتمادات سهلة ومتسقة عبر بيئة عمل Rust.
- أداة تنسيق الكود Rustfmt تضمن تنسيق كود متسق عبر المطورين.
- يوفر rust-analyzer الدعم لبيئات التطوير المتكاملة (IDE) لإكمال الكود الفوري ورسائل الخطأ الداخلية.

باستخدام هذه الأدوات وغيرها في بيئة عمل Rust يمكن للمطورين أن يكونوا اكثر انتاجية أثناء كتابة كود على مستوى الأنظمة.

### الطلاب

Rust موجهة للطلاب وأولئك الذين يهتمون بتعلم مفاهيم الأنظمة. باستخدام Rust، تعلم العديد من الأشخاص مواضيع مثل تطوير أنظمة التشغيل. كما أن المجتمع مرحب جدًا وسعيد بالإجابة على أسئلة الطلاب. تسعى فرق Rust من خلال جهودمن ضمنها هذا الكتاب، إلى جعل مفاهيم الأنظمة أكثر سهولة لمزيد من الناس، بالأخص المبتدئين في البرمجة.

### الشركات

مئات الشركات، الكبيرة والصغيرة، تستخدم Rust في الإنتاج لمجموعة متنوعة من المهام، بما في ذلك أدوات سطر الأوامر، خدمات الويب، أدوات DevOps، الأجهزة المضمنة، تحليل وترميز الصوت والفيديو، العملات المشفرة، المعلوماتية الحيوية، محركات البحث، تطبيقات إنترنت الأشياء، التعلم الآلي، حتى أجزاء رئيسية من متصفح الويب Firefox.

### مطورو المصادر المفتوحة

Rust موجهة الذين يرغبون في بناء لغة Rust، والمجتمع، وبناء أدوات التطوير، والمكتبات. نحن نرحب بمساهماتك في Rust.

### الأشخاص الذين يقدرون السرعة والاستقرار

Rust موجهة للأشخاص الذين يرغبون في لغة تتميز بالسرعة والاستقرار.عندما نتحدث عن السرعة، نعني كلا من مدى سرعة تنفيذ كود Rust ومدى سرعة كتابة البرامج باستخدام Rust. كما ان فحوصات مترجم Rust تحقق لنا الاستقرار من خلال التنويه بامكانية اضافة التحسينات او إعادة هيكلة الكود. هذا على النقيض من الاكواد القديمة الهشة في اللغات التي لا تحتوي على هذه الفحوصات، والتي غالباً ما يخشى المطور تعديلها. تهدف Rust لجعل الكود الآمن سريعاً كذلك من خلال السعي لتحقيق تجريدات بدون تكلفة إضافية، أي الميزات عالية المستوى التي تُترجم إلى أكواد منخفضة المستوى بنفس سرعة الكود المكتوب يدوياً.

تأمل لغة Rust في دعم العديد من المستخدمين الآخرين أيضًا؛ ما ذكر هنا هم مجرد بعض أصحاب المصلحة الكبار. عمومًا، الطموح الأكبر لـ Rust هو القضاء على التنازلات التي قَبِلَ بها المبرمجون لعقود من خلال توفير الأمان _و_ الإنتاجية، السرعة _و_ السهولة في الاستخدام. جرب Rust وشاهد ما إذا كانت اختياراتها تناسبك

## لمن هذا الكتاب

يفترض هذا الكتاب أنك قد كتبت اكواد بلغة برمجة أخرى لكنه لا يفترض أي شيء عن أي لغة برمجة معينة. لقد حاولنا جعل المادة واسعة النطاق ومتاحة لأولئك القادمين من خلفيات برمجية متنوعة. لن نقضي الكثير من الوقت في الحديث عن _ما_ هي البرمجة أو كيفية التفكير فيها. فإذا كنت جديدًا تمامًا في البرمجة، فستكون من الأفضل لك قراءة كتاب يشرح مقدمة للبرمجة.

## كيفية استخدام هذا الكتاب

بشكل عام، يفترض هذا الكتاب أنك تقرأه بالتسلسل من الأمام إلى الخلف. تبني الفصول اللاحقة على المفاهيم الموجودة في الفصول السابقة، وقد لا تتعمق الفصول السابقة في تفاصيل موضوع معين ولكن ستعود إلى هذا الموضوع في فصل لاحق.

ستجد نوعين من الفصول في هذا الكتاب: فصول مفاهيم وفصول مشاريع. في فصول المفاهيم، ستتعلم عن جانب من جوانب لغة Rust. في فصول المشاريع، سنبني برامج صغيرة معًا، ونطبق ما تعلمته حتى الآن. الفصول ٢، ١٢، و ٢٠ هي فصول مشاريع؛ والباقي هي فصول مفاهيم.

يشرح الفصل ١ كيفية تثبيت Rust، وكيفية كتابة برنامج "Hello, world!"، وكيفية استخدام Cargo، مدير الحزم وأداة البناء في Rust. الفصل ٢ هو مقدمة عملية لكتابة برنامج في Rust، حيث ستبني لعبة تخمين الأرقام. هنا نغطي المفاهيم على مستوى عالٍ، وستوفر الفصول اللاحقة تفاصيل إضافية. إذا كنت تريد العمل على الفور، فإن الفصل ٢ هو المكان المناسب لذلك. يغطي الفصل ٣ ميزات Rust التي تشبه تلك الموجودة في لغات البرمجة الأخرى، وفي الفصل ٤ ستتعلم عن نظام الملكية في Rust. إذا كنت تفضل تعلم كل التفاصيل قبل الانتقال إلى التالي، فقد ترغب في تخطي الفصل ٢ والانتقال مباشرة إلى الفصل ٣، ثم العودة إلى الفصل ٢ عندما ترغب في العمل على مشروع يطبق التفاصيل التي تعلمتها.

يناقش الفصل ٥ التراكيب والدوال التابعة ويغطي الفصل ٦ التعدادات، وتعبيرات `match`، وبنيه `if let` للتحكم بتدفق البرنامج. كما انك ستستخدم التراكيب والتعدادات لإنشاء أنواع مخصوصة في Rust.

في الفصل ٧، ستتعلم عن نظام الوحدات في Rust وقواعد الخصوصية لتنظيم الكود الخاص بك وواجهة التطبيق البرمجية العامة API. يناقش الفصل ٨ بعض هياكل البيانات المستخدمة في التجميعات Collections التي توفرها المكتبة القياسية، مثل المتجهات vectors، السلاسل النصية strings، والخرائط hash maps. يستعرض الفصل ٩ فلسفة وتقنيات معالجة الأخطاء في Rust.

يغوص الفصل ١٠ في الانواع المعممة ، السمات، ودورات الحياة ، والتي تمنحك القدرة على كتابة كود ينطبق على أنواع متعددة. يتناول الفصل ١١ كل ما يتعلق بالاختبارات، والتي حتى مع ضمانات أمان Rust، لا تزال ضرورية لضمان صحة منطق البرنامج. سنبني في الفصل ١2 تطبيقنا الخاص لمجموعة من الخصائص الموجودة في أداة سطر الاوامر `grep` الي ستبحث عن نص معين داخل عدة ملفات، ولتنفيذ ذلك، سنلجأ إلي العديد من المفاهيم التي ناقشناها في الفصول السابقة.

يستكشف الفصل ١٣ الاغلاقات والمكررات: ميزات في Rust تأتي من لغات البرمجة الوظيفية. في الفصل ١٤، سنتناول Cargo بعمق أكبر ونتحدث عن أفضل الممارسات لمشاركة مكتباتك مع الآخرين. يناقش الفصل ١٥ المؤشرات الذكية التي توفرها المكتبة القياسية والسمات التي تتيح وظائفها.

في الفصل ١٦، سنستعرض نماذج مختلفة من البرمجة المتواقتة ونتحدث عن مساعدة Rust لك على البرمجة في خيوط متعددة دون قلق. ينظر الفصل ١٧ إلي تشابه مصطلحات لغة Rust مع مبادئ البرمجة كائنية التوجه التي قد تكون مألوفة لك.

الفصل ١٨ هو مرجع عن الأنماط والمطابقة النمطية، والتي تعد طرقًا قوية للتعبير عن الأفكار في برامج Rust. يحتوي الفصل ١٩ على مجموعة متنوعة من الموضوعات المتقدمة المثيرة للاهتمام، بما في ذلك Rust غير الآمن ،الماكروز macros ،والمزيد عن دورات الحياة، السمات، الأنواع، الدوال، والمغلفات.

في الفصل ٢٠، سنكمل مشروعًا ننفذ فيه خادم ويب منخفض المستوي و متعدد الخيوط!

أخيرًا، تتضمن بعض الملحقات بعض المعلومات المفيدة حول اللغة بتنسيق يشبه المرجع. يغطي الملحق أ كلمات Rust المحجوزة، يغطي الملحق ب عوامل Rust والرموز، يغطي الملحق جـ السمات القابلة للاشتقاق التي توفرها المكتبة القياسية، يغطي الملحق د بعض أدوات التطوير المفيدة، ويشرح الملحق هـ إصدارات Rust. في الملحق و يمكنك العثور على ترجمات الكتاب، وفي الملحق ز سنغطي كيفية تطوير Rust وما هو nightly Rust.

لا يوجد طريقة خاطئة لقراءة هذا الكتاب: إذا كنت ترغب في القفز للأمام، فافعل ذلك! قد تضطر إلى العودة إلى الفصول السابقة إذا واجهت أي ارتباك. لكن افعل ما يناسبك.

<span id="ferris"></span>

جزء مهم من عملية تعلم Rust هو تعلم كيفية قراءة رسائل الخطأ التي يعرضها المترجم: ستوجهك هذه الرسائل نحو الكود الذي يعمل. لذا، سنقدم العديد من الأمثلة التي لا تترجم مع رسالة الخطأ التي سيظهرها المترجم في كل حالة. اعلم أنه إذا أدخلت وقمت بتشغيل مثال عشوائي، فقد لا يترجم! تأكد من قراءة النص المحيط لترى ما إذا كان المثال الذي تحاول تشغيله من المفترض أن يخطئ. سيساعدك Ferris أيضًا في تمييز الكود الذي ليس من المفترض أن يعمل:

| فيريس Ferris                                                                                                     | المعني                               |
| ---------------------------------------------------------------------------------------------------------------- | ------------------------------------ |
| <img src="img/ferris/does_not_compile.svg" class="ferris-explain" alt="Ferris with a question mark"/>            | هذا الكود لا يمكن تجميعه. !          |
| <img src="img/ferris/panics.svg" class="ferris-explain" alt="Ferris throwing up their hands"/>                   | هذا الكود سينهار. !                  |
| <img src="img/ferris/not_desired_behavior.svg" class="ferris-explain" alt="Ferris with one claw up, shrugging"/> | لن يقدم هذا الكود النتيجة المرجوة. ! |

في معظم الاحوال سوف يتم توجيهك الي النسخة الصحيحة لاي كود غير قابل للتجميع .

## كود المصدر

يمكن العثور على ملفات المصدر التي تم إنشاء هذا الكتاب منها على
[GitHub][book].

[book]: https://github.com/rust-lang/book/tree/main/src