#### Tapşırıq

Lahiyə excel faylından məlumatları oxuyub məlumat bazasına yazmalıdır və dataya görə hesabatları email vasitəsi ilə göndərməlidir. Sizə excel məlumatları üçün misal var ona uyğun məlumat bazasınızı yaratmalısınız ve dataları orda saxlamlısınız.

##### Enpointler aşağıdaklar olmalıdır

- UploadData/POST/File(binary) - məlumat faylı yüklənməsi - fayl yalnız xlxs və xls ola bilər, max 5mb yükləyə bilməlidir, yüklənmiş faylın template uyğun olması lazımdır.
- SendReport/GET/Type(int) | StartDate(DateTime) | EndDate(DateTime) | AcceptorEmail(string[]) - hesabatın növü və email ünvanları göndərərək hesabat istəyi - Type enum olmalıdır və seçimlərin çölündə ola bilməz, emaillərin düzgün formatda bitiyini və code.edu.az domainə aid olduğunu yoxlamaq. StartDate-in EndDate-dən kiçik olduğunu yoxlamaq. Mailləri queue-dan göndərmək

##### Hesabat növləri

- 1 - Segment-ə görə satışlar - Hər segmentə görə tarix aralığında məhsul sayı, satiş toplamı, endirim toplamı, qazanc toplamı məlumatları

- 2 - Ölkəyə görə satışlar - Hər ölkəyə görə tarix aralığında məhsul sayı, satiş toplamı, endirim toplamı, qazanc toplamı məlumatları

- 3 - Məhsula görə satışlar - Hər məhsula görə tarix aralığında məhsul sayı, satiş toplamı, endirim toplamı, qazanc toplamı məlumatları

- 4 - Məhsula görə endirimlər - Hər məhsula görə tarix aralığında məhsula necə faiz endirim olunduğu məlumat

#### Logging

- Sistemdə bütün əməliyyatlar və xətalar loglanmalıdır.
- Hansı emaillərə hansi hesabatlar göndərilib loglanmalıdır.
