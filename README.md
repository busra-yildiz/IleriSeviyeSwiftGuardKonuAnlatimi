# IleriSeviyeSwiftGuardKonuAnlatimi
Swift programlama dilinde "guard" ifadesini kullanarak, belirli bir koşulu kontrol edebilir ve koşulun sağlanmadığı durumları ele alabilirsiniz. 
Guard yapısı, özellikle daha okunabilir ve güvenilir kod yazmanıza yardımcı olabilir. Guard ifadesi genellikle işlevlerin başında kullanılır ve belirli 
bir koşulu kontrol eder. Koşul sağlanmazsa, genellikle işlevin erken çıkmasına (return) veya belirli bir hata durumuna yol açar.

İşte Swift'te "guard" yapısını kullanarak nasıl çalıştığını gösteren bir örnek:
func sayHello(to name: String?) {
    // Guard ifadesi ile isim boş ise hata ver
    guard let name = name else {
        print("İsim belirtilmedi.")
        return
    }
    
    // İsim boş olmadığında buraya ulaşılır
    print("Merhaba, \(name)!")
}

sayHello(to: "John") // Merhaba, John!
sayHello(to: nil)    // İsim belirtilmedi.

Yukarıdaki örnekte, "sayHello(to:)" adlı bir işlev tanımlandı. Bu işlev, bir isim parametresi alır. "guard let name = name" ifadesi, "name" parametresinin 
nil olup olmadığını kontrol eder. Eğer "name" nil ise, "İsim belirtilmedi." mesajını yazdırır ve işlevi erken çıkarır. Nil olmayan bir değer ise, isim 
belirtilmiş demektir ve "Merhaba, (name)!" mesajını yazdırır.

Guard ifadesi, özellikle fonksiyonların başında, istenmeyen durumları erken tespit etmek ve kodun daha düzenli ve anlaşılır olmasını sağlamak için 
kullanışlıdır.
