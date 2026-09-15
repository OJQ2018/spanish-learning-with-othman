const phrases = [
  ["Hola, ¿cómo estás?", "مرحباً، كيف حالك؟"],
  ["Buenos días.", "صباح الخير."],
  ["Buenas tardes.", "مساء الخير."],
  ["Buenas noches.", "مساء الخير / ليلة سعيدة."],
  ["¿Cómo te llamas?", "ما اسمك؟"],
  ["Me llamo Ahmed.", "اسمي أحمد."],
  ["Mucho gusto.", "تشرفت بمعرفتك."],
  ["¿De dónde eres?", "من أين أنت؟"],
  ["Soy de Marruecos.", "أنا من المغرب."],
  ["¿Dónde vives?", "أين تعيش؟"],
  ["Vivo en Alemania.", "أعيش في ألمانيا."],
  ["¿Hablas español?", "هل تتحدث الإسبانية؟"],
  ["Estoy aprendiendo español.", "أنا أتعلم الإسبانية."],
  ["No entiendo esta frase.", "لا أفهم هذه الجملة."],
  ["¿Puedes repetirlo?", "هل يمكنك تكرار ذلك؟"],
  ["Habla más despacio, por favor.", "تحدث ببطء أكثر من فضلك."],
  ["¿Qué significa esta palabra?", "ماذا تعني هذه الكلمة؟"],
  ["¿Cómo se dice esto en español?", "كيف نقول هذا بالإسبانية؟"],
  ["Gracias por tu ayuda.", "شكراً على مساعدتك."],
  ["Nos vemos pronto.", "أراك قريباً."],

  ["Me he despertado temprano.", "استيقظت مبكراً."],
  ["Todavía tengo sueño.", "ما زلت أشعر بالنعاس."],
  ["Voy a lavarme la cara.", "سأغسل وجهي."],
  ["Voy a ducharme.", "سأستحم."],
  ["Necesito cepillarme los dientes.", "أحتاج إلى تنظيف أسناني."],
  ["Voy a vestirme.", "سأرتدي ملابسي."],
  ["No encuentro mis zapatos.", "لا أجد حذائي."],
  ["Mis llaves están sobre la mesa.", "مفاتيحي على الطاولة."],
  ["Voy a preparar el desayuno.", "سأحضر الفطور."],
  ["Hoy tengo mucha prisa.", "لدي عجلة كبيرة اليوم."],
  ["Necesito descansar un poco.", "أحتاج إلى الراحة قليلاً."],
  ["Voy a ordenar mi habitación.", "سأرتب غرفتي."],
  ["La casa está muy tranquila.", "المنزل هادئ جداً."],
  ["Tengo que limpiar la cocina.", "يجب أن أنظف المطبخ."],
  ["Voy a lavar la ropa.", "سأغسل الملابس."],
  ["¿Dónde está el baño?", "أين الحمام؟"],
  ["Cierra la puerta, por favor.", "أغلق الباب من فضلك."],
  ["Abre la ventana, por favor.", "افتح النافذة من فضلك."],
  ["Apaga la luz cuando salgas.", "أطفئ الضوء عندما تخرج."],
  ["Voy a dormir temprano esta noche.", "سأنام مبكراً الليلة."],

  ["Tengo hambre.", "أنا جائع."],
  ["Tengo mucha sed.", "أنا عطشان جداً."],
  ["Quiero beber agua fría.", "أريد شرب ماء بارد."],
  ["Voy a preparar un café.", "سأحضر قهوة."],
  ["¿Quieres té o café?", "هل تريد الشاي أم القهوة؟"],
  ["El desayuno está listo.", "الفطور جاهز."],
  ["La comida huele muy bien.", "رائحة الطعام جميلة جداً."],
  ["La sopa está caliente.", "الحساء ساخن."],
  ["La ensalada está fresca.", "السلطة طازجة."],
  ["Este pan está delicioso.", "هذا الخبز لذيذ."],
  ["No quiero comer mucho.", "لا أريد أن آكل كثيراً."],
  ["¿Qué vamos a cenar?", "ماذا سنتناول على العشاء؟"],
  ["Voy a cortar las verduras.", "سأقطع الخضار."],
  ["Necesitamos comprar leche.", "نحتاج إلى شراء الحليب."],
  ["No queda mucho arroz.", "لم يتبق الكثير من الأرز."],
  ["Pon el plato sobre la mesa.", "ضع الطبق على الطاولة."],
  ["La comida está demasiado salada.", "الطعام مالح جداً."],
  ["Este postre es muy dulce.", "هذه الحلوى حلوة جداً."],
  ["¿Quieres otra taza de café?", "هل تريد كوباً آخر من القهوة؟"],
  ["La cuenta, por favor.", "الحساب من فضلك."],

  ["¿Qué quieres comer?", "ماذا تريد أن تأكل؟"],
  ["Quiero una pizza pequeña.", "أريد بيتزا صغيرة."],
  ["Me gustaría una hamburguesa.", "أود هامبرغر."],
  ["Quiero una ensalada sin cebolla.", "أريد سلطة بدون بصل."],
  ["¿Qué me recomiendas?", "ماذا تنصحني؟"],
  ["Quiero probar algo nuevo.", "أريد تجربة شيء جديد."],
  ["¿Tiene este plato carne?", "هل يحتوي هذا الطبق على لحم؟"],
  ["No como carne de cerdo.", "لا آكل لحم الخنزير."],
  ["¿Tiene azúcar?", "هل يحتوي على السكر؟"],
  ["Quiero agua sin gas.", "أريد ماءً بدون غاز."],
  ["Quiero agua con gas.", "أريد ماءً غازياً."],
  ["¿Me trae la carta?", "هل تحضر لي قائمة الطعام؟"],
  ["¿Cuánto cuesta este plato?", "كم سعر هذا الطبق؟"],
  ["¿Puedo pagar con tarjeta?", "هل يمكنني الدفع بالبطاقة؟"],
  ["Acepto la cuenta.", "أوافق على الحساب."],
  ["Quiero pedir para llevar.", "أريد طلب الطعام لأخذه معي."],
  ["¿Cuánto tardará mi pedido?", "كم سيستغرق طلبي؟"],
  ["La comida todavía no ha llegado.", "الطعام لم يصل بعد."],
  ["Todo está muy rico.", "كل شيء لذيذ جداً."],
  ["Gracias, estaba todo perfecto.", "شكراً، كان كل شيء ممتازاً."],

  ["Voy al supermercado después del trabajo.", "سأذهب إلى السوبرماركت بعد العمل."],
  ["Necesito comprar algunas cosas.", "أحتاج إلى شراء بعض الأشياء."],
  ["¿Dónde está la leche?", "أين الحليب؟"],
  ["¿Cuánto cuesta este producto?", "كم سعر هذا المنتج؟"],
  ["Es demasiado caro.", "هذا غالٍ جداً."],
  ["¿Tiene algo más barato?", "هل لديك شيء أرخص؟"],
  ["Quiero comprar esta camiseta.", "أريد شراء هذا القميص."],
  ["¿Tiene otra talla?", "هل لديك مقاس آخر؟"],
  ["¿Tiene otro color?", "هل لديك لون آخر؟"],
  ["Quiero probarme estos zapatos.", "أريد تجربة هذا الحذاء."],
  ["¿Dónde están los probadores?", "أين غرف القياس؟"],
  ["Me queda bien esta chaqueta.", "هذه السترة مناسبة لي."],
  ["Me queda demasiado grande.", "إنه كبير جداً عليّ."],
  ["Me queda pequeño.", "إنه صغير عليّ."],
  ["¿Puedo devolverlo mañana?", "هل يمكنني إرجاعه غداً؟"],
  ["Tengo el recibo conmigo.", "لدي الإيصال معي."],
  ["¿Está en oferta esta semana?", "هل عليه تخفيض هذا الأسبوع؟"],
  ["¿Hay algún descuento?", "هل يوجد أي خصم؟"],
  ["Necesito una bolsa.", "أحتاج إلى كيس."],
  ["No necesito una bolsa.", "لا أحتاج إلى كيس."],

  ["¿Dónde está la estación?", "أين المحطة؟"],
  ["¿Dónde está la parada de autobús?", "أين موقف الحافلة؟"],
  ["Quiero ir al centro.", "أريد الذهاب إلى وسط المدينة."],
  ["¿Cómo llego al centro?", "كيف أصل إلى وسط المدينة؟"],
  ["¿Está lejos de aquí?", "هل هو بعيد من هنا؟"],
  ["¿Está cerca de la estación?", "هل هو قريب من المحطة؟"],
  ["¿Puedo ir andando?", "هل يمكنني الذهاب سيراً؟"],
  ["Voy en autobús.", "سأذهب بالحافلة."],
  ["Voy en tren.", "سأذهب بالقطار."],
  ["Necesito un taxi.", "أحتاج إلى سيارة أجرة."],
  ["¿Cuánto cuesta el billete?", "كم سعر التذكرة؟"],
  ["Quiero un billete de ida y vuelta.", "أريد تذكرة ذهاب وعودة."],
  ["¿A qué hora sale el tren?", "في أي ساعة يغادر القطار؟"],
  ["¿A qué hora llega el tren?", "في أي ساعة يصل القطار؟"],
  ["¿Este tren va a Madrid?", "هل هذا القطار يذهب إلى مدريد؟"],
  ["¿Dónde tengo que cambiar?", "أين يجب أن أبدّل؟"],
  ["He perdido mi tren.", "لقد فاتني القطار."],
  ["El tren tiene retraso.", "القطار متأخر."],
  ["¿Está libre este asiento?", "هل هذا المقعد فارغ؟"],
  ["Avísame cuando lleguemos.", "أخبرني عندما نصل."],

  ["Tengo una reserva.", "لدي حجز."],
  ["La reserva está a mi nombre.", "الحجز باسمي."],
  ["Quiero hacer el check-in.", "أريد تسجيل الدخول."],
  ["Quiero hacer el check-out.", "أريد تسجيل الخروج."],
  ["¿A qué hora es el check-out?", "في أي ساعة تسجيل الخروج؟"],
  ["¿Dónde está mi habitación?", "أين غرفتي؟"],
  ["¿En qué piso está?", "في أي طابق هي؟"],
  ["¿Dónde está el ascensor?", "أين المصعد؟"],
  ["¿Hay wifi en la habitación?", "هل يوجد واي فاي في الغرفة؟"],
  ["¿Cuál es la contraseña del wifi?", "ما كلمة مرور الواي فاي؟"],
  ["La habitación está muy limpia.", "الغرفة نظيفة جداً."],
  ["La cama es cómoda.", "السرير مريح."],
  ["No funciona el aire acondicionado.", "مكيف الهواء لا يعمل."],
  ["No hay agua caliente.", "لا يوجد ماء ساخن."],
  ["Necesito otra toalla.", "أحتاج إلى منشفة أخرى."],
  ["¿Puede traerme una almohada?", "هل يمكنك إحضار وسادة لي؟"],
  ["La televisión no funciona.", "التلفاز لا يعمل."],
  ["He perdido la llave.", "لقد فقدت المفتاح."],
  ["Necesito hablar con recepción.", "أحتاج إلى التحدث مع الاستقبال."],
  ["¿El desayuno está incluido?", "هل الفطور مشمول؟"],

  ["Hoy tengo que trabajar.", "يجب أن أعمل اليوم."],
  ["Trabajo desde casa.", "أعمل من المنزل."],
  ["Trabajo en una oficina.", "أعمل في مكتب."],
  ["Estoy buscando trabajo.", "أبحث عن عمل."],
  ["Tengo una entrevista mañana.", "لدي مقابلة غداً."],
  ["Estoy preparando mi currículum.", "أجهز سيرتي الذاتية."],
  ["¿A qué hora empiezas a trabajar?", "في أي ساعة تبدأ العمل؟"],
  ["Empiezo a las ocho.", "أبدأ في الساعة الثامنة."],
  ["¿A qué hora terminas?", "في أي ساعة تنتهي؟"],
  ["Termino a las cinco.", "أنتهي في الساعة الخامسة."],
  ["Hoy tengo mucho trabajo.", "لدي الكثير من العمل اليوم."],
  ["Necesito terminar este informe.", "أحتاج إلى إنهاء هذا التقرير."],
  ["Lo haré mañana por la mañana.", "سأفعل ذلك غداً صباحاً."],
  ["Estoy ocupado ahora mismo.", "أنا مشغول الآن."],
  ["¿Puedes ayudarme con esto?", "هل يمكنك مساعدتي في هذا؟"],
  ["Tenemos una reunión a las diez.", "لدينا اجتماع الساعة العاشرة."],
  ["Necesito tomar algunas notas.", "أحتاج إلى تدوين بعض الملاحظات."],
  ["¿Puedes enviarme el documento?", "هل يمكنك إرسال الوثيقة لي؟"],
  ["He enviado el correo electrónico.", "لقد أرسلت البريد الإلكتروني."],
  ["Todavía no he recibido respuesta.", "لم أتلق رداً بعد."],

  ["Tengo que estudiar esta tarde.", "يجب أن أدرس بعد ظهر اليوم."],
  ["Estoy haciendo mis deberes.", "أقوم بواجباتي."],
  ["Necesito preparar un examen.", "أحتاج إلى التحضير لامتحان."],
  ["¿Has terminado el ejercicio?", "هل أنهيت التمرين؟"],
  ["No entiendo esta pregunta.", "لا أفهم هذا السؤال."],
  ["¿Puedes explicármelo otra vez?", "هل يمكنك شرحه لي مرة أخرى؟"],
  ["Ahora lo entiendo mejor.", "الآن أفهمه بشكل أفضل."],
  ["Necesito más tiempo para estudiar.", "أحتاج إلى مزيد من الوقت للدراسة."],
  ["Voy a estudiar en la biblioteca.", "سأدرس في المكتبة."],
  ["La biblioteca está muy tranquila.", "المكتبة هادئة جداً."],
  ["Tengo clase a las nueve.", "لدي درس في التاسعة."],
  ["La clase termina a las once.", "ينتهي الدرس في الحادية عشرة."],
  ["¿Puedes prestarme un bolígrafo?", "هل يمكنك إعطائي قلماً لأستعمله؟"],
  ["He olvidado mi cuaderno.", "لقد نسيت دفتري."],
  ["Necesito imprimir este documento.", "أحتاج إلى طباعة هذه الوثيقة."],
  ["¿Dónde está la sala de estudio?", "أين غرفة الدراسة؟"],
  ["Mañana tengo un examen.", "لدي امتحان غداً."],
  ["Estoy un poco nervioso por el examen.", "أنا متوتر قليلاً بسبب الامتحان."],
  ["Creo que estoy preparado.", "أعتقد أنني مستعد."],
  ["Después de estudiar voy a descansar.", "بعد الدراسة سأرتاح."],

  ["¿Tienes hermanos?", "هل لديك إخوة؟"],
  ["Tengo un hermano mayor.", "لدي أخ أكبر."],
  ["Tengo una hermana menor.", "لدي أخت أصغر."],
  ["Mi familia vive cerca.", "عائلتي تعيش قريباً."],
  ["Mi familia vive lejos.", "عائلتي تعيش بعيداً."],
  ["Voy a visitar a mi familia.", "سأزور عائلتي."],
  ["Hablo con mi madre todos los días.", "أتحدث مع أمي كل يوم."],
  ["Hablo con mi padre por teléfono.", "أتحدث مع أبي عبر الهاتف."],
  ["Mi hermano está trabajando.", "أخي يعمل."],
  ["Mi hermana está estudiando.", "أختي تدرس."],
  ["¿Cómo está tu familia?", "كيف حال عائلتك؟"],
  ["Todos están bien.", "الجميع بخير."],
  ["Voy a visitar a un amigo.", "سأزور صديقاً."],
  ["¿Quieres venir conmigo?", "هل تريد أن تأتي معي؟"],
  ["Vamos a salir esta noche.", "سنخرج الليلة."],
  ["Podemos ir al cine.", "يمكننا الذهاب إلى السينما."],
  ["Podemos dar un paseo.", "يمكننا الذهاب في نزهة."],
  ["Me alegra verte.", "سعيد برؤيتك."],
  ["Te he echado de menos.", "اشتقت إليك."],
  ["Puedes contar conmigo.", "يمكنك الاعتماد علي."],

  ["Estoy feliz hoy.", "أنا سعيد اليوم."],
  ["Estoy triste.", "أنا حزين."],
  ["Estoy preocupado.", "أنا قلق."],
  ["Estoy nervioso.", "أنا متوتر."],
  ["Estoy tranquilo ahora.", "أنا هادئ الآن."],
  ["Estoy enfadado.", "أنا غاضب."],
  ["Estoy sorprendido.", "أنا متفاجئ."],
  ["Estoy aburrido.", "أشعر بالملل."],
  ["Estoy emocionado.", "أنا متحمس."],
  ["Tengo miedo.", "أنا خائف."],
  ["No tengo miedo.", "أنا لست خائفاً."],
  ["Estoy muy cansado.", "أنا متعب جداً."],
  ["Me siento mejor hoy.", "أشعر بتحسن اليوم."],
  ["No me siento bien.", "لا أشعر أنني بخير."],
  ["Necesito descansar.", "أحتاج إلى الراحة."],
  ["Estoy de buen humor.", "مزاجي جيد."],
  ["Hoy estoy de mal humor.", "مزاجي سيئ اليوم."],
  ["No estoy seguro de eso.", "لست متأكداً من ذلك."],
  ["Estoy de acuerdo contigo.", "أنا أتفق معك."],
  ["No estoy de acuerdo.", "أنا لا أتفق."],

  ["Tienes razón.", "أنت على حق."],
  ["No tienes razón.", "أنت مخطئ."],
  ["Es una buena idea.", "إنها فكرة جيدة."],
  ["Es una mala idea.", "إنها فكرة سيئة."],
  ["No importa.", "لا يهم."],
  ["Eso depende.", "هذا يعتمد."],
  ["No lo sé.", "لا أعرف."],
  ["No tengo ni idea.", "ليس لدي أي فكرة."],
  ["Quiero saber la verdad.", "أريد معرفة الحقيقة."],
  ["Dime la verdad.", "قل لي الحقيقة."],
  ["Creo que tienes razón.", "أعتقد أنك على حق."],
  ["Creo que es demasiado caro.", "أعتقد أنه غالٍ جداً."],
  ["Creo que podemos hacerlo.", "أعتقد أننا نستطيع فعل ذلك."],
  ["No creo que sea necesario.", "لا أعتقد أن ذلك ضروري."],
  ["Para mí, está bien.", "بالنسبة لي، هذا جيد."],
  ["En mi opinión, es mejor así.", "في رأيي، هكذا أفضل."],
  ["Prefiero quedarme en casa.", "أفضل البقاء في المنزل."],
  ["Prefiero ir mañana.", "أفضل الذهاب غداً."],
  ["Me parece interesante.", "يبدو لي الأمر ممتعاً."],
  ["No me parece difícil.", "لا يبدو لي صعباً."],

  ["¿Qué hora es?", "كم الساعة؟"],
  ["Son las ocho de la mañana.", "الساعة الثامنة صباحاً."],
  ["Son las tres de la tarde.", "الساعة الثالثة بعد الظهر."],
  ["Son las diez de la noche.", "الساعة العاشرة مساءً."],
  ["Llego en diez minutos.", "سأصل خلال عشر دقائق."],
  ["Te llamo en una hora.", "سأتصل بك بعد ساعة."],
  ["Nos vemos mañana.", "أراك غداً."],
  ["Nos vemos el lunes.", "أراك يوم الاثنين."],
  ["Hoy es martes.", "اليوم الثلاثاء."],
  ["Mañana es miércoles.", "غداً الأربعاء."]
];

