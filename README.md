# Sistema publicador/suscriptor con Java RMI

Práctica de **Sistemas Distribuidos** (DATSI, ETSIINF-UPM, curso 2025-26). Es un sistema **publish/subscribe** distribuido en **Java RMI**:

- `broker_node`: servidor *broker* que gestiona los **temas** (`Topic`), las suscripciones y la notificación de eventos (`PubSubImpl`, `Server`).
- `client_node`: biblioteca cliente (`pubsubcln.Client`) y aplicaciones de prueba (crear temas, publicar, suscribirse, suscripción con patrones *glob*...).
- `common`: interfaces remotas compartidas (`PubSub`, `Subscriber`, `Event`, `SubscriberCallback`).

## Ejecución
```
./compile_all.sh
cd broker_node && ./start_rmiregistry.sh && ./execute_broker.sh
cd client_node && ./execute.sh <test>
```

Parte del esqueleto proporcionado por la asignatura; `ejemplos_JavaRMI/` es material de apoyo del profesor.

## Autor
Mario Fustes González
