---
description: 暂时不支持Claude模型
---

{% hint style="warning" %}
Este documento ha sido traducido del chino por IA y aún no ha sido revisado.
{% endhint %}

# Vertex AI

## Visión General del Tutorial

### 1. Obtener la Clave API

* Antes de obtener la clave API de Gemini, necesitas tener un proyecto de Google Cloud (si ya tienes uno, puedes omitir este paso)
* Ve a [Google Cloud](https://console.cloud.google.com/projectcreate) para crear un proyecto, completa el nombre del proyecto y haz clic en "Crear proyecto"

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

* Accede a la [consola de Vertex AI](https://console.cloud.google.com/vertex-ai)
* Habilita [Vertex AI API](https://console.cloud.google.com/apis/library/aiplatform.googleapis.com?inv=1\&invt=Ab0iBA) en el proyecto creado

<figure><img src="../../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

## 2. Configurar Permisos de Acceso API

* Abre la página de permisos de [cuentas de servicio](https://console.cloud.google.com/iam-admin/serviceaccounts) y crea una cuenta de servicio

<figure><img src="../../.gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure>

* En la página de administración de cuentas de servicio, encuentra la cuenta recién creada, haz clic en `Claves` y crea una nueva clave en formato JSON

<figure><img src="../../.gitbook/assets/image (80).png" alt=""><figcaption></figcaption></figure>

* Después de crearla exitosamente, el archivo clave se guardará automáticamente en tu computadora en formato JSON. **Consérvalo adecuadamente**

## 3. Configurar Vertex AI en Cherry Studio

* Selecciona el proveedor de servicios Vertex AI
* Completa los campos correspondientes con los datos del archivo JSON

<figure><img src="../../.gitbook/assets/image (81).png" alt=""><figcaption></figcaption></figure>

Haz clic en "Agregar [Modelo](https://console.cloud.google.com/vertex-ai/model-garden)", ¡y podrás comenzar a usar la plataforma sin problemas!