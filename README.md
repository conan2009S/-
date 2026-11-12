
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>𝒇ℓ𝑜𝑟𝑒 𝒔𝒉𝒂𝒊𝒎𝒂 - تصميم بوكيه خاص</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts: Cairo & Playfair Display -->
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;500;600;700;800&family=Playfair+Display:ital,wght@1,600;1,700&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        brand: {
                            50: '#fdf4f5',
                            100: '#fbe8eb',
                            200: '#f7d5db',
                            300: '#f0b4c0',
                            400: '#e5889e',
                            500: '#d75f7c',
                            600: '#c24161',
                            700: '#a3304c',
                            800: '#882b43',
                            900: '#73293c',
                        },
                        sage: {
                            50: '#f4f7f4',
                            100: '#e4ece4',
                            500: '#7c9a7c',
                            700: '#526b52'
                        }
                    },
                    fontFamily: {
                        cairo: ['Cairo', 'sans-serif'],
                        brandFont: ['Playfair Display', 'serif']
                    }
                }
            }
        }
    </script>
    <style>
        body {
            font-family: 'Cairo', sans-serif;
            background-color: #eccddd;
            color: #33272a;
        }
        .brand-title {
            font-family: 'Playfair Display', serif;
            font-style: italic;
            letter-spacing: 1px;
        }
        .custom-shadow {
            box-shadow: 0 10px 30px -5px rgba(215, 95, 124, 0.1);
        }
        .custom-card-active {
            border-color: #e794a7 !important;
            background-color: #ad3d4a !important;
            transform: translateY(-2px);
        }
        .ribbon-option.selected {
            ring-width: 4px;
            ring-color: #c53355;
            transform: scale(1.1);
        }
    </style>
</head>
<body class="pb-16 pt-4">

    <!-- Header / Branding -->
    <header class="max-w-4xl mx-auto px-4 mb-8">
        <div class="bg-white/80 backdrop-blur-md rounded-3xl p-6 md:p-8 text-center border border-brand-100 custom-shadow relative overflow-hidden">
            <div class="absolute -top-10 -right-10 w-32 h-32 bg-brand-100 rounded-full blur-2xl opacity-60"></div>
            <div class="absolute -bottom-10 -left-10 w-32 h-32 bg-brand-200 rounded-full blur-2xl opacity-60"></div>
            
            <span class="inline-block px-4 py-1 rounded-full bg-brand-50 text-brand-600 text-xs font-semibold mb-2 border border-brand-200">
                <i class="fa-solid font-sparkles text-brand-500 ml-1"></i> متجر الورود العصري
            </span>
            <h1 class="text-4xl md:text-5xl font-extrabold text-brand-700 brand-title mb-2 tracking-wide">
                𝒇ℓ𝑜𝑟𝑒 𝒔𝒉𝒂𝒊𝒎𝒂
            </h1>
            <p class="text-gray-500 font-medium text-lg flex items-center justify-center gap-2">
                <span class="h-0.5 w-8 bg-brand-300 rounded-full"></span>
                <span>اختاري تصميمك الخاص</span>
                <span class="h-0.5 w-8 bg-brand-300 rounded-full"></span>
            </p>
        </div>
    </header>

