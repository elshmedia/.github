# 🛸 ELSH MEDIA · CENTRAL COMMAND

> **Status:** Operational | **Cluster Nodes:** 38 Active Channels | **Environment:** GitOps Automated

Bienvenidos a la matriz central de control de **ELSH MEDIA**. Desde esta consola se gestiona, orquesta y automatiza el despliegue masiva de contenido multimedia en cascada hacia la red internacional de portales de la organización.

---

## 💻 Core Infrastructure Components

El sistema operativo y motor de distribución se compone de tres microservicios desacoplados:

*   **[media-orchestrator](https://elshmedia.github.com/media-orchestrator):** ⚙️ El motor ejecutable en Python. Contiene la capa de red Scotty (HTTP POST crudo), la inyección de sesiones activas de Brave Browser y los manifiestos de despliegue estilo **Helm Charts (Jinja2)**.
*   **[media-registry](https://elshmedia.github.com/media-registry):** 🗄️ El State Store centralizado. Aloja el inventario maestro global (`inventory.yaml`) y las firmas reutilizables de toda la red de canales.
*   **[dashboard](https://elshmedia.github.com/dashboard):** 📊 REPO PÚBLICO ESPEJO. Capa de presentación estática en GitHub Pages que sirve la telemetría del clúster con estilos locales e inmunidad contra bloqueadores en: `https: / / elshmedia.github.io / dashboard /`

---

## 🛸 Bootstrapping / Levantar el Entorno

Para clonar de forma automática toda la galaxia de repositorios, herramientas CLI de producción y canales ordenados alfabéticamente en cualquier máquina limpia (Windows 11 Pro / Mac Air), clona el repositorio semilla y ejecuta el CLI maestro:

```bash
git clone git@github.com:elshmedia/elshmedia.git
cd elshmedia
./elshmedia.sh setup
```

Para actualizar los KPIs y el panel web de métricas a demanda desde la raíz:
```bash
./elshmedia.sh metrics
```

---

## 🐠 Active Production Content Brands (Top Nodes)

La matriz de canales independientes se despliega bajo repositorios dedicados con prefijo `x-*` para garantizar el aislamiento absoluto de entornos:

*   **[x-aquarixtop](https://elshmedia.github.com/x-aquarixtop):** 🌟 Canal Principal Monetizado (Nicho: Acuarismo Avanzado - Idioma: ES).
*   **x-drgeograph:** 🌍 Canal de Geografía y Curiosidades Globales (Idioma: ES).
*   **x-buceandoxmundo:** 🤿 Canal de Aventura Subacuática y Exploración (Idioma: ES).
*   *Resto del clúster (35 canales adicionales) aprovisionados en el catálogo central.*

---

## 🔒 Security Policy & DR System

1.  **Zero-Binaries Policy:** Los archivos de video pesados (`*.mp4`, `*.mov`) están estrictamente vetados en la nube de GitHub mediante políticas locales de `.gitignore`. La infraestructura opera con bytes de texto declarativo YAML a costo \$0.
2.  **Disaster Recovery (DR Plan):** Ante contingencias, la restauración del parque de contenido histórico indexado se realiza modificando el puntero del canal en el manifiesto correspondiente y gatillando un *re-deploy* local de la marca.
