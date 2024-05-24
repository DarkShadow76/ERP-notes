**FB50** - registrar manualmente asientos de diario en las cuentas de mayor de la empresa.

**FB03** - visualizar documentos contables que ya se han registrado en el sistema.

**MMBE** - visualizar el stock de materiales en un almacén específico.

**MM03** - visualizar los datos maestros de materiales.

**ME21N** - crear pedidos de compra.

**ME23N** - visualizar órdenes de compra.

**MIGO_GR** - registrar la recepción de mercancías.

**MIRO** - procesar facturas de proveedores.

**F-53** - registrar pagos manuales a proveedores.

Ordenes de compra:

**ME21N:** Crear pedidos de compra

**ME23N:** Visualizar órdenes de compra

Recepción de mercancía:

**MIGO_GR:** Registrar la recepción de mercancías

Facturación:

**MIRO:** Procesar facturas de proveedores

Contabilidad:

**FB50:** Registrar manualmente asientos de diario en las cuentas de mayor de la empresa

**FB03:** Visualizar documentos contables que ya se han registrado en el sistema

Inventario:

**MMBE:** Visualizar el stock de materiales en un almacén específico

**MM03:** Visualizar los datos maestros de materiales

Pagos:

**F-53:** Registrar pagos manuales a proveedores

### Paso a Paso en FB50

1. **Navegar a la transacción FB50:**

   - **Ruta:** Accounting > Financial Accounting > General Ledger > Document Entry > FB50 - G/L Account Posting

   - **Transacción:** FB50



2. **Completar los Datos de Cabecera:**

   - **Document Date (Fecha de documento):** Fecha de hoy.

   - **Posting Date (Fecha de contabilización):** Fecha de hoy.

   - **Document Type (Tipo de documento):** SA (G/L Account Document).

   - **Currency (Moneda):** USD.



3. **Completar los Datos de Posición:**



   **Primera línea:**

   - **G/L Account (Cuenta de mayor):** [Cuenta de Alternate Bank Account]

   - **D/C (Débito o crédito):** Credit (Cr)

   - **Amount in doc.curr (Importe):** 10,000

   - **Tax code (Código de impuestos):** XI

   - **Tax jurisdiction code (Código de jurisdicción fiscal):** FL0000000



   **Segunda línea:**

   - **G/L Account (Cuenta de mayor):** [Cuenta de Rent Expense]

   - **D/C (Débito o crédito):** Debit (Dr)

   - **Amount in doc.curr (Importe):** 7,000

   - **Tax code (Código de impuestos):** XI

   - **Tax jurisdiction code (Código de jurisdicción fiscal):** FL0000000

   - **Cost Center (Centro de costo):** ## IT Costs (Reemplaza ## con tu usercode).



   **Tercera línea:**

   - **G/L Account (Cuenta de mayor):** [Cuenta de Rent Expense]

   - **D/C (Débito o crédito):** Debit (Dr)

   - **Amount in doc.curr (Importe):** 3,000

   - **Tax code (Código de impuestos):** XI

   - **Tax jurisdiction code (Código de jurisdicción fiscal):** FL0000000

   - **Cost Center (Centro de costo):** ## Marketing Costs (Reemplaza ## con tu usercode).



4. **Revisar y Guardar:**

   - Verifica que todos los datos estén correctos.

   - Haz clic en el botón "Save" (Guardar) o presiona Ctrl+S para guardar el documento.



### Detalles Adicionales



- **Alternate Bank Account:** Especifica el número de la cuenta de banco alterna que se utilizará para el crédito.

- **Rent Expense:** Especifica el número de la cuenta de gastos de alquiler que se utilizará para los débitos.

- **Cost Centers (Centros de costo):** Asegúrate de tener los códigos correctos para IT Costs y Marketing Costs. Si necesitas crearlos, asegúrate de hacerlo antes de registrar el asiento contable.



### Resumen del Asiento Contable



1. **Crédito:**

   - **Cuenta de mayor:** [Cuenta de Alternate Bank Account]

   - **Importe:** 10,000 USD

   - **Código de impuestos:** XI

   - **Código de jurisdicción fiscal:** FL0000000



2. **Débitos:**

   - **Cuenta de mayor:** [Cuenta de Rent Expense]

     - **Importe:** 7,000 USD

     - **Código de impuestos:** XI

     - **Código de jurisdicción fiscal:** FL0000000

     - **Centro de costo:** ## IT Costs



   - **Cuenta de mayor:** [Cuenta de Rent Expense]

     - **Importe:** 3,000 USD

     - **Código de impuestos:** XI

     - **Código de jurisdicción fiscal:** FL0000000

     - **Centro de costo:** ## Marketing Costs



Para resolver este caso en el módulo MM de SAP, sigue estos pasos detallados:



### Paso 1: Generar la Orden de Compra



1. **Navegar a la transacción ME21N:**

   - **Ruta:** Logistics > Materials Management > Purchasing > Purchase Order > Create > Vendor/Supplying Plant Known > ME21N - Create Purchase Order

   - **Transacción:** ME21N