<main class="max-w-4xl mx-auto px-4 space-y-8">
        <!-- 1. أنواع الورود (اختيار متعدد) -->
        <section class="bg-white rounded-3xl p-6 md:p-8 border border-gray-100 custom-shadow">
            <div class="flex items-center justify-between mb-6">
                <div>
                    <h2 class="text-xl font-bold text-gray-800 flex items-center gap-2">
                        <span class="w-8 h-8 rounded-full bg-brand-100 text-brand-600 flex items-center justify-center text-sm font-extrabold">1</span>
                        أنواع الورود
                    </h2>
                    <p class="text-xs text-gray-400 mt-1">يمكنك اختيار نوع واحد أو عدة أنواع بحرية</p>
                </div>
                <span class="text-xs bg-brand-50 text-brand-600 px-3 py-1 rounded-full border border-brand-200 font-medium" id="selectedFlowersCount">0 محدد</span>
            </div>

            <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-4" id="flowersGrid">
                <!-- Rose items dynamically generated or static HTML -->
                <!-- Item 1 -->
                <div onclick="toggleFlower(this, 'باقة صغيره (bouquet)')" data-name="باقةصغيره (bouquet)" class="flower-card cursor-pointer border-2 border-gray-100 rounded-2xl p-3 text-center transition-all duration-300 hover:border-brand-300 relative group">
                    <div class="check-badge hidden absolute top-2 left-2 w-6 h-6 bg-brand-500 text-white rounded-full flex items-center justify-center text-xs shadow-sm">
                        <i class="fa-solid fa-check"></i>
                    </div>
                    <div class="w-full h-28 rounded-xl bg-gray-50 mb-3 overflow-hidden flex items-center justify-center">
                        <img src="https://images.unsplash.com/photo-1518709268805-4e9042af9f23?auto=format&fit=crop&w=300&q=80" alt="باقةصغيره" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300" onerror="this.src='https://placehold.co/200x200/fbe8eb/73293c?text=جوري'">
                    </div>
                    <h3 class="font-bold text-gray-700 text-sm">باقة صغيره</h3>
                    <p class="text-xs text-gray-400">bouquet</p>
                </div>
    
    <!-- Item 2: توليب -->
    <div onclick="toggleFlower(this, 'توليب (Tulips)')" data-name="توليب (Tulips)" class="flower-card cursor-pointer border-2 border-gray-100 rounded-2xl p-3 text-center transition-all duration-300 hover:border-brand-300 relative group">
        <div class="check-badge hidden absolute top-2 left-2 w-6 h-6 bg-brand-500 text-white rounded-full flex items-center justify-center text-xs shadow-sm">
            <i class="fa-solid fa-check"></i>
        </div>
        <div class="w-full h-28 rounded-xl bg-gray-50 mb-3 overflow-hidden flex items-center justify-center p-1">
            <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVR42mNkYAAAAAYAAjCB0C8AAAAASUVORK5CYII=" data-real-img="tulip" alt="توليب" class="w-full h-full object-contain group-hover:scale-105 transition-transform duration-350" onerror="this.src='https://images.unsplash.com/photo-1520763185298-1b434c919102?auto=format&fit=crop&w=300&q=80'">
        </div>
        <h3 class="font-bold text-gray-700 text-sm">توليب</h3>
        <p class="text-xs text-gray-400">Tulips</p>
    </div>

<!-- Item 3: ليليوم -->
    <div onclick="toggleFlower(this, 'ليليوم (Lilies)')" data-name="ليليوم (Lilies)" class="flower-card cursor-pointer border-2 border-gray-100 rounded-2xl p-3 text-center transition-all duration-300 hover:border-brand-300 relative group">
        <div class="check-badge hidden absolute top-2 left-2 w-6 h-6 bg-brand-500 text-white rounded-full flex items-center justify-center text-xs shadow-sm">
            <i class="fa-solid fa-check"></i>
        </div>
        <div class="w-full h-28 rounded-xl bg-gray-50 mb-3 overflow-hidden flex items-center justify-center p-1">
            <img src="lilium.png" alt="ليليوم" class="w-full h-full object-contain group-hover:scale-105 transition-transform duration-300" onerror="this.src='https://images.unsplash.com/photo-1582794543139-8ac9cb0f7b11?auto=format&fit=crop&w=300&q=80'">
        </div>
        <h3 class="font-bold text-gray-700 text-sm">ليليوم</h3>
        <p class="text-xs text-gray-400">Lilies</p>
    </div>

    <!-- Item 4: دوار الشمس -->
    <div onclick="toggleFlower(this, 'دوار الشمس (Sunflower)')" data-name="دوار الشمس (Sunflower)" class="flower-card cursor-pointer border-2 border-gray-100 rounded-2xl p-3 text-center transition-all duration-300 hover:border-brand-300 relative group">
        <div class="check-badge hidden absolute top-2 left-2 w-6 h-6 bg-brand-500 text-white rounded-full flex items-center justify-center text-xs shadow-sm">
            <i class="fa-solid fa-check"></i>
        </div>
        <div class="w-full h-28 rounded-xl bg-gray-50 mb-3 overflow-hidden flex items-center justify-center p-1">
            <img src="sunflower.png" alt="دوار الشمس" class="w-full h-full object-contain group-hover:scale-105 transition-transform duration-300" onerror="this.src='https://images.unsplash.com/photo-1597848212624-a19eb35e2651?auto=format&fit=crop&w=300&q=80'">
        </div>
        <h3 class="font-bold text-gray-700 text-sm">دوار الشمس</h3>
        <p class="text-xs text-gray-400">Sunflower</p>
    </div>

    <!-- Item 5: كركديه -->
    <div onclick="toggleFlower(this, 'كركديه (Hibiscus)')" data-name="كركديه (Hibiscus)" class="flower-card cursor-pointer border-2 border-gray-100 rounded-2xl p-3 text-center transition-all duration-300 hover:border-brand-300 relative group">
        <div class="check-badge hidden absolute top-2 left-2 w-6 h-6 bg-brand-500 text-white rounded-full flex items-center justify-center text-xs shadow-sm">
            <i class="fa-solid fa-check"></i>
        </div>
        <div class="w-full h-28 rounded-xl bg-gray-50 mb-3 overflow-hidden flex items-center justify-center p-1">
            <img src="hibiscus.png" alt="كركديه" class="w-full h-full object-contain group-hover:scale-105 transition-transform duration-300" onerror="this.src='https://images.unsplash.com/photo-1550950158-d0d960dff51b?auto=format&fit=crop&w=300&q=80'">
        </div>
        <h3 class="font-bold text-gray-700 text-sm">كركديه</h3>
        <p class="text-xs text-gray-400">Hibiscus</p>
    </div>

    <!-- Item 6: جربيرا -->
    <div onclick="toggleFlower(this, 'جربيرا (Gerbera)')" data-name="جربيرا (Gerbera)" class="flower-card cursor-pointer border-2 border-gray-100 rounded-2xl p-3 text-center transition-all duration-300 hover:border-brand-300 relative group">
        <div class="check-badge hidden absolute top-2 left-2 w-6 h-6 bg-brand-500 text-white rounded-full flex items-center justify-center text-xs shadow-sm">
            <i class="fa-solid fa-check"></i>
        </div>
        <div class="w-full h-28 rounded-xl bg-gray-50 mb-3 overflow-hidden flex items-center justify-center p-1">
            <img src="gerbera.png" alt="جربيرا" class="w-full h-full object-contain group-hover:scale-105 transition-transform duration-300" onerror="this.src='https://images.unsplash.com/photo-1563241527-3004b7be0ffd?auto=format&fit=crop&w=300&q=80'">
        </div>
        <h3 class="font-bold text-gray-700 text-sm">جربيرا</h3>
        <p class="text-xs text-gray-400">Gerbera</p>
    </div>

