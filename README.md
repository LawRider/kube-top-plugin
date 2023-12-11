# kubeplugins
Bash скрипт kubeplugin призначений для виводу показників використання ресурсів (CPU, Memory) в Kubernetes кластері.

Для використання плагіну треба:

1.  Додати файлу права на виконання:

   ```bash
   sudo chmod +x kubeplugin
   ```

2.  Скопіювати файл з новою назвою

   ```bash
   sudo cp kubeplugin /usr/local/bin/kubectl-usage
   ```

Приклади використання:

1. Показати інформацію для нод:

   ```bash
   kubectl usage node
   ```

   Приклад виводу:

   ```bash
    Resource       Name                                                        CPU            Memory         
    node           gke-temp-project-default-pool-245c01cb-rfe6                 107m           11%
   ```

   

2. Показати інформацію для подів у неймспейсі default:

   ```bash
   kubectl usage pod
   ```

   Приклад виводу:

   ```bash
    Resource       Namespace      Name                                                        CPU            Memory         
    pod            default        demo-874956d5f-cwm7f                                        0m             0Mi
   ```

   

3. Показати інформацію для подів у конкретному неймспейсі:

   ```bash
   kubectl usage pod <namespace>
   ```

   Приклад виводу:

   ```bash
    Resource       Namespace      Name                                                        CPU            Memory         
    pod            kube-system    event-exporter-gke-7bf6c99dcb-2b5zw                         1m             21Mi           
    pod            kube-system    fluentbit-gke-rj59k                                         7m             23Mi           
    pod            kube-system    gke-metrics-agent-5bzcf                                     4m             46Mi           
    pod            kube-system    konnectivity-agent-6f7858c6bc-trc5t                         1m             7Mi            
    pod            kube-system    konnectivity-agent-autoscaler-5d9dbcc6d8-q6xrr              1m             3Mi            
    pod            kube-system    kube-dns-5bfd847c64-bbkp7                                   2m             30Mi           
    pod            kube-system    kube-dns-autoscaler-84b8db4dc7-gzckb                        1m             3Mi            
    pod            kube-system    kube-proxy-gke-temp-project-default-pool-245c01cb-rfe6      1m             34Mi           
    pod            kube-system    l7-default-backend-d86c96845-ldnx6                          1m             2Mi            
    pod            kube-system    metrics-server-v0.5.2-6bcf6bdbbb-7z7rd                      20m            30Mi           
    pod            kube-system    pdcsi-node-9ss2x                                            6m             10Mi
   ```
