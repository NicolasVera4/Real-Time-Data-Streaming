# 🛠️ Real-Time Data Streaming Pipeline with Apache Kafka, Spark & Cassandra

Este proyecto implementa un pipeline de procesamiento de datos en tiempo real utilizando tecnologías modernas del ecosistema Big Data, orquestadas y contenidas con Docker.

---

## 📌 Descripción del Proyecto

Se construyó una arquitectura distribuida capaz de ingerir eventos generados por una API, almacenarlos temporalmente en Kafka, procesarlos con Apache Spark y persistirlos en una base de datos NoSQL (Cassandra). Todo el flujo está orquestado por Apache Airflow, permitiendo una automatización controlada de los procesos.

---

## 🗺️ Arquitectura General

![Arquitectura del sistema](/home/nicolas/arquitectura.png)

---

## ⚙️ Tecnologías Utilizadas

| Componente      | Descripción                                              |
|-----------------|----------------------------------------------------------|
| **Apache Kafka**      | Sistema de mensajería para el procesamiento de eventos en tiempo real. |
| **Apache Spark**      | Framework distribuido para procesamiento de datos (Spark Structured Streaming). |
| **Apache Cassandra**  | Base de datos NoSQL optimizada para escritura a gran velocidad. |
| **Apache Airflow**    | Orquestador de flujos de datos (DAGs). |
| **PostgreSQL**        | Base de datos relacional para ingesta inicial. |
| **Docker**            | Contenerización de todos los servicios del ecosistema. |
| **Confluent Platform**| Incluye Control Center, Schema Registry, Kafka Connect, etc. |

---

## 🧩 Componentes del Pipeline

1. **API de eventos**: Genera eventos simulados de usuarios.
2. **Airflow DAG**: Extrae datos de PostgreSQL y los envía a Kafka.
3. **Kafka Topic**: Almacena los eventos para ser consumidos en streaming.
4. **Spark Streaming App**: Procesa los eventos del tópico y los transforma.
5. **Cassandra**: Almacén de destino final para los datos procesados.
6. **Control Center**: Monitoreo y gestión visual de Kafka.
7. **Schema Registry**: Validación y versionado de los esquemas Avro/JSON.

---