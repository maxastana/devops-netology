Задача 1
1. На лекции мы познакомились с node_exporter. В демонстрации его исполняемый файл запускался в background. Этого достаточно для демо, но не для настоящей production-системы, где процессы должны находиться под внешним управлением. Используя знания из лекции по systemd, создайте самостоятельно простой unit-файл для node_exporter:
- поместите его в автозагрузку,
- предусмотрите возможность добавления опций к запускаемому процессу через внешний файл (посмотрите, например, на systemctl cat cron),
- удостоверьтесь, что с помощью systemctl процесс корректно стартует, завершается, а после перезагрузки автоматически поднимается.

![image](https://user-images.githubusercontent.com/65549218/144243329-d216175c-9913-4453-810b-64ec3eadef56.png)

Проверка службы
Рестарт, статус, стоп, старт, статус
![image](https://user-images.githubusercontent.com/65549218/144244409-3ccc6cf0-df81-4a54-ac4a-966ed04e2a10.png)
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Задача 2

Ознакомьтесь с опциями node_exporter и выводом /metrics по-умолчанию. Приведите несколько опций, которые вы бы выбрали для базового мониторинга хоста по CPU, памяти, диску и сети.

Ответ:

						CPU
	node_cpu_seconds_total{cpu="0",mode="idle"} 18223.66
	node_cpu_seconds_total{cpu="0",mode="system"} 6.65
	node_cpu_seconds_total{cpu="0",mode="user"} 10.05
	node_cpu_seconds_total{cpu="1",mode="idle"} 18043.79
	node_cpu_seconds_total{cpu="1",mode="system"} 5.27
	node_cpu_seconds_total{cpu="1",mode="user"} 8.57
	
						Memory
	node_memory_MemAvailable_bytes 
    node_memory_MemFree_bytes
	
						Disk		
	node_disk_io_time_seconds_total{device="sda"} 46.936
	node_disk_read_bytes_total{device="sda"} 2.41414144e+08
	node_disk_read_time_seconds_total{device="sda"} 21.113
	node_disk_write_time_seconds_total{device="sda"} 117.513
	
						Network
	node_network_receive_errs_total{device="enp0s3"} 0
	node_network_receive_bytes_total{device="enp0s3"} 9.5060737e+07
	node_network_transmit_bytes_total{device="enp0s3"} 6.065389e+06
	node_network_transmit_errs_total
	
	