<!-- Item 7 -->
                <div onclick="toggleFlower(this, 'جيربيرا (Gerbera)')" data-name="جيربيرا (Gerbera)" class="flower-card cursor-pointer border-2 border-gray-100 rounded-2xl p-3 text-center transition-all duration-300 hover:border-brand-300 relative group">
                    <div class="check-badge hidden absolute top-2 left-2 w-6 h-6 bg-brand-500 text-white rounded-full flex items-center justify-center text-xs shadow-sm">
                        <i class="fa-solid fa-check"></i>
                    </div>
                    <div class="w-full h-28 rounded-xl bg-gray-50 mb-3 overflow-hidden flex items-center justify-center">
                        <img src="https://images.unsplash.com/photo-1567696911980-2eed69a46042?auto=format&fit=crop&w=300&q=80" alt="جيربيرا" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300" onerror="this.src='https://placehold.co/200x200/fbe8eb/73293c?text=جيربيرا'">
                    </div>
                    <h3 class="font-bold text-gray-700 text-sm">جيربيرا</h3>
                    <p class="text-xs text-gray-400">Gerbera</p>
                </div>

                <!-- Item 8 -->
                <div onclick="toggleFlower(this, 'هيدرانجيا (Hydrangea)')" data-name="هيدرانجيا (Hydrangea)" class="flower-card cursor-pointer border-2 border-gray-100 rounded-2xl p-3 text-center transition-all duration-300 hover:border-brand-300 relative group">
                    <div class="check-badge hidden absolute top-2 left-2 w-6 h-6 bg-brand-500 text-white rounded-full flex items-center justify-center text-xs shadow-sm">
                        <i class="fa-solid fa-check"></i>
                    </div>
                    <div class="w-full h-28 rounded-xl bg-gray-50 mb-3 overflow-hidden flex items-center justify-center">
                        <img src="https://images.unsplash.com/photo-1508610048659-a06b669e3321?auto=format&fit=crop&w=300&q=80" alt="هيدرانجيا" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300" onerror="this.src='https://placehold.co/200x200/fbe8eb/73293c?text=هيدرانجيا'">
                    </div>
                    <h3 class="font-bold text-gray-700 text-sm">هيدرانجيا</h3>
                    <p class="text-xs text-gray-400">Hydrangea</p>
                </div>
            </div>
        </section>

        <!-- 2. نمط الأطراف والألوان -->
        <section class="bg-white rounded-3xl p-6 md:p-8 border border-gray-100 custom-shadow">
            <h2 class="text-xl font-bold text-gray-800 flex items-center gap-2 mb-6">
                <span class="w-8 h-8 rounded-full bg-brand-100 text-brand-600 flex items-center justify-center text-sm font-extrabold">2</span>
                تفاصيل نمط وألوان الورد
            </h2>

