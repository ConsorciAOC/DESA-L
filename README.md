# DESA-L

### Índex

- [DESA-L](#desa-l)
		- [Índex](#índex)
- [1 Introducció <a name="1"></a>](#1-introducció-)
	- [1.1	Definició de nomenclatura de DESA’L <a name="1.1"></a>](#11definició-de-nomenclatura-de-desal-)
- [2 Model de Metadades <a name="2"></a>](#2-model-de-metadades-)
	- [2.1 Metadades de fitxer <a name="2.1"></a>](#21-metadades-de-fitxer-)
	- [2.1	Metadades d'expedient <a name="2.1"></a>](#21metadades-dexpedient-)
	- [2.2 Metadades de Document <a name="2.2"></a>](#22-metadades-de-document-)
- [3 Autenticació <a name="3"></a>](#3-autenticació-)
	- [3.1	Mètode d’autenticació <a name="3.1"></a>](#31mètode-dautenticació-)
	- [3.2	Permisologia DESA’L - Model de Control <a name="3.2"></a>](#32permisologia-desal---model-de-control-)
- [4 Capa Fitxer <a name="4"></a>](#4-capa-fitxer-)
	- [4.1 Càrrega de fitxer <a name="4.1"></a>](#41-càrrega-de-fitxer-)
		- [Petició](#petició)
		- [Resposta](#resposta)
		- [Codis de resposta](#codis-de-resposta)
	- [4.2 Descàrrega de fitxer <a name="4.1"></a>](#42-descàrrega-de-fitxer-)
		- [Petició](#petició-1)
		- [Resposta](#resposta-1)
		- [Codis de resposta](#codis-de-resposta-1)
- [5 Capa Expedient <a name="5"></a>](#5-capa-expedient-)
	- [5.1 Alta d&#39;Expedient <a name="5.1"></a>](#51-alta-dexpedient-)
		- [Petició Modalitat 1](#petició-modalitat-1)
		- [Resposta Modalitat 1](#resposta-modalitat-1)
		- [Petició Modalitat 2](#petició-modalitat-2)
		- [Resposta](#resposta-2)
		- [Codis de resposta](#codis-de-resposta-2)
	- [5.2 Modificació Expedient <a name="5.2"></a>](#52-modificació-expedient-)
		- [Petició](#petició-2)
		- [Resposta](#resposta-3)
		- [Codis de resposta](#codis-de-resposta-3)
	- [5.3 Eliminació d&#39;Expedient <a name="5.3"></a>](#53-eliminació-dexpedient-)
		- [Petició](#petició-3)
		- [Resposta](#resposta-4)
		- [Codis de resposta](#codis-de-resposta-4)
	- [5.4 Descàrrega d&#39;Expedient <a name="5.4"></a>](#54-descàrrega-dexpedient-)
		- [Petició](#petició-4)
		- [Resposta](#resposta-5)
		- [Codis de resposta](#codis-de-resposta-5)
	- [5.5 Descàrrega d&#39;Expedient en format ZIP <a name="5.5"></a>](#55-descàrrega-dexpedient-en-format-zip-)
		- [Modalitat 1: Descarregar metadades](#modalitat-1-descarregar-metadades)
		- [Petició](#petició-5)
		- [Resposta](#resposta-6)
		- [Modalitat 2: Descarregar metadades i Fitxers](#modalitat-2-descarregar-metadades-i-fitxers)
		- [Petició](#petició-6)
		- [Resposta](#resposta-7)
		- [Exemple XML inclòs en el fitxer ZIP](#exemple-xml-inclòs-en-el-fitxer-zip)
		- [Codis de resposta](#codis-de-resposta-6)
	- [5.6 Consulta estat ticket <a name="5.6"></a>](#56-consulta-estat-ticket-)
		- [Petició](#petició-7)
		- [Petició](#petició-8)
		- [Resposta pendent](#resposta-pendent)
		- [Resposta disponible](#resposta-disponible)
		- [Codis de resposta](#codis-de-resposta-7)
	- [5.7 Descarrega d&#39;Expedient en format ENI <a name="5.7"></a>](#57-descarrega-dexpedient-en-format-eni-)
		- [Petició](#petició-9)
		- [Resposta](#resposta-8)
		- [Codis de resposta](#codis-de-resposta-8)
- [6 Capa Document <a name="6"></a>](#6-capa-document-)
	- [6.1 Alta de Document <a name="6.1"></a>](#61-alta-de-document-)
		- [Petició alta document basic](#petició-alta-document-basic)
		- [Resposta alta document basic](#resposta-alta-document-basic)
		- [Petició alta document complet](#petició-alta-document-complet)
		- [Resposta document complert](#resposta-document-complert)
		- [Codis de Resposta](#codis-de-resposta-9)
	- [6.2 Modificació de Document <a name="6.2"></a>](#62-modificació-de-document-)
		- [Petició document model complet](#petició-document-model-complet)
		- [Resposta](#resposta-9)
		- [Codis de resposta](#codis-de-resposta-10)
	- [6.3 Eliminació de Document <a name="6.3"></a>](#63-eliminació-de-document-)
		- [Petició](#petició-10)
		- [Resposta](#resposta-10)
		- [Codis de resposta](#codis-de-resposta-11)
	- [6.4 Descarrega Document <a name="6.4"></a>](#64-descarrega-document-)
		- [Petició Modalitat 1: Descarrega Document](#petició-modalitat-1-descarrega-document)
		- [Resposta](#resposta-11)
		- [Petició Modalitat 2: Descarrega Document i contingut (fitxer)](#petició-modalitat-2-descarrega-document-i-contingut-fitxer)
		- [Resposta](#resposta-12)
		- [Codis de resposta](#codis-de-resposta-12)
	- [6.5 Descarrega Document en format ENI <a name="6.5"></a>](#65-descarrega-document-en-format-eni-)
		- [Petició](#petició-11)
		- [Resposta](#resposta-13)
		- [Codis de resposta](#codis-de-resposta-13)


# 1 Introducció <a name="1"></a>

DESA’L és un repositori documental transversal, flexible i parametritzable que s’ha habilitat a tots i cadascun dels ens als que l’AOC ofereix el seu catàleg de serveis d’administració electrònica. El repositori documental del DESA’L ofereix funcionalitats per a la captura, catalogació, classificació, custòdia, retenció, cerca i recuperació de documents electrònics generats pels serveis d’administració electrònica de l’AOC, o fins i tot de tercers.

DESA’L garanteix en tot moment la integritat dels documents, l’absència de malware, l’autenticitat dels integradors i l’auditoria exhaustiva de totes les operacions realitzades.

DESA’L permet enriquir els documents del repositori amb un llenguatge comú i compartit, anomenat model de metadades, que permet categoritzar els documents i, opcionalment, classificar-los en expedients (aquests expedients són la contrapartida als procediments administratius als que donen resposta el nostre catàleg de serveis d’administració electrònica).

DESA’L també ofereix funcionalitats avançades de cerca d’expedients i documents a partir d’un conjunt determinat de metadades definides com a indexables, i també permet la compartició d’expedients i documents amb serveis de tercers gràcies a les funcionalitats d’exportació en format ENI (Esquema Nacional d’Interoperabilitat).

Totes les funcionalitats que ofereix DESA’L són accessibles a través d’una API REST en format JSON. Aquest manual detalla la missatgeria associada a aquesta API, així com el procediment a seguir per realitzar la integració amb el servei DESA’L. 


**Important:** AAbans d’iniciar la integració amb el DESA’L és imprescindible que demaneu als responsables del DESA’L una reunió prèvia on us puguin assessorar i recomanar, entre d’altres temes, si heu de fer servir expedients, quin model de metadades de document heu d’escollir, com heu d’informar les metadades, quins permisos hauran de tenir els altres serveis integradors sobre els vostres expedients o documents, etc.

Els responsables del DESA’L s’encarregaran a la seva vegada de gestionar la vostra alta com a servei de DESA’L i us proporcionaran les credencials d’accés dels diferents entorns.

## 1.1	Definició de nomenclatura de DESA’L <a name="1.1"></a>

Per tal de garantir la comprensió de la nomenclatura que s’utilitza al DESA’L, a continuació definim les diferents entitats que conformen la nova solució:

- **Servei** : cada servei d’administració electrònica de l’AOC, o de tercers, que requereix la integració amb el DESA’L, ja sigui per nodrir el repositori amb nous documents i/o expedients, o bé per recuperar o cercar qualsevol d’aquests documents o expedients. L’alta d’un nou servei integrador s’ha de realitzar de forma exclusiva pel personal de l’AOC i el procediment per fer-ho resta fora de l’abast d’aquest manual.

- **Organisme** : cadascun dels diferents ens públics (ajuntaments, consells comarcals, diputacions, etc.) als que l’AOC presta servei a través del seu catàleg de serveis d’administració electrònica, i als que s’ha habilitat el repositori documental del DESA’L. L’alta d’un nou organisme al repositori documental del DESA’L s’ha de realitzar de forma exclusiva pel personal de l’AOC i el procediment per fer-ho resta fora de l’abast d’aquest manual.

- **Expedient** : és una entitat d’alt nivell formada pel conjunt ordenat de documents i actuacions que serveixen d’antecedent i fonament a la resolució administrativa, així com les diligències encaminades a executar-la. De forma més pràctica podem veure-ho com una carpeta que conté les seves pròpies metadades i un conjunt ordenat de documents que estan relacionats amb el procediment administratiu al que dona resposta l’expedient. L’ús d’expedients és opcional, però recomanem  encaridament el seu ús per les funcionalitats d’alt valor afegit que DESA’L ofereix. DESA’L no té cap limitació en quant al nombre de documents que pot contenir un únic expedient.

- **Fitxer** : binari (PDF, Word, imatge, etc.) que es puja i s’emmagatzema a DESA’L per tal que els serveis d’administració electrònica autoritzats el puguin referenciar a través d’un o més documents. Es tracta d’un element de baix nivell que s’utilitza únicament per evitar duplicats en els binaris. El seu cicle de vida per tant anirà condicionat al cicle de vida dels documents associats. La mida màxima que admet DESA’L per als fitxers és de 4,2GB.

- **Document** : entitat essencial del DESA’L formada per un conjunt de metadades i la relació amb un i només un fitxer de DESA’L . El document és l’entitat d’alt nivell amb la que realment han de treballar en tot moment els integradors. DESA’L contempla 2 models de metadades a nivell de document: bàsic i complet. DESA’L permet que un mateix fitxer (binari PDF, Word, ...) estigui referenciat per més d’un document i que cadascun d’aquests documents pugui tenir uns permisos i unes polítiques de retenció pròpies. D’altra banda, un document de DESA’L pot pertànyer de forma opcional a un, i només un, expedient.

# 2 Model de Metadades <a name="2"></a>

El model de metadades de cadascuna de les entitats (fitxer, document i expedient) ve definit pel conjunt de metadades que tindran associades cadascuna d’aquestes entitats, la seva tipologia i mida, si poden ser o no editables, així com si es poden fer servir per a les cerques.

En el model de metadades es podem distingir tres grups diferents de tipus de metadades:

**Metadades que ha d’aportar l’integrador.**

Es tracta de metadades que ha d’informar l’integrador en el moment de crear l’entitat. 

**Metadades que crea DESA’L automàticament.**

Es tracta de metadades que genera automàticament DESA’L en el moment de crear l’entitat i són metadades que DESA’L retorna en la resposta del mètode corresponent d’alta o modificació de l’entitat.

**Metadades ENI.**

Es tracta de metadades que genera automàticament DESA’L en el moment d’exportar un expedient o document en format ENI, d’acord a les especificacions tècniques publicades a les normes tècniques d’interoperabilitat corresponents. 

**Ampliació del model de metadades** **_InfoAddicional_** 

El servei integrador pot estendre els models de metadades d’expedient o document fent ús de la metadada infoAddicional. Aquesta metadada és de tipus Text, no té cap limitació de mida i està pensada per emmagatzemar en ella una llista de claus – valor d’acord a les necessitats específiques del servei integrador.

A continuació es presenten els diferents models de metadades que utilitza DESA’L per a cada tipus d’entitat. Per cada metadada s’especifica les següents característiques que determina el seu comportament:

| **Camp** | **Descripció** |
| --- | --- |
| **Nom element** | Variable que indica el nom de la metadada |
| **Consignació** | Variable que indica si és obligatòria o opcional. També existeix la possibilitat que sigui obligatòria, però condicionada al valor d’una alta metadada (la metadada relacionada es detalla en el camp observacions).|| **Longitud camp** | Variable que indica la longitud màxima permesa |
| **Tipus de camp** | Variable que indica el format que ha de tenir el camp. Poden ser de tipus:<ul><li>**Text**</li><li>**Número**</li><li>**Data i Hora.** S’utilitzarà format DD/MM/AAAA HH24:MI:SS</li><li>**Taula validada.** Taula predefinida amb uns valors determinats que poden ser ampliats en qualsevol moment per par dels administradors de DESA’L. Sempre es podran afegir nous valors a la taula, però mai es podran eliminar valors per evitar cap tipus d’inconsistència.</li><li>**URI**</li><li>**Booleà**</li></ul>|| **Validació o procedència de dades** | Variable que identifica com s&#39;ha d&#39;obtenir el valor en cas de necessari. |
| **Equivalència ENI** | Nom de la metadada a la missatgeria ENI. |
| **Equivalència MUX** | Nom de la metadada a la missatgeria de MUXv3. |
| **Qui informa** | Variable que identifica qui ha de aportar aquest valor. Es definiran dues opcions:<lu><li> **Aplicació que s&#39;integra**. Metadades que ha d&#39;aportar l&#39;integrador en el moment de crear l&#39;entitat.</li><li>- **DESA&#39;L**. Metadades que crea DESA&#39;L automàticament i que retorna a l&#39;integrador en la resposta del mètode de creació</li></lu>|
| **Automàtic** | Variable que indica si l&#39;ha de crear el sistema de manera automàtica o el sistema espera rebre aquesta dada |
| **Únic** | Variable que indica si el valor ha de ser únic dins el repositori documental o si es pot repetir. |
| **Repetitiu** | Variable que indica si la metadada pot tenir més d&#39;un valor o ha de ser únic. És a dir, si la metadada és de tipus llista. |
| **Indexable** | Variable que indica si internament, DESA&#39;L ha d&#39;indexar aquesta metadada per tal que es pugui incorporar en un futur com a criteri de cerca. |
| **Cercable** | Variable que indica si la metadada pot ser utilitzada com a criteri de filtre en els mètodes de cerca de document i expedient. |
| **Modificable en edició** | Variable que indica si el valor es podrà modificar un cop creada l&#39;entitat. L&#39;integrador només podrà modificar les dades que tinguin la variables Qui l&#39;informa igual a &quot;Aplicació que s&#39;integra&quot;. |
| **Observacions** | Variable que dona més detalls o que aclareix d&#39;algun aspecte important a tenir en compte de la metadada. |

## 2.1 Metadades de fitxer <a name="2.1"></a>

| **Nom element** | **Consignació** | **Longitud camp** | **Tipus de camp** | **Validació i procedència dades** | **Equivalencia ENI** | **Equivalencia MUX** | **Qui l&#39;informa** | **Automàtic** | **Únic** | **Repetitiu** | **Indexable** | **Cercable** | **Modificable edició** | **Observacions** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **CodiINE** | Obligatori | 10 | Text | -- | -- | -- | Aplicació que s'integra | No | No | No | N/A | N/A | N/A | Codi INE de l'ens propietari del fitxer |
| **CodiServei** | Obligatori | 10 | Text | -- | -- | -- | Aplicació que s'integra | No | No | No | N/A | N/A | N/A | Codi del servei propietari del fitxer |
| **NomFitxer** | Obligatori | 250 | Text | -- | NombreFichero | nomFitxer | Aplicació que s'integra | No | No | No | N/A | N/A | N/A | Nom del fitxer incloent l’extensió |
| **Mida** |	Obligatori | 	500 | 	Text | 	Validar que no sigui superior a 4,2GB	 | TamanoLogico | Mida | Aplicació que s'integra | No | No | No | N/A | N/A | N/A | És necessari informar la mida del fitxer per generar correctament la URL pre-signada per a fer la càrrega del binari a S3 |
| **FormatFitxer** | Opcional | 200 | Text | Disposem de la llista de tots els tipus acceptats | NombreFormato | tipusMIME | Aplicació que s'integra | Si | No | No | N/A | N/A | No | -- |
| -- | --| --| --| -- | -- | -- | **METADADES QUE CREA DESA'L AUTOMÀTICAMENT** | -- | --| -- | -- | -- | -- | -- |
| **UUIDFitxer** | Obligatori | 20 | Text | -- | SecuenciaIdentificador | --  | DESA'L | Si | Si | No | N/A | N/A | No	Identificador únic del fitxer  |
| **FormatFitxer** | Obligatori | 200 | Text | --  | NombreFormato | tipusMIME | DESA'L | Si | No | No | N/A | N/A | No | Content Type del fitxer. DESA’L el calcula automàticament si no s'informa a la petició d’alta del fitxer |
| **Hash** | Obligatori | 100 | Text | -- | Valor | hash | DESA'L | Si | Si | No | N/A | N/A | No | Hash del fitxer. |
| **HashAlgoritme** | Obligatori | 100 | Text | --  | Algoritmo | DESA'L | Si | No | No | N/A | N/A | No | Algoritme de hash utilitzat per calcular _hash_.  |
| **Mida**	 | Obligatori i condicional | 100 | Número | -- | TamanoLogico | Mida | DESA'L | Si | No | No | N/A | N/A | No | Mida real del fitxer. |
| **DataAlta**	 | Obligatori | -- | Data i hora | -- | -- | dataCapturaDocument | DESA'L | Si | No | No | N/A | N/A | No | Data de creació del fitxer.  |
| **Estat** | Obligatori | -- | Text | -- | -- | -- | DESA'L | Si | No | No | N/A | N/A | N/A | Aquest camp serveix per controlar l'estat del fitxer: <ul><li>- pendent (el fitxer s'està analitzant: virus, càlcul hash, etc)</li><li>- acceptat (ha passat totes les validacions i ja es pot utilitzar)</li><li>- rebutjat (no ha passat els controls)</li></ul> |




## 2.1	Metadades d'expedient <a name="2.1"></a>


| **Nom element** | **Consignació** | **Longitud** | **Tipus de  camp** | **Equivalencia ENI** | **Qui l'informa** | **Automàtic** | **Únic** | **Repetitiu**  | **Indexable** | **Cercable** | **Modificable en edició** | **Observacions** |
| -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
| **codiINE**	| Obligatori | 10 | Text | -- | Aplicació que s'integra	| No | No | No	| Si | Si | No | Codi INE de l’ens propietari de l’expedient |
| **codiServei** | Obligatori |	10 | Taula | -- | Aplicació que s'integra | No | No | No |Si	| Si | No | Codi del servei propietari de l’expedient |
|**identificador**|	Obligatori|	50|	Text|--|	 	Aplicació que s'integra	|No	|No|	No	|Si|	Si|	Si|	Número d’expedient |
|**titol** |	Obligatori|	500	|Text|	NombreNatural	|Aplicació que s'integra	|No|	No|	No|	Si|	Si|	Si|	Títol o assumpte de l'expedient|
|**dataInici**|	Obligatori|--|	 	Data i hora	|FechaAperturaExpediente|	Aplicació que s'integra	|Si|	No|	No	|Si	|Si|	Si|	Data d’obertura de l’expedient |
|**dataFi**	|Opcional|	validar formato data|	Data i hora	 |--|	Aplicació que s'integra|	No|	No	|No	|Si	|Si	|Si	| Data de tancament de l’expedient|
| **usuari** |	Opcional	|100	|Text	|--| 	Aplicació que s'integra	|No	|No	|No	|Si|	No|	No|	Dades identificatives de l’usuari que crea l'expedient|
|**unitatResponsable**|	Opcional|	250	|Text|--|	 	Aplicació que s'integra	|No	|No	|No|	Si|	No|	Si	|--|
| **codiClassificacio**	|Obligatori|	50|	Text|	CodigoClasificacion	|Aplicació que s'integra|	No|	No|	No|	Si|	Si|	Si	|--|
|**nomClassificacio**	|Obligatori|	250|	Text|	DenominacionClase	|Aplicació que s'integra|	No|	No|	No|	No|	No|	Si	|--|
|  **codiSIA**|	Opcional|	50	|Text	|CodigoClasificacion|	Aplicació que s'integra	|No	|No	|No	|Si	|Si	|Si	  |--|
|**nivellAcces**|	Opcional	| --|	Text|	NivelAcceso	|Aplicació que s'integra|	No|	No|	No	|Si	|No| 	Si	| <ul><li>A-Secret</li><li>B-Reservat</li><li>C-Confidencial</li><li>E-No classificat</li> </li>|
|**clasificacioENS**|	Opcional|	--| 	Text	|ClasificacionENS|	Aplicació que s'integra	|No	|No	|No	|Si|No|	Si|	Baix,Mig, Alt|
|**sensibilitatDadesCaracterPersonal**|	Opcional	| 	--|Text	|SensibilidadDatosCaracterPersonal	|Aplicació que s'integra|	No|	No|	No|	Si|	No|	Si|	Basic, Mig, Alt|
| **estatExpedient**|	Obligatori|	 --|	Text	|Estado|	Aplicació que s'integra	|No	|No	|No	|Si|	No|	Si| <ul><li>	E01 (Abierto)</li><li>E02 (Cerrado)</li><li>E03 (Índice para remisión cerrado).</li></ul>|
|**interessat**|	Opcional|	15	|Text|	Interesado|	Aplicació que s'integra|	No|	No	|Si|	Si|	Si|	Si|	Llista de ciutadans/persones jurídiques o administracions vinculades amb l’expedient<ul><li>a) Si ciudadà informar:DNI, NIE, NIF</li><li>b) Si administració informar: <Órgano> (DIR3)</li></ul>|
|**descripcio** |	Opcional|	500	|Text|	Descripcio|	Aplicació que s'integra	|No	|No|	No	|Si	|Si	|Si	 |--|
| **infoAddicional** | 	Opcional|--	| 	Text |--|	 	Aplicació que s'integra	|No|	No|	Si|	No|	No	|Si|	Llista de claus-valors que l’integrador pot fer servir per ampliar el model de metadades d’acord a les seves necessitats específiques|
|-- |-- |-- |-- |-- |-- |METADADES QUE CREA DESA'L AUTOMÀTICAMENT |-- |-- |-- |-- |-- |-- |
| **UUIDExpedient**|	Obligatori|	36	|Text|	SecuenciaIdentificador|	DESA'L|	Si|	Si|	No|	Si|	Si|	No|	Identificador únic de l'expedient|
|**dataAlta**	|Obligatori	 |--|	Data i hora	 |--|	DESA'L|	Si|	No|	No|	Si|	Si|	No|	Data d'alta de l'expedient a DESA'L|
| **versioNTI**	|Obligatori	 |--|	URI	|VersionNTI	|DESA'L|	Si|	No|	No	|No	|No	|No	|Valor per defecte: http://administracionelectronica.gob.es/ENI/XSD/v1.0/expediente-e |
|**identificadorENI**	|Obligatori	|52|	Text|	Identificador|	DESA'L|	Si|	No|	No|	Si|	No|	No	|Identificador utilitzat per a les exportacions ENI amb el format: ES_<Órgano>_<AAAA>_<UUIDExpedient>|
| **organ**	|Obligatori	|20	|Text|	Organo	|DESA'L|	Si|	No|	Si|	Si|	No|	No|	Equivalència codi INE amb el DIR3 |


A continuació detallem les diferents metadades i la seva definició per Exportació ENI:

| **Nom element** |**Consignació**|**Longitud camp**|	Tipus de camp|	Validació i procedència dades	|Equivalencia DESA'L|	Qui l'informa	|Automàtic|	Repetitiu	|Cercable|	Modificable en edició	|Observacions|
|--|--|--|--|--|--|--|--|--|--|--|--|
|--|--|--|--|--|METADADES QUE CREA DESA'L AUTOMÀTICAMENT AL FER UNA EXPORTACIÓ ENI|--|--|--|--|--|--|
| **versionNTI**|	Obligatori	|--| 	URI	|DESA'L|	N/A	|DESA'L|	Si|	No|	N/A	|N/A|	Valor per defecte: http://administracionelectronica.gob.es/ENI/XSD/v1.0/expediente-e|
|**identificador**|	Obligatori|	52|	Text	|DESA'L|	N/A	|DESA'L|	Si|	No|	N/A	|N/A|	L'element s'informa a partir d'altres metadades: ES_<Órgano>_<AAAA>_<Identificador>|
|**organo**|	Obligatori|	20	|Text	|DESA'L	|N/A|	DESA'L|	Si|	Si	|N/A|	N/A	|Equivalència codi INE amb el DIR3 |
|**fechaAperturaExpediente**|	Obligatori	|-- |	Data i hora|	DESA'L|	DataInici|	DESA'L|	Si|	No	|N/A|	N/A	 |--|
|**clasificacion**|	Obligatori	 |--|	Text|	DESA'L|	CodiSIA/CodiClassificacio|	DESA'L|	Si|	No|	N/A|	N/A	|Si existeix el codi SIA s'agafa aquest sinó el codi de classificació|
|**estado**|	Obligatori	|--| 	Text|	DESA'L	|EstatExpedient	|DESA'L|	Si|	No	|N/A|	N/A	 |--|
|**interesado**|	Opcional|--|	 	Text	|DESA'L	|Interessat	|DESA'L	|Si|	Si|	N/A	|N/A	|--| 


## 2.2 Metadades de Document <a name="2.2"></a>

DESA’L disposa de 2 models de metadades per als documents: el model bàsic i el model complet. Cada servei integrador utilitzarà un i només un d’aquests 2 models per a tots els documents que generi. Un cop donat d’alta el servei i definit el model de metadades dels seus documents no es podrà canviar de model. D’aquesta forma en el moment de crear el document aquest  heretarà el model de metadades que ha d’utilitzar en funció del servei propietari al que pertanyi i aquest model de metadades es mantindrà al llarg de tot el seu cicle de vida (és a dir no podrà canviar de cap manera el model de metadades d’un document un cop aquest hagi estat creat).

**Metadades de document bàsic.**

Es tracta del model de metadades mínim per poder donar d'alta un document al repositori documental del DESA’L. Els serveis que utilitzin aquest model de metadades bàsic no podran realitzar l’exportació en format ENI de documents ni d’expedients (en cas de sol·licitar l’exportació ENI DESA’L retornarà un error). Aquest model de metadades tindrà un ús molt restringit i el seu ús ha de ser especialment consensuat amb els responsables del DESA’L.



**Important:** el model de metadades de document que haurà de fer servir el vostre servei s’ha de consensuar amb els responsables del DESA’L. Un cop escollit el model de metadades del servei, no es podrà canviar.



A continuació es detallen les diferents metadades del model bàsic:


| Nom element |	Consignació	|Longitud camp |	Tipus de camp|	Equivalencia ENI|	Equivalencia MUX	|Qui l'informa|	Automàtic|	Únic|	Repetitiu	|Indexable	|Cercable	|Modificable edició|	Observacions|
|-- |-- |-- |-- |-- |-- |-- |-- |-- |-- |-- |-- |-- |-- |-- |
|**codiINE**	|Obligatori	|10|	Text|--|--|	 	 	Aplicació que s'integra|	No|	No|	No|	Si|	Si|	No	|Codi INE de l'ens propietari del document |
|**codiServei**|	Obligatori	|10	|Taula	|--|--| 	 	Aplicació que s'integra	|No	|No|	No|	Si|	Si|	No|	Codi del servei propietari del document|
|**nomFitxer**|	Obligatori i condicional|	250	|Text	|NombreFichero|	nomFitxer	|Aplicació que s'integra|	No|	No	|No	|Si	|No	|Si	|Nom del fitxer amb extensió. Només s'ha d’informar si contingut és 1|
|**nomNatural**|	Obligatori|	500	|Text|	NombreNatural|	nomNatural|	Aplicació que s'integra	|No|	No|	No	|Si	|Si|	Si|	Nom natural (sense extensió)|
|**dataDocument** |Obligatori	 	|--|Data i hora|	FechaInicio	| 	-- | Aplicació que s'integra|	No	|No	|No	|Si	|Si	|Si|--|
|**contingut**|	Obligatori	 |--|	Text	|--|--| 	 	Aplicació que s'integra|	No|	No|	No|	Si|	No|	No|	<ul><li>1) fitxer</li><li>2)URL</li><li>3) identificador extern</li></ul>|
|**interessat**|	Opcional|	20	|Text|	Interesado	|--| 	Aplicació que s'integra|	No|	No|	Si|	Si|	Si|	Si|	Llista de ciutadans/persones jurídiques o administracions vinculades amb l’expedient<ul><li>a) Si ciudadà informar:DNI, NIE, NIF</li><li>b) Si administració informar: <Órgano> (DIR3)</li></ul>|
|**usuari**|	Opcional|	250	|Text	|--|--| 	 	Aplicació que s'integra	|No	|No	|No	|Si	|No	|No	|Dades identificatives qui crea el document|
|**numeroRegistre**|	Opcional|	100	|Text|--|--|	 	 	Aplicació que s'integra	|No	|No	|No	|Si|	Si|	Si	 |--|
|**CSV**|	Opcional|	100	|Text	|--|--| 	 	Aplicació que s'integra|	No|	Si	|No	|Si	|Si	|No|Si el servei integrador informa el CSV, DESA’L comprovarà que sigui únic i en cas contrari retornarà un error.|
|**identificadorExpedientDesal**|Opcional|	100	|Text	|idEntidadRelacionada	|--| 	Aplicació que s'integra|	No|	No|	No|	No|	No|	Si|	Identificador de l'expedient de DESA'L al que pertany el document. DESA’L comprovarà que l'expedient existeixi i en cas contrari retornarà un error.|
| **identificadorExpedientExtern**|	Opcional|	100|	Text|	idEntidadRelacionada|--|	 	Aplicació que s'integra|	No|	No|	No|	Si|	Si|	Si|	Identificador informatiu, l'expedient no ha d'estar donat d'alta a DESA'L i DESA’L no farà cap tipus de valició d’aquest camp.|
|**UUIDFitxer**	|Obligatori i condicional|	20	|Text	|idEntidadRelacionada	 	|--|Aplicació que s'integra|	No|	No	|No	|Si	|Si|	Si|	Pensat per aquells documents que están relacionats amb un fitxer. Només s'ha d’informar si  contingut és 1.|
|**URLDocumentExtern**|	Obligatori i condicional	| --|	URI	|idEntidadRelacionada	|URL|	Aplicació que s'integra	|No	|No	|No	|No	|No	|Si	|Pensat per aquells documents que no tenen un fitxer associat i que el contingut del document está ubicat en un repositori extern. Només s'informa si contingut és 2|
|**identificadorDocumentExtern**|	Obligatori i condicional|	100|	Text|	idEntidadRelacionada|	identificador|	Aplicació que s'integra|	No|	No|	No	|Si|	Si|	Si|	Pensat per aquells documents que no tenen un fitxer associat i que el contingut del document está ubicat en un repositori extern. Només s'informa si contingut és 3|
|**infoAddicional**|	Opcional|	--| 	Text	| 	--|--| 	Aplicació que s'integra|	No|	No|	Si|	No|	No	|Si	|Llista de claus-valors que l’integrador pot fer servir per ampliar el model de metadades d’acord a les seves necessitats específiques|
|-- |-- |-- |-- |-- |-- |-- |METADADES QUE CREA DESA'L AUTOMÀTICAMENT |-- |-- |-- |-- |-- |-- |-- |
| **UUIDDocument**|	Obligatori|	36	|Text|	SecuenciaIdentificador|	uuid|	DESA'L|	Si|	Si|	No|	Si|	Si|	No|	Identificador únic del document|
|**CSV**|	Obligatori i condicional|	100|	Text|--|--|	 DESA'L	|Si	|Si	|No	|Si	|Si	|No	|CSV únic del document. Si l’integrador no l’inforna, DESA’L el generarà automàticament.|
|**formatFitxer**|	Obligatori i condicional|	200	|Text|	NombreFormato|	tipusMIME	|DESA'L	|Si	|No	|No	|Si|	No|	No	|Content Type del fitxer. Només es retorna si contingut és 1.|
|**hash**|	Obligatori i condicional|	100	|Text|	Valor	|hash	|DESA'L	|Si|	No|	No|	No	|No	|Si	|Valor hash del fitxer. Només es retorna si contingut és 1.|
|**hashAlgoritme** |	Obligatori i condicional|	100	|Text|	Algoritmo	 |--|	DESA'L|	Si|	No|	No|	No|	No|	Si	|Algoritme de hash utilitzat per calcular el hash del fitxer. Només es retorna si contingut és 1|
| **tamany**|	Obligatori i condicional|	100|	Número|	TamanoLogico	|Mida|	DESA'L|	Si|	No|	No|	Si|	No|	Si|	Mida del fitxer. Només es retorna si contingut és 1|
|**dataAlta**|	Obligatori	 |--|	Data i hora	 |--|	dataCapturaDocument	|DESA'L|	Si|	No|	No	|Si	|Si|	No|	Data d'alta del document a DESA'L|
|**identificadorExpedientDesal**|	opcional i condicional|	100	|Text|	idEntidadRelacionada	|--| 	DESA'L|	Si|	No|	Si|	No	|No	|No	|UUID de l’expedient amb el que està vinculat el document.|
| **versioNTI**|	Obligatori	 |--|	URI	|VersionNTI|	VersionNTI	|DESA'L|	Si|	No|	No|	No|	No|	No|	Valor per defecte: http://administracionelectronica.gob. es/ENI/XSD/v1.0/documento-e|
|**identificador**|	Obligatori|	52|	Text|	Identificador	|Identificador|	DESA'L|	Si|	No|	No	|Si	|No	|No	|Identificador del document en format ENI: ES_<Órgano>_<AAAA>_<UUIDDocument>|
|**organ**|	Obligatori|	20	|Text|	Organo|	Organo|	DESA'L|	Si|	No|	Si|	Si|	No	|No	|Equivalència codi INE amb el DIR3 del ens propietari del document.|



**Metadades de document complert.**

Es tracta del model de metadades que majoritàriament han d’utilitzar els serveis integradors. Aquest model inclou totes les metadades del document bàsic (amb les mateixes tipologies i validacions) i n’afegeix d’altres específiques que a continuació es detallen. El model complet sí que permet l’exportació en format ENI.      

| **Nom element** | **Consignació** | **Longitud camp** | **Tipus de camp** |  **Equivalencia ENI** | **Equivalencia MUX** | **Qui l&#39;informa** | **Automàtic** | **Únic** | **Repetitiu** | **Indexable** | **Cercable** | **Modificable edició** | **Observacions** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **estatElaboracio** | Obligatori | -- | Text | EstadoElaboracion | estatElaboracio | Aplicació que s'integra | No | No | No | Si | No | Si | <ul><li>EE01 - Original</li><li>EE02 - Copia electrónica auténtica con cambio de formato</li><li>EE04 - Copia electrónica parcial auténtica</li><li>EE99 - Otros.</li></ul>|
	
| **origen** | Obligatori | -- | boolea | OrigenCiudadanoAdministracion | origen | Aplicació que s'integra | No | No | No | No | No | Si | <ul><li>false= Ciudadano</li><li>true=Administración</li><ul>|
| **tipusDocumental** | Obligatori | -- | Text | TipoDocumental | tipusDocumentalNTI | Aplicació que s'integra | No | No | No | Si | No | Si | <ul><li>TD01 - Resolución</li><li>TD02 - Acuerdo</li><li>TD03 - Contrato</li><li>TD04 - Convenio</li><li>TD05 - Declaración</li><li>TD06 - Comunicación</li><li>TD07 - Notificación</li><li>TD08 - Publicación</li><li>TD09 - Acuse de recibo</li><li>TD10 - Acta</li><li>TD11 - Certificado</li><li>TD12 - Diligencia</li><li>TD13 - Informe</li><li>TD14 - Solicitud</li><li>TD15 - Denuncia</li><li>TD16 - Alegación</li><li>TD17 - Recursos</li><li>TD18 - Comunicación ciudadano</li><li>TD19 - Factura</li><li>TD20 - Otros incautados</li><li>TD51 - Ley</li><li>TD52 - Moción</li><li>TD53 - Instrucción</li><li>TD54 - Convocatoria</li><li>TD55 - Orden del día</li><li>TD56 - Informe de Ponencia</li><li>TD57 - Dictamen de Comisión</li><li>TD58 - Iniciativa legislativa</li><li>TD59 - Pregunta</li><li>TD60 - Interpelación</li><li>TD61 - Respuesta</li><li>TD62 - Proposición no de ley</li><li>TD63 - Enmienda</li><li>TD64 - Propuesta de resolución</li><li>TD65 - Comparecencia</li><li>TD66 - Solicitud de información</li><li>TD67 - Escrito</li><li>TD68 - Iniciativa legislativa</li><li>TD69 - Petición</li><li>TD99 - Otros.</li></ul>|
| **tipusSignatura** |	Obligatori	 	| --|Text	|TipoFirma|	tipusSignatura|	Aplicació que s'integra	| No|	No|	No|	Si|	No|	Si| <ul><li>TF01 - CSV </li><li>TF02 - XAdES internally detached signature</li><li>TF03 - XAdES enveloped signature</li><li>TF04 - CAdES detached/explicit signature </li><li>TF05 - CAdES attached/implicit signature</li><li>TF06 - PAdES</li><li>TF07 - XAdES Manifest</li></ul>|
| **CSVSignatura**|	Obligatori i condicional|	100	|Text	|ValorCSV|	valorCSV	|Aplicació que s'integra|	No|	No|	No|	Si|	Si|	Si	|Només s’ha d’informar si _TipoFirma_ és _TF01_ |
| **regulacioGeneracioCSVSignatura** |	Obligatori i condicional|	500	|Text	|RegulacionGeneracionCSV	|regulacioGeneracioCSV|	Aplicació que s'integra|	No	|No|	No|	No	|No|	Si|	Només s’ha d'informar si _TipoFirma_ és _TF01|
| **referenciaSignatura**	|Obligatori i condicional|	100	|Text	|ReferenciaFirma	|identificadorDocumentSignat|	Aplicació que s'integra|	No|	No|	No|	No	|No|	Si|	Referència al fitxer que inclou la signatura (UUID fitxer). Només s’ha d’informar si TipoFirma és TF03 o TF04. |
|**identificadorDocumentOrigen**	|Opcional i condicional|	250|	Text|	IdentificadorDocumentoOrigen	|identificadorDocumentOrigen|	Aplicació que s'integra|	No|	No|	No|	Si|	No	|Si|	Identificador normalizat del document origen al que correspon la còpia. Només s’ha d’informar si EstadoElaboracion és EE02, EE03 o EE04.|
|**tipusDocumentalSICRESD**	|Opcional|	--| 	Text|--|	 	tipusDocumentalSICRES	|Aplicació que s'integra|	No|	No|	No|	No|	No|	Si|<ul><li>	‘01’ = Formulario (el documento adjunto es un formulario con campos rellenos por el ciudadano remitente)</li><li>‘02’ = Documento adjunto al formulario (además del formulario, otro documento es adjuntado, acompañando al formulario)</li><li>‘03’ = Fichero técnico interno (el documento adjunto es un fichero interno. Por lo general, estos ficheros pueden resultar útiles para la Entidad Registral de destino, pero no son ficheros para presentar directamente a los usuarios de gestión).</li></ul>|
|**descripcio**|Opcional|	500	|Text	|Descripcion|	Observacions	|Aplicació que s'integra|	No|	No|	No|	Si|	Si|	Si|--|
|	 **nivellAcces**|	Opcional	| --| 	Enum|	NivelAcceso	 |--|	Aplicació que s'integra|	No|	No|	No|	Si|	No	|Si| <ul><li>A-Secret</li><li>B-Reservat</li><li>C-Confidencial</li><li>E-No classificat</li></ul> |
|**clasificacioENS** |	Opcional|--|	 	Enum	|ClasificacionENS	| -- | 	Aplicació que s'integra |	No |	No	| No	| Si |	No |	Si |	Baix, Mig, Alt |
| **sensibilitatDadesCaracterPersonal** |	Opcional	 |	-- |Enum |	SensibilidadDatosCaracterPersonal |--|	 	Aplicació que s'integra|	No|	No|	No|	Si|	No|	Si|	Basic, Mig, Alt |
| **documentEssencial** | 	Opcional	|--| 	boolea|	DocumentoEsencial	|--| 	Aplicació que s'integra|	No|	No|	No|	Si|	No|	Si|	True(si), False (NO) |
| **idioma**|	Opcional|	50|	Text|	Idioma	 |--|	Aplicació que s'integra	 |--|	No	 |	--| No |	No |--	 | --|
| **codiClassificacio** | 	Opcional |	50	|Text	| CodigoClasificacion	|--| 	Aplicació que s'integra|	No|	No|	No|	Si	|Si	|Si	 |--|
| **nomClassificacio** | Opcional | 250	| Text | DenominacionClase | -- | Aplicació que s'integra | No | No | No | No |	No | Si	 | -- |
| **codiSIA** | Opcional | 50 | Text | -- | -- |Aplicació que s'integra | No | No	|No |Si| Si |Si | -- |

 
# 3 Autenticació <a name="3"></a>

## 3.1	Mètode d’autenticació <a name="3.1"></a>

DESA’L implementa un mètode d’autenticació segur que permet garantir l’autenticitat del servei integrador, i la seva legitimitat per executar la petició, abans de procedir a executar qualsevol dels mètodes de l’API i abans d’accedir a qualsevol de les dades del repositori documental. 

Cada petició realitzada pel servei integrador és tractada pel DESA’L de forma totalment independent i requereix per tant d’un procés d’autenticació propi que autoritzi l’execució. DESA’L per tant no manté cap tipus d’estat ni de sessió amb el servei integrador.

**Important:** cada servei integrador disposarà d’unes credencials pròpies que li permetran interactuar amb els diferents entorns del DESA’L (DEV, PRE i PRO). Els responsables del DESA’L us facilitaran els jocs de credencials per a cada entorn, però és responsabilitat del servei integrador custodiar aquestes credencials de forma segura i evitar comprometre-les o exposar-les en els repositoris de codi font.

Les credencials d’autenticació del servei integrador no es renovaran periòdicament, però sí que és possible generar unes noves credencials si aquestes han estat compromeses. En cas de necessitar-ho us haureu de posar en contacte amb els responsables del DESA’L.


En els següents enllaços s’adjunta la documentació que explica com s’ha de generar la signatura de les peticions que es realitzin a l’API del DESA’L:

https://docs.aws.amazon.com/es_es/general/latest/gr/signing_aws_api_requests.html


https://docs.aws.amazon.com/apigateway/latest/developerguide/how-to-call-api-using-generated-sdk.html

També estan disponibles els SDKs d’AWS en diferents tipus de llenguatge que faciliten el procés d’autenticació:

https://docs.aws.amazon.com/es_es/apigateway/latest/developerguide/how-to-call-api-using-generated-sdk.html

https://docs.aws.amazon.com/es_es/apigateway/latest/developerguide/how-to-generate-sdk-javascript.html

https://docs.aws.amazon.com/es_es/apigateway/latest/developerguide/how-to-call-apigateway-generated-java-sdk.html


**Important:** l’AOC disposa d’un client Java que facilita molt tant la implementació del procés d’autenticació amb l’API del DESA’L com la pròpia invocació dels diferents mètodes. Si creieu que pot ser del vostre interès, sol·liciteu als responsables del DESA’L que us el facilitin.

## 3.2	Permisologia DESA’L - Model de Control <a name="3.2"></a>

Tot i que els serveis integradors amb DESA’L no us heu de preocupar de gestionar les autoritzacions i els permisos sobre els expedients i documents que doneu d’alta en el repositori documental del DESA’L, sí que creiem que és necessari que conegueu com funciona el sistema de permisos de DESA’L per tal que consensueu amb els responsables del DESA’L les autoritzacions que DESA’L haurà d’aplicar sobre els vostres expedients i documents.

Cada servei integrador que doni d’alta un nou expedient o un nou document esdevindrà el servei propietari d’aquest expedient o document. De forma anàloga, l’ens (organisme) que s’associï a l’expedient o document en el moment de la creació esdevindrà l’ens propietari de l’expedient o del document. Aquestes 2 dades, servei propietari i ens propietari, no es poden canviar al llarg del cicle de vida de l’expedient o document.

El servei propietari i l’ens propietari són la base per establir el sistema de permisos (model de control en terminologia DESA’L) que DESA’L aplicarà sobre els expedients i els documents. El funcionament del model de control és el següent: per defecte, tots els mètodes de l’API de DESA’L estan denegats, de forma que es requereix una autorització explícita al model de control de DESA’L per permetre qualsevol operació (fins i tot per al servei i ens propietaris!). Les autoritzacions es defineixen en base a 5 paràmetres:


| **Camp** | **Descripció** |
| --- | --- |
| **Mètode API** | Mètode específic de l&#39;API que es vol autoritzar |
| **Servei propietari** | Servei propietari del document o expedient sobre el que actuarà la regla d&#39;autorització |
| **Ens propietari** | Ens propietari del document o expedient sobre el que actuarà la regla d&#39;autorització |
| **Servei integrador** | Servei integrador que vol executar el mètode API |
| **Ens integrador** | Ens integrador que vol executar el mètode API |

La taula del model de control no té cap limitació en quant al nombre de registres que pot contenir. Aquests 5 paràmetres permeten definir un nivell màxim de granularitat i es poden combinar en tantes regles com sigui necessari. En paral·lel també es permet l’ús del comodí TOTS tant a nivell de servei integrador com de l’ens integrador per facilitar la gestió d’aquesta taula fent públiques determinades operacions a qualsevol integrador del DESA’L.

Cal destacar que qualsevol petició a l’API de DESA’L requerirà que hi hagi com a mínim una regla al model de control que autoritzi de forma explícita la seva execució. Cada regla és totalment independent de la resta i DESA’L les avalua de forma individual una a una fins que troba una regla que autoritza l’execució. La validació del model de control es realitza un cop verificada l’autenticat de l’integrador, però abans de l’execució del mètode.

A mode de resum, i per facilitar l’enteniment de la configuració de permisos que permet el  model de control del DESA’L, mostrem algunes de les opcions que DESA’L permet configurar:


- Configurar un servei, o també un organisme, de només lectura. Això es pot fer simplement no afegint cap permís a les operacions de modificació i esborrat d&#39;un determinat servei (o organisme)
- Configurar un servei totalment com a públic associant el comodí TOTS al servei integrador i a l&#39;ens integrador de tots els mètodes d&#39;aquest servei. Aquest ús públic es pot també limitar a determinades operacions com la descàrrega, la cerca o la modificació.
- Permetre a un organisme realitzar qualsevol operació única i exclusivament sobre els documents/expedients que estiguin vinculats a aquest organisme. P. ex. això permetria a un organisme com l&#39;Ajuntament de Terrassa accedir a qualsevol document/expedient seu.
- Permetre únicament a un conjunt reduït de serveis transversals (p. ex. el MyGov, el Portal de Transparència o el MUXv3) la cerca i/o descàrrega de documents o expedients d&#39;un determinat servei (p. ex. l&#39;eNotum), però no permetre en cap cas als serveis transversals la possibilitat de crear, modificar o esborrar els documents de l&#39;eNotum.
- Garantir a un servei que ell gestioni de forma exclusiva els seus propis documents/expedients i que exclogui a qualsevol altre servei integrador (incloent els serveis transversals de l&#39;AOC com MUXv3, MyGov o el Portal de Transparència) qualsevol tipus d&#39;accés a aquests documents/expedients.

# 4 Capa Fitxer <a name="4"></a>

A continuació es descriu en detall la capa de fitxers que DESA’L ofereix als integradors. Aquesta capa és responsable de la gestió dels binaris (PDF, Word, ...) que hem d’hostatjar a DESA’L. Es tracta d’una capa de baix nivell que hem d’utilitzar exclusivament mentre no disposem del document de DESA’L. 

La càrrega o descàrrega dels binaris dels fitxers es farà sempre a través de l’assignació d’una URL presignada d’S3 amb un temps d’expiració d’una hora. Passat aquest temps, l’URL presignada deixarà d’estar disponible i s’haurà de negociar una de nova amb DESA’L.

La capa de fitxer disposa únicament de 2 mètodes carregar fitxer i descarregar fitxer, tot i que el mètode de descarrega fitxer només estarà disponible mentre el fitxer no estigui vinculat a cap document. En cas d’estar vinculat a un document, la descàrrega del fitxer s’haurà de realitzar través del mètode de descàrrega de document que es detalla a l’apartat _**6.4 Descarregar Document**_.


**Important:** la capa de fitxer de DESA’L no disposa de cap política de permisos o autoritzacions. Qualsevol integrador que conegui un UUIDFitxer podrà descarregar aquest fitxer fins que el fitxer es vinculi a un document. Aquesta decisió de disseny ve determinada per garantir la política de permisos del model de control.

En cas de voler pujar una nova versió d’un fitxer, s’haurà de carregar un nou fitxer, amb un nou identificador UUIDFitxer. Posteriorment s’haurà d’actualitzar el document per vincular-lo a aquest nou fitxer. D’aquesta forma DESA’L no permet la gestió del versionat de fitxers.

**Important:** DESA’L té definida una política de purga per als fitxers carregats que no estiguin vinculats a cap document. Aquesta purga esborra de forma automàtica, i sense cap tipus d’excepció, tots els fitxers més antics d’un any que no estiguin vinculats a documents. 

Cal destacar que tot i que DESA’L podria arribar a permetre el seu ús com a simple capa d’emmagatzematge a través de l’ús exclusiu de la capa de Fitxer, realment no es tractaria d’un ús natural i el servei integrador hauria de tenir molt en compte aquesta política de purga automàtica.

## 4.1 Càrrega de fitxer <a name="4.1"></a>

La càrrega d’un fitxer a DESA’L s’ha de realitzar en 2 passos. Inicialment l’integrador ha d’executar el mètode de càrrega de fitxer del DESA’L per tal d’obtenir la URL presignada de S3 i a continuació haurà de realitzar la posterior càrrega del fitxer al bucket de S3 de DESA’L a partir d’aquesta URL.

DESA’L té un límit de mida de fitxer màxim de 4.2GB. Si s’intenta carregar un fitxer més gran, DESA’L retornarà un codi d’error i no permetrà la càrrega.

Cada fitxer que és carregat a DESA’L ha de ser analitzat pel sistema d’antivirus (basat en la solució ClamAV) de manera asíncrona. Existeixen diversos estats pels que ha de passar un fitxer abans de poder estar totalment disponible per al servei integrador:


- _**Pendent**_ – Fitxer pendent d&#39;analitzar pel sistema d&#39;antivirus. Fitxer encara no disponible per a poder ser utilitzat per part de l&#39;integrador. De mitja, l&#39;anàlisi de virus d&#39;un document PDF/Word inferior als 10MB és d&#39;uns 3 segons.
- _**Acceptat**_ – Fitxer analitzat, fitxer lliure de virus i preparat per a ser utilitzat per l&#39;integrador.
- _**Rebutjat**_ – Fitxer analitzat, **fitxer amb virus que ha estat eliminat pel DESA&#39;L** i que per tant no pot ser utilitzat per l&#39;integrador.

### Petició

A continuació es detallen els camps que el servei integrador ha d’informar en el primer pas per poder fer la càrrega d’un nou fitxer:

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| codiINE | Body | Si | Text | 10 | N/A |
| codiServei | Body | Si | Text | 10 | N/A |
| nomFitxer | Body | Si | Text | 250 | N/A |
| mida | Body | Si | Número | - | Unitat en bytes |
| formatFitxer | Body | Si | Text | 200 | N/A |

--**CONTINUAR AQUI**--

**URL** :[https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/fitxer](https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/fitxer)

**Method** : POST

**Auth** :&quot;AWS Signature&quot;

**AccessKey** : XXXXXXXXXXX

**SecretKey** : YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY
**AWSRegion** : eu-west-1

**Body** :

{

&quot;codiINE&quot;: &quot;0123456789&quot;,

&quot;codiServei&quot;: &quot;eVALISA&quot;,

&quot;mida&quot;: 651720,

&quot;nomFitxer&quot;: &quot;exemple1.pdf&quot;,

&quot;formatFitxer&quot;: &quot;pdf&quot;

}

 ![Shape17](RackMultipart20220211-4-2fc1qu_html_96bc06e22c4bead4.gif)

### Resposta

I també un exemple de resposta:

{

&quot;uuidFitxer&quot;: &quot;915844f3-ea3c-4c22-a1ec-1ab222d34301&quot;,

&quot;codiINE&quot;: &quot;0123456789&quot;,

&quot;codiServei&quot;: &quot;eVALISA&quot;,

&quot;nomFitxer&quot;: &quot;exemple1.pdf&quot;,

&quot;mida&quot;: &quot;651720&quot;,

&quot;formatFitxer&quot;: &quot;pdf&quot;,

&quot;urlPresignada&quot;: &quot;https://desal-temp-bucket.s3.eu-west-1.amazonaws.com/a7a4bb56-6086-4321-94eb-0d173666b3b2?X-Amz-Security-Token=IQoJb3JpZ2luX2VjELX%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCWV1LXdlc3QtMSJHMEUCIQCFcW%2F8QxhOycfciphk%2F5LQQKetZjrQ09KvOkGqZkWh6wIgWB6hn%2Bj7sugyk8%2FCFx%2B0r8WUAwU%2BT6d%2BXYzbCjm2ED8qxAIIXhABGgwyNTA3NTM4MDYyNjYiDM%2FB68K8p8alV1qK8yqhAorv7ISwSZXPaoohuTUVSgA7fRahRdoLkMNJKDxB95f73qlv03QvmNmq5cgAzbnYC20rQRbrUhzV1SA7jq9%2BKf44eQ6k0gAaNe%2BekzRaU3fe6boJxEFc8BY90EXXjRTJdXk%2Be5uDK8sGId1MZDFwplOVtQwfylr9shecQ%2BqwcP4zlRrshMgf1zM%2BMOWsRPt2xXIyW8sOvrNXPhGf68NwMLjfzjhVfqsWwOKVNa9wRHlcFIIshJlzJmLCjzGy%2Fi%2FNEZR1cd9JhSGsfp3yXelYaEp%2Fn%2B2NHFbSW1zCzTuXbDPhJd6W29qmlgWmB5JwdwhJ1N5yrFmNWs1s7jKqCLucqL04ETNa2tE02bKs66Ecp0bu7hhIJOhlpN8PNc%2Bn3DtU5UAwuaOPjAY6mgG%2FTmfyXhbCTz%2FceBiFcjJ6h1KY0Jcvzqq1WjnZbN47fu88PZnnB3pxT3428Bco3Ow9Xo5ag3U5PVWs14p8OFjcQ0SRt%2B2WP92N9rOxv180UNc9i6A%2Ban88El6%2FT6EApqMdC16r0agnN8aufQ3gv7gFwGH9z%2Fob5a4hmFcbQWrSDUThnpyZ4k4RLm2mTVTSMN5M%2Fp%2Bz%2Fr399q4t&amp;X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Date=20211104T122745Z&amp;X-Amz-SignedHeaders=content-length%3Bhost&amp;X-Amz-Expires=3599&amp;X-Amz-Credential=ASIATUYQXN65MSBM33L3%2F20211104%2Feu-west-1%2Fs3%2Faws4\_request&amp;X-Amz-Signature=c00aae9ad9db7f2898633a0d9994ba965aba2a0855d0f79f0d52ba918b386fdd&quot;,

&quot;codiResposta&quot;: &quot;0&quot;,

&quot;descripcioResposta&quot;: &quot;Operació realitzada correctament&quot;

}

 ![Shape18](RackMultipart20220211-4-2fc1qu_html_d1e15b72eb885b83.gif)

### Codis de resposta

A continuació es detallen els possibles codis d&#39;error per càrrega de fitxer (per al codi d&#39;error 10, XXXXXX especifica la metadada en qüestió i per al codi d&#39;error 100 XXXXXX ofereix més detalls de l&#39;error no controlat):

| **Codi** | **Descripció** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 10 | Error: la petició no és correcta. Hi ha metadades obligatòries sense informar o metadades informades no vàlides (XXXXXX). Operació NO realitzada. |
| 11 | Error: el codi INE indicat no és vàlid. Operació NO realitzada. |
| 12 | Error: el codi de servei indicat no és vàlid. Operació NO realitzada. |
| 13 | Error: la mida del fitxer supera el màxim permès. Operació NO realitzada. |
| 14 | Error: el nom del fitxer no és vàlid. Operació NO realitzada. |
| 15 | Error: el MIME/Type indicat no és vàlid. Operació NO realitzada. |
| 100 | Error no controlat: XXXXXX. Si us plau, reintenti l&#39;operació en uns minuts. Operació NO realitzada. |

## 4.2 Descàrrega de fitxer <a name="4.1"></a>

Aquest mètode permet demanar la descàrrega d&#39;un fitxer allotjat al repositori documental del DESA&#39;L, sempre i quan aquest fitxer no estigui encara referenciat per cap document de DESA&#39;L. La descarrega d&#39;un fitxer es farà també en 2 passos: una primera petició síncrona a a l&#39;API de DESA&#39;L que a partir de l&#39;UUIDFitxer retornarà l&#39;URL presignada de S3 i a continuació la descàrrega pròpiament del binari a partir de la URL presignada de S3.

**Important:** la descàrrega de fitxer només es pot executar mentre el fitxer no estigui referenciat per un document de DESA&#39;L. Un cop el fitxer estigui vinculat a un document, la recuperació només es podrà fer a través dels mètodes de document (p. ex. _ **6.4Descarregar Document** _)

### Petició 

A continuació es detallen els camps que han d&#39;informar el servei integrador per poder realitzar la descàrrega del fitxer i un exemple de resposta:

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| uuidFitxer | QueryParam | Si | Text | - | N/A |
| codiINE | QueryParam | Si | Text | 10 | N/A |
| codiServei | QueryParam | Si | Text | 10 |

 |

A continuació detallem un exemple de petició per a descàrrega de fitxer:

**URL** :[https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/fitxer?uuidFitxer=915844f3-ea3c-4c22-a1ec-1ab222d34301&amp;codiINE=0123456789&amp;codiServei=eVALISA](https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/fitxer?uuidFitxer=915844f3-ea3c-4c22-a1ec-1ab222d34301&amp;codiINE=123456789&amp;codiServei=eVALISA)

**Method** : GET

**Auth** :&quot;AWS Signature&quot;

**AccessKey** : XXXXXXXXXXX

**SecretKey** : YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY
**AWSRegion** : eu-west-1

**Body: (**buit)

 ![Shape19](RackMultipart20220211-4-2fc1qu_html_1143a38de23d2002.gif)

### Resposta

A continuació detallem un exemple de resposta per a descàrrega de fitxer:

{

&quot;uuidFitxer&quot;: &quot;18e4a137-5c35-423e-b183-c68816a79006&quot;,

&quot;codiINE&quot;: &quot;0000000000&quot;,

&quot;codiServei&quot;: &quot;enojordi&quot;,

&quot;nomFitxer&quot;: &quot;DESA&#39;L-Functional requirements English.pdf&quot;,

&quot;mida&quot;: &quot;651720&quot;,

&quot;formatFitxer&quot;: &quot;pdf&quot;,

&quot;urlPresignada&quot;: &quot;https://desal-download-bucket.s3.eu-west-1.amazonaws.com/2928c5a7-d729-4d16-b85a-c192c6755705/b970f2dd-24ce-4b8b-8b85-eaa2b9b81061?X-Amz-Security-Token=IQoJb3JpZ2luX2VjELn%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCWV1LXdlc3QtMSJHMEUCIQDK2n%2BMusQYqClBQSiGWmG%2BaKiOzGMTMl9%2Bv6VmX%2Bjv1wIgakoApPpXqAP%2B4VSIRGwGCmx%2Fq%2FB7khatzOtTwyNDE74qxAIIYhABGgwyNTA3NTM4MDYyNjYiDH%2FaIqcOyk8%2BF2ViqCqhAkfBwkDm1e6MDpHCImBJLOi%2BpaEYcIRBXvep9NB2PG4o3esRrUQ8bQCYXRUAd6zKX1wdQUVHQnclPAKbBOVVdh7doTqiUePLMvRwWhaRcO3TaA%2FItnVhpD5st9MkR2Imp87bAJNEXCxAj5cv5DLpe9y3Z3m1h%2BxkEhHPRPRKTm7gEeRS4OncZ0Q4FLV9I47FoFmixpPyRbqc6YfTDmNw%2BZQguLrDbbyjKHnSy1qqer0Ea0UQ1j6qnsxULDK3U2IwLeUfpIAH%2BN3bNyg28N51NHwc9aS2mnW3aDiym%2BCtTPhUYCmfclToPRBSRSgG6riiAKAHnJYGxVvcTjwKgiITAkDjF3GEmAhrBQa4JoPOL%2BwMEsqoZXTJD2TkaLqf3km%2FjPEwzZ6QjAY6mgGuWeatNPC12yd4QL0Yhx5WAFLU6vg%2Bz3r5RPiIrHSc2%2FSo34mY1v5jUCTFtzfyB9nCsf3uYd%2FIV64PGXN0apcMr0Cdp1sUBvv9JMkzhxoVx0CH7JLY6MGQnZVx9CYdY%2FKNxSbfXV%2FeEOnvhXJnJmxzYBtnTUsVYydWNs%2BpFSyRiEcIFx0FTog2Zpxs6RLckfhq02Xe6KAEazGT&amp;X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Date=20211104T165030Z&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Expires=3599&amp;X-Amz-Credential=ASIATUYQXN65CIDT26RK%2F20211104%2Feu-west-1%2Fs3%2Faws4\_request&amp;X-Amz-Signature=6be64e14e9bbcb4fe14fc21975b8948f5271cc8e3e4c6c7e0c57f5113ae9a0d3&quot;,

&quot;codiResposta&quot;: &quot;0&quot;,

&quot;hash&quot;: &quot;e3b199ba3d1c77660481c78f79f509ac272f35304f9b5a9c662caa7f336d6897&quot;,

&quot;hashAlgoritme&quot;: &quot;SHA-256&quot;,

&quot;descripcioResposta&quot;: &quot;Operació realitzada correctament&quot;

}

 ![Shape20](RackMultipart20220211-4-2fc1qu_html_4bd309b30d208a1b.gif)

### Codis de resposta

A continuació es detallen els possibles codis d&#39;error per a la descàrrega del fitxer (XXXXXX ofereix més detalls de l&#39;error no controlat):

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 11 | Error: l&#39;identificador del fitxer indicat no és vàlid. Operació NO realitzada. |
| 12 | Error: el codi de servei indicat no és vàlid. Operació NO realitzada. |
| 13 | Error: el codi INE especificat no és vàlid. Operació NO realitzada. |
| 14 | Error: el document físic conté virus i ha estat eliminat. Operació NO realitzada. |
| 100 | Error no controlat: XXXXXX. Si us plau, reintenti l&#39;operació en uns minuts. Operació NO realitzada. |

# 5 Capa Expedient <a name="5"></a>

L&#39;expedient és una entitat d&#39;alt nivell formada pel conjunt ordenat de documents i actuacions que serveixen d&#39;antecedent i fonament a la resolució administrativa, així com les diligències encaminades a executar-la. De forma més pràctica podem veure-ho com una carpeta que conté les seves pròpies metadades i un conjunt ordenat de documents que estan relacionats amb el procediment administratiu al que dona resposta l&#39;expedient. L&#39;ús d&#39;expedients és opcional, però recomanem encaridament el seu ús per les funcionalitats d&#39;alt valor afegit que DESA&#39;L ofereix. DESA&#39;L no té cap limitació en quant al nombre de documents que pot contenir un únic expedient.

A continuació es detallen tots els mètodes de l&#39;API de DESA&#39;L que permeten la gestió d&#39;expedients.

## 5.1 Alta d&#39;Expedient <a name="5.1"></a>

L&#39;alta d&#39;expedient és un mètode síncron que presenta 2 modalitats:

- **Modalitat 1** : es dona d&#39;alta únicament l&#39;expedient i més endavant el servei integrador anirà vinculant els documents a través de l&#39;UUIDExpedint que retorna DESA&#39;L (bé donant d&#39;alta aquests documents i associant-los a l&#39;expedient, o bé actualitzant els documents ja existents per establir el vincle amb el seu expedient)
- **Modalitat 2** : es dona d&#39;alta l&#39;expedient i de forma simultània en la mateixa operació la llista de documents associats a aquest expedient (posteriorment es podran associar més documents a aquest expedient). Aquesta modalitat s&#39;executa de forma atòmica, és a dir, o bé es dona d&#39;alta l&#39;expedient i tots i cadascun dels documents indicats, o en cas d&#39;error no es dona d&#39;alta cap entitat a DESA&#39;L.

A continuació es defineixen els camps que l&#39;integrador ha d&#39;informar per a donar d&#39;alta un nou expedient en qualsevol de les dues modalitats i la resposta que retorna DESA&#39;L:

### Petició Modalitat 1

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| codiINE | Body | Sí | Text | 10 | N/A |
| codiServei | Body | Sí | Text | 10 | N/A |
| identificador | Body |
 |
 | 50 | N/A |
| titol | Body | Sí | Text | 500 | N/A |
| dataInici | Body | Sí | Data | - | Format: DD/MM/AAAA HH:mm:SS |
| dataFi | Body | No | Data | - | Format: DD/MM/AAAA HH:mm:SS |
| Usuari | Body | No | Text | 100 | N/A |
| unitatResponsable | Body | No | Text | 250 | N/A |
| codiClassificacio | Body | Sí | Text | 50 | N/A |
| nomClassificacio | Body | Sí | Text | 250 | N/A |
| codiSIA | Body | No | Text | 50 | N/A |
| nivellAccess | Body | No | Text |
 | N/A |
| clasificacioENS | Body | No | Text |
 | N/A |
| sensibilitatDadesCaracterPersonal | Body | No | Text |
 | N/A |
| estatExpedient | Body | Sí | Text |
 | N/A |
| interessat | Body | No | Llista | - | Llista d&#39;interessats |
| descripció | Body | No | Text | 500 | N/A |
| infoAddicional | Body | No | Llista | - | Llista d&#39;elements clau/valor |

A continuació es detalla un exemple de petició:

**URL** :[https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/expedient](https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/expedient)

**Method** : POST

**Auth** :&quot;AWS Signature&quot;

**AccessKey** : XXXXXXXXXXX

**SecretKey** : YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY
**AWSRegion** : eu-west-1

**Body** :

{

&quot;codiINE&quot;: &quot;0123456789&quot;,

&quot;codiServei&quot;: &quot;eVALISA&quot;,

&quot;identificador&quot;: &quot;ident123&quot;,

&quot;titol&quot;: &quot;titol123&quot;,

&quot;dataInici&quot;: &quot;12/05/2021 22:45:15&quot;,

&quot;dataFi&quot;: &quot;07/06/2021 22:45:15&quot;,

&quot;usuari&quot;: &quot;usuari123&quot;,

&quot;unitatResponsable&quot;: &quot;unitatResponsable123&quot;,

&quot;codiClassificacio&quot;: &quot;codiClassificacio123&quot;,

&quot;nomClassificacio&quot;: &quot;nomClassificacio123&quot;,

&quot;codiSIA&quot;: &quot;codiSia123&quot;,

&quot;nivellAcces&quot;: &quot;C&quot;,

&quot;clasificacioENS&quot;: &quot;Baix&quot;,

&quot;sensibilitatDadesCaracterPersonal&quot;: &quot;Basic&quot;,

&quot;estatExpedient&quot;: &quot;E01&quot;,

&quot;interessat&quot;: [

&quot;82828282S&quot;

],
 &quot;descripcio&quot;: &quot;descripcio123&quot;,

&quot;infoAddicional&quot;: [

{

&quot;key&quot;: &quot;info1&quot;,

&quot;value&quot;: &quot;text1&quot;

}

]
 }

 ![Shape21](RackMultipart20220211-4-2fc1qu_html_2fbee4912b8588be.gif)

### Resposta Modalitat 1

{

&quot;uuidExpedient&quot;: &quot;19ecec92-5a70-4a9c-9eb1-1f10051614ae&quot;,

&quot;codiServei&quot;: &quot;eVALISA&quot;,

&quot;codiINE&quot;: &quot;00123456789&quot;,

&quot;titol&quot;: &quot;titol123&quot;,

&quot;dataInici&quot;: &quot;12/05/2021 22:45:15&quot;,

&quot;dataFi&quot;: &quot;07/06/2021 22:45:15&quot;,

&quot;usuari&quot;: &quot;usuari123&quot;,

&quot;unitatResponsable&quot;: &quot;unitatResponsable123&quot;,

&quot;codiClassificacio&quot;: &quot;codiClassificacio123&quot;,

&quot;nomClassificacio&quot;: &quot;nomClassificacio123&quot;,

&quot;codiSIA&quot;: &quot;codiSia123&quot;,

&quot;nivellAcces&quot;: &quot;C&quot;,

&quot;clasificacioENS&quot;: &quot;Baix&quot;,

&quot;sensibilitatDadesCaracterPersonal&quot;: &quot;Basic&quot;,

&quot;estatExpedient&quot;: &quot;E01&quot;,

&quot;interessat&quot;: [

&quot;82828282S&quot;

],

&quot;descripcio&quot;: &quot;descripcio123&quot;,

&quot;infoAddicional&quot;: [

{

&quot;key&quot;: &quot;82828282S&quot;,

&quot;value&quot;: &quot;11118282S&quot;

}

],

&quot;dataAlta&quot;: &quot;04/11/2021 18:20:16&quot;,

&quot;versioNTI&quot;: &quot;http://administracionelectronica.gob. es/ENI/XSD/v1.0/documento-e&quot;,

&quot;identificador&quot;: &quot;ident123&quot;,

&quot;organ&quot;: &quot;DIR3&quot;,

&quot;identificadorDesal&quot;: &quot;ES\_0000000000\_2021\_19ecec92-5a70-4a9c-9eb1-1f10051614ae&quot;,

&quot;codiResposta&quot;: &quot;0&quot;,

&quot;descripcioResposta&quot;: &quot;Operació realitzada correctament&quot;,

&quot;documents&quot;: null

}

 ![Shape22](RackMultipart20220211-4-2fc1qu_html_f9a4e57f4fc9e10a.gif)

### Petició Modalitat 2

En aquest cas, prèviament a l&#39;alta de l&#39;expedient, l&#39;integrador haurà d&#39;haver pujat al repositori documental del DESA&#39;L tots els fitxers que sigui necessari vincular als documents de l&#39;expedient, invocant tantes vegades com sigui necessari el mètode _ **4.1Càrrega de fitxer** _. D&#39;altra banda, el detall de les metadades que s&#39;han d&#39;informar per a cada document es detallen a l&#39;apartat _ **6.1Alta de Document** _ d&#39;aquest manual.

Abans de procedir a l&#39;alta de l&#39;expedient i del/s document/s, DESA&#39;L comprovarà que tots els fitxers referenciats existeixin i estiguin en _ **Estat** __ **Acceptat,** _ i de forma anàloga comprovarà que tots els documents a donar d&#39;alta compleixin les validacions que s&#39;han d&#39;aplicar en l&#39;alta de document. Només que hi hagi un únic fitxer o document que no sigui vàlid, DESA&#39;L rebutjarà tota l&#39;operació (recordem que l&#39;alta d&#39;expedient és una operació que DESA&#39;L ha d&#39;executar de forma atòmica) i indicarà explícitament en la resposta quin document no és vàlid i el motiu pel qual no ho és.

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| codiINE | Body | Sí | Text | 10 | N/A |
| codiServei | Body | Sí | Text | 10 | N/A |
| identificador | Body |
 |
 | 50 | N/A |
| titol | Body | Sí | Text | 500 | N/A |
| dataInici | Body | Sí | Data | - | Format: DD/MM/AAAA HH:mm:SS |
| dataFi | Body | No | Data | - | Format: DD/MM/AAAA HH:mm:SS |
| Usuari | Body | No | Text | 100 | N/A |
| unitatResponsable | Body | No | Text | 250 | N/A |
| codiClassificacio | Body | Sí | Text | 50 | N/A |
| nomClassificacio | Body | Sí | Text | 250 | N/A |
| codiSIA | Body | No | Text | 50 | N/A |
| nivellAccess | Body | No | Text |
 | N/A |
| clasificacioENS | Body | No | Text |
 | N/A |
| sensibilitatDadesCaracterPersonal | Body | No | Text |
 | N/A |
| estatExpedient | Body | Sí | Text |
 | N/A |
| interessat | Body | No | Llista | - | Llista d&#39;interessats |
| descripció | Body | No | Text | 500 | N/A |
| infoAddicional | Body | No | Llista | - | Llista d&#39;elements clau/valor |
| documents | Body |
 | Llista |
 | Llista de documents. Model del document definit a l&#39;apartat _ **6.1** _ |

**URL** :[https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/expedient](https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/expedient)

**Method** : POST

**Auth** :&quot;AWS Signature&quot;

**AccessKey** : XXXXXXXXXXX

**SecretKey** : YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY
**AWSRegion** : eu-west-1

**Body** :

{

&quot;codiINE&quot;: &quot;0123456789&quot;,

&quot;codiServei&quot;: &quot;eVALISA&quot;,

&quot;identificador&quot;: &quot;ident123&quot;,

&quot;titol&quot;: &quot;titol123&quot;,

&quot;dataInici&quot;: &quot;12/05/2021 22:45:15&quot;,

&quot;dataFi&quot;: &quot;07/06/2021 22:45:15&quot;,

&quot;usuari&quot;: &quot;usuari123&quot;,

&quot;unitatResponsable&quot;: &quot;unitatResponsable123&quot;,

&quot;codiClassificacio&quot;: &quot;codiClassificacio123&quot;,

&quot;nomClassificacio&quot;: &quot;nomClassificacio123&quot;,

&quot;codiSIA&quot;: &quot;codiSia123&quot;,

&quot;nivellAcces&quot;: &quot;C&quot;,

&quot;clasificacioENS&quot;: &quot;Baix&quot;,

&quot;sensibilitatDadesCaracterPersonal&quot;: &quot;Basic&quot;,

&quot;estatExpedient&quot;: &quot;E01&quot;,

&quot;interessat&quot;: [

&quot;82828282S&quot;

],
 &quot;descripcio&quot;: &quot;descripcio123&quot;,

&quot;infoAddicional&quot;: [

{

&quot;key&quot;: &quot;info1&quot;,

&quot;value&quot;: &quot;text1&quot;

}

],

&quot;documents&quot;: [

{

&quot;codiINE&quot;: &quot;0123456789&quot;,

&quot;codiServei&quot;: &quot;eVALISA&quot;,

&quot;nomFitxer&quot;: &quot;DESA&#39;L-Functional requirements English.pdf&quot;,

&quot;nomNatural&quot;: &quot;DESA&#39;L-Functional requirements English&quot;,

&quot;dataDocument&quot;: &quot;20/04/2121 22:45:15&quot;,

&quot;contingut&quot;: &quot;1&quot;,

&quot;interessat&quot;: [

&quot;82828282S&quot;

],

&quot;usuari&quot;: &quot;Joan Ningú&quot;,

&quot;numeroRegistre&quot;: &quot;1234&quot;,

&quot;csv&quot;: null,

&quot;identificadorExpedientDesal&quot;: &quot;&quot;,

&quot;identificadorExpedientExtern&quot;: null,

&quot;uuidFitxer&quot;: &quot;158a0ba3-ed06-42f8-8fc2-08f858428ab0&quot;,

&quot;urlDocumentExtern&quot;: null,

&quot;identificadorDocumentExtern&quot;: null,

&quot;infoAddicional&quot;: [

{

&quot;key&quot;: &quot;82828282S&quot;,

&quot;value&quot;: &quot;11118282S&quot;

}

],

&quot;estatElaboracio&quot;: &quot;EE01&quot;,

&quot;origen&quot;: true,

&quot;tipusDocumental&quot;: &quot;TD01&quot;,

&quot;tipusSignatura&quot;: &quot;TF01&quot;,

&quot;cSVSignatura&quot;: &quot;csvSigEx&quot;,

&quot;regulacioGeneracioCSVSignatura&quot;: &quot;regGen5345&quot;,

&quot;referenciaSignatura&quot;: null,

&quot;identificadorDocumentOrigen&quot;: null,

&quot;tipusDocumentalSICRESD&quot;: &quot;01&quot;,

&quot;descripcio&quot;: &quot;descripció d&#39;exemple&quot;,

&quot;nivellAcces&quot;: &quot;A&quot;,

&quot;clasificacioENS&quot;: &quot;Baix&quot;,

&quot;sensibilitatDadesCaracterPersonal&quot;: &quot;Basic&quot;,

&quot;documentEssencial&quot;: true,

&quot;idioma&quot;: &quot;es-ES&quot;,

&quot;codiClassificacio&quot;: &quot;25&quot;,

&quot;nomClassificacio&quot;: &quot;prioritari&quot;,

&quot;codiSIA&quot;: &quot;5512&quot;

}

]
 }

 ![Shape23](RackMultipart20220211-4-2fc1qu_html_29dd5646f4d34e49.gif)

### Resposta

{

&quot;uuidExpedient&quot;: &quot;a920d3e7-cfac-4c28-8bdf-6f911ea0fc31&quot;,

&quot;codiServei&quot;: &quot;eVALISA&quot;,

&quot;codiINE&quot;: &quot;0123456789&quot;,

&quot;titol&quot;: &quot;titol123&quot;,

&quot;dataInici&quot;: &quot;12/05/2021 22:45:15&quot;,

&quot;dataFi&quot;: &quot;07/06/2021 22:45:15&quot;,

&quot;usuari&quot;: &quot;usuari123&quot;,

&quot;unitatResponsable&quot;: &quot;unitatResponsable123&quot;,

&quot;codiClassificacio&quot;: &quot;codiClassificacio123&quot;,

&quot;nomClassificacio&quot;: &quot;nomClassificacio123&quot;,

&quot;codiSIA&quot;: &quot;codiSia123&quot;,

&quot;nivellAcces&quot;: &quot;C&quot;,

&quot;clasificacioENS&quot;: &quot;Baix&quot;,

&quot;sensibilitatDadesCaracterPersonal&quot;: &quot;Basic&quot;,

&quot;estatExpedient&quot;: &quot;E01&quot;,

&quot;interessat&quot;: null,

&quot;descripcio&quot;: &quot;descripcio123&quot;,

&quot;infoAddicional&quot;: null,

&quot;dataAlta&quot;: &quot;05/11/2021 07:30:24&quot;,

&quot;versioNTI&quot;: &quot;http://administracionelectronica.gob. es/ENI/XSD/v1.0/documento-e&quot;,

&quot;identificador&quot;: &quot;ident123&quot;,

&quot;organ&quot;: &quot;DIR3&quot;,

&quot;identificadorDesal&quot;: &quot;ES\_0000000000\_2021\_a920d3e7-cfac-4c28-8bdf-6f911ea0fc31&quot;,

&quot;codiResposta&quot;: &quot;0&quot;,

&quot;descripcioResposta&quot;: &quot;Operació realitzada correctament&quot;,

&quot;documents&quot;: [

{

&quot;uuidDocument&quot;: &quot;c9f6a4f0-1b1c-4ffe-82d4-3320db6faff4&quot;,

&quot;uuidFitxer&quot;: &quot;158a0ba3-ed06-42f8-8fc2-08f858428ab0&quot;,

&quot;codiINE&quot;: &quot;0123456789&quot;,

&quot;codiServei&quot;: &quot;eVALISA&quot;,

&quot;nomNatural&quot;: &quot;DESA&#39;L-Functional requirements English&quot;,

&quot;sensibilitatDadesCaracterPersonal&quot;: &quot;Basic&quot;,

&quot;documentEssencial&quot;: true,

&quot;idioma&quot;: &quot;es-ES&quot;,

&quot;codiClassificacio&quot;: &quot;25&quot;,

&quot;nomClassificacio&quot;: &quot;prioritari&quot;,

&quot;codiSIA&quot;: &quot;5512&quot;,

&quot;infoAddicional&quot;: [

{

&quot;key&quot;: &quot;82828282S&quot;,

&quot;value&quot;: &quot;11118282S&quot;

}

],

&quot;csv&quot;: &quot;00000000000511202163351D4B5740&quot;,

&quot;formatFitxer&quot;: &quot;iso&quot;,

&quot;hash&quot;: &quot;e3b199ba3d1c77660481c78f79f509ac272f35304f9b5a9c662caa7f336d6897&quot;,

&quot;hashAlgoritme&quot;: &quot;SHA-256&quot;,

&quot;mida&quot;: &quot;651720&quot;,

&quot;nomFitxer&quot;: &quot;DESA&#39;L-Functional requirements English.pdf&quot;,

&quot;uRLDocumentExtern&quot;: null,

&quot;dataAlta&quot;: &quot;05/11/2021 07:30:25&quot;,

&quot;dataDocument&quot;: &quot;20/04/2121 22:45:15&quot;,

&quot;contingut&quot;: &quot;1&quot;,

&quot;identificadorExpedientDesal&quot;: &quot;a920d3e7-cfac-4c28-8bdf-6f911ea0fc31&quot;,

&quot;identificadorExpedientExtern&quot;: null,

&quot;versioNTI&quot;: &quot;http://administracionelectronica.gob. es/ENI/XSD/v1.0/documento-e&quot;,

&quot;identificador&quot;: &quot;ES\_0000000000\_2021\_c9f6a4f0-1b1c-4ffe-82d4-3320db6faff4&quot;,

&quot;organ&quot;: &quot;DIR3&quot;,

&quot;estatElaboracio&quot;: &quot;EE01&quot;,

&quot;origen&quot;: true,

&quot;tipusDocumental&quot;: &quot;TD01&quot;,

&quot;tipusSignatura&quot;: &quot;TF01&quot;,

&quot;cSVSignatura&quot;: &quot;csvSigEx&quot;,

&quot;regulacioGeneracioCSVSignatura&quot;: &quot;regGen5345&quot;,

&quot;referenciaSignatura&quot;: null,

&quot;identificadorDocumentOrigen&quot;: null,

&quot;tipusDocumentalSICRESD&quot;: &quot;01&quot;,

&quot;descripcio&quot;: &quot;descripció d&#39;exemple&quot;,

&quot;nivellAcces&quot;: &quot;A&quot;,

&quot;clasificacioENS&quot;: &quot;Baix&quot;,

&quot;identificadorDocumentExtern&quot;: null,

&quot;codiResposta&quot;: &quot;0&quot;,

&quot;descripcioResposta&quot;: &quot;Operació realitzada correctament&quot;,

&quot;urlPresignada&quot;: null,

&quot;interessat&quot;: [

&quot;82828282S&quot;

],

&quot;usuari&quot;: &quot;Joan Ningú&quot;,

&quot;numeroRegistre&quot;: &quot;1234&quot;

}

]

}

 ![Shape24](RackMultipart20220211-4-2fc1qu_html_2af8ed997e3cebd6.gif)

Destaquem com en la Modalitat 2 tenim un codi de resposta i una descripció resposta global de tota l&#39;operació (remarcada en color groc) i un codi de resposta i una descripció resposta individual (remarcada en color verd) per a cada document que permet a l&#39;integrador saber exactament quin document no és vàlid i per què.

### Codis de resposta

A continuació es detallen els possibles codis de resposta per l&#39;alta d&#39;expedient (per al codi d&#39;error 11, XXXXXX especifica la metadada en qüestió i per al codi d&#39;error 100 XXXXXX ofereix més detalls de l&#39;error no controlat):

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 10 | Error: no tens autorització per realitzar aquesta operació. Operació NO realitzada. |
| 11 | Error: la petició no és correcta. Hi ha metadades obligatòries sense informar o metadades informades no vàlides (XXXXXX). Operació NO realitzada. |
| 12 | Error: el número d&#39;expedient ja existeix en el servei i organismo indicats. Operació NO realitzada. |
| 100 | Error no controlat: XXXXXX. Si us plau, reintenti l&#39;operació en uns minuts. Operació NO realitzada.. |

## 5.2 Modificació Expedient <a name="5.2"></a>

Aquest mètode permet la modificació de qualsevol metadada identificada com a editable de l&#39;expedient. Es permetrà la modificació de l&#39;expedient independentment del seu estat (fins i tot si l&#39;expedient es troba en _ **Estat Tancat** _).

Es permetrà realitzar la modificació d&#39;una o vàries metadades a la vegada. Les metadades que l&#39;integrador no informi en la seva petició, no es modificaran i mantindran el seu valor original. En cas d&#39;error, DESA&#39;L no modificarà cap de les metadades.

En el cas que l&#39;integrador necessiti esborrar una metadada, podrà fer-ho informant el valor null o una cadena buida si la metadada és de tipus Text. DESA&#39;L validarà però, que aquesta metadada no sigui obligatòria i en cas afirmatiu rebutjarà la petició.

### Petició

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| uuidExpedient | PathParam | Sí | Text | - |
 |
| codiINE | QueryParam | Sí | Text | 10 |
 |
| identificador | Body | No |
 | 50 | N/A |
| titol | Body | No | Text | 500 | N/A |
| dataInici | Body | No | Data | - | Format: DD/MM/AAAA HH:mm:SS |
| dataFi | Body | No | Data | - | Format: DD/MM/AAAA HH:mm:SS |
| unitatResponsable | Body | No | Text | 250 | N/A |
| codiClassificacio | Body | No | Text | 50 | N/A |
| nomClassificacio | Body | No | Text | 250 | N/A |
| codiSIA | Body | No | Text | 50 | N/A |
| nivellAccess | Body | No | Text |
 | N/A |
| clasificacioENS | Body | No | Text |
 | N/A |
| sensibilitatDadesCaracterPersonal | Body | No | Text |
 | N/A |
| estatExpedient | Body | No | Text |
 | N/A |
| interessat | Body | No | Llista | - | Llista de literals |
| descripció | Body | No | Text | 500 | N/A |
| infoAddicional | Body | No | Llista | - | Llista de literals |

**URL** :[https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/expedient](https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/expedient)/{uuidExpedient}?codiINE=0123456789

**Method** : PUT

**Auth** :&quot;AWS Signature&quot;

**AccessKey** : XXXXXXXXXXX

**SecretKey** : YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY
**AWSRegion** : eu-west-1

**Body** :

{

&quot;identificador&quot;: &quot;Testident123&quot;,

&quot;titol&quot;: &quot;Testtitol123&quot;,

&quot;dataInici&quot;: &quot;12/05/2021 22:45:15&quot;,

&quot;dataFi&quot;: &quot;07/06/2021 22:45:15&quot;,

&quot;unitatResponsable&quot;: &quot;unitatResponsable123&quot;,

&quot;codiClassificacio&quot;: &quot;codiClassificacio123&quot;,

&quot;nomClassificacio&quot;: &quot;nomClassificacio123&quot;,

&quot;codiSIA&quot;: &quot;codiSia123&quot;,

&quot;nivellAcces&quot;: &quot;C&quot;,

&quot;clasificacioENS&quot;: &quot;Baix&quot;,

&quot;sensibilitatDadesCaracterPersonal&quot;: &quot;Basic&quot;,

&quot;estatExpedient&quot;: &quot;E01&quot;,

&quot;interessat&quot;: [

&quot;82828282S&quot;

],

&quot;descripcio&quot;: &quot;descripcio123&quot;,

&quot;infoAddicional&quot;: [

{

&quot;key&quot;: &quot;82828282S&quot;,

&quot;value&quot;: &quot;11118282S&quot;

}

]

}

 ![Shape25](RackMultipart20220211-4-2fc1qu_html_4ba42b1760d39657.gif)

### Resposta

{

&quot;uuidExpedient&quot;: &quot;7b1941b5-39c7-46ee-8d39-6f87547bc477&quot;,

&quot;codiServei&quot;: &quot;eVALISA&quot;,

&quot;codiINE&quot;: &quot;0123456789&quot;,

&quot;titol&quot;: &quot;Testtitol123&quot;,

&quot;dataInici&quot;: &quot;12/05/2021 22:45:15&quot;,

&quot;dataFi&quot;: &quot;07/06/2021 22:45:15&quot;,

&quot;usuari&quot;: &quot;usuari123&quot;,

&quot;unitatResponsable&quot;: &quot;unitatResponsable123&quot;,

&quot;codiClassificacio&quot;: &quot;codiClassificacio123&quot;,

&quot;nomClassificacio&quot;: &quot;nomClassificacio123&quot;,

&quot;codiSIA&quot;: &quot;codiSia123&quot;,

&quot;nivellAcces&quot;: &quot;C&quot;,

&quot;clasificacioENS&quot;: &quot;Baix&quot;,

&quot;sensibilitatDadesCaracterPersonal&quot;: &quot;Basic&quot;,

&quot;estatExpedient&quot;: &quot;E01&quot;,

&quot;interessat&quot;: [

&quot;82828282S&quot;

],

&quot;descripcio&quot;: &quot;descripcio123&quot;,

&quot;infoAddicional&quot;: [

{

&quot;key&quot;: &quot;82828282S&quot;,

&quot;value&quot;: &quot;11118282S&quot;

}

],

&quot;dataAlta&quot;: &quot;06/08/2021 12:42:03&quot;,

&quot;versioNTI&quot;: &quot;http://administracionelectronica.gob. es/ENI/XSD/v1.0/documento-e&quot;,

&quot;identificador&quot;: &quot;Testident123&quot;,

&quot;organ&quot;: &quot;DIR3&quot;,

&quot;identificadorDesal&quot;: &quot;Teste&quot;,

&quot;codiResposta&quot;: &quot;0&quot;,

&quot;descripcioResposta&quot;: &quot;Operació realitzada correctament&quot;

}

 ![Shape26](RackMultipart20220211-4-2fc1qu_html_e576da95cd5a3277.gif)

### Codis de resposta

A continuació es detallen els possibles codis de resposta per a la modificació de l&#39;expedient (per al codi d&#39;error 11, XXXXXX especifica la metadada en qüestió i per al codi d&#39;error 100 XXXXXX ofereix més detalls de l&#39;error no controlat):

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 10 | Error: no tens autorització per realitzar aquesta operació. Operació NO realitzada. |
| 11 | Error: la petició no és correcta. Hi ha metadades obligatòries sense informar o metadades informades no vàlides (XXXXXX). Operació NO realitzada. |
| 12 | Error: l&#39;expedient no existetix al servei o organisme indicats. Operació NO realitzada. |
| 100 | Error no controlat: XXXXXX. Si us plau, reintenti l&#39;operació en uns minuts. Operació NO realitzada. |

## 5.3 Eliminació d&#39;Expedient <a name="5.3"></a>

Aquest mètode permet realitzar l&#39;esborrat d&#39;un expedient. L&#39;esborrat de l&#39;expedient es pot realitzar independentment de l&#39;estat de l&#39;expedient (fins i tot si l&#39;expedient es troba en _ **Estat Obert** _).

En el procés d&#39;eliminació de l&#39;expedient també s&#39;eliminaran en cascada tots els documents que aquest expedient tingui associats (és a dir, tots aquells documents amb la metadada _ **IdentificadorExpedientDesal** _ igual a l&#39;_ **UUIDExpedient** _ informat per l&#39;integrador) i de forma anàloga tots els fitxers referenciats per aquests documents que no estiguin referenciats per altres documents.

És important destacar que DESA&#39;L no realitzarà cap doble validació per eliminar en cascada els documents i/o fitxers referenciats per l&#39;expedient. Si en el model de control l&#39;integrador disposa d&#39;autorització per esborrar l&#39;expedient, DESA&#39;L realitzarà la operació en la seva totalitat tot i que no tingui permisos explícits per esborrar documents.

**Important:** l&#39;operació d&#39; **eliminar expedient** fa un esborrat físic de l&#39;expedient i dels documents que aquest tingui associats. Aquesta operació per tant **és irreversible** i DESA&#39;L no demanarà cap tipus de confirmació.

Així doncs, és responsabilitat del servei integrador implementar qualsevol política de confirmació amb l&#39;usuari que demana l&#39;operació i la implementació de qualsevol mecanisme de backup que pugui requerir, ja sigui dins el propi DESA&#39;L o amb algun altre repositori extern.

### Petició

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| uuidExpedient | PathParam | Sí | Text | - | N/A |
| codiINE | QueryParam | Sí | Text | 10 | N/A |
| codiServei | QueryParam | Sí | Text | 10 | N/A |

**URL** :[https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/expedient](https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/expedient)/{uuidExpedient}?codiINE=0123456789&amp;codiServei=eVALISA

**Method** : DELETE

**Auth** :&quot;AWS Signature&quot;

**AccessKey** : XXXXXXXXXXX

**SecretKey** : YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY
**AWSRegion** : eu-west-1

**Body** : (buit)

 ![Shape27](RackMultipart20220211-4-2fc1qu_html_faac99e2c4046f83.gif)

### Resposta

{

&quot;uuidExpedient&quot;: &quot;e12d9a61-6c98-4a1e-9e0f-96e97755d77c&quot;,

&quot;codiServei&quot;: &quot;eVALISA&quot;,

&quot;codiResposta&quot;: &quot;0&quot;,

&quot;descripcioResposta&quot;: &quot;Operació realitzada correctament&quot;

}

 ![Shape28](RackMultipart20220211-4-2fc1qu_html_8adf05a7a5ad809a.gif)

### Codis de resposta

A continuació es detallen els possibles codis de resposta de la petició d&#39;eliminació d&#39;expedient. Per al codi d&#39;error 100, XXXXXX ofereix més detalls de l&#39;error no controlat:

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament |
| 10 | Error: no tens autorització per realitzar aquesta operació. Operació NO realitzada. |
| 11 | Error: la petició no és correcta. Operació NO realitzada. |
| 12 | Error: l&#39;expedient indicat no existeix al servei i organisme indicats. Operació NO realitzada. |
| 100 | Error no controlat: XXXXXX. Si us plau, reintenti l&#39;operació en uns minuts. Operació NO realitzada. |

## 5.4 Descàrrega d&#39;Expedient <a name="5.4"></a>

Aquest mètode síncron permet obtenir les metadades de l&#39;expedient i dels documents associats a partir de l&#39;UUIDExpedient.

La descàrrega d&#39;expedients es pot realitzar independentment de l&#39;estat en que es trobi l&#39;expedient.

### Petició

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| uuidExpedient | PathParam | Sí | Text | - | N/A |
| codiINE | QueryParam | Sí | Text | 10 | N/A |
| codiServei | QueryParam | Sí | Text | 10 | N/A |

**URL** : https://goo1q9s080.execute-api.eu-west-1.amazonaws.com/pre/expedient/f176b0fd-9194-4068-877f-0f3eb80ad3fa?codiINE=9821920002&amp;codiServei=eVALISA

**Method** : GET

**Auth** :&quot;AWS Signature&quot;

**AccessKey** : XXXXXXXXXXX

**SecretKey** : YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY
**AWSRegion** : eu-west-1

**Body** : (buit)

**Body** : (buit)

 ![Shape29](RackMultipart20220211-4-2fc1qu_html_d1e93335dc0314cd.gif)

### Resposta

{

&quot;codiServei&quot; : &quot;eVALISA&quot;,

&quot;codiINE&quot; : &quot;9821920002&quot;,

&quot;uuidExpedient&quot; : &quot;3f90e981-8161-46c6-b15b-b3b4b646aad0&quot;,

&quot;titol&quot; : &quot;reenviar de nou url i pdf&quot;,

&quot;dataInici&quot; : &quot;08/11/2021 16:28:43&quot;,

&quot;usuari&quot; : &quot;82828282S&quot;,

&quot;codiClassificacio&quot; : &quot;IC00091&quot;,

&quot;nomClassificacio&quot; : &quot;Gestió dels serveis de tramitació interadministrativa&quot;,

&quot;estatExpedient&quot; : &quot;E01&quot;,

&quot;interessat&quot; : [],

&quot;infoAddicional&quot; : [],

&quot;dataAlta&quot; : &quot;08/11/2021 17:28:52&quot;,

&quot;versioNTI&quot; : &quot;http://administracionelectronica.gob.es/ENI/XSD/v1.0/documento-e&quot;,

&quot;identificador&quot; : &quot;35055&quot;,

&quot;organ&quot; : &quot;A09018933&quot;,

&quot;identificadorDesal&quot; : &quot;ES\_9821920002\_2021\_3f90e981-8161-46c6-b15b-b3b4b646aad0&quot;,

&quot;documents&quot; : [ {

&quot;codiServei&quot; : &quot;eVALISA&quot;,

&quot;codiINE&quot; : &quot;9821920002&quot;,

&quot;uuidDocument&quot; : &quot;9ac44522-2278-4159-bde8-e590eebebca1&quot;,

&quot;nomNatural&quot; : &quot;URL&quot;,

&quot;idioma&quot; : &quot;Català&quot;,

&quot;infoAddicional&quot; : [],

&quot;dataAlta&quot; : &quot;08/11/2021 17:28:54&quot;,

&quot;dataDocument&quot; : &quot;08/11/2021 16:28:43&quot;,

&quot;contingut&quot; : &quot;2&quot;,

&quot;identificadorExpedientDesal&quot; : &quot;3f90e981-8161-46c6-b15b-b3b4b646aad0&quot;,

&quot;versioNTI&quot; : &quot;http://administracionelectronica.gob.es/ENI/XSD/v1.0/documento-e&quot;,

&quot;identificador&quot; : &quot;ES\_9821920002\_2021\_9ac44522-2278-4159-bde8-e590eebebca1&quot;,

&quot;organ&quot; : &quot;A09018933&quot;,

&quot;estatElaboracio&quot; : &quot;EE01&quot;,

&quot;origen&quot; : true,

&quot;tipusDocumental&quot; : &quot;TD99&quot;,

&quot;tipusSignatura&quot; : &quot;TF01&quot;,

&quot;regulacioGeneracioCSVSignatura&quot; : &quot;Resolució sobre l&#39;ús del sistema de codi segur de verificació del Consorci AOC&quot;,

&quot;tipusDocumentalSICRESD&quot; : &quot;02&quot;,

&quot;nivellAcces&quot; : &quot;E&quot;,

&quot;interessat&quot; : [],

&quot;usuari&quot; : &quot;82828282S&quot;,

&quot;codiResposta&quot; : 0,

&quot;descripcioResposta&quot; : &quot;Operació realitzada correctament.&quot;,

&quot;csv&quot; : &quot;98219200020811202132T8M3IE3OUU&quot;,

&quot;urlDocumentExtern&quot; : &quot;http://www.google.es&quot;,

&quot;cSVSignatura&quot; : &quot;98219200020811202132T8M3IE3OUU&quot;

}, {

&quot;codiServei&quot; : &quot;eVALISA&quot;,

&quot;codiINE&quot; : &quot;9821920002&quot;,

&quot;uuidDocument&quot; : &quot;dc99e82b-0341-435f-881b-7ed55bb885a2&quot;,

&quot;nomNatural&quot; : &quot;URL&quot;,

&quot;idioma&quot; : &quot;Català&quot;,

&quot;infoAddicional&quot; : [],

&quot;dataAlta&quot; : &quot;08/11/2021 17:28:54&quot;,

&quot;dataDocument&quot; : &quot;08/11/2021 16:28:43&quot;,

&quot;contingut&quot; : &quot;2&quot;,

&quot;identificadorExpedientDesal&quot; : &quot;3f90e981-8161-46c6-b15b-b3b4b646aad0&quot;,

&quot;versioNTI&quot; : &quot;http://administracionelectronica.gob.es/ENI/XSD/v1.0/documento-e&quot;,

&quot;identificador&quot; : &quot;ES\_9821920002\_2021\_dc99e82b-0341-435f-881b-7ed55bb885a2&quot;,

&quot;organ&quot; : &quot;A09018933&quot;,

&quot;estatElaboracio&quot; : &quot;EE01&quot;,

&quot;origen&quot; : true,

&quot;tipusDocumental&quot; : &quot;TD99&quot;,

&quot;tipusSignatura&quot; : &quot;TF01&quot;,

&quot;regulacioGeneracioCSVSignatura&quot; : &quot;Resolució sobre l&#39;ús del sistema de codi segur de verificació del Consorci AOC&quot;,

&quot;tipusDocumentalSICRESD&quot; : &quot;02&quot;,

&quot;nivellAcces&quot; : &quot;E&quot;,

&quot;interessat&quot; : [],

&quot;usuari&quot; : &quot;82828282S&quot;,

&quot;codiResposta&quot; : 0,

&quot;descripcioResposta&quot; : &quot;Operació realitzada correctament.&quot;,

&quot;csv&quot; : &quot;9821920002081120213URJ3PE513TO&quot;,

&quot;urlDocumentExtern&quot; : &quot;http://www.aoc.cat&quot;,

&quot;cSVSignatura&quot; : &quot;9821920002081120213URJ3PE513TO&quot;

}],

&quot;codiResposta&quot; : 0,

&quot;descripcioResposta&quot; : &quot;Operació realitzada correctament.&quot;

}

 ![Shape30](RackMultipart20220211-4-2fc1qu_html_2c79acab5706f21b.gif)

### Codis de resposta

A continuació es detallen els possibles codis de resposta per a la descàrrega d&#39;expedient:

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 10 | Error: no tens autorització per realitzar aquesta operació. Operació NO realitzada. |
| 11 | Error: la petició no és correcta. Operació NO realitzada. |
| 12 | Error: l&#39;expedient indicat no existeix en el servei i organisme indicats. Operació NO realitzada. |
| 100 | Error no controlat: XXXXXX. Si us plau, reintenti l&#39;operació en uns minuts. Operació NO realitzada. |

## 5.5 Descàrrega d&#39;Expedient en format ZIP <a name="5.5"></a>

Aquest mètode asíncron permet obtenir i descarregar en un fitxer ZIP les metadades de l&#39;expedient i dels documents associats a partir de l&#39;UUIDExpedient (Modalitat 1). De forma opcional permet també recuperar l&#39;URL per poder descarregar tots els binaris dels documents (Modalitat 2). A diferència de la majoria de mètodes de l&#39;API del DESA&#39;L que treballen en format JSON, aquest mètode retorna la metadades en un fitxer XML que es troba dins el fitxer ZIP a descarregar.

La descàrrega d&#39;expedients es pot realitzar independentment de l&#39;estat en que es trobi l&#39;expedient.

Tal i com indiquem, la descàrrega d&#39;expedient es un procés asíncron. La resposta d&#39;aquesta petició asíncrona retorna un codi de tiquet que ens servirà per poder consultar l&#39;estat de la descàrrega i obtenir la URL de descàrrega del fitxer ZIP tan bon punt estigui disponible. Per poder saber si el fitxer ZIP ja està disponible, DESA&#39;L ofereix el mètode _ **5.6Consulta ticket** _ que permet obtenir la URL presignada per tal que l&#39;integrador pugui descarregar el zip. Aquesta URL presignada té un temps d&#39;expiració d&#39;una hora, passat aquest temps no serà vàlida i s&#39;haurà de tornar a realitzar una petició.

### Modalitat 1: Descarregar metadades

Aquesta modalitat permet descarregar un fitxer ZIP que conté únicament un fitxer XML amb totes les metadades de l&#39;expedient i dels documents associats.

### Petició

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| uuidExpedient | PathParam | Sí | Text | - | N/A |
| codiINE | QueryParam | Sí | Text | 10 | N/A |
| codiServei | QueryParam | Sí | Text | 10 | N/A |
| modality | QueryParam | Sí | Número | - | Per a modalitat 1, indicar &quot;1&quot; |

**URL** : [https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/expedient/{uuidExpedient}/download?codiServei=eVALISA&amp;codiINE=0123456789&amp;modality=1](https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/expedient/%7BuuidExpedient%7D/download?codiServei=eVALISA&amp;codiINE=123456789&amp;modality=1)

**Method** : GET

**Auth** :&quot;AWS Signature&quot;

**AccessKey** : XXXXXXXXXXX

**SecretKey** : YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY
**AWSRegion** : eu-west-1

**Body** : (buit)

**Body** : (buit)

 ![Shape31](RackMultipart20220211-4-2fc1qu_html_d1e93335dc0314cd.gif)

### Resposta

{

&quot;codiResposta&quot;: &quot;0&quot;,

&quot;descripcioResposta&quot;: &quot;Operació realitzada correctament&quot;,

&quot;idTicket&quot;: &quot;f22fd5d3-ced5-4022-a407-389101fc3286&quot;

}

 ![Shape32](RackMultipart20220211-4-2fc1qu_html_3783de7c95a508d7.gif)

### Modalitat 2: Descarregar metadades i Fitxers

Aquesta modalitat permet descarregar també un fitxer ZIP que conté el fitxer XML amb les metadades de l&#39;expedient i dels documents associats, però el fitxer ZIP també conté el contingut dels fitxers vinculats amb els documents de l&#39;expedient.

### Petició

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| uuidExpedient | PathParam | Sí | Text | - | N/A |
| codiINE | QueryParam | Sí | Text | 10 | N/A |
| codiServei | QueryParam | Sí | Text | 10 | N/A |
| modality | QueryParam | Sí | Número | - | Per a modalitat 2, indicar &quot;2&quot; |

**URL** : [https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/expedient/{uuidExpedient}/download?codiServei=eVALISA&amp;codiINE=0123456789&amp;modality=2](https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/expedient/%7BuuidExpedient%7D/download?codiServei=eVALISA&amp;codiINE=123456789&amp;modality=2)

**Method** : GET

**Auth** :&quot;AWS Signature&quot;

**AccessKey** : XXXXXXXXXXX

**SecretKey** : YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY
**AWSRegion** : eu-west-1

**Body** : (buit)

**Body** : (buit)

 ![Shape33](RackMultipart20220211-4-2fc1qu_html_d1e93335dc0314cd.gif)

### Resposta

{

&quot;codiResposta&quot;: &quot;0&quot;,

&quot;descripcioResposta&quot;: &quot;Operació realitzada correctament&quot;,

&quot;idTicket&quot;: &quot;fasdfd5d3-c34d5-4652-a987-987101fc3286&quot;

}

 ![Shape34](RackMultipart20220211-4-2fc1qu_html_3783de7c95a508d7.gif)

### Exemple XML inclòs en el fitxer ZIP

\&lt;XmlExpedient\&gt;

\&lt;uuidExpedient\&gt;985e4e19-01f3-4819-8f13-7be6b95185e3\&lt;/uuidExpedient\&gt;

\&lt;codiServei\&gt;eVALISA\&lt;/codiServei\&gt;

\&lt;codiIne\&gt;7515090124\&lt;/codiIne\&gt;

\&lt;titol\&gt;prova nova versió de DESA&#39;L PRE\&lt;/titol\&gt;

\&lt;dataInici\&gt;16/11/2021 12:46:45\&lt;/dataInici\&gt;

\&lt;usuari\&gt;45541608K\&lt;/usuari\&gt;

\&lt;codiClassificacio\&gt;IC00091\&lt;/codiClassificacio\&gt;

\&lt;nomClassificacio\&gt;Gestió dels serveis de tramitació interadministrativa\&lt;/nomClassificacio\&gt;

\&lt;estatExpedient\&gt;E01\&lt;/estatExpedient\&gt;

\&lt;dataAlta\&gt;16/11/2021 13:46:52\&lt;/dataAlta\&gt;

\&lt;versioNTI\&gt;http://administracionelectronica.gob.es/ENI/XSD/v1.0/documento-e\&lt;/versioNTI\&gt;

\&lt;identificador\&gt;1416811\&lt;/identificador\&gt;

\&lt;organ\&gt;A09018845\&lt;/organ\&gt;

\&lt;identificadorDesal\&gt;ES\_7515090124\_2021\_985e4e19-01f3-4819-8f13-7be6b95185e3\&lt;/identificadorDesal\&gt;

\&lt;documents\&gt;

\&lt;document\&gt;

\&lt;uuidDocument\&gt;fc9041c2-e730-44b7-b812-05b131efed3e\&lt;/uuidDocument\&gt;

\&lt;uuidService\&gt;eVALISA\&lt;/uuidService\&gt;

\&lt;idioma\&gt;Català\&lt;/idioma\&gt;

\&lt;nomNatural\&gt;ORGANISMS\_DIR3\_v1\&lt;/nomNatural\&gt;

\&lt;csv\&gt;751509012416112021PRN084GP4JF\&lt;/csv\&gt;

\&lt;formatFitxer\&gt;text/plain\&lt;/formatFitxer\&gt;

\&lt;has\&gt;1847d151f72f5d4e12b80815076725047c4972472fc905bd0a5de2d19891f618\&lt;/has\&gt;

\&lt;hashAlgoritme\&gt;SHA-256\&lt;/hashAlgoritme\&gt;

\&lt;mida\&gt;33894\&lt;/mida\&gt;

\&lt;nomFitxer\&gt;ORGANISMS\_DIR3\_v1.txt\&lt;/nomFitxer\&gt;

\&lt;uuidFitxer\&gt;61b8480d-10a4-4403-b6dd-ef68c23f4f4a\&lt;/uuidFitxer\&gt;

\&lt;dataAlta\&gt;16/11/2021 13:46:53\&lt;/dataAlta\&gt;

\&lt;dataDocument\&gt;16/11/2021 12:46:45\&lt;/dataDocument\&gt;

\&lt;identificadorExpedientDesal\&gt;985e4e19-01f3-4819-8f13-7be6b95185e3\&lt;/identificadorExpedientDesal\&gt;

\&lt;versionNTI\&gt;http://administracionelectronica.gob.es/ENI/XSD/v1.0/documento-e\&lt;/versionNTI\&gt;

\&lt;identificador\&gt;ES\_7515090124\_2021\_fc9041c2-e730-44b7-b812-05b131efed3e\&lt;/identificador\&gt;

\&lt;organ\&gt;A09018845\&lt;/organ\&gt;

\&lt;estatElaboracio\&gt;EE01\&lt;/estatElaboracio\&gt;

\&lt;origen\&gt;true\&lt;/origen\&gt;

\&lt;tipusDocumental\&gt;TD99\&lt;/tipusDocumental\&gt;

\&lt;tipusSignatura\&gt;TF01\&lt;/tipusSignatura\&gt;

\&lt;cSVSignatura\&gt;751509012416112021PRN084GP4JF\&lt;/cSVSignatura\&gt;

\&lt;regulacioGeneracioCSVSignatura\&gt;Resolució sobre l&#39;ús del sistema de codi segur de verificació del Consorci AOC\&lt;/regulacioGeneracioCSVSignatura\&gt;

\&lt;tipusDocumentalSICRESD\&gt;02\&lt;/tipusDocumentalSICRESD\&gt;

\&lt;nivellAcces\&gt;E\&lt;/nivellAcces\&gt;

\&lt;usuari\&gt;82828282S\&lt;/usuari\&gt;

\&lt;codiINE\&gt;7515090124\&lt;/codiINE\&gt;

\&lt;contingut\&gt;1\&lt;/contingut\&gt;

\&lt;/document\&gt;

\&lt;document\&gt;

\&lt;uuidDocument\&gt;0a2b2ddd-d68b-40d5-98d4-24b07805f972\&lt;/uuidDocument\&gt;

\&lt;uuidService\&gt;eVALISA\&lt;/uuidService\&gt;

\&lt;idioma\&gt;Català\&lt;/idioma\&gt;

\&lt;nomNatural\&gt;fitxer de log\&lt;/nomNatural\&gt;

\&lt;csv\&gt;751509012416112021UUQHC7V7E028\&lt;/csv\&gt;

\&lt;formatFitxer\&gt;text/plain\&lt;/formatFitxer\&gt;

\&lt;has\&gt;8cefb75231f0910873aff2854031d2fc8a6a4108818cdbbc9737a0b2f0f6ef4f\&lt;/has\&gt;

\&lt;hashAlgoritme\&gt;SHA-256\&lt;/hashAlgoritme\&gt;

\&lt;mida\&gt;10254\&lt;/mida\&gt;

\&lt;nomFitxer\&gt;fitxer de log.txt\&lt;/nomFitxer\&gt;

\&lt;uuidFitxer\&gt;7aeea8d1-63c1-443f-8c54-625ca9713eb7\&lt;/uuidFitxer\&gt;

\&lt;dataAlta\&gt;16/11/2021 13:46:53\&lt;/dataAlta\&gt;

\&lt;dataDocument\&gt;16/11/2021 12:46:45\&lt;/dataDocument\&gt;

\&lt;identificadorExpedientDesal\&gt;985e4e19-01f3-4819-8f13-7be6b95185e3\&lt;/identificadorExpedientDesal\&gt;

\&lt;versionNTI\&gt;http://administracionelectronica.gob.es/ENI/XSD/v1.0/documento-e\&lt;/versionNTI\&gt;

\&lt;identificador\&gt;ES\_7515090124\_2021\_0a2b2ddd-d68b-40d5-98d4-24b07805f972\&lt;/identificador\&gt;

\&lt;organ\&gt;A09018845\&lt;/organ\&gt;

\&lt;estatElaboracio\&gt;EE01\&lt;/estatElaboracio\&gt;

\&lt;origen\&gt;true\&lt;/origen\&gt;

\&lt;tipusDocumental\&gt;TD99\&lt;/tipusDocumental\&gt;

\&lt;tipusSignatura\&gt;TF01\&lt;/tipusSignatura\&gt;

\&lt;cSVSignatura\&gt;751509012416112021UUQHC7V7E028\&lt;/cSVSignatura\&gt;

\&lt;regulacioGeneracioCSVSignatura\&gt;Resolució sobre l&#39;ús del sistema de codi segur de verificació del Consorci AOC\&lt;/regulacioGeneracioCSVSignatura\&gt;

\&lt;tipusDocumentalSICRESD\&gt;02\&lt;/tipusDocumentalSICRESD\&gt;

\&lt;nivellAcces\&gt;E\&lt;/nivellAcces\&gt;

\&lt;usuari\&gt;82828282S \&lt;/usuari\&gt;

\&lt;codiINE\&gt;7515090124\&lt;/codiINE\&gt;

\&lt;contingut\&gt;1\&lt;/contingut\&gt;

\&lt;/document\&gt;

\&lt;/documents\&gt;

\&lt;/XmlExpedient\&gt;

### Codis de resposta

A continuació es detallen els possibles codis de resposta per a la descàrrega de l&#39;expedient en format ZIP:

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 10 | Error: no tens autorització per realitzar aquesta operació. Operació NO realitzada. |
| 11 | Error: la petició no és correcta. Operació NO realitzada. |
| 12 | Error: l&#39;expedient indicat no existeix en el servei i organisme indicats. Operació NO realitzada. |
| 100 | Error no controlat: XXXXXX. Si us plau, reintenti l&#39;operació en uns minuts. Operació NO realitzada. |

## 5.6 Consulta estat ticket <a name="5.6"></a>

Per obtenir la URL del fitxer ZIP dels mètodes asíncrons de l&#39;API de DESA&#39;L com la descàrrega d&#39;expedient en format ZIP, la descàrrega d&#39;expedient en format ENI o la descàrrega de document en format ENI, l&#39;integrador haurà de realitzar un polling sobre el mètode de consulta de l&#39;estat del ticket que retornen aquests mètodes asíncrons.

En el moment en que el fitxer ZIP estigui disponible, el mètode de consulta d&#39;estat del ticket retornarà la URL al fitxer ZIP. Si pel contrari el fitxer ZIP encara no està disponible.

### Petició

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| uuidExpedient | PathParam | Sí | Text | - | N/A |
| codiINE | QueryParam | Sí | Text | 10 | N/A |
| codiServei | QueryParam | Sí | Text | 10 | N/A |
| idTicket | QueryParam | Sí | Text | - | N/A |

### Petició

**URL** : [https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/expedient/{uuidExpedient}/statusdownload?codiServei=eVALISA&amp;codiINE=0123456789&amp;idTicket=36904808-2de9-4a56-a443-b09eb407548a](https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/expedient/%7BuuidExpedient%7D/statusdownload?codiServei=eVALISA&amp;codiINE=123456789&amp;idTicket=36904808-2de9-4a56-a443-b09eb407548a)

**Method** : GET

**Auth** :&quot;AWS Signature&quot;

**AccessKey** : XXXXXXXXXXX

**SecretKey** : YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY
**AWSRegion** : eu-west-1

**Body** : (buit)

**Body** : (buit)

 ![Shape35](RackMultipart20220211-4-2fc1qu_html_d1e93335dc0314cd.gif)

### Resposta pendent

{

&quot;idTicket&quot;: &quot;8b7d65d3-1d37-412e-a650-2341298389a1&quot;,

&quot;codiResposta&quot;: &quot;1&quot;,

&quot;descripcioResposta&quot;: &quot;Petició pendent&quot;

}

 ![Shape36](RackMultipart20220211-4-2fc1qu_html_6ad2da954b677fd5.gif)

### Resposta disponible

{

&quot;idTicket&quot;: &quot;36904808-2de9-4a56-a443-b09eb407548a&quot;,

&quot;urlPresignada&quot;: &quot;https://desal-download-expedient-bucket.s3.amazonaws.com/36904808-2de9-4a56-a443-b09eb407548a.zip?AWSAccessKeyId=ASIATUYQXN65OKN6BROJ&amp;Signature=sqC1n1POqvVsPvJLHRwV2cZL7BQ%3D&amp;x-amz-security-token=IQoJb3JpZ2luX2VjEH0aCWV1LXdlc3QtMSJGMEQCICXu%2BewPSHFZtJ0dUtjjOGGrhglTDt1YEPG%2FBeJql70kAiBMBSbvl%2BywlIj%2FOHLbOfdXdWF0T07mruKOoKpDEkf2xSqDBAim%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F8BEAAaDDI1MDc1MzgwNjI2NiIMH0r8Utb7unDLaW7sKtcDBrTDl%2Bd8c7SN%2FQ4RpW1cyo3KusIJD%2BSZvgJp4sT9sjlmuIBFSVXm%2F%2BRJM1uEZZowdGLmFiauZA3xDW36a15A9kdN1WllBzXptWM0Ui%2FOs04UYYf2oH4kXhoKkMMXDp9pqEwoApu069ilWmnbZdKRtPlFwYPVMpH49xSLHg9dlstqmJn6tpnUNt8Xa1So%2Fxz9FaSe9WqKeDE0jZjqFNITmJvwMp2K8YL79lku7Ob22cQyWODeZuZw6jK53f2ZPanDbmdrfwJnLLDbWQeHVfJxrtuqa3Zv%2FD1Gexa7yiTcWMAvu%2FzZ54TddDR1BbDOvvMU52ter3ncHsNVLajksTbfxO%2FQTaFG2tjZaTocig3Xh2%2BY3IEj0P%2BQp1u7kX07uGmDUkytWBF7Ghay%2BCBO7dGnTdaArOxqYDutTz9j8gFAfw3MKJYlFc5v%2BnK3J20EG2f8g9e6BSPeHn3nqkHjV3w7vXq2FBHUqLKdadL14wUQKUZienAOEg2WblU4auRhdAIgkPanalCrtOdDEc%2F3JGvkOrRQRXXWk4bWhOkiGzNn5Go0%2BocNbQaQHYw9glVo%2BK%2BRUOEyzyjcFAD6SGdJtZ9eZC760sY3IA0XStcJEIUT5GyKESDk4HN5MKSo%2BYgGOqYB6Ew6NKDP9lHhqXYuySYys8eFqqdvS7tczp9MxUM5M9GyYKaHn5SEfGFGUvY9S5BaxygkF6RVTnyIvzzxJiaBYlUmL9NTDtj8no9gRiHwoL1T%2BFoO4W9Duv4%2B5tQtrBruXka3%2FDOyThDQ8RaZQyOG6yiSd6Agyq2cwf6tgpXbzufHimbYe5TkxlisK9mPiB2zFgiO98urTOtdQny2XPu%2FA1D%2BQhtL0w%3D%3D&amp;Expires=1629471100&quot;,

&quot;codiResposta&quot;: &quot;0&quot;,

&quot;descripcioResposta&quot;: &quot;Petició disponible&quot;

}

 ![Shape37](RackMultipart20220211-4-2fc1qu_html_edee770fd7454f67.gif)

### Codis de resposta

A continuació es detallen els possibles codis de resposta per a la modificació de l&#39;expedient (per al codi d&#39;error 11, XXXXXX especifica la metadada informada malament i per al codi d&#39;error 100 XXXXXX ofereix més detalls de l&#39;error no controlat):

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Petició disponible |
| 1 | Petició pendent |
| 10 | Error: no tens autorització per realitzar aquesta operació. Operació NO realitzada. |
| 11 | Error: la petició no és correcta (XXXXXX). Operació NO realitzada. |
| 100 | Error no controlat: XXXXXX. Si us plau, reintenti l`operació en uns minuts. Operació NO realitzada. |

## 5.7 Descarrega d&#39;Expedient en format ENI <a name="5.7"></a>

Aquest mètode asíncron permet obtenir i descarregar l&#39;expedient en format ENI (Esquema Nacional de Interoperabilidad) per poder exportar-ho i compartir-ho amb tercers. Les especificacions del format ENI per a expedients estan disponibles al següent enllaç:

[https://administracionelectronica.gob.es/pae\_Home/pae\_Estrategias/pae\_Interoperabilidad\_Inicio/pae\_Normas\_tecnicas\_de\_interoperabilidad/pae\_URI\_Version\_NTI\_expediente-e.html](https://administracionelectronica.gob.es/pae_Home/pae_Estrategias/pae_Interoperabilidad_Inicio/pae_Normas_tecnicas_de_interoperabilidad/pae_URI_Version_NTI_expediente-e.html)

DESA&#39;L genera un XML d&#39;acord a aquestes especificacions. L&#39;XML inclou la informació detallada tant del propi expedient com de cadascun dels documents associats a aquest expedient. A més a més, s&#39;inclou també un índex on es resumeix el contingut del fitxer ENI. D&#39;aquesta forma si un expedient conté 10 documents associats, el fitxer XML amb format ENI contindrà les metadades de l&#39;expedient, les metadades dels documents associats i l&#39;índex (per exemple per un expedient amb 10 documents associats, tindríem 12 blocs de metadades: un per l&#39;índex, un altre per a l&#39;expedient i 10 per als documents).

De forma anàloga a la descàrrega de l&#39;expedient en format ZIP, el procés de creació del fitxer ENI és asíncron. Per poder saber si el fitxer ENI ja està disponible i per poder recuperar-ho un cop ja ho estigui, el servei integrador ha d&#39;executar la consulta d&#39;estat del ticket (_ **5.6Consulta estat ticket** _).

### Petició

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| uuidExpedient | PathParam | Sí | Text | - | N/A |
| codiINE | QueryParam | Sí | Text | 10 | N/A |
| codiServei | QueryParam | Sí | Text | 10 | N/A |

**URL** : [https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/expedientENI/{uuidExpedient}/download?codiServei=eVALISA&amp;codiINE=0123456789](https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/expedientENI/%7BuuidExpedient%7D/download?codiServei=eVALISA&amp;codiINE=123456789)

**Method** : GET

**Auth** :&quot;AWS Signature&quot;

**AccessKey** : XXXXXXXXXXX

**SecretKey** : YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY
**AWSRegion** : eu-west-1

**Body** : (buit)

**Body** : (buit)

 ![Shape38](RackMultipart20220211-4-2fc1qu_html_d1e93335dc0314cd.gif)

### Resposta

{

&quot;codiResposta&quot;: &quot;0&quot;,

&quot;descripcioResposta&quot;: &quot;Operació realitzada correctament&quot;,

&quot;idTicket&quot;: &quot;6c534ef1-74f3-4dbc-9a4c-1c51f5a56d2b&quot;

}

 ![Shape39](RackMultipart20220211-4-2fc1qu_html_64542e98126c8a92.gif)

### Codis de resposta

A continuació es detallen els possibles codis de resposta per a la descàrrega de l&#39;expedient en format ENI:

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 10 | Error: no tens autorització per realitzar aquesta operació. Operació NO realitzada. |
| 11 | Error: la petició no és correcta. Operació NO realitzada. |
| 12 | Error: l&#39;expedient indicat no existeix en el servei i organisme indicats. Operació NO realitzada. |
| 100 | Error no controlat: XXXXXX. Si us plau, reintenti l&#39;operació en uns minuts. Operació NO realitzada. |

# 6 Capa Document <a name="6"></a>

El document és l&#39;entitat essencial del DESA&#39;L. Està format per un conjunt de metadades i la relació amb un i només un fitxer de DESA&#39;L. DESA&#39;L també permet gestionar documents on el binari no es custodia al propi repositori del DESA&#39;L, sinó que està hostatjat en un repositori extern. En aquests casos al document de DESA&#39;L només es guarda la referència al repositori extern ja sigui a través d&#39;una URL externa o d&#39;un CSV del repositori extern.

El document és l&#39;entitat d&#39;alt nivell amb la que realment han de treballar en tot moment els integradors. DESA&#39;L permet que un mateix fitxer (binari PDF, Word, ...) estigui referenciat per més d&#39;un document i que cadascun d&#39;aquests documents pugui tenir uns permisos i unes polítiques de retenció pròpies. D&#39;altra banda, un document de DESA&#39;L pot pertànyer de forma opcional a un, i només un, expedient.

Per poder crear un document a DESA&#39;L prèviament cal carregar el seu contingut com a fitxer amb el mètode de càrrega de fitxer (_ **4.1Càrrega de fitxer** _), però un cop creat el document hem de realitzar totes les gestions a nivell de document i deixar totalment de banda la capa de fitxer que és de baix nivell.

DESA&#39;L contempla 2 models de metadades a nivell de document: bàsic i complet (el model complet hereta del model bàsic i per tant incorpora totes les seves metadades). El servei integrador haurà de consensuar amb els responsables del DESA&#39;L quin d&#39;aquests 2 models de metadades ha de fer servir per a la creació dels seus documents. Aquesta decisió es molt important per què un cop enregistrat el servei integrador a DESA&#39;L no es podrà modificar el model de metadades dels seus documents.

## 6.1 Alta de Document <a name="6.1"></a>

Aquest mètode de l&#39;API permet la creació d&#39;un nou document associat a un servei, incorporant les seves metadades.

Un document pot estar vinculat o no a un expedient. La relació entre el document i l&#39;expedient amb el que està vinculat s&#39;estableix amb la metadada _ **IdentificadorExpedientDesal** _ del document. Aquesta metadada és opcional perquè un document pot estar associat a un expedient DESA&#39;L, a un expedient extern (en aquest cas el vincle s&#39;estableix amb la metadada _ **IdentificadorExpedientExtern** _, cal destacar que DESA&#39;L no realitza cap tipus de validació del contingut d&#39;aquesta metadada) o directament no estar vinculat a cap tipus d&#39;expedient. En qualsevol moment es poden modificar aquestes metadades per establir un nou vincle entre el document i l&#39;expedient, o bé per eliminar el vincle entre ells.

La relació entre un document i el seu contingut (fitxer) es realitza a partir de la metadada _ **Contingut** _ que pot tenir 3 possibles valors i que requereix que el servei integrador informi una i només una de les següents metadades:

1. És el cas més comú: el contingut del document està hostatjat al propi DESA&#39;L amb un fitxer. El vincle entre el document i el fitxer s&#39;estableix definint la metadada _ **UUIDFitxer** _ del document. És important destacar que abans de poder crear el document, el servei integrador ha d&#39;haver carregat el fitxer a DESA&#39;L.

- El contingut del document està hostatjat en algun repositori extern i és accessible a través d&#39;una URL que s&#39;informa en la metadada _ **URLDocumentExtern** _. DESA&#39;L però, no realitza cap tipus de validació d&#39;aquesta URL i tampoc comprova que l&#39;URL estigui realment disponible.
- El contingut del document està hostatjat en algun repositori extern i és accessible a través d&#39;un identificador únic, o CSV, extern que el servei integrador controla. Aquest CSV s&#39;informa en la metadada _ **URLDocumentExtern.** _ DESA&#39;L però no realitza cap tipus de validació d&#39;aquest CSV i tampoc comprova que el CSV existeixi.

### Petició alta document basic

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| codiINE | Body | Si | Text | 10 |
 |
| codiServei | Body | Si | Taula | 10 |
 |
| nomFitxer | Body | Condicional | Text | 250 | Només s&#39;informa si contingut igual a 1 |
| nomNatural | Body | Si | Text | 500 | Nom natural (sense extensió) |
| dataDocument | Body | Si | Data i hora |
 | Format: DD/MM/AAAA HH:mm:SS |
| contingut | Body | Si | Text |
 |
 |
| interessat | Body | Si | Llista | 20 | Llista d&#39;interessats |
| usuari | Body | Si | Text | 250 | Dades identificatives qui crea el document |
| numeroRegistre | Body | Si | Text | 100 |   |
| CSV | Body | Si | Text | 100 |   |
| identificadorExpedientDesal | Body | Si | Text | 100 |   |
| identificadorExpedientExtern | Body | Si | Text | 100 |   |
| UUIDFitxer | Body | Condicional | Text | 20 | Només s&#39;informa si contingut igual a 1 |
| URLDocumentExtern | Body | Condicional | URI |   | Només s&#39;informa si contingut igual a 2 |
| identificadorDocumentExtern | Body | Condicional | Text | 100 | Només s&#39;informa si contingut igual a 3 |
| infoAddicional | Body | No | Llista |   | Llista d&#39;elements clau/valor |

**URL** : [https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/document](https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/document)

**Method** : POST

**Auth** :&quot;AWS Signature&quot;

**AccessKey** : XXXXXXXXXXX

**SecretKey** : YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY
**AWSRegion** : eu-west-1

**Body** :

{

&quot;codiINE&quot;: &quot;0123456789&quot;,

&quot;codiServei&quot;: &quot;eVALISA&quot;,

&quot;nomFitxer&quot;: &quot;exemple.pdf&quot;,

&quot;nomNatural&quot;: &quot;exemple&quot;,

&quot;dataDocument&quot; : &quot;20/07/2021 11:29:03&quot;,

&quot;contingut&quot;: &quot;1&quot;,

&quot;interessat&quot;: [

&quot;82828282S&quot;

],

&quot;usuari&quot;: &quot;Joan Ningú&quot;,

&quot;numeroRegistre&quot;: &quot;1234&quot;,

&quot;csv&quot;: null,

&quot;identificadorExpedientDesal&quot;: &quot;fb3a2d2f-b778-45be-bfad-1a8e4c4bd867&quot;,

&quot;uuidFitxer&quot;: &quot;98ae4860-766b-4546-aeee-e32f581073af&quot;,

&quot;infoAddicional&quot;: [

{

&quot;key&quot;: &quot;titolkey&quot;,

&quot;value&quot;: &quot;valor&quot;

}

]

}

 ![Shape40](RackMultipart20220211-4-2fc1qu_html_667d31ad63295b57.gif)

### Resposta alta document basic

{

&quot;uuidDocument&quot;: &quot;969a05d0-61e3-4f7a-aba7-109ee529aa5a&quot;,

&quot;uuidFitxer&quot;: &quot;98ae4860-766b-4546-aeee-e32f581073af&quot;,

&quot;codiINE&quot;: &quot;0123456789&quot;,

&quot;codiServei&quot;: &quot;eVALISA&quot;,

&quot;nomNatural&quot;: &quot;exemple&quot;,

&quot;sensibilitatDadesCaracterPersonal&quot;: null,

&quot;documentEssencial&quot;: null,

&quot;idioma&quot;: null,

&quot;codiClassificacio&quot;: null,

&quot;nomClassificacio&quot;: null,

&quot;codiSIA&quot;: null,

&quot;infoAddicional&quot;: [

{

&quot;key&quot;: &quot;titolkey&quot;,

&quot;value&quot;: &quot;valor&quot;

}

],

&quot;csv&quot;: &quot;00000000000911202133956E16A1D7&quot;,

&quot;formatFitxer&quot;: &quot;application/pdf&quot;,

&quot;hash&quot;: &quot;28f1d6e79edec9224a37bcfeb5c70b3e64ce05fad25ac311da305eb42d4594c8&quot;,

&quot;hashAlgoritme&quot;: &quot;SHA-256&quot;,

&quot;mida&quot;: &quot;615339&quot;,

&quot;nomFitxer&quot;: &quot;exemple.pdf&quot;,

&quot;uRLDocumentExtern&quot;: null,

&quot;dataAlta&quot;: &quot;09/11/2021 15:36:05&quot;,

&quot;dataDocument&quot;: &quot;20/07/2021 11:29:03&quot;,

&quot;contingut&quot;: &quot;1&quot;,

&quot;identificadorExpedientDesal&quot;: &quot;fb3a2d2f-b778-45be-bfad-1a8e4c4bd867&quot;,

&quot;identificadorExpedientExtern&quot;: null,

&quot;versioNTI&quot;: &quot;http://administracionelectronica.gob.es/ENI/XSD/v1.0/documento-e&quot;,

&quot;identificador&quot;: &quot;ES\_0000000000\_2021\_969a05d0-61e3-4f7a-aba7-109ee529aa5a&quot;,

&quot;organ&quot;: &quot;DIR3&quot;,

&quot;estatElaboracio&quot;: null,

&quot;origen&quot;: null,

&quot;tipusDocumental&quot;: null,

&quot;tipusSignatura&quot;: null,

&quot;cSVSignatura&quot;: null,

&quot;regulacioGeneracioCSVSignatura&quot;: null,

&quot;referenciaSignatura&quot;: null,

&quot;identificadorDocumentOrigen&quot;: null,

&quot;tipusDocumentalSICRESD&quot;: null,

&quot;descripcio&quot;: null,

&quot;nivellAcces&quot;: null,

&quot;clasificacioENS&quot;: null,

&quot;identificadorDocumentExtern&quot;: null,

&quot;codiResposta&quot;: &quot;0&quot;,

&quot;descripcioResposta&quot;: &quot;Operació realitzada correctament&quot;,

&quot;urlPresignada&quot;: null,

&quot;interessat&quot;: [

&quot;82828282S&quot;

],

&quot;usuari&quot;: &quot;Joan Ningú&quot;,

&quot;numeroRegistre&quot;: &quot;1234&quot;

}

 ![Shape41](RackMultipart20220211-4-2fc1qu_html_274f5ae720911b00.gif)

### Petició alta document complet

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| codiINE |  Body | Si | Text | 10 |   |
| codiServei | Body | Si | Taula | 10 |   |
| nomFitxer | Body | Condicional | Text | 250 | Només s&#39;informa si contingut igual a 1 |
| nomNatural | Body | Si | Text | 500 | Nom natural (sense extensió) |
| dataDocument | Body | Si | Data i hora |   | Format: DD/MM/AAAA HH:mm:SS |
| contingut | Body | Si | Text |   |   |
| interessat | Body | Si | Llista | 20 | Llista d&#39;interessats |
| usuari | Body | Si | Text | 250 | Dades identificatives qui crea el document |
| numeroRegistre | Body | Si | Text | 100 |   |
| CSV | Body | Si | Text | 100 |   |
| identificadorExpedientDesal | Body | Si | Text | 100 |   |
| identificadorExpedientExtern | Body | Si | Text | 100 |   |
| UUIDFitxer | Body | Condicional | Text | 20 | Només s&#39;informa si contingut igual a 1 |
| URLDocumentExtern | Body | Condicional | URI |   | Només s&#39;informa si contingut igual a 2 |
| identificadorDocumentExtern | Body | Condicional | Text | 100 | Només s&#39;informa si contingut igual a 3 |
| infoAddicional | Body | No | Llista |   | Llista d&#39;elements clau/valor |
| estatElaboracio | Body | Si | Text |   | EE01 - Original
 EE02 - Copia electrónica auténtica con cambio de formato
 EE03 - Copia electrónica auténtica de documento papel
 EE04 - Copia electrónica parcial auténtica
 EE99 - Otros. |
| origen | Body | Si | boolea |   | false= Ciutadà
 true=Administració |
| tipusDocumental | Body  | Si | Text |   | TD01 - Resolución
 TD02 - Acuerdo
 TD03 - Contrato
 TD04 - Convenio
 TD05 - Declaración
 TD06 - Comunicación
 TD07 - Notificación
 TD08 - Publicación
 TD09 - Acuse de recibo
 TD10 - Acta
 TD11 - Certificado
 TD12 - Diligencia
 TD13 - Informe
 TD14 - Solicitud
 TD15 - Denuncia
 TD16 - Alegación
 TD17 - Recursos
 TD18 - Comunicación ciudadano
 TD19 - Factura
 TD20 - Otros incautados
 TD51 - Ley
 TD52 - Moción
 TD53 - Instrucción
 TD54 - Convocatoria
 TD55 - Orden del día
 TD56 - Informe de Ponencia
 TD57 - Dictamen de Comisión
 TD58 - Iniciativa legislativa
 TD59 - Pregunta
 TD60 - Interpelación
 TD61 - Respuesta
 TD62 - Proposición no de ley
 TD63 - Enmienda
 TD64 - Propuesta de resolución
 TD65 - Comparecencia
 TD66 - Solicitud de información
 TD67 - Escrito
 TD68 - Iniciativa legislativa
 TD69 - Petición
 TD99 - Otros. |
| tipusSignatura | Body  | Si | Text |   | TF01 - CSV
 TF02 - XAdES internally detached signature
 TF03 - XAdES enveloped signature
 TF04 - CAdES detached/explicit signature
 TF05 - CAdES attached/implicit signature
 TF06 - PAdES
 TF07 - XAdES Manifest |
| CSVSignatura | Body  | Condicional | Text | 100 | S&#39;informa si TipoFirma =TF01 |
| regulacioGeneracioCSVSignatura | Body  | Condicional | Text | 500 | S&#39;informa si TipoFirma =TF01 |
| referenciaSignatura | Body  | Condicional | Text | 100 | Només cas TF03 i TF04. Referencia al fitxer que inclou la signatura (UUID - fitxer) |
| identificadorDocumentOrigen | Body  | Condicional | Text | 250 | Només si s&#39;ha indicat EE02,EE03 i EE04 a EstadoElaboracion |
| tipusDocumentalSICRESD | Body  | No | Text |   | &#39;01&#39; = Formulari (el document adjunt és un formulari amb camps omplerts per el ciutadà remitent)
 &#39;02&#39; = Document adjunt al formulari (a part del formulari, s&#39;adjunta un altre document acompanyant el formulari)
 &#39;03&#39;= Fitxer tècnic intern (el document adjunt és un fitxer intern. En general, aquests fitxers poden resultar útils per la Entitat Reistral destí, però no són fitxers per presentar directament als usuaris de gestió) |
| descripcio | Body  | No | Text | 500 |   |
| nivellAcces | Body  | No | Enum |   | A-Secret
 B-Reservat
 C-Confidencial
 E-No classificat |
| clasificacioENS | Body  | No | Enum |   | Baix
 Mig
 Alt |
| sensibilitatDadesCaracterPersonal | Body  | No | Enum |   | Basic
 Mig
 Alt |
| documentEssencial | Body  | No | boolea |   | True (si)
 False (NO) |
| idioma | Body  | No | Text | 50 |   |
| codiClassificacio | Body  | No | Text | 50 |   |
| nomClassificacio | Body  | No | Text | 250 |   |
| codiSIA | Body  | No | Text | 50 |   |

**URL** : [https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/document](https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/document)

**Method** : POST

**Auth** :&quot;AWS Signature&quot;

**AccessKey** : XXXXXXXXXXX

**SecretKey** : YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY
**AWSRegion** : eu-west-1

**Body** :

{

&quot;codiINE&quot;: &quot;0123456789&quot;,

&quot;codiServei&quot;: &quot;eVALISA&quot;,

&quot;nomFitxer&quot;: &quot;exemple.pdf&quot;,

&quot;nomNatural&quot;: &quot;exemple&quot;,

&quot;dataDocument&quot; : &quot;20/07/2021 11:29:03&quot;,

&quot;contingut&quot;: &quot;1&quot;,

&quot;interessat&quot;: [

&quot;82828282S&quot;

],

&quot;usuari&quot;: &quot;Joan Ningú&quot;,

&quot;numeroRegistre&quot;: &quot;1234&quot;,

&quot;csv&quot;: null,

&quot;identificadorExpedientDesal&quot;: &quot;fb3a2d2f-b778-45be-bfad-1a8e4c4bd867&quot;,

&quot;uuidFitxer&quot;: &quot;673e7405-104c-46ed-8359-21d5b16c70b5&quot;,

&quot;infoAddicional&quot;: [

{

&quot;key&quot;: &quot;82828282S&quot;,

&quot;value&quot;: &quot;11118282S&quot;

}

],

&quot;estatElaboracio&quot;: &quot;EE01&quot;,

&quot;origen&quot;: false,

&quot;tipusDocumental&quot;: &quot;TD100&quot;,

&quot;tipusSignatura&quot;: &quot;TF01&quot;,

&quot;cSVSignatura&quot;: &quot;csvSigEx&quot;,

&quot;regulacioGeneracioCSVSignatura&quot;: &quot;regGen5345&quot;,

&quot;referenciaSignatura&quot;: null,

&quot;identificadorDocumentOrigen&quot;: null,

&quot;tipusDocumentalSICRESD&quot;: &quot;01&quot;,

&quot;descripcio&quot;: &quot;DDescripcioTeste&quot;,

&quot;nivellAcces&quot;: &quot;A&quot;,

&quot;clasificacioENS&quot;: &quot;Baix&quot;,

&quot;sensibilitatDadesCaracterPersonal&quot;: &quot;Basic&quot;,

&quot;documentEssencial&quot;: true,

&quot;idioma&quot;: &quot;es-ES&quot;,

&quot;codiClassificacio&quot;: &quot;999TesteCodi222&quot;,

&quot;nomClassificacio&quot;: &quot;prioritari&quot;,

&quot;codiSIA&quot;: &quot;5512&quot;

}

 ![Shape42](RackMultipart20220211-4-2fc1qu_html_b7b07bf296438e2e.gif)

### Resposta document complert

{

&quot;uuidDocument&quot;: &quot;145a9ce5-69d9-442c-b50b-a1d566516414&quot;,

&quot;uuidFitxer&quot;: &quot;673e7405-104c-46ed-8359-21d5b16c70b5&quot;,

&quot;codiINE&quot;: &quot;0123456789&quot;,

&quot;codiServei&quot;: &quot;eVALISA&quot;,

&quot;nomNatural&quot;: &quot;exemple&quot;,

&quot;sensibilitatDadesCaracterPersonal&quot;: &quot;Basic&quot;,

&quot;documentEssencial&quot;: true,

&quot;idioma&quot;: &quot;es-ES&quot;,

&quot;codiClassificacio&quot;: &quot;999TesteCodi222&quot;,

&quot;nomClassificacio&quot;: &quot;prioritari&quot;,

&quot;codiSIA&quot;: &quot;5512&quot;,

&quot;infoAddicional&quot;: [

{

&quot;key&quot;: &quot;82828282S&quot;,

&quot;value&quot;: &quot;11118282S&quot;

}

],

&quot;csv&quot;: &quot;0000000000091120215424C765E780&quot;,

&quot;formatFitxer&quot;: &quot;application/pdf&quot;,

&quot;hash&quot;: &quot;e3b199ba3d1c77660481c78f79f509ac272f35304f9b5a9c662caa7f336d6897&quot;,

&quot;hashAlgoritme&quot;: &quot;SHA-256&quot;,

&quot;mida&quot;: &quot;651720&quot;,

&quot;nomFitxer&quot;: &quot;exemple.pdf&quot;,

&quot;uRLDocumentExtern&quot;: null,

&quot;dataAlta&quot;: &quot;09/11/2021 16:16:47&quot;,

&quot;dataDocument&quot;: &quot;20/07/2021 11:29:03&quot;,

&quot;contingut&quot;: &quot;1&quot;,

&quot;identificadorExpedientDesal&quot;: &quot;fb3a2d2f-b778-45be-bfad-1a8e4c4bd867&quot;,

&quot;identificadorExpedientExtern&quot;: null,

&quot;versioNTI&quot;: &quot;http://administracionelectronica.gob.es/ENI/XSD/v1.0/documento-e&quot;,

&quot;identificador&quot;: &quot;ES\_0000000000\_2021\_145a9ce5-69d9-442c-b50b-a1d566516414&quot;,

&quot;organ&quot;: &quot;DIR3&quot;,

&quot;estatElaboracio&quot;: &quot;EE01&quot;,

&quot;origen&quot;: false,

&quot;tipusDocumental&quot;: &quot;TD100&quot;,

&quot;tipusSignatura&quot;: &quot;TF01&quot;,

&quot;cSVSignatura&quot;: &quot;csvSigEx&quot;,

&quot;regulacioGeneracioCSVSignatura&quot;: &quot;regGen5345&quot;,

&quot;referenciaSignatura&quot;: null,

&quot;identificadorDocumentOrigen&quot;: null,

&quot;tipusDocumentalSICRESD&quot;: &quot;01&quot;,

&quot;descripcio&quot;: &quot;DDescripcioTeste&quot;,

&quot;nivellAcces&quot;: &quot;A&quot;,

&quot;clasificacioENS&quot;: &quot;Baix&quot;,

&quot;identificadorDocumentExtern&quot;: null,

&quot;codiResposta&quot;: &quot;0&quot;,

&quot;descripcioResposta&quot;: &quot;Operació realitzada correctament&quot;,

&quot;urlPresignada&quot;: null,

&quot;interessat&quot;: [

&quot;82828282S&quot;

],

&quot;usuari&quot;: &quot;Joan Ningú&quot;,

&quot;numeroRegistre&quot;: &quot;1234&quot;

}

 ![Shape43](RackMultipart20220211-4-2fc1qu_html_274f5ae720911b00.gif)

### Codis de Resposta

A continuació es detallen els possibles codis de resposta per l&#39;alta de document (per al codi d&#39;error 11, XXXXXX especifica la metadada en qüestió i per al codi d&#39;error 100 XXXXXX ofereix més detalls de l&#39;error no controlat):

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 10 | Error: no tens autorització per realitzar aquesta operació. Operació NO realitzada. |
| 11 | Error: la petició no és correcta. Hi ha metadades obligatòries sense informar o metadades informades no vàlides (XXXXXX). Operació NO realitzada. |
| 12 | Error: el número d&#39;expedient indicat no existeix en el servei i organisme indicats. Operació NO realitzada. |
| 13 | Error: el fitxer físic indicat no existeix. Operació NO realitzada. |
| 14 | Error: el fitxer físic conté virus i ha estat eliminat. Operació NO realitzada. |
| 100 | Error no controlat: XXXXXX. Si us plau, reintenti l&#39;operació en uns minuts. Operació NO realitzada. |
| 101 | Error: el document físic indicat està en procés de validació. Si us plau, reintenta l&#39;operació en uns minuts. Operació NO realitzada. |

## 6.2 Modificació de Document <a name="6.2"></a>

Aquest mètode permet realitzar la modificació de les metadades editables d&#39;un document. Donat que el vincle entre el document i l&#39;expedient al que està associat (_ **IdentificadorExpedientDesal** _), o el vincle entre el document i el fitxer que defineix el contingut (_ **UUIDFitxer** _) són metadades, aquest és el mètode que el servei integrador ha d&#39;executar per poder actualitzar el contingut binari del document o l&#39;expedient amb el que està associat el document.

DESA&#39;L comprovarà que totes les metadades que el servei integrador vol actualitzar realment siguin editables i en cas contrari rebutjarà la totalitat de l&#39;operació. El servei integrador només ha d&#39;informar en aquesta petició les metadades que necessita actualitzar, doncs DESA&#39;L no modificarà la resta de metadades.

Si el servei integrador vol eliminar una metadada (p. ex. per eliminar el vincle entre el document i l&#39;expedient) podrà fer-ho informant explícitament un _ **null** _ en la metadada en qüestió (o una cadena buida si la metadada és de tipus Text).

**Important:** Si el servei integrador actualitza la metadada _ **UUIDFitxer** _ d&#39;un document per actualitzar el contingut binari d&#39;aquest, DESA&#39;L comprovarà si hi ha algun altre document que referenciï a aquest fitxer. En cas contrari, eliminarà el fitxer de forma irreversible.

El següent diagrama mostra les 2 possibilitats amb les que es pot trobar DESA&#39;L en el moment de modificar la metadada _ **UUIDFitxer** _ i com actua en cada cas:

![](RackMultipart20220211-4-2fc1qu_html_ae92ccdd5d7814d2.png)

![](RackMultipart20220211-4-2fc1qu_html_d5b0e04a0526004f.png)

En la resposta del mètode de modificació de document, DESA&#39;L retorna totes les metadades del document tal i com han quedat després de l&#39;execució d&#39;aquest mètode.

### Petició document model complet

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| uuidDocument | PathParam | Sí | Text | - |
 |
| codiINE | QueryParam | Sí | Text | 10 |
 |
| nomFitxer | Body | No | Text | 250 |
 |
| nomNatural | Body | No | Text | 500 |
 |
| dataDocument | Body | No | Data i hora |
 | Format: DD/MM/AAAA HH:mm:SS |
| interessat | Body | No | Text |
 | Llista d&#39;interessats |
| numeroRegistre | Body | No | Text |
 |
 |
| identificadorExpedientDesal | Body | No | Text |
 |
 |
| identificadorExpedientExtern | Body | No | Text |
 |
 |
| UUIDFitxer | Body | No | Text |
 |
 |
| URLDocumentExtern | Body | No | Text |
 |
 |
| identificadorDocumentExtern | Body | No | Text |
 |
 |
| estatElaboracio | Body | No | Text |
 | EE01 - OriginalEE02 - Copia electrónica auténtica con cambio de formatoEE03 - Copia electrónica auténtica de documento papelEE04 - Copia electrónica parcial auténticaEE99 - Otros. |
| origen | Body | No | Boolean |
 | false= Ciudadàtrue=Administració |
| tipusDocumental | Body | No | Text |
 | TD01 - ResoluciónTD02 - AcuerdoTD03 - ContratoTD04 - ConvenioTD05 - DeclaraciónTD06 - ComunicaciónTD07 - NotificaciónTD08 - PublicaciónTD09 - Acuse de reciboTD10 - ActaTD11 - CertificadoTD12 - DiligenciaTD13 - InformeTD14 - SolicitudTD15 - DenunciaTD16 - AlegaciónTD17 - RecursosTD18 - Comunicación ciudadanoTD19 - FacturaTD20 - Otros incautadosTD51 - LeyTD52 - MociónTD53 - InstrucciónTD54 - ConvocatoriaTD55 - Orden del díaTD56 - Informe de PonenciaTD57 - Dictamen de ComisiónTD58 - Iniciativa legislativaTD59 - PreguntaTD60 - InterpelaciónTD61 - RespuestaTD62 - Proposición no de leyTD63 - EnmiendaTD64 - Propuesta de resoluciónTD65 - ComparecenciaTD66 - Solicitud de informaciónTD67 - EscritoTD68 - Iniciativa legislativaTD69 - PeticiónTD99 - Otros. |
| tipusSignatura | Body | No | Text |
 | TF01 - CSV TF02 - XAdES internally detached signatureTF03 - XAdES enveloped signatureTF04 - CAdES detached/explicit signature TF05 - CAdES attached/implicit signatureTF06 - PAdESTF07 - XAdES Manifest |
| CSVSignatura | Body | No | Text |
 | S&#39;informa si a TipoFirma =TF01 |
| regulacioGeneracioCSVSignatura | Body | No | Text |
 | S&#39;informa si a TipoFirma =TF01 |
| referenciaSignatura | Body | No | Text |
 | Només cas TF03 i TF04. Referencia al fitxer que inclou la signatura (uuidFitxer) |
| identificadorDocumentOrigen | Body | No | Text |
 | Identificador normalizat del document origen al que correspon la copia. Només si s&#39;ha indicat EE02,EE03 i EE04 a EstadoElaboracion |
| tipusDocumentalSICRESD | Body | No | Text |
 | &#39;01&#39; = Formulario (el documento adjunto es un formulario con campos rellenos por el ciudadano remitente) &#39;02&#39; = Documento adjunto al formulario (además del formulario, otro documento es adjuntado, acompañando al formulario) &#39;03&#39; = Fichero técnico interno (el documento adjunto es un fichero interno. Por lo general, estos ficheros pueden resultar útiles para la Entidad Registral de destino, pero no son ficheros para presentar directamente a los usuarios de gestión). |
| descripcio | Body | No | Text |
 |
 |
| nivellAcces | Body | No | Text |
 | A-SecretB-ReservatC-ConfidencialE-No classificat |
| clasificacioENS | Body | No | Text |
 | BaixMigAlt |
| sensibilitatDadesCaracterPersonal | Body | No |
 |
 | BasicMigAlt |
| documentEssencial | Body | No |
 |
 | True (si)False (NO) |
| codiClassificacio | Body | No |
 |
 |
 |
| nomClassificacio | Body | No |
 |
 |
 |
| codiSIA | Body | No |
 |
 |
 |
| infoAddicional | Body | No | Llista |
 | Llista d&#39;elements clau/valor |

**URL** :[https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/document](https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/document)/{uuidDocument}?codiINE=0123456789

**Method** : PUT

**Auth** :&quot;AWS Signature&quot;

**AccessKey** : XXXXXXXXXXX

**SecretKey** : YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY
**AWSRegion** : eu-west-1

**Body** :

{

&quot;clasificacioENS&quot;: &quot;Mig&quot;,

&quot;nivellAcces&quot;: &quot;A&quot;,

&quot;descripcio&quot;: &quot;descripció alternativa&quot;,

&quot;infoAddicional&quot;: [

{

&quot;key&quot;: &quot;valor&quot;,

&quot;value&quot;: &quot;11111&quot;

},

{

&quot;key&quot;: &quot;valor2&quot;,

&quot;value&quot;: &quot;2222&quot;

}

]

}

 ![Shape44](RackMultipart20220211-4-2fc1qu_html_b043d48bf41e5f20.gif)

### Resposta

{

&quot;uuidDocument&quot;: &quot;237131d6-9061-47f3-a745-5e93bb385588&quot;,

&quot;uuidFitxer&quot;: &quot;2f55600c-d725-4690-b6dd-0dfb44841bfc&quot;,

&quot;codiINE&quot;: &quot;0123456789&quot;,

&quot;codiServei&quot;: &quot;eVALISA&quot;,

&quot;nomNatural&quot;: &quot;DESA&#39;L-Functional requirements English&quot;,

&quot;sensibilitatDadesCaracterPersonal&quot;: &quot;Basic&quot;,

&quot;documentEssencial&quot;: true,

&quot;idioma&quot;: &quot;es-ES&quot;,

&quot;codiClassificacio&quot;: &quot;25&quot;,

&quot;nomClassificacio&quot;: &quot;prioritari&quot;,

&quot;codiSIA&quot;: &quot;5512&quot;,

&quot;infoAddicional&quot;: [

{

&quot;key&quot;: &quot;valor&quot;,

&quot;value&quot;: &quot;11111&quot;

},

{

&quot;key&quot;: &quot;valor2&quot;,

&quot;value&quot;: &quot;2222&quot;

}

],

&quot;csv&quot;: &quot;00000000000911202146064A1D3210&quot;,

&quot;formatFitxer&quot;: &quot;pdf&quot;,

&quot;hash&quot;: &quot;e3b199ba3d1c77660481c78f79f509ac272f35304f9b5a9c662caa7f336d6897&quot;,

&quot;hashAlgoritme&quot;: &quot;SHA-256&quot;,

&quot;mida&quot;: &quot;651720&quot;,

&quot;nomFitxer&quot;: &quot;DESA&#39;L-Functional requirements English.pdf&quot;,

&quot;uRLDocumentExtern&quot;: null,

&quot;dataAlta&quot;: &quot;09/11/2021 11:13:49&quot;,

&quot;dataDocument&quot;: &quot;20/04/2121 22:45:15&quot;,

&quot;contingut&quot;: &quot;1&quot;,

&quot;identificadorExpedientDesal&quot;: &quot;996aad10-f7d8-46dd-b746-66dd1824268b&quot;,

&quot;identificadorExpedientExtern&quot;: null,

&quot;versioNTI&quot;: &quot;http://administracionelectronica.gob.es/ENI/XSD/v1.0/documento-e&quot;,

&quot;identificador&quot;: &quot;ES\_0000000000\_2021\_237131d6-9061-47f3-a745-5e93bb385588&quot;,

&quot;organ&quot;: &quot;DIR3\_SGP\_&quot;,

&quot;estatElaboracio&quot;: &quot;EE01&quot;,

&quot;origen&quot;: true,

&quot;tipusDocumental&quot;: &quot;TD01&quot;,

&quot;tipusSignatura&quot;: &quot;TF01&quot;,

&quot;cSVSignatura&quot;: &quot;csvSigEx&quot;,

&quot;regulacioGeneracioCSVSignatura&quot;: &quot;regGen5345&quot;,

&quot;referenciaSignatura&quot;: null,

&quot;identificadorDocumentOrigen&quot;: null,

&quot;tipusDocumentalSICRESD&quot;: &quot;01&quot;,

&quot;descripcio&quot;: &quot;descripció alternativa&quot;,

&quot;nivellAcces&quot;: &quot;A&quot;,

&quot;clasificacioENS&quot;: &quot;Mig&quot;,

&quot;identificadorDocumentExtern&quot;: null,

&quot;codiResposta&quot;: &quot;0&quot;,

&quot;descripcioResposta&quot;: &quot;Operació realitzada correctament&quot;,

&quot;urlPresignada&quot;: null,

&quot;interessat&quot;: [

&quot;82828282S&quot;

],

&quot;usuari&quot;: null,

&quot;numeroRegistre&quot;: &quot;1234&quot;

}

 ![Shape45](RackMultipart20220211-4-2fc1qu_html_95d645666fcbd63f.gif)

### Codis de resposta

A continuació es detallen els possibles codis de resposta per la modificació del document (per al codi d&#39;error 11, XXXXXX especifica la metadada en qüestió i per al codi d&#39;error 100 XXXXXX ofereix més detalls de l&#39;error no controlat):

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 10 | Error: no tens autorització per realitzar aquesta operació. Operació NO realitzada. |
| 11 | Error: la petició no és correcta. Hi ha metadades obligatòries sense informar o metadades informades no vàlides (XXXXXX). Operació NO realitzada. |
| 12 | Error: el número d&#39;expedient indicat no existeix en el servei i organisme indicats. Operació NO realitzada. |
| 13 | Error: el fitxer físic indicat no existeix. Operació NO realitzada. |
| 14 | Error: el fitxer físic conté virus i ha estat eliminat. Operació NO realitzada. |
| 100 | Error no controlat: XXXXXX. Si us plau, reintenti l&#39;operació en uns minuts. Operació NO realitzada. |
| 101 | Error: el document físic indicat està en procés de validació. Si us plau, reintenta l&#39;operació en uns minuts. Operació NO realitzada. |

## 6.3 Eliminació de Document <a name="6.3"></a>

Aquest mètode permet eliminar un document, i en cascada, el propi fitxer associat si aquest només està referenciat pel document en qüestió.

**Important:** Si el servei integrador elimina un document i aquest està associat a un fitxer a través de la metadada UUIDFitxer, DESA&#39;L comprovarà si hi ha algun altre document que referenciï a aquest fitxer. En cas contrari, eliminarà el fitxer de forma irreversible.

El següent diagrama mostra les 2 possibilitats amb les que es pot trobar DESA&#39;L en el moment d&#39;eliminar el document si aquest està associat amb un fitxer a través de la metadada _ **UUIDFitxer** _:

![](RackMultipart20220211-4-2fc1qu_html_c211b9be3f7f47b.png)

![](RackMultipart20220211-4-2fc1qu_html_3795e2fb3f064218.png)

### Petició

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| uuidDocument | PathParam | Sí | Text | - |
 |
| codiINE | QueryParam | Sí | Text | 10 |
 |
| codiServei | QueryParam | Sí | Text | 10 |
 |

**URL** :[https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/document](https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/document)/{uuidDocument}?codiINE=0123456789&amp;codiServei=eVALISA

**Method** : DELETE

**Auth** :&quot;AWS Signature&quot;

**AccessKey** : XXXXXXXXXXX

**SecretKey** : YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY
**AWSRegion** : eu-west-1

**Body** : (buit)

 ![Shape46](RackMultipart20220211-4-2fc1qu_html_faac99e2c4046f83.gif)

### Resposta

{

&quot;uuidDocument&quot;: &quot;014c352f-9ddf-4dc4-a885-591d5b3948b2&quot;,

&quot;codiResposta&quot;: &quot;0&quot;,

&quot;descripcioResposta&quot;: &quot;Operació realitzada correctament&quot;

}

 ![Shape47](RackMultipart20220211-4-2fc1qu_html_3783de7c95a508d7.gif)

### Codis de resposta

A continuació es detallen els possibles codis de resposta per l&#39;eliminació de document (per al codi d&#39;error 11, XXXXXX especifica la metadada en qüestió i per al codi d&#39;error 100 XXXXXX ofereix més detalls de l&#39;error no controlat):

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 10 | Error: no tens autorització per realitzar aquesta operació. Operació NO realitzada. |
| 11 | Error: la petició no és correcta. Hi ha metadades obligatòries sense informar o metadades informades no vàlides (XXXXXX). Operació NO realitzada. |
| 12 | Error: el número d&#39;expedient indicat no existeix en el servei i organisme indicats. Operació NO realitzada. |
| 13 | Error: el fitxer físic indicat no existeix. Operació NO realitzada. |
| 14 | Error: el fitxer físic conté virus i ha estat eliminat. Operació NO realitzada. |
| 100 | Error no controlat: XXXXXX. Si us plau, reintenti l&#39;operació en uns minuts. Operació NO realitzada. |
| 101 | Error: el document físic indicat està en procés de validació. Si us plau, reintenta l&#39;operació en uns minuts. Operació NO realitzada. |

## 6.4 Descarrega Document <a name="6.4"></a>

Aquest mètode permet obtenir de forma síncrona les metadades d&#39;un document a partir del seu _ **UUIDDocument** _ (Modalitat 1) i de forma opcional l&#39;URL presignada per poder descarregar el contingut (Modalitat 2).

### Petició Modalitat 1: Descarrega Document

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| uuidDocument | PathParam | Sí | Text | - |
 |
| codiServei | QueryParam | Sí | Text | 10 |
 |
| codiINE | QueryParam | Sí | Text | 10 |
 |
| Modalitat | QueryParam | Sí | Número | 1 | Posar &quot;1&quot; per a modalitat 1 |

**URL** : [https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/document/{uuidDocument}/download?codiServei=eVALISA&amp;codiINE=0123456789&amp;modality=1](https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/document/%7BuuidDocument%7D/download?codiServei=eVALISA&amp;codiINE=123456789&amp;modality=1)

**Method** : GET

**Auth** :&quot;AWS Signature&quot;

**AccessKey** : XXXXXXXXXXX

**SecretKey** : YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY
**AWSRegion** : eu-west-1

**Body** : (buit)

**Body** : (buit)

 ![Shape48](RackMultipart20220211-4-2fc1qu_html_d1e93335dc0314cd.gif)

### Resposta

{

&quot;uuidDocument&quot;: &quot;c60b572d-7f6a-414e-8c0d-debc581b0809&quot;,

&quot;uuidFitxer&quot;: &quot;98ae4860-766b-4546-aeee-e32f581073af&quot;,

&quot;codiINE&quot;: &quot;0000000000&quot;,

&quot;codiServei&quot;: &quot;eSUPERTEAM&quot;,

&quot;nomNatural&quot;: &quot;exemple&quot;,

&quot;sensibilitatDadesCaracterPersonal&quot;: null,

&quot;documentEssencial&quot;: null,

&quot;idioma&quot;: null,

&quot;codiClassificacio&quot;: null,

&quot;nomClassificacio&quot;: null,

&quot;codiSIA&quot;: null,

&quot;infoAddicional&quot;: [

{

&quot;key&quot;: &quot;82828282S&quot;,

&quot;value&quot;: &quot;11118282S&quot;

}

],

&quot;csv&quot;: &quot;0000000000030820214CAB16719C9F&quot;,

&quot;formatFitxer&quot;: &quot;application/pdf&quot;,

&quot;hash&quot;: &quot;28f1d6e79edec9224a37bcfeb5c70b3e64ce05fad25ac311da305eb42d4594c8&quot;,

&quot;hashAlgoritme&quot;: &quot;SHA-256&quot;,

&quot;mida&quot;: &quot;615339&quot;,

&quot;nomFitxer&quot;: &quot;exemple.pdf&quot;,

&quot;uRLDocumentExtern&quot;: null,

&quot;dataAlta&quot;: &quot;03/08/2021 10:29:56&quot;,

&quot;dataDocument&quot;: &quot;20/07/2321 11:29:03&quot;,

&quot;contingut&quot;: &quot;1&quot;,

&quot;identificadorExpedientDesal&quot;: &quot;fb3a2d2f-b778-45be-bfad-1a8e4c4bd867&quot;,

&quot;identificadorExpedientExtern&quot;: null,

&quot;versioNTI&quot;: &quot;http://administracionelectronica.gob.es/ENI/XSD/v1.0/documento-e&quot;,

&quot;identificador&quot;: &quot;ES\_0000000000\_2021\_c60b572d-7f6a-414e-8c0d-debc581b0809&quot;,

&quot;organ&quot;: &quot;DIR3&quot;,

&quot;estatElaboracio&quot;: null,

&quot;origen&quot;: null,

&quot;tipusDocumental&quot;: null,

&quot;tipusSignatura&quot;: null,

&quot;cSVSignatura&quot;: null,

&quot;regulacioGeneracioCSVSignatura&quot;: null,

&quot;referenciaSignatura&quot;: null,

&quot;identificadorDocumentOrigen&quot;: null,

&quot;tipusDocumentalSICRESD&quot;: null,

&quot;descripcio&quot;: null,

&quot;nivellAcces&quot;: null,

&quot;clasificacioENS&quot;: null,

&quot;identificadorDocumentExtern&quot;: null,

&quot;codiResposta&quot;: &quot;0&quot;,

&quot;descripcioResposta&quot;: &quot;Operació realitzada correctament&quot;,

&quot;urlPresignada&quot;: null,

&quot;interessat&quot;: [

&quot;82828282S&quot;

],

&quot;usuari&quot;: &quot;Joan Ningú&quot;,

&quot;numeroRegistre&quot;: &quot;1234&quot;

}

 ![Shape49](RackMultipart20220211-4-2fc1qu_html_b08e206e52940045.gif)

### Petició Modalitat 2: Descarrega Document i contingut (fitxer)

La modalitat 2 només es pot executar si el document té un contingut igual 1 (fitxer).

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| uuidDocument | PathParam | Sí | Text | - |
 |
| codiServei | QueryParam | Sí | Text | 10 |
 |
| codiINE | QueryParam | Sí | Text | 10 |
 |
| Modalitat | QueryParam | Sí | Número | 1 | Posar &quot;2&quot; per a modalitat 2 |

**URL** : [https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/document/{uuidDocument}/download?codiServei=eVALISA&amp;codiINE=0123456789&amp;modality=2](https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/document/%7BuuidDocument%7D/download?codiServei=eVALISA&amp;codiINE=123456789&amp;modality=2)

**Method** : GET

**Auth** :&quot;AWS Signature&quot;

**AccessKey** : XXXXXXXXXXX

**SecretKey** : YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY
**AWSRegion** : eu-west-1

**Body** : (buit)

**Body** : (buit)

 ![Shape50](RackMultipart20220211-4-2fc1qu_html_d1e93335dc0314cd.gif)

### Resposta

{

&quot;uuidDocument&quot;: &quot;93f96e11-91f4-4d7b-9d8f-eb76ef7980fd&quot;,

&quot;uuidFitxer&quot;: &quot;673e7405-104c-46ed-8359-21d5b16c70b5&quot;,

&quot;codiINE&quot;: &quot;0123456789&quot;,

&quot;codiServei&quot;: &quot;enojordi&quot;,

&quot;nomNatural&quot;: &quot;exemple&quot;,

&quot;sensibilitatDadesCaracterPersonal&quot;: &quot;Basic&quot;,

&quot;documentEssencial&quot;: true,

&quot;idioma&quot;: &quot;es-ES&quot;,

&quot;codiClassificacio&quot;: &quot;25&quot;,

&quot;nomClassificacio&quot;: &quot;prioritari&quot;,

&quot;codiSIA&quot;: &quot;5512&quot;,

&quot;infoAddicional&quot;: [

{

&quot;key&quot;: &quot;82828282S&quot;,

&quot;value&quot;: &quot;11118282S&quot;

}

],

&quot;csv&quot;: &quot;00000000001607202159490E031CC5&quot;,

&quot;formatFitxer&quot;: &quot;application/pdf&quot;,

&quot;hash&quot;: &quot;e3b199ba3d1c77660481c78f79f509ac272f35304f9b5a9c662caa7f336d6897&quot;,

&quot;hashAlgoritme&quot;: &quot;SHA-256&quot;,

&quot;mida&quot;: &quot;651720&quot;,

&quot;nomFitxer&quot;: &quot;exemple.pdf&quot;,

&quot;uRLDocumentExtern&quot;: null,

&quot;dataAlta&quot;: &quot;2021-07-16 12:38:47&quot;,

&quot;dataDocument&quot;: &quot;2021-04-21 22:45:15&quot;,

&quot;contingut&quot;: &quot;1&quot;,

&quot;identificadorExpedientDesal&quot;: &quot;fb3a2d2f-b778-45be-bfad-1a8e4c4bd867&quot;,

&quot;identificadorExpedientExtern&quot;: null,

&quot;versioNTI&quot;: &quot;http://administracionelectronica.gob. es/ENI/XSD/v1.0/documento-e&quot;,

&quot;identificador&quot;: &quot;ES\_0000000000\_2021\_93f96e11-91f4-4d7b-9d8f-eb76ef7980fd&quot;,

&quot;organ&quot;: &quot;DIR3&quot;,

&quot;estatElaboracio&quot;: &quot;EE01&quot;,

&quot;origen&quot;: false,

&quot;tipusDocumental&quot;: &quot;TD01&quot;,

&quot;tipusSignatura&quot;: &quot;TF01&quot;,

&quot;cSVSignatura&quot;: &quot;csvSigEx&quot;,

&quot;regulacioGeneracioCSVSignatura&quot;: &quot;regGen5345&quot;,

&quot;referenciaSignatura&quot;: null,

&quot;identificadorDocumentOrigen&quot;: null,

&quot;tipusDocumentalSICRESD&quot;: null,

&quot;descripcio&quot;: &quot;descripció d&#39;exemple&quot;,

&quot;nivellAcces&quot;: &quot;A&quot;,

&quot;clasificacioENS&quot;: &quot;Baix&quot;,

&quot;identificadorDocumentExtern&quot;: null,

&quot;codiResposta&quot;: &quot;0&quot;,

&quot;descripcioResposta&quot;: &quot;Operació realitzada correctament&quot;,

&quot;urlPresignada&quot;: &quot;https://desal-download-bucket.s3.eu-west-1.amazonaws.com/exemple?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEEIaCWV1LXdlc3QtMSJGMEQCIFKd%2F5gswBy7L4R6MFKZUfVohaF6hxcOrMyZwONZlZL2AiAG5%2BS5MuWZDqDjYjJ4eqOMFBEjocbcRgj2EGqarrfEwirNAgjr%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F8BEAEaDDI1MDc1MzgwNjI2NiIM6dRNvJG80v7TKaIPKqECPdcezwLnU8N3Mkz5vLOOP9om3aNskuP%2BuJD%2B59CdLko5%2BOn5%2Bxkjm5ig%2Fd7%2BRsMvRXocpyLR924zzwsv9ytwiGdb4h0IF5h7MxHLfbZTaGQJnx%2FpKfGDR6L5uZA6M5zDi4MW9vwz%2BebNbwGlZxYGjdCApsMopDKngNcGbpUN6EdvejzRlo3q0iw80J0J1gFbQMnECkkEtK0qCCmXz9gu4PViy68TTjwPYKdll4Mso%2FfmpPOjHV0snF5ejIjgA0BxrBYMtljeS2Jx7jmTpUqPMlsnGgpTcjLE3D9kcHNd3GuHb%2FnldeViOXIY7BERI6usFx03hr6LK5%2Fr5OaNBHZ9fXKBnuBDpcSQSxkPGWUE7epBMTPFGvcFIhdxT0%2Bpx0vmwTDNpK6MBjqbAaGFdXfVv0gCiHkJ41lK6%2F%2Bu0ookd9hYU5u8BsPA8MulC9k77hG%2BNDulogiUptpYLgFF9z6ZjbrsE6hHTjW%2BzvMkdVywCiBMcqpRCB6cGoOuM2Gzt%2FCfJq93VH4wzwsnGi3zrODJw9fW4Yyq%2BsPekbPIDbzSL943kLTJoc2nN2l0MLT390gdDTspS0g0G7QMylpKue80LC%2B6NrTi&amp;X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Date=20211110T093518Z&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Expires=3599&amp;X-Amz-Credential=ASIATUYQXN65HMGGXLUH%2F20211110%2Feu-west-1%2Fs3%2Faws4\_request&amp;X-Amz-Signature=14df32903e90241f19dca7b0585da3c7e6bb5227dbed569782522dfa8ce75110&quot;,

&quot;interessat&quot;: [

&quot;82828282S&quot;

],

&quot;usuari&quot;: &quot;Joan Ningú&quot;,

&quot;numeroRegistre&quot;: &quot;1234&quot;

}

 ![Shape51](RackMultipart20220211-4-2fc1qu_html_bbebc68b99b4198b.gif)

### Codis de resposta

A continuació es detallen els possibles codis de resposta per a la descàrrega del document (per al codi d&#39;error 100 XXXXXX ofereix més detalls de l&#39;error no controlat):

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 10 | Error: no tens autorització per realitzar aquesta operació. Operació NO realitzada. |
| 11 | Error: la petició no és correcta. Operació NO realitzada. |
| 12 | Error: el document indicat no existeix en el servei i organisme indicats. Operació NO realitzada. |
| 100 | Error no controlat: XXXXXX. Si us plau, reintenti l&#39;operació en uns minuts. Operació NO realitzada. |

## 6.5 Descarrega Document en format ENI <a name="6.5"></a>

Aquest mètode permetrà obtenir i descarregar un document en format ENI per tal de poder compartir-ho amb un tercer.

Aquest mètode asíncron permet obtenir i descarregar el document en format ENI (Esquema Nacional de Interoperabilidad) per poder exportar-ho i compartir-ho amb tercers. Les especificacions del format ENI per a documents estan disponibles al següent enllaç:

[https://administracionelectronica.gob.es/pae\_Home/pae\_Estrategias/pae\_Interoperabilidad\_Inicio/pae\_Normas\_tecnicas\_de\_interoperabilidad/pae\_URI\_Version\_NTI\_expediente-e.html](https://administracionelectronica.gob.es/pae_Home/pae_Estrategias/pae_Interoperabilidad_Inicio/pae_Normas_tecnicas_de_interoperabilidad/pae_URI_Version_NTI_expediente-e.html)

DESA&#39;L genera un XML d&#39;acord a aquestes especificacions. De forma anàloga a la descàrrega de l&#39;expedient en format ENI, el procés de creació del fitxer ENI és asíncron. Per poder saber si el fitxer ENI ja està disponible i per poder recuperar-ho un cop ja ho estigui, el servei integrador ha d&#39;executar la consulta d&#39;estat del ticket (_ **5.6 Consulta estat ticket** _).

### Petició

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| uuidDocument | PathParam | Sí | Text | - |
 |
| codiINE | QueryParam | Sí | Text | 10 |
 |
| codiServei | QueryParam | Sí | Text | 10 |
 |

**URL** : [https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/documentENI/{uuidDocument}/download?codiServei=eVALISA&amp;codiINE=0123456789](https://v04y86nmj2.execute-api.eu-west-1.amazonaws.com/pro/documentENI/%7BuuidDocument%7D/download?codiServei=eVALISA&amp;codiINE=0123456789)

**Method** : GET

**Auth** :&quot;AWS Signature&quot;

**AccessKey** : XXXXXXXXXXX

**SecretKey** : YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY
**AWSRegion** : eu-west-1

**Body** : (buit)

**Body** : (buit)

 ![Shape52](RackMultipart20220211-4-2fc1qu_html_d1e93335dc0314cd.gif)

### Resposta

{

&quot;uuidDocument&quot;: &quot;014c352f-9ddf-4dc4-a885-591d5b3948b2&quot;,

&quot;codiResposta&quot;: &quot;0&quot;,

&quot;descripcioResposta&quot;: &quot;Operació realitzada correctament&quot;

}

 ![Shape53](RackMultipart20220211-4-2fc1qu_html_3783de7c95a508d7.gif)

### Codis de resposta

A continuació es detallen els possibles codis de resposta per a la descàrrega del document en format ENI:

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 10 | Error: no tens autorització per realitzar aquesta operació. Operació NO realitzada. |
| 11 | Error: la petició no és correcta. Operació NO realitzada. |
| 12 | Error: l&#39;expedient indicat no existeix en el servei i organisme indicats. Operació NO realitzada. |
| 100 | Error no controlat: XXXXXX. Si us plau, reintenti l&#39;operació en uns minuts. Operació NO realitzada. |

[1](#sdfootnote1anc)DESA&#39;L també permet gestionar documents on el binari no es custodia al propi repositori del DESA&#39;L, sinó que està hostatjat en un repositori extern. En aquests casos al document de DESA&#39;L només es guarda la referència al repositori extern ja sigui a través d&#39;una URL externa o d&#39;un CSV del repositori extern.
