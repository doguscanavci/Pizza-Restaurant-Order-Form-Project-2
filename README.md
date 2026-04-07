# Sprint Challenge: Teknolojik Yemekler - SPA

## English

### Task: Single Page Application (SPA) - Teknolojik Yemekler
#### Task Description
As part of the Sprint 8 challenge, I built a Single Page Application (SPA) named **"Teknolojik Yemekler"** tailored for hungry developers. The project simulates a realistic food ordering flow including a zesty Home Page, a comprehensive Pizza Order Form, and a Success Page, emphasizing functional state architecture and dynamic user experiences.

#### Technical Requirements:
* **State Management & Lifting:** Handle multi-step navigation and transfer final purchase orders from the form to the success page using only the **Prop-Lifting** technique without global state managers.
* **Form Validation:** Implement complex, multi-rule validation (e.g., minimum 3 characters for names, between 4 and 10 dynamic toppings) with dynamic error messaging and conditional submit locking.
* **Data Transport:** Use `axios` to execute automated POST requests to a mock server, handling custom API key headers (`x-api-key: reqres-free-v1`) and managing operational errors.
* **Automated Testing:** Conduct End-to-End (E2E) automation tests utilizing Cypress to ensure full application flow stability.

#### Checklist:
- [x] Implemented a linkable Hero landing page that smoothly directs users to the ordering interface.
- [x] Configured semantic form controls managing radio inputs for sizes, custom select dropdowns for dough thickness, and controlled array pools for checkbox toppings.
- [x] Structured real-time price computations dynamically scaling with ingredient counts and individual pizza counters.
- [x] Established strict button validation rules disabling submission during invalid inputs or incomplete selections.
- [x] Orchestrated secure `axios.post` pipelines mapping raw `formData` states into beautifully human-readable `Success` objects.
- [x] Formulated robust Cypress testing sequences verifying text input, compound checking, and mock submissions.
- [x] Designed seamless application styling utilizing pixel-perfect TailwindCSS matching Figma specifications.

#### My Learning Journey & Reflection
* **Controlled Component Mastery:** This project solidified my understanding of handling non-standard complex inputs (like arrays of checkboxes for pizza toppings). Building functions that safely insert and remove values from sub-arrays without mutating the original state was a huge milestone.
* **Architecting Dynamic Form Interactivity:** Managing the computed properties using the `[name]: value` syntax allowed me to appreciate scalable code. A single event handler seamlessly coordinates user actions across textareas, selects, and radio components.
* **Data Synchronization & Form Safety:** Synchronizing price calculations and structural validations within unified reactive workflows taught me how to enforce client-side safety. Disabling user endpoints programmatically mitigates the leak of broken or corrupted client payloads into active data pipes.

#### Tech Stack
* React.js (Functional Components, Hooks)
* React Router (SPA Routing)
* TailwindCSS & Reactstrap (Responsive & Figma-aligned layout)
* Axios (Asynchronous HTTP requests & header configurations)
* Cypress (End-to-End Test Automation)

---

## Türkçe

### Görev: Tek Sayfa Uygulaması (SPA) - Teknolojik Yemekler
#### Görev Tanımı
Sprint 8 değerlendirmesi kapsamında, acıkan yazılımcılara yönelik olarak tasarlanan **"Teknolojik Yemekler"** markası için işlevsel bir yemek siparişi web uygulaması (SPA) geliştirdim. Proje; interaktif bir Anasayfa, kapsamlı ve kurallı bir Sipariş Formu ile Sipariş Onay adımlarını içererek, bileşenler arası veri akışını ve dinamik kullanıcı deneyimini simüle eder.

#### Teknik Gereksinimler:
* **Veri Akışı ve Prop-Lifting:** Herhangi bir global state yönetim kütüphanesi kullanmadan, sipariş formundaki dataları onay sayfasına sadece **Prop-Lifting (State'i yukarı taşıma)** tekniğiyle güvenli bir şekilde aktarmak.
* **Form Doğrulama (Validation):** İsim alanında en az 3 karakter, ek malzemelerde ise en az 4, en fazla 10 adet seçim sınırını dinamik hata yönetim mekanizmalarıyla denetlemek ve formu koşullu olarak kilitlemek.
* **Asenkron Veri Transferi:** `axios` kullanarak `https://reqres.in/api/pizza` mock API servisine `x-api-key: reqres-free-v1` header bilgisiyle güvenli POST istekleri atmak ve ağ hatalarını yönetmek.
* **Otomasyon Testleri:** Kullanıcı senaryolarının kararlılığını ölçmek adına Cypress entegrasyonu sağlayarak uçtan uca test senaryoları kurgulamak.

#### Kontrol Listesi:
- [x] Hero alanındaki yönlendirme butonu ile sipariş formuna geçiş sağlayan anasayfa kurgulandı.
- [x] Boyut için radyo butonları, hamur kalınlığı için seçici (select) alanı ve ek malzemeler için çoklu seçim (checkbox) havuzu semantik olarak inşa edildi.
- [x] Seçilen malzeme adedine ve pizza sayacına göre dinamik olarak anlık hesaplama yapan fiyat paneli entegre edildi.
- [x] Eksik veri girişinde veya yetersiz malzeme seçiminde "Sipariş Ver" butonunu hem HTML hem de JS tarafında kilitleyen validasyon kuralları uygulandı.
- [x] `axios.post` hattı kurularak ham `formData` durumları, başarı sayfasının anlayacağı `Success` şablonuna dönüştürüldü.
- [x] Metin girişi, çoklu malzeme seçimi ve form gönderim akışlarını doğrulayan en az 3 anlamlı Cypress e2e testi yazıldı.
- [x] Proje klasöründeki Figma yönergelerine ve renk kodlarına tam uyumlu, responsive TailwindCSS tasarımı tamamlandı.

#### Gelişim Süreci ve Notlarım
* **Kontrollü Bileşen (Controlled Component) Yetkinliği:** Bu proje, dizi (array) tabanlı checkbox verilerini React state'i üzerinde mutasyona uğratmadan (`filter` ve `spread` operatörleri kullanarak) ekleyip çıkarabilme mantığımı üst seviyeye taşıdı.
* **Dinamik Form Yönetimi:** Değişken nesne anahtarlarını `[name]: value` söz dizimiyle yakalamak, kodun ölçeklenebilirliğini anlamamı sağladı. Tek bir fonksiyon ile input, select ve textarea bileşenlerinin tamamını kusursuzca yönetebildim.
* **Veri Senkronizasyonu ve Form Güvenliği:** Hesaplanan fiyatlar ile formun gönderilebilir olma durumunu (`isFormValid`) tek bir reaktif akışta senkronize etmek, hatalı payload'ların API hattına sızmasını engelleyen harika bir istemci tarafı koruma deneyimi sundu.

#### Kullanılan Teknolojiler
* React.js (Fonksiyonel Bileşenler, Hook Yapıları)
* React Router (SPA Sayfa Yönetimi ve Routing)
* TailwindCSS & Reactstrap (Arayüz Düzeni ve Figma Uyumluluğu)
* Axios (Asenkron HTTP İstekleri ve Header Yönetimi)
* Cypress (Uçtan Uca Otomasyon Testleri)