<!-- نمط الأطراف -->
            <div class="mb-6">
                <label class="block text-sm font-semibold text-gray-700 mb-3">اختر شكل الأطراف لكل ورده:</label>
                <div class="grid grid-cols-2 gap-4">
                    <label class="edge-option cursor-pointer border-2 border-brand-500 bg-brand-50/50 p-4 rounded-2xl text-center flex items-center justify-center gap-3 transition-all" onclick="selectEdge(this, 'عادي')">
                        <input type="radio" name="edge_style" value="عادي" checked class="hidden">
                        <span class="w-5 h-5 rounded-full border-2 border-brand-500 flex items-center justify-center">
                            <span class="w-2.5 h-2.5 rounded-full bg-brand-500"></span>
                        </span>
                        <span class="font-bold text-gray-800">عادي (Standard)</span>
                    </label>
                    <label class="edge-option cursor-pointer border-2 border-gray-200 p-4 rounded-2xl text-center flex items-center justify-center gap-3 transition-all" onclick="selectEdge(this, 'كيرلي')">
                        <input type="radio" name="edge_style" value="كيرلي" class="hidden">
                        <span class="w-5 h-5 rounded-full border-2 border-gray-300 flex items-center justify-center">
                            <span class="w-2.5 h-2.5 rounded-full bg-transparent"></span>
                        </span>
                        <span class="font-bold text-gray-800">كيرلي (Curly)</span>
                    </label>
                </div>
            </div>

            <!-- ألوان الورود والأطراف -->
            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                <div>
                    <label for="flowerColor" class="block text-sm font-semibold text-gray-700 mb-2">
                        <i class="fa-solid fa-palette text-brand-500 ml-1"></i> لون الورده:
                    </label>
                    <input type="text" id="flowerColor" placeholder="مثال: أحمر، وردي فوشي، أبيض ونودي..." 
                           class="w-full px-4 py-3 rounded-xl border border-gray-200 focus:border-brand-500 focus:ring-2 focus:ring-brand-200 outline-none transition-all text-sm">
                </div>

                <div>
                    <label for="edgeColor" class="block text-sm font-semibold text-gray-700 mb-2">
                        <i class="fa-solid fa-paint-brush text-brand-500 ml-1"></i> لون الأطراف:
                    </label>
                    <input type="text" id="edgeColor" placeholder="مثال: ذهبي، أبيض، وردي غامق..." 
                           class="w-full px-4 py-3 rounded-xl border border-gray-200 focus:border-brand-500 focus:ring-2 focus:ring-brand-200 outline-none transition-all text-sm">
                </div>
            </div>
        </section>

        <!-- 3. تصاميم البوكيهات الخاصة بالمتجر -->
        <section class="bg-white rounded-3xl p-6 md:p-8 border border-gray-100 custom-shadow">
            <div class="mb-6">
                <h2 class="text-xl font-bold text-gray-800 flex items-center gap-2">
                    <span class="w-8 h-8 rounded-full bg-brand-100 text-brand-600 flex items-center justify-center text-sm font-extrabold">3</span>
                    بوكيهات وتصاميم المتجر الخاصة
                </h2>
                <p class="text-xs text-gray-400 mt-1">تصاميم هِندسية ثابتة الشكل، ويتغير لون الورد حسب طلبك</p>
            </div>

<div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">
                <!-- Bouquet 1 -->
                <div onclick="selectBouquet(this, 'بوكيه كلاسيك فلور 𝒇ℓ𝑜𝑟𝑒')" class="bouquet-card cursor-pointer border-2 border-gray-100 rounded-2xl p-4 transition-all duration-300 hover:border-brand-300 relative">
                    <div class="w-full h-40 rounded-xl bg-gray-50 mb-3 overflow-hidden">
                        <img src="c:\Users\TOSHIBA\Desktop\فلور\صور\حامل اكسسوار_2026-11-10_20-38-53.jpg" alt="بوكيه كلاسيك" class="w-full h-full object-cover" onerror="this.src='https://placehold.co/300x200/fbe8eb/73293c?text=بوكيه+كلاسيك'">
                    </div>
                    <span class="text-xs font-semibold text-brand-600 bg-brand-50 px-2.5 py-0.5 rounded-md inline-block mb-1">تصميم ثابت الشكل</span>
                    <h3 class="font-bold text-gray-800 text-sm">🪷 حامل اكسسوار مضيئ 𝒇ℓ𝑜𝑟𝑒</h3>
                    <p class="text-xs text-gray-400 mt-1">ترتيب دائري فخم ومكثف</p>
                </div>

                <!-- Bouquet 2 -->
                <div onclick="selectBouquet(this, 'بوكيه عصري مودرن')" class="bouquet-card cursor-pointer border-2 border-gray-100 rounded-2xl p-4 transition-all duration-300 hover:border-brand-300 relative">