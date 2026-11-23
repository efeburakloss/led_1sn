# led_1sn
# Arduino 1 Saniye Aralıklarla Yanıp Sönen LED (Blink)

Bu proje, Arduino Uno kullanarak harici bir LED'in 1 saniye aralıklarla yakılıp söndürülmesini sağlayan temel bir giriş seviyesi elektronik ve gömülü sistem uygulamasıdır.

## Kullanılan Malzemeler
* 1x Arduino Uno
* 1x Breadboard (Devre Tahtası)
* 1x Kırmızı LED
* 1x 220Ω Direnç
* 2x Jumper Kablo

## Devre Bağlantısı
1. **Arduino Pin 13** ucundan çıkan kabloyu breadboard üzerindeki **220Ω direncin** bir bacağına bağlayın.
2. Direncin diğer bacağını LED'in **uzun bacağı (Anot / +)** ile aynı dikey sütuna yerleştirin.
3. LED'in **kısa bacağını (Katot / -)** başka bir kablo ile Arduino üzerindeki **GND** pinine bağlayın.
4. wokwi üzerinde devre bağlantısı:
5. https://wokwi.com/projects/481510713492699137
6. Not: 220Ω direnç, LED üzerinden geçen akımı sınırlandırarak LED'in zarar görmesini engeller.

## Çalışma Mantığı
* `setup()` fonksiyonu içerisinde 13 numaralı pin çıkış (`OUTPUT`) olarak ayarlanır.
* `loop()` döngüsü içerisinde `digitalWrite(13, HIGH)` komutu ile LED 1 saniye (`delay(1000)`) boyunca yakılır, ardından `digitalWrite(13, LOW)` komutu ile 1 saniye boyunca söndürülür. Bu işlem güç kesilene kadar sürekli tekrarlanır.
