# Proyecto VR Forest para Meta Quest

Este proyecto está configurado para crear una experiencia de bosque caminable en realidad virtual para lentes Meta Quest (Quest 2 y Quest 3).

## 🎯 Características

- ✅ Sistema VR completo con XR Interaction Toolkit
- ✅ Bosque transitable con terreno y colisiones
- ✅ Locomoción continua para caminar libremente
- ✅ Árboles, rocas y elementos del bosque
- ✅ Iluminación y niebla atmosférica
- ✅ Optimizado para Meta Quest

## 🚀 Cómo Usar

### Paso 1: Crear la Escena VR

1. Abre Unity
2. En el menú superior, ve a: **VR Setup → Create VR Forest Scene**
3. Espera a que se complete el proceso (aparecerá un mensaje de éxito)
4. La escena se creará automáticamente en `Assets/Scenes/VRForestScene.unity`

### Paso 2: Configurar para Meta Quest

1. Ve a **File → Build Settings**
2. Selecciona **Android** como plataforma
3. Haz clic en **Switch Platform** (si no está ya seleccionado)
4. Conecta tu Meta Quest con un cable USB
5. Habilita el modo desarrollador en tus lentes
6. Haz clic en **Build And Run**

### Paso 3: Probar en Unity (Opcional)

Antes de compilar para Quest, puedes probar en Unity:

1. Abre la escena `VRForestScene.unity`
2. Presiona Play
3. Usa el **XR Device Simulator** para simular los controles VR:
   - **Ratón derecho + mover**: Rotar cámara
   - **WASD**: Mover posición
   - **Q/E**: Subir/bajar

## 🎮 Controles en Meta Quest

Una vez en los lentes:

- **Joystick izquierdo**: Caminar por el bosque
- **Joystick derecho**: Girar la cámara
- Puedes caminar libremente por todo el terreno

## 🔧 Configuraciones Importantes

### Si el terreno no tiene colisiones:

1. Selecciona el objeto "Forest Terrain" en la jerarquía
2. En el Inspector, verifica que el componente **Terrain Collider** esté activo

### Si no puedes moverte en VR:

1. Selecciona el objeto "XR Origin" en la jerarquía
2. Verifica que tenga el componente **VRLocomotionSetup**
3. Asegúrate que los valores de `moveSpeed` y `turnSpeed` sean mayores a 0

### Si los objetos no tienen colisiones:

Los árboles y rocas deberían tener colisiones automáticamente. Si no:
1. Selecciona el objeto problemático
2. Añade un **Collider** apropiado (Capsule Collider para árboles, Mesh Collider para rocas)

## 📱 Requisitos de Meta Quest

- Meta Quest 2 o Meta Quest 3
- Modo desarrollador habilitado
- Cable USB-C para desarrollo
- Unity 2021.3 o superior
- Android Build Support instalado en Unity

## 🐛 Solución de Problemas

### "XR Origin prefab not found"
- Asegúrate de tener instalado el paquete **XR Interaction Toolkit**
- Ve a Window → Package Manager → XR Interaction Toolkit → Import Samples

### "Terrain layers not found"
- Verifica que la carpeta `TriForge Assets` esté completa
- Los archivos de terreno deben estar en `Assets/TriForge Assets/Fantasy Worlds - DEMO Content/Textures/Terrain/`

### El proyecto no compila para Android
1. Ve a **Edit → Project Settings → Player**
2. En la pestaña Android:
   - Minimum API Level: Android 6.0 (API 23) o superior
   - Target API Level: Automatic (highest installed)
3. En **XR Plug-in Management**:
   - Habilita **Oculus** (para Meta Quest)

## 📝 Notas Adicionales

- El bosque tiene un tamaño de 100x100 unidades
- El terreno usa texturas del template Fantasy Worlds
- La niebla está configurada para dar atmósfera al bosque
- Los objetos se distribuyen aleatoriamente cada vez que creas la escena

## 🎨 Personalización

Puedes modificar el script `VRForestSceneSetup.cs` para:
- Cambiar el tamaño del terreno
- Añadir más árboles o rocas
- Modificar la iluminación
- Ajustar la densidad de la niebla

¡Disfruta tu experiencia de bosque en VR! 🌲🥽