2. **Completar los Datos Organizativos y de la Orden de Compra:**

   - **Vendor (Proveedor):** [Código del proveedor “## Olympic Protective Gear”]

   - **Purchasing Organization (Organización de compras):** [Tu organización de compras]

   - **Purchasing Group (Grupo de compras):** [Tu grupo de compras]

   - **Company Code (Código de la empresa):** [Tu código de la empresa]



3. **Completar los Detalles del Producto:**

   - **Item Overview (Visión general del ítem):**

     - **Material (Material):** SHRT10##A (T-Shirt)

     - **Quantity (Cantidad):** 200

     - **Net Price (Precio neto):** 15 USD por unidad

     - **Delivery Date (Fecha de entrega):** 15 de junio de 2024

     - **Plant (Centro):** [Centro de distribución de Miami]



4. **Guardar la Orden de Compra:**

   - Haz clic en el icono de guardar o presiona Ctrl+S.



### Paso 2: Realizar la Entrada de Mercancías por 180 Unidades



1. **Navegar a la transacción MIGO:**

   - **Ruta:** Logistics > Materials Management > Inventory Management > Goods Movement > Goods Receipt for Purchase Order > MIGO - Goods Movement

   - **Transacción:** MIGO



2. **Completar los Detalles de la Entrada de Mercancías:**

   - **Document Date (Fecha del documento):** [Fecha de hoy]

   - **Reference (Referencia):** [Número de la orden de compra]

   - **Goods Receipt (Recepción de mercancías):** Seleccionar el tipo de movimiento 101 (Recepción de Mercancías).

   - **Purchase Order (Orden de compra):** [Número de la orden de compra]



3. **Completar la Cantidad Recibida:**

   - En la sección **Item Overview (Visión general del ítem)**, actualizar la cantidad recibida a 180.



4. **Verificar y Guardar:**

   - Verifica los datos y guarda la entrada de mercancías.



### Paso 3: Registrar el Ingreso de la Factura por las 180 Unidades



1. **Navegar a la transacción MIRO:**

   - **Ruta:** Logistics > Materials Management > Logistics Invoice Verification > Document Entry > MIRO - Enter Incoming Invoice

   - **Transacción:** MIRO



2. **Completar los Detalles de la Factura:**

   - **Invoice Date (Fecha de la factura):** [Fecha de la factura]

   - **Posting Date (Fecha de contabilización):** [Fecha de hoy]

   - **Reference (Referencia):** [Número de referencia de la factura]

   - **Amount (Importe):** 2,700 USD (180 unidades x 15 USD)

   - **Tax Code (Código de impuestos):** [Si aplica]

   - **Purchase Order/Scheduling Agreement (Orden de compra/Acuerdo de entrega):** [Número de la orden de compra]



3. **Simulate y Post:**

   - Haz clic en **Simulate** para revisar el asiento contable.

   - Luego haz clic en **Post** para registrar la factura.



### Paso 4: Realizar el Pago de la Factura



1. **Navegar a la transacción F-53:**

   - **Ruta:** Accounting > Financial Accounting > Accounts Payable > Document Entry > Outgoing Payment > Post > F-53 - Post Outgoing Payments

   - **Transacción:** F-53



2. **Completar los Detalles del Pago:**

   - **Document Date (Fecha del documento):** [Fecha de hoy]

   - **Company Code (Código de la empresa):** [Tu código de la empresa]

   - **Currency (Moneda):** USD

   - **Bank Account (Cuenta bancaria):** [Cuenta bancaria desde la cual se realizará el pago]

   - **Vendor (Proveedor):** [Código del proveedor]

   - **Amount (Importe):** 2,700 USD



3. **Completar Detalles de Compensación:**

   - Haz clic en el botón para seleccionar la factura correspondiente.

   - Verifica los datos y guarda la transacción.



### Paso 5: Registrar la Recepción de las Unidades Faltantes



Para verificar cuántas unidades faltan por recepcionar:



1. **Navegar a la transacción ME23N:**

   - **Ruta:** Logistics > Materials Management > Purchasing > Purchase Order > Display > ME23N - Display Purchase Order

   - **Transacción:** ME23N



2. **Ingresar el Número de la Orden de Compra:**

   - Consulta el historial de pedidos para ver las cantidades recibidas y pendientes.



Para registrar las unidades faltantes:



1. **Navegar a la transacción MIGO:**

   - **Ruta:** Logistics > Materials Management > Inventory Management > Goods Movement > Goods Receipt for Purchase Order > MIGO - Goods Movement

   - **Transacción:** MIGO



2. **Completar los Detalles de la Entrada de Mercancías:**

   - **Document Date (Fecha del documento):** [Fecha de hoy]

   - **Reference (Referencia):** [Número de la orden de compra]

   - **Goods Receipt (Recepción de mercancías):** Seleccionar el tipo de movimiento 101 (Recepción de Mercancías).

   - **Purchase Order (Orden de compra):** [Número de la orden de compra]



3. **Completar la Cantidad Recibida:**

   - En la sección **Item Overview (Visión general del ítem)**, actualizar la cantidad recibida a 20 (cantidad faltante).



4. **Verificar y Guardar:**

   - Verifica los datos y guarda la entrada de mercancías.



### Resumen



- **Orden de Compra:** Generada para 200 unidades.

- **Entrada de Mercancías:** Realizada para 180 unidades.

- **Factura:** Registrada para 180 unidades.

- **Pago:** Realizado para la factura de 180 unidades.

- **Unidades Faltantes:** 20 unidades pendientes de recepción.

- **Transacción para Registrar Unidades Faltantes:** MIGO.
