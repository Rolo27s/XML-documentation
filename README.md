# XML (eXtensible Markup Language)
Es un metalenguaje que permite definir lenguajes de marcas desarrollado por el World Wide Web Consortium (W3C) utilizado para almacenar datos en forma legible. <br>
Proviene del lenguaje SGML (Lenguaje de marcado generalizado standard) <br>
 A diferencia de otros lenguajes, XML da soporte a bases de datos, siendo útil cuando varias aplicaciones deben comunicarse entre sí o integrar información. <br>
 <br>
 Ejemplo de estructura básica de un documento XML
 ```ssh
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE Edit_Mensaje SYSTEM "Edit_Mensaje.dtd">
<Edit_Mensaje>
     <Mensaje>
          <Remitente>
               <Nombre>Nombre del remitente</Nombre>
               <Mail> Correo del remitente </Mail>
          </Remitente>
          <Destinatario>
               <Nombre>Nombre del destinatario</Nombre>
               <Mail>Correo del destinatario</Mail>
          </Destinatario>
          <Texto>
               <Asunto>
                    Este es mi documento con una estructura muy sencilla 
                    no contiene atributos ni entidades...
               </Asunto>
               <Parrafo>
                    Este es mi documento con una estructura muy sencilla 
                    no contiene atributos ni entidades...
               </Parrafo>
          </Texto>
     </Mensaje>
</Edit_Mensaje>
```
<br>

Ejemplo de código del DTD del documento «Edit_Mensaje.dtd»:
```ssh
    <?xml version="1.0" encoding="ISO-8859-1" ?>
    <!-- Este es el DTD de Edit_Mensaje -->

    <!ELEMENT Mensaje (Remitente, Destinatario, Texto)*>
    <!ELEMENT Remitente (Nombre, Mail)>
    <!ELEMENT Nombre (#PCDATA)>
    <!ELEMENT Mail (#PCDATA)>
    <!ELEMENT Destinatario (Nombre, Mail)>
    <!ELEMENT Nombre (#PCDATA)>
    <!ELEMENT Mail (#PCDATA)>
    <!ELEMENT Texto (Asunto, Parrafo)>
    <!ELEMENT Asunto (#PCDATA)>
    <!ELEMENT Parrafo (#PCDATA)>
```
