# Reflection on Hello Minikube

1. Compare the application logs before and after you exposed it as a Service. Try to open the app several times while the proxy into the Service is running. What do you see in the logs? Does the number of logs increase each time you open the app?
![alt text](<Screenshot 2024-05-17 180210.png>)
![alt text](<Screenshot 2024-05-17 180218.png>)
Terdapat perbedaan antar logs pertama dan kedua. Pada gambar pertama saya membuka app sebanyak 2 kali dan pada kedua saya membuka app 8 kali. Hal tersebut dapat dilihat dari banyak jumlah GET /

2. Notice that there are two versions of `kubectl get` invocation during this tutorial section. The first does not have any option, while the latter has `-n` option with value set to `kube-system`. What is the purpose of the `-n` option and why did the output not list the pods/services that you explicitly created?<br>

    Pada kubernetes, -n adalah flag yang digunakan untuk menentukan dari namespace mana service kita ingin ambil. Namespace sendiri cukup penting dalam kubernetes jika terdapat banyak user dalam suatu environments yang tersebar dalam beberapa team atau proyek. Dengan namespace, kita dapat menggunakan resources dengan nama yang sama dalam namespace yang berbeda.
