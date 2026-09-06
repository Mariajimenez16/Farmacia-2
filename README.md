# Sistema de Farmacia — Reto 2: Patrones de Diseño Arquitectónico
 
Evolución del sistema de farmacia (Reto 1, SOLID) incorporando **Facade**, **Factory Method** y **Strategy** sobre esa misma base, sin romper SOLID ni cambiar el comportamiento observable del sistema.
 
## Equipo
 
| Integrante | Rol |
|---|---|
| Natalia Giraldo Morales  | Arquitecta de comunicación gráfica (vistas y diagramas) |
| María Alexandra Jiménez Suárez | Arquitecto Líder (patrones, diseño TO-BE) |
| Juan José Álvarez Restrepo | Arquitecta de Verificación (SOLID, pruebas) |
| Carolina Ramírez Lotero | Arquitecta de Riesgos y despliegue |
 
*Curso Arquitectura de Software — UPB, docente Cesar Augusto López Gallego.*
 
 
## Video de sustentación
 
🎥 **[Link al video de YouTube — pendiente de agregar]**
 
## Patrones adoptados
 
| Patrón | Resuelve | Dónde vive |
|---|---|---|
| **Facade** | `Program.cs` armaba todo a mano con `new`, mezclando ensamblaje con login y menú | `FarmaciaFachada` + `ServicioVenta` |
| **Factory Method** | `ProductoFactory` conocía todas las implementaciones concretas y no permitía agregar variantes sin tocarla | `FabricaProducto` + subclases por tipo |
| **Strategy** | `IDescuento` existía pero no tenía ningún consumidor real, ni forma de intercambiar la regla de descuento | `IDescuento` + `DescuentoPorcentaje`, `DescuentoMontoFijo`, `DescuentoSinDescuento`, `ServicioDescuento` |
 
Se evaluaron 9 patrones en total; los descartados (Abstract Factory, Builder, Adapter, Decorator, Template Method, State) tienen su justificación técnica documentada en `Documento/`.
 
## Estructura del repositorio
 
```
├── Código/          # Solución .NET (BibFarmacia, AppFarmaciaConsola, VerificacionReto2)
├── Diagramas/        # AS-IS y TO-BE (UML, capas SOLID + Patrones)
├── Documento/        # Actividades 1-6: puntos de dolor, bitácora, matriz SOLID, riesgos
└── Vistas/           # Vista de negocio y vista de desarrollo
```
 
## Cómo ejecutar
 
```bash
dotnet run --project Código/AppFarmaciaConsola
```
 
## Uso de IA
 
Las consultas a la IA se usaron para explorar alternativas y contrastarlas contra el código real, nunca como reemplazo del análisis del equipo — cada propuesta se verificó contra las clases y relaciones existentes antes de aceptarla, ajustarla o descartarla. Detalle completo en la bitácora (`Documento/`).
 
