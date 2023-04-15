# Info

easyUML v1.3 build for those still using NetBeans 8.2 after Update Centers were decommissioned and cannot upgrade certain dependencies to use easyUML version 1.4 (latest).

> Versión 1.3 de easyUML para quienes utilizan NetBeans 8.2 después de que  sus servidores de actualizaciones fueron dados de baja, y no pueden actualizar ciertas dependencias para poder instalar la versión 1.4 de easyUML (la última).

# Setup

- Download the contents of the "**updates**" folder, contained within the "**build**" folder.
- On NetBeans, go to ***Tools*** > ***Plugins*** > ***Downloaded*** > ***Add Plugins...***
- Select all the ***nbm*** files inside ***updates*** folder.
- Leave all checked, then click ***Install***.
- Click ***Next*** > ***Accept terms*** > ***Install*** > ***Continue*** > ***Restart IDE now***.

> - Descargar el contenido de la carpeta "***updates***" que está dentro de la carpeta "***build***".
> - En NetBeans, ir a ***Tools*** > ***Plugins*** > ***Downloaded*** > ***Add Plugins...***
> - Seleccionar todos los archivos ***nbm*** dentro de la carpeta ***updates***.
> - Dejar todos marcados y hacer click en ***Install***.
> - Click en ***Next*** > ***Accept terms*** > ***Install*** > ***Continue*** > ***Restart IDE now***.

## Build

- Clone this repository.
- Open Bash inside repo's folder and generate a keystore:

> keytool -genkey -keyalg RSA -storepass ***your_pass*** -alias ***your_alias***
> -keystore nbproject/private/keystore
- Answer the questions. Save your answers.
- Open NetBeans and open this project.
- Using project tree, open ***UML > Important FIles > Per-user NetBeans Platform Config***.
- Add the next lines with your own values and save changes:

> storepass=YOUR_STOREPASS_USED_ON_KEYSTORE
keystore.dname=YOUR_PERSONAL_VALUES_USED_ON_KEYSTORE
keystore.location=nbproject/private/
keystore.name=keystore
keystore.alias=YOUR_ALIAS
keystore.password=SAME_AS_STOREPASS

- Right click on **UML** project > ***Clean & Build***.
- Right click on **UML** project > ***Package as*** > ***NBMs***.
- Your new generated **nbm** files should be inside **build/updates**.