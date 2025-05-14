<script>
    import Footer from '$lib/components/footer.svelte';
</script>

<main class="flex flex-col min-h-screen bg-gray-900 text-white">
    <div class="flex-grow flex items-center justify-center py-8">
        <div class="max-w-4xl p-8 w-full">
            <h1 class="text-5xl font-bold mb-10 text-center">Hogyan legyél ingyenélő</h1>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div class="bg-gray-800 rounded-lg p-6 hover:bg-gray-700 transition-all shadow-xl flex flex-col">
                    <h2 class="text-2xl font-bold mb-4 text-blue-400">Ingyen Mobilnet</h2>
                    <p class="text-gray-300 mb-4">Ingyenes mobil internet elérésére külső szolgáltatásokon keresztül.</p>
                    <div class="mt-auto">
                        <a href="./ingyen-mobilnet/" class="inline-block bg-blue-600 hover:bg-blue-700 text-white font-semibold py-2 px-4 rounded transition-colors">
                            Részletek
                        </a>
                    </div>
                </div>
                
                <div class="bg-gray-800 rounded-lg p-6 hover:bg-gray-700 transition-all shadow-xl flex flex-col">
                    <h2 class="text-2xl font-bold mb-4 text-green-400">V2Ray V2mess Szerver Hostolás</h2>
                    <p class="text-gray-300 mb-4">Saját V2Ray szerver létrehozásának lépései és konfiguráció.</p>
                    <div class="mt-auto">
                        <a href="#" class="inline-block bg-gray-600 cursor-not-allowed text-gray-400 font-semibold py-2 px-4 rounded transition-colors">
                            Hamarosan
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="pb-4">
        <Footer />
    </div>
</main>
