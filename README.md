1. **How much data your publisher program will send to the message broker in one run?**
- Dalam satu run program publisher memanggil publish_event sebanyak 5 kali, sehingga akan mengirim 5 pesan ke broker. Setiap pesan adalah hasil serialisasi Borsh dari struct yang berisi dua string (user_id + user_name), yaitu sekitar puluhan byte per pesan.

2. **The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?**
- URL amqp://guest:guest@localhost:5672 sama persis di publisher dan subscriber artinya keduanya terhubung ke broker AMQP yang sama di mesin lokal (localhost) pada port 5672 dengan kredensial user/pass guest/guest.

3. **Running RabbitMQ as message broker**
![Running RabbitMQ as message broker](img/Running_RabbitMQ_as_message_broker.jpg)

4. **Sending and processing event**
![Sending and processing event 1](img/Sending_and_processing_event_1.jpg)
![Sending and processing event 2](img/Sending_and_processing_event_2.jpg)

