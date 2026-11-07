# FinPay - Müştəri Analitikası və Retention Sistemi
Datalent Bootcamp Machine Learning Capstone 2026

##Layihənin İcmalı
Bu layihə FinPay rəqəmsal bankçılıq platformasının müştəri davranışlarını təhlil etmək, növbəti ayın xərcləmələrini proqnozlaşdırmaq (`Regression`) və müştəri itkisini qabaqcadan müəyyənləşdirmək (`Classification`) məqsədi ilə hazırlanmışdır.

## İstifadə olunan Texnologiyalar
* **Python** (Pandas, NumPy, Scikit-Learn)
* **Visualisation:** Matplotlib, Seaborn
* **Modelling:** Random Forest Regressor & Classifier, Pipelines

## Əsas Mərhələlər
1. **Data Understanding & EDA:** Məlumat strukturunun yoxlanılması, çatışmayan dəyərlərin və vizual qanunauyğunluqların təhlili.
2. **Data Cleaning:** Dublikatların silinməsi, anomaliyaların təmizlənməsi və missinq dəyərlərin doldurulması.
3. **Feature Engineering:** Borc-gəlir nisbəti (`debt_to_income`), əməliyyat intensivliyi və engagement skorlarının yaradılması.
4. **Modelling & Evaluation:** Reqressiya və klassifikasiya modellərinin qurulması, metrikaların qiymətləndirilməsi.
5. **Customer Segmentation:** Müştərilərin risk və dəyər matrisinə əsasən qruplaşdırılması və retention prioritetlərinin müəyyənləşdirilməsi.

## Layihəni necə işə salmalı?
1. Reponu klonlayın: `git clone <repo-url>`
2. Kitabxanaları quraşdırın: `pip install -r requirements.txt`
3. Notebook faylını Jupyter vasitəsilə işə salın.


##FinPay Management - Rəhbərliyin Final Sorğusu və Cavabları

1. **Kim churn etməyə daha yaxındır?**
   * **Cavab:** İlk 6-12 ay ərzində olan (tenure-u aşağı), tətbiqə daxilolma tezliyi azalan (`app_logins` aşağı, `days_since_last_login` yüksək), hesabında çoxlu uğursuz əməliyyat (`failed_transactions`) və dəstək müraciəti (`support_tickets`) olan müştərilər tərk etməyə daha yaxındır.

2. **Kim daha dəyərlidir?**
   * **Cavab:** Yüksək aylıq gəlirə malik, aktiv şəkildə kartdan istifadə edən və `next_month_spending` proqnozu medandan yuxarı olan müştərilər şirkət üçün maliyyə baxımından ən dəyərli seqmentdir.

3. **Kim prioritet olmalıdır?**
   * **Cavab:** Retention (müştəri saxlanılması) komandasının məhdud resursları nəzərə alınmaqla, ilk növbədə **"High Value / High Risk"** (Yüksək Dəyərli və Yüksək Riskli) qrupundakı müştərilər prioritetləşdirilməlidir.

4. **Proqnozlara nə qədər etibar etmək olar?**
   * **Cavab:** Reqressiya modeli $R^2 \approx 0.73$ göstəricisi ilə gələcək xərcləmələri yüksək dəqiqliklə proqnozlaşdırır. Klassifikasiya modelində isə sinif balanssızlığı səbəbindən ROC-AUC və Precision-Recall tarazlığı nəzərə alınmalıdır, yəni proqnozlar istiqamətverici siqnal kimi istifadə edilməlidir.

5. **Biznes növbəti addım olaraq nə etməlidir?**
   * **Cavab:** Ödəniş sistemindəki (Payment Gateway) texniki xətalar aradan qaldırılmalı, yeni qoşulanlar üçün xüsusi *Onboarding* proqramları başladılmalı və riskli müştərilərə fərdi keşbek/bonus kampaniyaları təklif olunmalıdır.
