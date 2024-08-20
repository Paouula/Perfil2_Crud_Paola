CREATE TABLE pf_usuario(
    nombre VARCHAR2(100) not null,
    email VARCHAR2(100) not null,
    contra VARCHAR(100) not null
);

CREATE TABLE pf_ticket(
    num_ticket NUMBER GENERATED 
    BY DEFAULT AS IDENTITY PRIMARY KEY,
    titulo_ticket VARCHAR2(100) not null, 
    descripcion_ticket VARCHAR2(500) not null,
    autor_ticket VARCHAR(100) not null,
    email_contacto_autor VARCHAR(100) not null, 
    fecha_creacion DATE not null,
    estado_ticket VARCHAR(20) CHECK (estado_ticket IN('Activo', 'Finalizado'))NOT NULL,
    fecha_finalización DATE not null
);
