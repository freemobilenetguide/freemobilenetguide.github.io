<script>
    import Footer from '$lib/components/footer.svelte';
</script>
<main class="flex items-center justify-center min-h-screen bg-gray-900 text-white">
  <div class="max-w-2xl p-8">
    <a href="../" class="inline-block mb-6 text-blue-400 hover:underline">← Vissza a főoldalra</a>
    <h1 class="text-4xl font-bold mb-6">Ingyen Mobilnet Method Skellytől</h1>
    
    <div class="space-y-6 text-gray-300">
       <div class="bg-red-900/30 border-l-4 border-red-800 p-3 rounded-r-md mt-3">
        <p class="text-red-400">
          ⚠️ <strong>Fontos tudnivalók:</strong>
          <ul class="list-disc list-inside space-y-2 mt-2">
            <li>Kevés, de <strong>megvan az esély hogy lekorlátozzák vagy letiltják a SIM kártyádat</strong></li>
            <li>Csak <strong>saját felelősségre</strong> használd, vagy olyan SIM kártyával amit nem sajnálsz</li>
            <li>A leírtak <strong>kizárólag oktatási célból</strong> lettek megosztva</li>
            <li>Az alábbiakban leírt módszer nagy valószínűséggel a SIM szolgáltatód <strong>ÁSZF-e ellen van</strong></li>
            <li>Ha a telefonod támogatja a <strong>Dual SIM-et</strong>, ajánlott egy új, olcsó SIM kártyát használni</li>
            <li>A SIM aktiválásához <strong>minimum 14 éves életkor szükséges</strong></li>
          </ul>
      </div>

      
      <div class="bg-gray-800 rounded-lg p-4 shadow-md mb-8">
        <h2 class="text-2xl font-semibold mb-3 text-white">Tartalomjegyzék</h2>
        <ul class="space-y-2">
          <li>
            <a href="#zero-rated" class="text-blue-400 hover:underline flex items-center">
              <span class="mr-2">1.</span> Zero Rated oldal keresése
            </a>
          </li>
          <li>
            <a href="#vmess-server" class="text-green-400 hover:underline flex items-center">
              <span class="mr-2">2.</span> V2Ray VMESS szerver beszerzése
            </a>
          </li>
          <li>
            <a href="#apps" class="text-purple-400 hover:underline flex items-center">
              <span class="mr-2">3.</span> Szükséges alkalmazások
            </a>
          </li>
          <li>
            <a href="#settings" class="text-yellow-400 hover:underline flex items-center">
              <span class="mr-2">4.</span> Beállítások
            </a>
          </li>
          <li>
            <a href="#connection" class="text-blue-400 hover:underline flex items-center">
              <span class="mr-2">5.</span> Csatlakozás
            </a>
          </li>
          <li>
            <a href="#hotspot" class="text-green-400 hover:underline flex items-center">
              <span class="mr-2">6.</span> Hotspot megosztás
            </a>
          </li>
          <li>
            <a href="#troubleshooting" class="text-red-400 hover:underline flex items-center">
              <span class="mr-2">7.</span> Hibaelhárítás
            </a>
          </li>
        </ul>
      </div>
      
      <div id="zero-rated" class="bg-gray-800 rounded-lg p-4 mb-6 shadow-md">
        <h2 class="text-2xl font-semibold mb-3 text-blue-400">Első lépés: Zero Rated oldal keresése</h2>
        <p class="mb-3">Először is mielőtt elkezdenéd, kell keresned egy <span class="font-semibold text-blue-300">"zero rated" oldalt</span>. Ez azt jelenti hogy a sim szolgáltatód megengedi hogy felmenj egy megadott oldalra/oldalakra mobilnet nélkül is.</p>
        
        <p>A szolgáltatók általába meg szokták engedni hogy felmenj a saját oldalukra úgy is hogyha elfogyott a mobilneted. Például:</p>
        
        <div class="bg-gray-700 p-3 rounded-md my-3">
          <ul class="list-disc list-inside pl-2 space-y-1">
            <li><span class="font-semibold">Yettel:</span> <code class="bg-gray-600 p-1 rounded">yettel.hu</code>, <code class="bg-gray-600 p-1 rounded">speedtest.net</code>, <code class="bg-gray-600 p-1 rounded">fast.com</code></li>
            <li><span class="font-semibold">Telekom:</span> Sajnos nem működik (kiírja, hogy nincs net)</li>
            <li><span class="font-semibold">Vodafone (One):</span> Sajnos nem működik itt se</li>
          </ul>
        </div>
        
        <div class="bg-yellow-900/30 border-l-4 border-yellow-500 p-3 rounded-r-md mt-3">
          <p class="text-yellow-300">⚠️ Sajnos van olyanra esély hogy nem fognak menni az oldalak, tehát ez személytől is függ hogy megy vagy nem.</p>
        </div>
      </div>
      
      <div id="vmess-server" class="bg-gray-800 rounded-lg p-4 mb-6 shadow-md">
        <h2 class="text-2xl font-semibold mb-3 text-green-400">V2Ray VMESS szerver beszerzése</h2>
        <p class="mb-3">Ha sikerült találnod egy zero rated oldalt, akkor kell szerezz egy V2Ray VMESS szervert.</p>
        <ol class="list-disc list-inside space-y-2 pl-2 my-3">
          <li>Ezt akár saját szervereddel is bírod hosztolni</li>
          <li>
            Az egyszerűség kedvéért itt van két oldal, ahol ingyen tudsz szervert generálni:
            <ul class="list-disc list-inside pl-4 text-blue-400">
              <li><a href="https://sshs8.com/v2ray-best-vmess-server/" class="text-blue-400">sshs8.com </a></li>
              <li><a href="https://www.vpnjantit.com/free-v2ray-vmess" class="text-blue-400">vpnjantit.com <span class="text-white">(itt akár néhány száz forintért több hónapos prémium szervert is vásárolhatsz. Ez nem kötelező, de ajánlott, ha nem szeretnél hetente új szervert generálni.)</span></a></li>
            </ul>
          </li>
          <li>Válaszd ki az egyik legközelebbi szervert (pl. Németország) a kis késés érdekében</li>
          <li>Írj be egy random jelszót, majd nyomj rá, hogy <span class="font-bold">"Create an Account"</span></li>
          <li>Másold ki az <span class="font-bold">"Link no TLS"</span> értéket az adatok közül</li>

        </ol>
        



        
        <div class="bg-blue-900/30 border-l-4 border-blue-500 p-3 rounded-r-md mt-3">
          <p class="text-blue-300">💡 Ez egy komplett link, amivel nem kell egyesével kimásolnod az adatokat hanem csak simán be tudd illeszteni ezt az appba ami kelleni fog ehhez.</p>
        </div>
      </div>
      
      <div id="apps" class="bg-gray-800 rounded-lg p-4 mb-6 shadow-md">
        <h2 class="text-2xl font-semibold mb-3 text-purple-400">Szükséges alkalmazások</h2>
        <div class="flex flex-col md:flex-row md:space-x-4 space-y-3 md:space-y-0 my-3">
          <div class="flex-1 bg-gray-700 p-3 rounded">
            <h3 class="font-semibold text-lg mb-2">Android</h3>
            <a href="https://play.google.com/store/apps/details?id=com.v2ray.ang" class="flex items-center text-blue-400 underline">
              <span class="mr-2">v2rayNG</span>
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
              </svg>
            </a>
          </div>
          <div class="flex-1 bg-gray-700 p-3 rounded">
            <h3 class="font-semibold text-lg mb-2">iOS</h3>
            <a href="https://apps.apple.com/app/v2box-v2ray-client/id6446042241" class="flex items-center text-blue-400 underline">
              <span class="mr-2">V2Box</span>
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
              </svg>
            </a>
          </div>
        </div>
      </div>
      
      <div id="settings" class="bg-gray-800 rounded-lg p-4 mb-6 shadow-md">
        <h2 class="text-2xl font-semibold mb-3 text-yellow-400">Beállítások</h2>
        
        <div class="mb-4">
          <h3 class="font-semibold text-lg mb-2">Alapbeállítás mindkét platformon:</h3>
          <ol class="list-decimal list-inside space-y-2 pl-2">
            <li><strong>Android:</strong> Nyomd meg a "+" gombot → "Import config from clipboard"</li>
            <li><strong>iOS:</strong> Nyomd meg a "+" gombot → "Import v2ray URI from clipboard"</li>
            <li>Ha megjelent az új szerver a listán, nyomj rá a szerkesztés gombra</li>
            <li>Keresd meg a <code class="bg-gray-600 p-1 rounded">ws host</code> mezőt (iOS-en: <code class="bg-gray-600 p-1 rounded">Request Host</code>)</li>
          </ol>
        </div>
        
        <div class="bg-gray-700 p-3 rounded my-4">
          <p class="font-semibold mb-2">Ide írd be a zero rated oldalt, például:</p>
          <ul class="list-disc list-inside pl-2 space-y-1">
            <li><code class="bg-gray-600 p-1 rounded">www.speedtest.net</code></li>
            <li><code class="bg-gray-600 p-1 rounded">www.yettel.hu</code></li>
          </ul>
        </div>
        
        <div class="bg-yellow-900/30 border-l-4 border-yellow-500 p-3 rounded-r-md mt-3">
          <p class="text-yellow-300">⚠️ Fontos hogy "www." legyen az elején, majd ha ez megvan akkor mentsd el jobb felül a pipa gombbal vagy iOSen alul Save gomb.</p>
        </div>
      </div>
      
      <div id="connection" class="bg-gray-800 rounded-lg p-4 mb-6 shadow-md">
        <h2 class="text-2xl font-semibold mb-3 text-blue-400">Csatlakozás</h2>
        <p>Már csak annyit kell csinálnod hogy rácsatlakozol a szerverre mobilnetről:</p>
        
        <div class="flex flex-col md:flex-row md:space-x-4 space-y-3 md:space-y-0 my-3">
          <div class="flex-1 bg-gray-700 p-3 rounded">
            <h3 class="font-semibold text-lg mb-2">Android</h3>
            <p>Válaszd ki a szervert, majd nyomd meg a jobb alsó <strong>Start</strong> gombot</p>
          </div>
          <div class="flex-1 bg-gray-700 p-3 rounded">
            <h3 class="font-semibold text-lg mb-2">iOS</h3>
            <p>Válaszd ki a szervert, majd húzd jobbra a <strong>Slide to Connect</strong> csúszkát</p>
          </div>
        </div>
      </div>
      
      <div class="border-t-2 border-gray-700 my-8 relative">

      </div>
      
      <div id="hotspot" class="bg-gray-800 rounded-lg p-4 mb-6 shadow-md">
        <h2 class="text-2xl font-semibold mb-3 text-green-400">Hotspot megosztás</h2>
        
        <div class="mb-4">
          <h3 class="font-semibold text-lg mb-2 text-yellow-300">Megosztás csak böngészéshez (TCP)</h3>
          <p class="mb-3">Ha úgy akarsz netet osztani hogy a másik eszközre ne kelljen appot letölteni akkor a hoszt (amiről osztod a neted) telefonról a "HTTP Injector" appot kell használnod és azon keresztül proxyval osztani hotspotot.</p>
          
          <div class="bg-gray-700 p-3 rounded my-3">
            <p class="text-yellow-300 mb-2">⚠️ Korlátozások:</p>
            <p>Ilyenkor csak is a TCP fog menni a megosztott eszközön és az UDP nem, ez azt jelenti hogy például a böngészőt birja másik eszköz használni de példáúl online játékok nem fognak menni.</p>
            
            <div class="mt-3 border-t border-gray-600 pt-2">
              <ul class="list-disc list-inside pl-2 text-sm">
                <li><strong>TCP:</strong> Közvetlen kapcsolatok (böngészés, email, üzenet küldés)</li>
                <li><strong>UDP:</strong> Gyors, valósidejű csatalkozásokra van használva (játékok - mivel ott számit a késés)</li>
              </ul>
            </div>
          </div>
        </div>
        
        <div class="mb-4">
          <h3 class="font-semibold text-lg mb-2 text-yellow-300">Teljes megosztás (TCP + UDP)</h3>
          <p>Ha úgy akarsz netet osztani hogy a másik eszközön menjen az UDP illetve TCP is azaz működjön rendesen és ne csak félig:</p>
          <ol class="list-decimal list-inside space-y-2 pl-2">
            <li>A másik eszközre is telepíteni kell ugyanazt az appot</li>
            <li>Egy <span style="font-weight: bold;">másik</span>  v2ray szerverrel csatlakozz ugyan úgy a netre az appon keresztül mint a hoszt eszközről</li>
          </ol>
        </div>
        
        <div class="bg-gray-800 border border-gray-700 rounded-lg p-4 mb-4">
          <h3 class="font-semibold text-lg mb-3 text-blue-400">HTTP Injector beállítása részletesen:</h3>
          
          <p class="mb-2">Ha esetleg a másik eszközön nem vagy net közelébe hogy le tudd tölteni az appot:</p>
          
          <ol class="list-decimal list-inside space-y-2 pl-2">
            <li>Azon az eszközön amin van net, töltsd le a HTTP Injector appot (Android és iOS is)</li>
            <li>Menj a Beállitásokba → "V2Ray/Xray"</li>
            <li>Felül nyomj rá a plusz ikonra, majd másold be a v2ray szerver linkjét, vagy másold át egyesével az adatokat. (Ha nincs a vágólapodon a link, exportáld a másik appból a megosztás gombbal a végén)</li>
            <li>A "Core" legyen V2Ray-re állítva (ne Xray-re)</li>
            <li>Vissza a kezdőlapra → Start gomb alatti menü → V2Ray/Xray → Save</li>
            <li>Nyomj rá a Start gombra utána felül "Tools" tab (harmadik lap) → Tethering Tools → Hotshare opció</li>
          </ol>
          
          <div class="bg-blue-900/30 border-l-4 border-blue-500 p-3 rounded-r-md mt-3 mb-4">
            <p class="text-blue-300">💡 A Hotshare opció kell, mivel a legtöbb embernek nincs rootolva/jailbreakelve telefonja.</p>
          </div>
          
          <p class="mb-2">Az app mutatni fogja mit kell csinálnod, de ha nem tudsz angolul:</p>
          <ol class="list-decimal list-inside space-y-2 pl-2">
            <li>Állítsd be a hotspot jelszavát</li>
            <li>Nyomd meg a "Start Wi-Fi Hotspot" gombot</li>
            <li>Pipáld be a "HTTP" opciót</li>
            <li>Nyomd meg a "START HOTSHARE" gombot</li>
          </ol>
          
          <div class="bg-gray-700 p-3 rounded my-3">
            <h4 class="font-semibold mb-2 underline">A másik eszközön:</h4>
            <ol class="list-decimal list-inside space-y-2 pl-2">
              <li>Csatlakozz a megosztott hotspothoz</li>
              <li>Állítsd be a proxyt:
                <ul class="list-disc list-inside pl-4 mt-1 space-y-1">
                  <li><strong>Android:</strong> Wifi csatlakozás előtt manuálisan</li>
                  <li><strong>iOS:</strong> Wifi név → proxy gomb → manuális</li>
                </ul>
              </li>
              <li>Proxy beállítások:
                <ul class="list-disc list-inside pl-4 mt-1 space-y-1">
                  <li>Szerver: <code class="bg-gray-600 p-1 rounded">192.168.0.54</code> (vagy amit mutat)</li>
                  <li>Port: <code class="bg-gray-600 p-1 rounded">44355</code> (vagy amit mutat)</li>
                  <li>A többi mezőt hagyd üresen</li>
                </ul>
              </li>
              <li>Mentsd el és csatlakozz újra a hálózatra</li>
            </ol>
          </div>
          
          <div class="bg-yellow-900/30 border-l-4 border-yellow-500 p-3 rounded-r-md mt-3">
            <p class="text-yellow-300">⚠️ Ilyenkor csak a TCP fog menni, de ez elég ahhoz, hogy az App Store-ból/Play Store-ból letöltsd ugyanazt az appot.</p>
          </div>
        </div>
        
        <div class="mb-4">
          <h3 class="font-semibold text-lg mb-2">Mindkét eszközön v2ray használata:</h3>
          <ol class="list-decimal list-inside space-y-2 pl-2">
            <li>Ha a másik telefonra sikerült letöltened az appot:</li>
            <li>Állítsd le a HTTP Injector appot</li>
            <li>A másik appal oszd meg a hotspotot (vagy HTTP Injector-ból is, de ki kell nyomnod a Hotshare-t)</li>
            <li>A másik eszközön írj vagy másolj be különböző szerver adatot. Ha bírsz, akkor Quick Share-el oszd meg a másik telefonról a szerver linkjét, ha az nem megy akkor egyesével ird be</li>
            <li>Töröld ki a proxy opciót és csatlakozz újra a hotspotra</li>
            <li>Mindkét eszközön be kell nyomni a V2ray szervert</li>
          </ol>
          

        </div>
      </div>
      
      <div id="troubleshooting" class="bg-gray-800 rounded-lg p-4 mb-6 shadow-md">
        <h2 class="text-2xl font-semibold mb-3 text-red-400">Hibaelhárítás</h2>
        <div class="bg-gray-700 p-3 rounded">
          <p class="font-semibold mb-2">TLS probléma:</p>
          <p>Lesznek olyan oldalak amik nem adnak "No TLS" linket tehát amikor beilleszted a linket és rányomsz a szerkesztésre, akkor alul a TLS be van nyomva.</p>
          
          <div class="bg-gray-600 p-3 rounded-md mt-3">
            <p class="mb-2">Megoldás:</p>
            <ol class="list-decimal list-inside space-y-1 pl-2">
              <li>Keresd meg az <code class="bg-gray-500 p-1 rounded">allowInsecure</code> opciót</li>
              <li>Állítsd át <code class="bg-gray-500 p-1 rounded">true</code> értékre</li>
            </ol>
          </div>
        </div>

        <div class="bg-gray-700 p-3 rounded mt-3">
          <p class="font-semibold mb-2">Ha nem megy a net:</p>
          <p>Ha esetleg nem megy a net, próbáld meg benyomni a repülőgépes üzemmódot, majd ki. Ez akkor is szokott segíteni amikor egyedül vagy rajta a neten.</p>
          
          <div class="bg-gray-600 p-3 rounded-md mt-3">
            <p class="mb-2">Megoldás:</p>
            <ol class="list-decimal list-inside space-y-1 pl-2">
              <li>Kapcsold be a repülőgép üzemmódot</li>
              <li>Várj pár másodpercet</li>
              <li>Kapcsold ki a repülőgép üzemmódot</li>
            </ol>
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</main>
