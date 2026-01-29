# 🛡️ To-Vault SDK

**To-Vault SDK** es una solución de huella digital (fingerprinting) y detección de fraude diseñada para capturar y analizar el entorno del dispositivo del usuario en tiempo real. Utiliza criptografía híbrida para garantizar que los datos de inteligencia lleguen al backend sin ser interceptados ni manipulados.

### 🔗 (PoC)
Puedes ver el SDK en acción y realizar pruebas de cifrado/descifrado en tiempo real en nuestro entorno controlado:
**[INSERTAR LINK AQUÍ]**

---

## 📊 Estructura de JSON

Al descifrar el JSON, el backend recibe un objeto enriquecido con telemetría de ejecución. A continuación, el esquema de datos propuesto:


```json
{
    "metadata": {
        "version": "1.0.0",
        "timestamp": "2026-01-29T18:29:56.209Z",
        "nonce": "1c1e10ccceeead8872539081cf843895",
        "projectId": "QA-LAB-2026",
        "userId": "user-test-rafael"
    },
    "payload": {
        "browser": {
            "userAgent": "Mozilla/5.0 (X11; Linux x86_64)...",
            "clientHints": {
                "architecture": "x86",
                "mobile": false,
                "platform": "Linux"
            },
            "language": "es-419",
            "timezone": "America/Caracas",
            "time": 13.7
        },
        "hardware": {
            "canvasHash": "209452b7",
            "security": {
                "noiseDetected": false,
                "integrityScore": 1,
                "isLying": false
            },
            "specs": {
                "cores": 8,
                "memory": 8,
                "screen": "1920x1080"
            },
            "time": 19.9
        },
        "network": {
            "network": {
                "publicIp": "38.68.184.29",
                "localIpCandidates": [
                    "05556089-4959-406a-ab92-9cfd01146be9.local"
                ],
                "vpnInferred": true
            },
            "automation": {
                "webdriver": false,
                "isBot": false
            },
            "riskScore": "High",
            "time": 981.9
        }
    },
    "health": {
        "executionTime": 5754.8,
        "errors": []
    }
}
```
---

## 🛠️ Próximos Pasos y Optimización (Roadmap v1.1)

Actualmente, el SDK se encuentra en una fase de refinamiento técnico

1. Optimización del Tiempo de Ejecución (Performance)
2. Refinamiento de cada uno de los atributos de huella

---