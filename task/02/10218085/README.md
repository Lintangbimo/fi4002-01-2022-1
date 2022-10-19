# 10218085
Lintang Bimo Sekti Wahyono


## materi sebelumnya
+ Tuliskan materi-materi sebelumnya yang telah diberikan dalam kuliah ini.
Monte carlo
Range kutta
Osilasi terdeam
Discrete forier transform
Pred prey
Matriks temperature
Euler




## materi paling menarik
+ Tuliskan materi yang paling menarik yang telah diberikan dan jelaskan mengapa menarik.
Monte carlo

## materi paling membosankan
+ Tuliskan materi yang telah diberikan yang paling membosankan dan jelaskan alasannya.
Osilasi

## materi yang sudah dipami
+ Tuliskan materi-materi yang telah dipahami.
Range kutta


## materi yang belum dipahami
+ Tuliskan materi-materi yang masih belum dipahami dan bagian mana yang belum serta ingin dipahami.
Monte carlo
Discrete fourier transform
Osilasi 2 pegas gitu2

## contoh program
+ Buat suatu contoh program dalam Python dan sertakan di sini dengan hasil keluarnnya.

```python
# contoh program python
```
import numpy as np
import matplotlib.pyplot as plt

# fungsi di python, menterjemahkan persamaan differensial/ dinamika siste fisis

def predprey(p, q, k1 = 10, k2 = 2, d = 0.002, c = 0.001):
    p_dot = k1*p-c*p*q
    q_dot = -k2*q+d*p*q
    return p_dot, q_dot

dt = 0.005
#num_step = 1400
num_steps = 3000

ps = np.empty(num_steps +1)
qs = np.empty(num_steps +1)
ts = np.empty(num_steps +1)

ps[0], qs[0], = (100.0, 3000.0)
# ps[0], qs[0] = (100.0, 100.0)

for i in range(num_steps):
    p_dot, q_dot = predprey(ps[i], qs[i])
    ps [i+1] = ps[i] + (p_dot * dt) # Metode Euler
    qs [i+1] = qs[i] + (q_dot * dt)
    ts [i+1] = i
    
plt.plot(ts,qs,ts,ps)
plt.show()
Hasilnya adalah

```
```


## cara perkuliahan
+ Tuliskan pendapat Anda mengenai cara perkuliahan selama ini dan cantumkan usulan untuk perkuliahan setelah UTS.
Bagus, substansial.

## topik sistem fisis
+ Tuliskan sistem fisis yang menarik bagi Anda untuk dikaji lebih dalam dan jelaskan alasannya mengapa.
Monte carlo, dikarenakan mampu menganalisis dengan cara random tembakan dan kita dapat mendapatkan grafik yang kita ingin ketahui

## simulasi dan visualisasi
+ Apakah Anda tertarik dengan simulasi dan visualisasi? Jelaskan topik yang ingin Anda simulasikan / visualisasikan serta cantumkan alasannya dan perkiraan pusataka Python yang perlu digunakan.
Tertarik, terurama.yang berhubungan dengan data scince, dikarenakan prospeknya bagus, 
