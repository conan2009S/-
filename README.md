# -<!DOCTYPE html>
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