const phrasesPart2 = [
  ["Ayer fue domingo.", "كان أمس الأحد."],
  ["Esta semana estoy ocupado.", "أنا مشغول هذا الأسبوع."],
  ["El próximo mes voy de viaje.", "سأسافر الشهر المقبل."],
  ["El año pasado vivía aquí.", "كنت أعيش هنا العام الماضي."],
  ["Tengo tiempo esta tarde.", "لدي وقت بعد ظهر اليوم."],
  ["No tengo tiempo ahora.", "ليس لدي وقت الآن."],
  ["Llegué demasiado temprano.", "وصلت مبكراً جداً."],
  ["Llegué un poco tarde.", "وصلت متأخراً قليلاً."],
  ["Nos queda poco tiempo.", "لم يتبق لنا وقت كثير."],
  ["Date prisa, por favor.", "أسرع من فضلك."],
  ["El tiempo está muy bonito hoy.", "الطقس جميل جداً اليوم."],
  ["Hace mucho calor.", "الجو حار جداً."],
  ["Hace mucho frío.", "الجو بارد جداً."],
  ["Está lloviendo.", "إنها تمطر."],
  ["Ha dejado de llover.", "توقف المطر."],
  ["Está nevando.", "إنها تتساقط الثلوج."],
  ["Hace viento.", "الجو عاصف."],
  ["El cielo está despejado.", "السماء صافية."],
  ["Hay muchas nubes.", "هناك الكثير من الغيوم."],
  ["Necesito un paraguas.", "أحتاج إلى مظلة."],
  ["Lleva una chaqueta.", "ارتدِ سترة."],
  ["No olvides el abrigo.", "لا تنس المعطف."],
  ["El sol está muy fuerte.", "الشمس قوية جداً."],
  ["Hoy es un día perfecto para caminar.", "اليوم مثالي للمشي."],
  ["Prefiero quedarme dentro cuando llueve.", "أفضل البقاء في الداخل عندما تمطر."],
  ["Mañana hará más frío.", "غداً سيكون الجو أبرد."],
  ["Espero que haga buen tiempo.", "آمل أن يكون الطقس جميلاً."],
  ["El invierno aquí es frío.", "الشتاء هنا بارد."],
  ["El verano suele ser caluroso.", "الصيف عادةً حار."],
  ["Me gusta caminar cuando hace buen tiempo.", "أحب المشي عندما يكون الطقس جميلاً."],

  ["Tengo que ir al banco.", "يجب أن أذهب إلى البنك."],
  ["Tengo que ir a la farmacia.", "يجب أن أذهب إلى الصيدلية."],
  ["Tengo una cita mañana.", "لدي موعد غداً."],
  ["Necesito cambiar la cita.", "أحتاج إلى تغيير الموعد."],
  ["¿A qué hora es la cita?", "في أي ساعة الموعد؟"],
  ["Voy a llegar tarde.", "سأتأخر."],
  ["Perdón por llegar tarde.", "آسف على التأخر."],
  ["Estoy casi allí.", "أنا على وشك الوصول."],
  ["Llegaré en diez minutos.", "سأصل خلال عشر دقائق."],
  ["¿Puedes esperarme unos minutos?", "هل يمكنك انتظاري بضع دقائق؟"],
  ["No puedo quedarme mucho tiempo.", "لا أستطيع البقاء وقتاً طويلاً."],
  ["Tengo que irme ahora.", "يجب أن أذهب الآن."],
  ["Volveré dentro de una hora.", "سأعود بعد ساعة."],
  ["Mañana voy a visitar a mis amigos.", "غداً سأزور أصدقائي."],
  ["Este fin de semana quiero descansar.", "أريد أن أرتاح في عطلة نهاية الأسبوع."],
  ["Hoy quiero quedarme en casa.", "أريد البقاء في المنزل اليوم."],
  ["Mañana vamos a salir juntos.", "غداً سنخرج معاً."],
  ["Puedes venir cuando quieras.", "يمكنك المجيء متى شئت."],
  ["Espero que vuelvas pronto.", "آمل أن تعود قريباً."],
  ["Espero que tengas un día maravilloso.", "أتمنى أن يكون يومك رائعاً."],

  ["¿Puedes abrir la ventana?", "هل يمكنك فتح النافذة؟"],
  ["¿Puedes cerrar la ventana?", "هل يمكنك إغلاق النافذة؟"],
  ["¿Puedes encender la televisión?", "هل يمكنك تشغيل التلفاز؟"],
  ["¿Puedes apagar la televisión?", "هل يمكنك إطفاء التلفاز؟"],
  ["¿Has cerrado la puerta con llave?", "هل أغلقت الباب بالمفتاح؟"],
  ["Estoy buscando mis gafas.", "أبحث عن نظارتي."],
  ["¿Has visto mi cartera?", "هل رأيت محفظتي؟"],
  ["No encuentro mi cartera.", "لا أجد محفظتي."],
  ["He perdido mi teléfono.", "لقد فقدت هاتفي."],
  ["¿Has visto mi teléfono?", "هل رأيت هاتفي؟"],
  ["Mi batería está casi vacía.", "بطارية هاتفي أوشكت على النفاد."],
  ["Necesito cargar mi teléfono.", "أحتاج إلى شحن هاتفي."],
  ["¿Tienes un cargador?", "هل لديك شاحن؟"],
  ["Mi teléfono no funciona.", "هاتفي لا يعمل."],
  ["No tengo conexión a internet.", "ليس لدي اتصال بالإنترنت."],
  ["¿Cuál es la contraseña?", "ما كلمة المرور؟"],

  ["Voy a preparar una taza de té.", "سأحضر كوباً من الشاي."],
  ["No sé qué cocinar.", "لا أعرف ماذا أطبخ."],
  ["Hoy no quiero cocinar.", "اليوم لا أريد الطبخ."],
  ["Vamos a pedir comida.", "سنطلب الطعام."],
  ["La comida llegará pronto.", "سيصل الطعام قريباً."],
  ["Tengo que sacar la basura.", "يجب أن أخرج القمامة."],
  ["Voy a lavar los platos.", "سأغسل الصحون."],
  ["La cocina necesita una limpieza.", "المطبخ يحتاج إلى تنظيف."],
  ["Voy a tender la ropa.", "سأنشر الملابس."],
  ["Necesito comprar detergente.", "أحتاج إلى شراء منظف."],
  ["La lavadora está funcionando.", "الغسالة تعمل."],
  ["¿Has visto las llaves de casa?", "هل رأيت مفاتيح المنزل؟"],
  ["Dejé las llaves en la entrada.", "تركت المفاتيح عند المدخل."],
  ["El teléfono está cargándose.", "الهاتف قيد الشحن."],
  ["Voy a poner el móvil en silencio.", "سأضع الهاتف على الوضع الصامت."],
  ["Necesito un poco de tranquilidad.", "أحتاج إلى بعض الهدوء."],
  ["Voy a sentarme un momento.", "سأجلس لحظة."],
  ["¿Puedes bajar el volumen?", "هل يمكنك خفض الصوت؟"],
  ["La música está demasiado alta.", "الموسيقى مرتفعة جداً."],
  ["Voy a abrir las cortinas.", "سأفتح الستائر."],
  ["Voy a cerrar las cortinas.", "سأغلق الستائر."],
  ["Hay mucho ruido afuera.", "هناك ضجيج كثير في الخارج."],
  ["Quiero dormir un poco.", "أريد أن أنام قليلاً."],

  ["¿Puedes ayudarme?", "هل يمكنك مساعدتي؟"],
  ["Necesito tu ayuda.", "أحتاج إلى مساعدتك."],
  ["¿Me puedes hacer un favor?", "هل يمكنك أن تقدم لي معروفاً؟"],
  ["Claro que sí.", "بالطبع."],
  ["Por supuesto.", "بالتأكيد."],
  ["No hay problema.", "لا توجد مشكلة."],
  ["Ahora mismo no puedo.", "لا أستطيع الآن."],
  ["Lo siento, estoy ocupado.", "آسف، أنا مشغول."],
  ["Te ayudaré después.", "سأساعدك لاحقاً."],
  ["Espera un momento.", "انتظر لحظة."],
  ["Dame cinco minutos.", "أعطني خمس دقائق."],
  ["Ven aquí, por favor.", "تعال إلى هنا من فضلك."],
  ["Mira esto.", "انظر إلى هذا."],
  ["Escucha con atención.", "استمع بانتباه."],
  ["Ten cuidado.", "انتبه."],
  ["No te preocupes.", "لا تقلق."],
  ["Todo estará bien.", "كل شيء سيكون بخير."],
  ["Confía en mí.", "ثق بي."],
  ["Hazlo con calma.", "افعل ذلك بهدوء."],
  ["Gracias por entenderme.", "شكراً لتفهمك."],

  ["¿Qué quieres hacer hoy?", "ماذا تريد أن تفعل اليوم؟"],
  ["Quiero ver una película.", "أريد مشاهدة فيلم."],
  ["Quiero escuchar música.", "أريد الاستماع إلى الموسيقى."],
  ["Quiero dar un paseo.", "أريد الذهاب في نزهة."],
  ["Quiero leer un libro.", "أريد قراءة كتاب."],
  ["Quiero jugar un poco.", "أريد أن ألعب قليلاً."],
  ["Voy a salir con mis amigos.", "سأخرج مع أصدقائي."],
  ["Vamos a tomar un café.", "هيا نشرب القهوة."],
  ["Vamos al parque.", "لنذهب إلى الحديقة."],
  ["¿Quieres ir al cine?", "هل تريد الذهاب إلى السينما؟"],
  ["¿Quieres venir conmigo?", "هل تريد المجيء معي؟"],
  ["Podemos hacerlo mañana.", "يمكننا فعل ذلك غداً."],
  ["Podemos hablar más tarde.", "يمكننا التحدث لاحقاً."],
  ["¿Qué te apetece hacer?", "ماذا ترغب في أن تفعل؟"],
  ["No quiero salir hoy.", "لا أريد الخروج اليوم."],
  ["Tengo ganas de viajar.", "أرغب في السفر."],
  ["Quiero conocer lugares nuevos.", "أريد اكتشاف أماكن جديدة."],
  ["Me gusta pasar tiempo contigo.", "أحب قضاء الوقت معك."],
  ["Hoy quiero relajarme.", "أريد الاسترخاء اليوم."],

  ["Necesito llamar a mi madre.", "أحتاج إلى الاتصال بأمي."],
  ["Voy a llamar a mi padre.", "سأتصل بأبي."],
  ["Te llamaré esta noche.", "سأتصل بك الليلة."],
  ["¿Puedes llamarme mañana?", "هل يمكنك الاتصال بي غداً؟"],
  ["Te enviaré un mensaje.", "سأرسل لك رسالة."],
  ["¿Has recibido mi mensaje?", "هل استلمت رسالتي؟"],
  ["No he visto tu mensaje.", "لم أر رسالتك."],
  ["Mi teléfono estaba apagado.", "كان هاتفي مغلقاً."],
  ["No tenía batería.", "لم تكن لدي بطارية."],
  ["¿Puedes enviarme la dirección?", "هل يمكنك إرسال العنوان لي؟"],
  ["Te mando una foto.", "سأرسل لك صورة."],
  ["¿Puedes compartir tu ubicación?", "هل يمكنك مشاركة موقعك؟"],
  ["Estoy en camino.", "أنا في الطريق."],
  ["Estoy esperando afuera.", "أنا أنتظر في الخارج."],
  ["¿Dónde estás ahora?", "أين أنت الآن؟"],
  ["Estoy en casa.", "أنا في المنزل."],
  ["Estoy en el trabajo.", "أنا في العمل."],
  ["Estoy en la estación.", "أنا في المحطة."],
  ["Nos vemos en la entrada.", "نلتقي عند المدخل."],
  ["Avísame cuando llegues.", "أخبرني عندما تصل."],

  ["Quiero aprender algo nuevo.", "أريد تعلم شيء جديد."],
  ["Estoy practicando español todos los días.", "أتمرن على الإسبانية كل يوم."],
  ["Necesito mejorar mi pronunciación.", "أحتاج إلى تحسين نطقي."],
  ["Quiero hablar español con más confianza.", "أريد التحدث بالإسبانية بثقة أكبر."],
  ["¿Puedes corregir mi frase?", "هل يمكنك تصحيح جملتي؟"],
  ["¿Cómo se pronuncia esta palabra?", "كيف تُنطق هذه الكلمة؟"],
  ["Voy a escribir una frase.", "سأكتب جملة."],
  ["Voy a leer en voz alta.", "سأقرأ بصوت عالٍ."],
  ["Necesito aprender más vocabulario.", "أحتاج إلى تعلم مفردات أكثر."],
  ["Esta palabra es difícil.", "هذه الكلمة صعبة."],
  ["Esta palabra es fácil.", "هذه الكلمة سهلة."],
  ["Ahora recuerdo la palabra.", "أتذكر الكلمة الآن."],
  ["He olvidado la palabra.", "لقد نسيت الكلمة."],
  ["¿Puedes hablar conmigo en español?", "هل يمكنك التحدث معي بالإسبانية؟"],
  ["Quiero practicar una conversación.", "أريد ممارسة محادثة."],
  ["Entiendo un poco de español.", "أفهم القليل من الإسبانية."],
  ["Todavía cometo muchos errores.", "ما زلت أرتكب أخطاء كثيرة."],
  ["No pasa nada si me equivoco.", "لا بأس إذا أخطأت."],
  ["Cada día aprendo algo nuevo.", "كل يوم أتعلم شيئاً جديداً."],
  ["Estoy mejorando poco a poco.", "أتحسن تدريجياً."],

  ["¿Dónde está el hospital?", "أين المستشفى؟"],
  ["Necesito un médico.", "أحتاج إلى طبيب."],
  ["Necesito una farmacia.", "أحتاج إلى صيدلية."],
  ["¿Hay una farmacia cerca?", "هل توجد صيدلية قريبة؟"],
  ["No me encuentro bien.", "لا أشعر أنني بخير."],
  ["Me duele la cabeza.", "رأسي يؤلمني."],
  ["Tengo dolor de garganta.", "لدي ألم في الحلق."],
  ["¿Puedes llamar a un médico?", "هل يمكنك الاتصال بطبيب؟"],
  ["Necesito ayuda.", "أحتاج إلى المساعدة."],
  ["¿Dónde puedo comprar medicamentos?", "أين يمكنني شراء الأدوية؟"],
  ["Tengo una cita con el médico.", "لدي موعد مع الطبيب."],
  ["¿A qué hora abre la farmacia?", "في أي ساعة تفتح الصيدلية؟"],
  ["¿A qué hora cierra?", "في أي ساعة تغلق؟"],
  ["Necesito comprar algo para el dolor.", "أحتاج إلى شراء شيء للألم."],
  ["Quiero hablar con el farmacéutico.", "أريد التحدث مع الصيدلي."],
  ["Tengo que cuidar mi salud.", "يجب أن أعتني بصحتي."],
  ["Hoy necesito dormir bien.", "أحتاج إلى النوم جيداً اليوم."],
  ["Voy a beber más agua.", "سأشرب المزيد من الماء."],
  ["Espero sentirme mejor mañana.", "آمل أن أشعر بتحسن غداً."],

  ["Quiero visitar España algún día.", "أريد زيارة إسبانيا يوماً ما."],
  ["Me gustaría conocer Madrid.", "أود زيارة مدريد."],
  ["Quiero visitar Barcelona.", "أريد زيارة برشلونة."],
  ["Me interesa la cultura española.", "الثقافة الإسبانية تهمني."],
  ["Quiero probar la comida local.", "أريد تجربة الطعام المحلي."],
  ["¿Qué lugares recomiendas?", "ما الأماكن التي تنصح بها؟"],
  ["¿Cuál es el lugar más famoso?", "ما المكان الأكثر شهرة؟"],
  ["¿Cómo llego al museo?", "كيف أصل إلى المتحف؟"],
  ["¿Cuánto cuesta la entrada?", "كم سعر الدخول؟"],
  ["¿A qué hora abre el museo?", "في أي ساعة يفتح المتحف؟"],
  ["¿A qué hora cierra?", "في أي ساعة يغلق؟"],
  ["Quiero hacer algunas fotos.", "أريد التقاط بعض الصور."],
  ["¿Puedo hacer una foto aquí?", "هل يمكنني التقاط صورة هنا؟"],
  ["Este lugar es precioso.", "هذا المكان جميل جداً."],
  ["La vista es increíble.", "الإطلالة رائعة."],
  ["Quiero comprar recuerdos.", "أريد شراء تذكارات."],
  ["Necesito un mapa de la ciudad.", "أحتاج إلى خريطة للمدينة."],
  ["¿Hay un hotel cerca?", "هل يوجد فندق قريب؟"],
  ["¿Dónde puedo comer cerca de aquí?", "أين يمكنني تناول الطعام بالقرب من هنا؟"],
  ["Estoy disfrutando mucho del viaje.", "أنا أستمتع بالرحلة كثيراً."],

  ["Tengo que organizar mi día.", "يجب أن أنظم يومي."],
  ["Primero voy a desayunar.", "أولاً سأفطر."],
  ["Después voy a trabajar.", "بعد ذلك سأعمل."],
  ["Luego voy a hacer compras.", "ثم سأذهب للتسوق."],
  ["Por la tarde voy a estudiar.", "بعد الظهر سأدرس."],
  ["Por la noche voy a descansar.", "في المساء سأرتاح."],
  ["Tengo muchas cosas que hacer.", "لدي أشياء كثيرة لأفعلها."],
  ["Hoy estoy bastante ocupado.", "أنا مشغول جداً اليوم."],
  ["Mañana tendré más tiempo.", "غداً سيكون لدي وقت أكثر."],
  ["Quiero terminar todo hoy.", "أريد إنهاء كل شيء اليوم."],
  ["Necesito hacer una lista.", "أحتاج إلى إعداد قائمة."],
  ["Voy a escribirlo para no olvidarlo.", "سأكتبه حتى لا أنساه."],
  ["No quiero olvidar mi cita.", "لا أريد أن أنسى موعدي."],
  ["Tengo que comprar comida.", "يجب أن أشتري الطعام."],
  ["Tengo que lavar la ropa.", "يجب أن أغسل الملابس."],
  ["Tengo que limpiar el baño.", "يجب أن أنظف الحمام."],
  ["Tengo que responder algunos mensajes.", "يجب أن أرد على بعض الرسائل."],
  ["Tengo que descansar esta noche.", "يجب أن أرتاح الليلة."],
  ["Quiero acostarme temprano.", "أريد الذهاب إلى السرير مبكراً."],
  ["Mañana será otro día.", "غداً يوم آخر."],

  ["¿Puedes abrir la puerta?", "هل يمكنك فتح الباب؟"],
  ["¿Puedes cerrar la puerta?", "هل يمكنك إغلاق الباب؟"],
  ["¿Puedes traerme agua?", "هل يمكنك إحضار الماء لي؟"],
  ["¿Puedes traerme una silla?", "هل يمكنك إحضار كرسي لي؟"],
  ["¿Puedes esperar aquí?", "هل يمكنك الانتظار هنا؟"],
  ["¿Puedes venir conmigo?", "هل يمكنك المجيء معي؟"],
  ["¿Puedes decirme la verdad?", "هل يمكنك قول الحقيقة لي؟"],
  ["¿Puedes mostrarme eso?", "هل يمكنك أن تريني ذلك؟"],
  ["¿Puedes escribirlo?", "هل يمكنك كتابته؟"],
  ["¿Puedes leerlo?", "هل يمكنك قراءته؟"],
  ["¿Puedes hablar más despacio?", "هل يمكنك التحدث ببطء أكثر؟"],
  ["¿Puedes repetir la última palabra?", "هل يمكنك تكرار الكلمة الأخيرة؟"],
  ["¿Puedes explicarlo otra vez?", "هل يمكنك شرحه مرة أخرى؟"],
  ["¿Puedes ayudarme a encontrarlo?", "هل يمكنك مساعدتي في العثور عليه؟"],
  ["¿Puedes reservar una mesa?", "هل يمكنك حجز طاولة؟"],
  ["¿Puedes llamar a un taxi?", "هل يمكنك طلب سيارة أجرة؟"],
  ["¿Puedes enviarme la información?", "هل يمكنك إرسال المعلومات لي؟"],
  ["¿Puedes guardar esto para mí?", "هل يمكنك الاحتفاظ بهذا لي؟"],
  ["¿Puedes recordármelo mañana?", "هل يمكنك تذكيري به غداً؟"],
  ["¿Puedes venir un poco antes?", "هل يمكنك المجيء أبكر قليلاً؟"],

  ["Quiero ahorrar un poco de dinero.", "أريد توفير بعض المال."],
  ["Hoy no quiero gastar mucho.", "اليوم لا أريد إنفاق الكثير."],
  ["Necesito pagar una factura.", "أحتاج إلى دفع فاتورة."]
];


