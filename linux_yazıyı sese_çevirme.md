Yazıyı sese çevirmek için çok çeşitli yapay zeka araçları var. Ama ben bunu basitçe [espeak-ng](https://github.com/espeak-ng/espeak-ng) ile göstereceğim.

Linux terminalde, bunları indiriyoruz:
``` bash
sudo apt install espeak-ng mbrola mbrola-tr1 mbrola-tr2
```
kullanım:
``` bash
espeak-ng -v tr "Ses deneme 123, merhaba 😀"
espeak-ng -v mb-tr1 "Ses deneme 123, merhaba 😀"
espeak-ng -v mb-tr2 "Ses deneme 123, merhaba 😀"
espeak-ng -v tr+croak "Boğuk konuşuyorum..."
espeak-ng -v tr+whisper "Fısıldıyorum..."
espeak-ng -v tr+f3 "kız sesi"
```

ses varyantlarını listelemek için:
``` bash
ls /usr/lib/x86_64-linux-gnu/espeak-ng-data/voices/!v/
```
çıktı:
```
 adam          david     gustave      linda    'Mr serious'    robosoft6
 Alex          Demonic   Henrique     m1        Nguyen         robosoft7
 Alicia        Denis     Hugo         m2        norbert        robosoft8
 Andrea        Diogo     iven         m3        pablo          sandro
 Andy          ed        iven2        m4        paul           shelby
 anika         edward    iven3        m5        pedro          steph
 anikaRobot    edward2   iven4        m6        quincy         steph2
 Annie         f1        Jacky        m7        RicishayMax    steph3
 announcer     f2        john         m8        RicishayMax2   Storm
 antonio       f3        kaukovalta   marcelo   RicishayMax3   travis
 AnxiousAndy   f4        klatt        Marco     rob            Tweaky
 aunty         f5        klatt2       Mario     robert         UniRobot
 belinda       fast      klatt3       max       robosoft       victor
 benjamin      Gene      klatt4       Michael   robosoft2      whisper
 boris         Gene2     klatt5       michel    robosoft3      whisperf
 caleb         grandma   klatt6       miguel    robosoft4      zac
 croak         grandpa   Lee          Mike      robosoft5
```

Bunları yukarıdaki örneklerdeki gibi başına `tr+...` ekleyerek kullanılabilirsin.

Aynı zamanda daha detaylı çıktılar için [SSML](https://github.com/espeak-ng/espeak-ng/blob/master/docs/markup.md#ssml-speech-synthesis-markup-language) formatını kullanabilirsin.