// تحويل الجزء الأول من [إسباني، عربي]
// إلى نفس صيغة الجزء الثاني
for (let i = 0; i < phrases.length; i++) {
  phrases[i] = {
    spanish: phrases[i][0],
    arabic: phrases[i][1]
  };
}

// إضافة الجمل 251 إلى 500
phrasesPart2.forEach(function(item) {
  phrases.push({
    spanish: item[0],
    arabic: item[1]
  });
});


// فحص العدد
console.log("عدد الجمل:", phrases.length);

if (phrases.length !== 500) {
  throw new Error(
    "⚠️ خطأ: عدد الجمل ليس 500! العدد الحالي: " + phrases.length
  );
}

console.log("✅ ممتاز! يوجد بالضبط 500 جملة.");


// عناصر الصفحة
const container = document.getElementById("phrases-list");
const searchInput = document.getElementById("searchInput");


// عرض الجمل
function renderPhrases(list) {
  container.innerHTML = "";

  if (list.length === 0) {
    container.innerHTML =
      '<div class="phrase-card"><div class="arabic">لا توجد نتائج.</div></div>';
    return;
  }

  list.forEach(function(item) {
    const card = document.createElement("div");
    card.className = "phrase-card";

    const textContent = document.createElement("div");
    textContent.className = "text-content";

    const spanishDiv = document.createElement("div");
    spanishDiv.className = "spanish";

    // الترقيم الأصلي يبقى ثابتاً حتى أثناء البحث
    spanishDiv.textContent =
      (phrases.indexOf(item) + 1) + ". " + item.spanish;

    const arabicDiv = document.createElement("div");
    arabicDiv.className = "arabic";
    arabicDiv.textContent = item.arabic;

    const button = document.createElement("button");
    button.textContent = "🔊 نطق";

    button.addEventListener("click", function() {
      speakSpanish(item.spanish);
    });

    textContent.appendChild(spanishDiv);
    textContent.appendChild(arabicDiv);

    card.appendChild(textContent);
    card.appendChild(button);

    container.appendChild(card);
  });
}


// النطق بالإسبانية
function speakSpanish(text) {
  window.speechSynthesis.cancel();

  const utterance = new SpeechSynthesisUtterance(text);

  utterance.lang = "es-ES";
  utterance.rate = 0.9;
  utterance.pitch = 1;

  window.speechSynthesis.speak(utterance);
}


// البحث بالعربي والإسباني
searchInput.addEventListener("input", function() {
  const searchText =
    searchInput.value.trim().toLowerCase();

  if (searchText === "") {
    renderPhrases(phrases);
    return;
  }

  const filteredPhrases = phrases.filter(function(item) {
    return (
      item.spanish.toLowerCase().includes(searchText) ||
      item.arabic.toLowerCase().includes(searchText)
    );
  });

  renderPhrases(filteredPhrases);
});


// تشغيل الجمل
renderPhrases(phrases);