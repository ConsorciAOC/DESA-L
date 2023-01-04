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
	- [5.8 Cerca d'Expedients](#cerca-expedients)
		- [Petició](#peticio-cerca-expedients)
		- [Exemple de petició](#exemple-peticio-cerca-expedients)
		- [Resposta](#resposta-cerca-expedients)
		- [Exemple de resposta](#exemple-resposta-cerca-expedients)
		- [Codis de resposta](#codis-resposta-cerca-expedients)
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
	- [6.6 Cerca de Documents](#cerca-documents)
		- [Petició](#peticio-cerca-doc)
		- [Exemple de petició](#exemple-peticio-cerca-documents)
		- [Resposta](#resposta-cerca-documents)
		- [Exemple de resposta](#exemple-resposta-cerca-documents)
		- [Codis de resposta](#codis-resposta-cerca-documents)
	- [6.7 Eliminació de Documents <a name="6.7"></a>](#eliminacio-documents)
		- [Petició](#peticio-eliminacio-documents)
		- [Resposta](#resposta-eliminacio-documents)
		- [Codis de resposta](#codis-resposta-eliminacio-documents)


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
| **Mida** | Obligatori | 500 | Text | 	Validar que no sigui superior a 4,2GB | TamanoLogico | Mida | Aplicació que s'integra | No | No | No | N/A | N/A | N/A | És necessari informar la mida del fitxer per generar correctament la URL pre-signada per a fer la càrrega del binari a S3 |
| **FormatFitxer** | Opcional | 200 | Text | Disposem de la llista de tots els tipus acceptats | NombreFormato | tipusMIME | Aplicació que s'integra | Si | No | No | N/A | N/A | No | -- |
| -- | --| --| --| -- | -- | -- | **METADADES QUE CREA DESA'L AUTOMÀTICAMENT** | -- | --| -- | -- | -- | -- | -- |
| **UUIDFitxer** | Obligatori | 20 | Text | -- | SecuenciaIdentificador | --  | DESA'L | Si | Si | No | N/A | N/A | No | Identificador únic del fitxer  |
| **FormatFitxer** | Obligatori | 200 | Text | --  | NombreFormato | tipusMIME | DESA'L | Si | No | No | N/A | N/A | No | Content Type del fitxer. DESA’L el calcula automàticament si no s'informa a la petició d’alta del fitxer |
| **Hash** | Obligatori | 100 | Text | -- | Valor | hash | DESA'L | Si | Si | No | N/A | N/A | No | Hash del fitxer. |
| **HashAlgoritme** | Obligatori | 100 | Text | --  | Algoritmo | -- |DESA'L | Si | No | No | N/A | N/A | No | Algoritme de hash utilitzat per calcular _hash_.  |
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

| **Nom element** |**Consignació**|**Longitud camp**|	**Tipus de camp**|	**Validació i procedència dades**	|**Equivalencia DESA'L**|	**Qui l'informa**	|**Automàtic**|	**Repetitiu**	|**Cercable**|	**Modificable en edició**	|**Observacions**|
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


| **Nom element** | **Consignació**	| **Longitud camp** | **Tipus de camp** | **Equivalencia ENI** | **Equivalencia MUX** | **Qui l'informa** | **Automàtic** | **Únic** | **Repetitiu** | **Indexable**	| **Cercable**	| **Modificable edició** | **Observacions** |
| -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
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
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | 
| **estatElaboracio** | Obligatori | -- | Text | EstadoElaboracion | estatElaboracio | Aplicació que s'integra | No | No | No | Si | No | Si | <ul><li>EE01 - Original</li><li>EE02 - Copia electrónica auténtica con cambio de formato</li><li>EE04 - Copia electrónica parcial auténtica</li><li>EE99 - Otros.</li></ul>|
| **origen** | Obligatori | -- | boolea | OrigenCiudadanoAdministracion | origen | Aplicació que s'integra | No | No | No | No | No | Si | <ul><li>false= Ciudadano</li><li>true=Administración</li><ul>|
| **tipusDocumental** | Obligatori | -- | Text | TipoDocumental | tipusDocumentalNTI | Aplicació que s'integra | No | No | No | Si | No | Si | <ul><li>TD01 - Resolución</li><li>TD02 - Acuerdo</li><li>TD03 - Contrato</li><li>TD04 - Convenio</li><li>TD05 - Declaración</li><li>TD06 - Comunicación</li><li>TD07 - Notificación</li><li>TD08 - Publicación</li><li>TD09 - Acuse de recibo</li><li>TD10 - Acta</li><li>TD11 - Certificado</li><li>TD12 - Diligencia</li><li>TD13 - Informe</li><li>TD14 - Solicitud</li><li>TD15 - Denuncia</li><li>TD16 - Alegación</li><li>TD17 - Recursos</li><li>TD18 - Comunicación ciudadano</li><li>TD19 - Factura</li><li>TD20 - Otros incautados</li><li>TD51 - Ley</li><li>TD52 - Moción</li><li>TD53 - Instrucción</li><li>TD54 - Convocatoria</li><li>TD55 - Orden del día</li><li>TD56 - Informe de Ponencia</li><li>TD57 - Dictamen de Comisión</li><li>TD58 - Iniciativa legislativa</li><li>TD59 - Pregunta</li><li>TD60 - Interpelación</li><li>TD61 - Respuesta</li><li>TD62 - Proposición no de ley</li><li>TD63 - Enmienda</li><li>TD64 - Propuesta de resolución</li><li>TD65 - Comparecencia</li><li>TD66 - Solicitud de información</li><li>TD67 - Escrito</li><li>TD68 - Iniciativa legislativa</li><li>TD69 - Petición</li><li>TD99 - Otros.</li></ul>|
| **tipusSignatura** |	Obligatori	 	| --|Text	|TipoFirma|	tipusSignatura|	Aplicació que s'integra	| No|	No|	No|	Si|	No|	Si| <ul><li>TF01 - CSV </li><li>TF02 - XAdES internally detached signature</li><li>TF03 - XAdES enveloped signature</li><li>TF04 - CAdES detached/explicit signature </li><li>TF05 - CAdES attached/implicit signature</li><li>TF06 - PAdES</li><li>TF07 - XAdES Manifest</li></ul>|
| **CSVSignatura**|	Obligatori i condicional|	100	|Text	|ValorCSV|	valorCSV	|Aplicació que s'integra|	No|	No|	No|	Si|	Si|	Si	|Només s’ha d’informar si _TipoFirma_ és _TF01_ |
| **regulacioGeneracioCSVSignatura** |	Obligatori i condicional|	500	|Text	|RegulacionGeneracionCSV	|regulacioGeneracioCSV|	Aplicació que s'integra|	No	|No|	No|	No	|No|	Si|	Només s’ha d'informar si _TipoFirma_ és _TF01|
| **referenciaSignatura**	|Obligatori i condicional|	100	|Text	|ReferenciaFirma	|identificadorDocumentSignat|	Aplicació que s'integra|	No|	No|	No|	No	|No|	Si|	Referència al fitxer que inclou la signatura (UUID fitxer). Només s’ha d’informar si TipoFirma és TF03 o TF04. |
|**identificadorDocumentOrigen**	|Opcional i condicional|	250|	Text|	IdentificadorDocumentoOrigen	|identificadorDocumentOrigen|	Aplicació que s'integra|	No|	No|	No|	Si|	No	|Si|	Identificador normalizat del document origen al que correspon la còpia. Només s’ha d’informar si EstadoElaboracion és EE02, EE03 o EE04.|
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


- _**Pendent**_ – Fitxer pendent d’analitzar pel sistema d’antivirus. Es pot crear un document que referenciï aquest fitxer, però el fitxer no es podrà descarregar per cap mètode de l’API (Descàrrega Fitxer, Descàrrega Document modalitat 2, Descàrrega Expedient modalitat 2, cerca Document, cerca Expedient, etc.) fins que hagi finalitzat l’anàlisi. De mitjana, l’anàlisi de virus d’un document PDF/Word inferior als 10MB és d’uns 3 segons.
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

![image](https://user-images.githubusercontent.com/32306731/155975311-6ba9a8e8-fae8-4fff-a6a7-e9d767f9679d.png)

### Resposta

I també un exemple de resposta:

![image](https://user-images.githubusercontent.com/32306731/155975395-32c057b3-4dee-4ae9-bb31-34184517cf17.png)

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

Aquest mètode permet demanar la descàrrega d’un fitxer allotjat al repositori documental del DESA’L, sempre i quan aquest fitxer no estigui encara referenciat per cap document de DESA’L. La descarrega d’un fitxer es farà també en 2 passos: una primera petició síncrona a a l’API de DESA’L que a partir de l’UUIDFitxer retornarà l’URL presignada de S3 i a continuació la descàrrega pròpiament del binari a partir de la URL presignada de S3. 

**Important:** la descàrrega de fitxer només es pot executar mentre el fitxer no estigui referenciat per un document de DESA&#39;L. Un cop el fitxer estigui vinculat a un document, la recuperació només es podrà fer a través dels mètodes de document (p. ex. _ **6.4Descarregar Document** _)

### Petició 

A continuació es detallen els camps que han d&#39;informar el servei integrador per poder realitzar la descàrrega del fitxer i un exemple de resposta:

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| uuidFitxer | QueryParam | Si | Text | - | N/A |
| codiINE | QueryParam | Si | Text | 10 | N/A |
| codiServei | QueryParam | Si | Text | 10 |

A continuació detallem un exemple de petició per a descàrrega de fitxer:

![image](https://user-images.githubusercontent.com/32306731/156004637-be4eafaf-7a27-4dcc-8c3b-a43b3097fee1.png)

### Resposta

A continuació detallem un exemple de resposta per a descàrrega de fitxer:

![image](https://user-images.githubusercontent.com/32306731/155975656-d45043f3-e53d-406a-9118-d3929ef42828.png)

### Codis de resposta

A continuació es detallen els possibles codis d’error per a la descàrrega del fitxer (XXXXXX ofereix més detalls de l’error no controlat):

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 1 | Error: el contingut del fitxer està esperant a ser analitzat pel antivirus. |
| 2 | Error: No s'ha fet el put del fitxer a S3 (URL-Presigned) |
| 4 | Error: Petició mal informada. |	
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
| identificador | Body | -- | -- | 50 | N/A |
| titol | Body | Sí | Text | 500 | N/A |
| dataInici | Body | Sí | Data | - | Format: DD/MM/AAAA HH:mm:SS |
| dataFi | Body | No | Data | - | Format: DD/MM/AAAA HH:mm:SS |
| Usuari | Body | No | Text | 100 | N/A |
| unitatResponsable | Body | No | Text | 250 | N/A |
| codiClassificacio | Body | Sí | Text | 50 | N/A |
| nomClassificacio | Body | Sí | Text | 250 | N/A |
| codiSIA | Body | No | Text | 50 | N/A |
| nivellAccess | Body | No | Text | -- | N/A |
| clasificacioENS | Body | No | Text | -- | N/A |
| sensibilitatDadesCaracterPersonal | Body | No | Text | -- | N/A |
| estatExpedient | Body | Sí | Text | -- | N/A |
| interessat | Body | No | Llista | - | Llista d&#39;interessats |
| descripció | Body | No | Text | 500 | N/A |
| infoAddicional | Body | No | Llista | - | Llista d&#39;elements clau/valor |

A continuació es detalla un exemple de petició:

![image](https://user-images.githubusercontent.com/32306731/155976066-b464e1e8-29c7-4de2-b14b-2ae8177528f4.png)

### Resposta Modalitat 1

![image](https://user-images.githubusercontent.com/32306731/155976147-5201489f-bb96-4cc4-8422-08995f85f88b.png)

### Petició Modalitat 2

En aquest cas, prèviament a l&#39;alta de l&#39;expedient, l&#39;integrador haurà d&#39;haver pujat al repositori documental del DESA&#39;L tots els fitxers que sigui necessari vincular als documents de l&#39;expedient, invocant tantes vegades com sigui necessari el mètode _ **4.1Càrrega de fitxer** _. D&#39;altra banda, el detall de les metadades que s&#39;han d&#39;informar per a cada document es detallen a l&#39;apartat _ **6.1Alta de Document** _ d&#39;aquest manual.

Abans de procedir a l&#39;alta de l&#39;expedient i del/s document/s, DESA&#39;L comprovarà que tots els fitxers referenciats existeixin i estiguin en _ **Estat** __ **Acceptat,** _ i de forma anàloga comprovarà que tots els documents a donar d&#39;alta compleixin les validacions que s&#39;han d&#39;aplicar en l&#39;alta de document. Només que hi hagi un únic fitxer o document que no sigui vàlid, DESA&#39;L rebutjarà tota l&#39;operació (recordem que l&#39;alta d&#39;expedient és una operació que DESA&#39;L ha d&#39;executar de forma atòmica) i indicarà explícitament en la resposta quin document no és vàlid i el motiu pel qual no ho és.

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| codiINE | Body | Sí | Text | 10 | N/A |
| codiServei | Body | Sí | Text | 10 | N/A |
| identificador | Body | -- | -- | 50 | N/A |
| titol | Body | Sí | Text | 500 | N/A |
| dataInici | Body | Sí | Data | -- | Format: DD/MM/AAAA HH:mm:SS |
| dataFi | Body | No | Data | -- | Format: DD/MM/AAAA HH:mm:SS |
| Usuari | Body | No | Text | 100 | N/A |
| unitatResponsable | Body | No | Text | 250 | N/A |
| codiClassificacio | Body | Sí | Text | 50 | N/A |
| nomClassificacio | Body | Sí | Text | 250 | N/A |
| codiSIA | Body | No | Text | 50 | N/A |
| nivellAccess | Body | No | Text | -- | N/A |
| clasificacioENS | Body | No | Text | -- | N/A |
| sensibilitatDadesCaracterPersonal | Body | No | Text | -- | N/A |
| estatExpedient | Body | Sí | Text | -- | N/A |
| interessat | Body | No | Llista | -- | Llista d&#39;interessats |
| descripció | Body | No | Text | 500 | N/A |
| infoAddicional | Body | No | Llista | - | Llista d&#39;elements clau/valor |
| documents | Body | -- | Llista | -- | Llista de documents. Model del document definit a l&#39;apartat _ **6.1** _ |

![image](https://user-images.githubusercontent.com/32306731/155976586-f28df982-bdf2-4163-8d38-a4c0b3117497.png)
![image](https://user-images.githubusercontent.com/32306731/155976658-097905e3-ea0d-4e3d-9643-c11bcb67ac34.png)


### Resposta

![image](https://user-images.githubusercontent.com/32306731/155976750-9f159dfe-c951-4a1e-b8c8-44602e481e97.png)
![image](https://user-images.githubusercontent.com/32306731/155976895-903239b2-6a22-46c6-86db-0bc546629946.png)

Destaquem com en la Modalitat 2 tenim un codi de resposta i una descripció resposta global de tota l’operació (remarcada en color groc) i un codi de resposta i una descripció resposta individual (remarcada en color verd) per a cada document que, en cas d’error degut al document, permet a l’integrador saber exactament quin document no és vàlid i el motiu (d’acord als codis d’error del mètode Alta Document).

### Codis de resposta

A continuació es detallen els possibles codis de resposta per l&#39;alta d&#39;expedient (per al codi d&#39;error 11, XXXXXX especifica la metadada en qüestió i per al codi d&#39;error 100 XXXXXX ofereix més detalls de l&#39;error no controlat):

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 4 | Error: Petició mal formada. |
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
| uuidExpedient | PathParam | Sí | Text | -- | -- |
| codiINE | QueryParam | Sí | Text | 10 | -- | -- |
| identificador | Body | No | -- | 50 | N/A |
| titol | Body | No | Text | 500 | N/A |
| dataInici | Body | No | Data | - | Format: DD/MM/AAAA HH:mm:SS |
| dataFi | Body | No | Data | - | Format: DD/MM/AAAA HH:mm:SS |
| unitatResponsable | Body | No | Text | 250 | N/A |
| codiClassificacio | Body | No | Text | 50 | N/A |
| nomClassificacio | Body | No | Text | 250 | N/A |
| codiSIA | Body | No | Text | 50 | N/A |
| nivellAccess | Body | No | Text | -- | N/A |
| clasificacioENS | Body | No | Text | -- | N/A |
| sensibilitatDadesCaracterPersonal | Body | No | Text | -- | N/A |
| estatExpedient | Body | No | Text | -- | N/A |
| interessat | Body | No | Llista | -- | Llista de literals |
| descripció | Body | No | Text | 500 | N/A |
| infoAddicional | Body | No | Llista | -- | Llista de literals |

![image](https://user-images.githubusercontent.com/32306731/155977453-40016d57-0190-4d02-bc05-8e5eba9e2630.png)

### Resposta

![image](https://user-images.githubusercontent.com/32306731/155977537-3eeb7b7a-eb8e-467a-a2ce-b59972c1f72f.png)

### Codis de resposta

A continuació es detallen els possibles codis de resposta per a la modificació de l&#39;expedient (per al codi d&#39;error 11, XXXXXX especifica la metadada en qüestió i per al codi d&#39;error 100 XXXXXX ofereix més detalls de l&#39;error no controlat):

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 4 | Error: Petició mal formada. |
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

![image](https://user-images.githubusercontent.com/32306731/155977638-3589ed67-1789-48d9-8103-60daceed0f25.png)

### Resposta

![image](https://user-images.githubusercontent.com/32306731/155977715-6531d18a-f173-4efe-bf2a-454b90bf4496.png)

### Codis de resposta

A continuació es detallen els possibles codis de resposta de la petició d&#39;eliminació d&#39;expedient. Per al codi d&#39;error 100, XXXXXX ofereix més detalls de l&#39;error no controlat:

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament |
| 4 | Error: Petició mal formada. |
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

![image](https://user-images.githubusercontent.com/32306731/155977813-cc6a7866-6796-478f-94cf-9e41b2088d1f.png)

### Resposta

![image](https://user-images.githubusercontent.com/32306731/155977994-9c518c3e-cd81-4c26-a1b1-8997f9e3088d.png)
![image](https://user-images.githubusercontent.com/32306731/155978050-6e111d39-279a-4063-ac86-2a8837819956.png)

### Codis de resposta

A continuació es detallen els possibles codis de resposta per a la descàrrega d&#39;expedient:

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 4 | Error: Petició mal formada. |
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
| uuidExpedient | PathParam | Sí | Text | -- | N/A |
| codiINE | QueryParam | Sí | Text | 10 | N/A |
| codiServei | QueryParam | Sí | Text | 10 | N/A |
| modality | QueryParam | Sí | Número | -- | Per a modalitat 1, indicar “1” |

![image](https://user-images.githubusercontent.com/32306731/155978255-c6a8dc1b-ee6b-4738-926e-b1c11b51c49e.png)

### Resposta

![image](https://user-images.githubusercontent.com/32306731/155978356-1a9650d4-500c-4cd2-b3e4-ff06e77bc8dd.png)

### Modalitat 2: Descarregar metadades i Fitxers

Aquesta modalitat permet descarregar també un fitxer ZIP que conté el fitxer XML amb les metadades de l&#39;expedient i dels documents associats, però el fitxer ZIP també conté el contingut dels fitxers vinculats amb els documents de l&#39;expedient.
	
**Important:** Si l’antivirus no ha pogut finalitzar l’anàlisi d’algun dels fitxers, la descàrrega de l’expedient fallarà amb un codi d’error 1 - El contingut del fitxer està esperant a ser analitzat pel antivirus.

### Petició

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| uuidExpedient | PathParam | Sí | Text | - | N/A |
| codiINE | QueryParam | Sí | Text | 10 | N/A |
| codiServei | QueryParam | Sí | Text | 10 | N/A |
| modality | QueryParam | Sí | Número | - | Per a modalitat 2, indicar &quot;2&quot; |

![image](https://user-images.githubusercontent.com/32306731/155978592-e43ae86b-c291-4ef5-815c-f03e238066dd.png)

### Resposta

![image](https://user-images.githubusercontent.com/32306731/155978681-8f84fd0d-f6ab-4ff6-90d3-91533d0d37bc.png)

### Exemple XML inclòs en el fitxer ZIP

![image](https://user-images.githubusercontent.com/32306731/155989879-e50e730e-c3af-4735-a6b8-08c3c8a80493.png)
![image](https://user-images.githubusercontent.com/32306731/155989985-ed59544f-43b7-4dec-9877-2248690265e7.png)
![image](https://user-images.githubusercontent.com/32306731/155990044-d60cac0d-c9ab-4e90-a09e-5aaf65256e71.png)



### Codis de resposta

A continuació es detallen els possibles codis de resposta per a la descàrrega de l&#39;expedient en format ZIP:

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 1 | Error: El contingut del fitxer està esperant a ser analitzat pel antivirus. |
| 4 | Error: Petició mal formada. |
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

![image](https://user-images.githubusercontent.com/32306731/155990290-b467e977-5d5e-47ed-95bf-1b7555ba1fe1.png)


### Resposta pendent

![image](https://user-images.githubusercontent.com/32306731/155990632-02954f93-1da8-4a1f-a63a-9ddac07370b2.png)


### Resposta disponible

![image](https://user-images.githubusercontent.com/32306731/156005221-18c9ac7a-2f47-4cf3-8a0f-7b2dcadc4980.png)

### Codis de resposta

A continuació es detallen els possibles codis de resposta per a la modificació de l&#39;expedient (per al codi d&#39;error 11, XXXXXX especifica la metadada informada malament i per al codi d&#39;error 100 XXXXXX ofereix més detalls de l&#39;error no controlat):

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Petició disponible |
| 1 | Error: El contingut del fitxer està esperant a ser analitzat pel antivirus. |
| 4 | Error: Petició mal formada. |
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

![image](https://user-images.githubusercontent.com/32306731/156005955-d5e41a09-b84d-4187-b5b6-c0b6284eaef0.png)

### Resposta

![image](https://user-images.githubusercontent.com/32306731/156006058-9068d58f-71bc-49dc-a42e-7170154ffada.png)

### Codis de resposta

A continuació es detallen els possibles codis de resposta per a la descàrrega de l&#39;expedient en format ENI:

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 1 | Error: L'expedient existeix però alguns dels seus fitxers estan sent analitzats per l'antivirus. |
| 4 | Error: Petició mal formada. |
| 10 | Error: no tens autorització per realitzar aquesta operació. Operació NO realitzada. |
| 11 | Error: la petició no és correcta. Operació NO realitzada. |
| 12 | Error: l&#39;expedient indicat no existeix en el servei i organisme indicats. Operació NO realitzada. |
| 100 | Error no controlat: XXXXXX. Si us plau, reintenti l&#39;operació en uns minuts. Operació NO realitzada. |

## 5.8 Cerca d'Expedients <a name="cerca-expedients" id="cerca-expedients"></a>

Aquest mètode de l'API permet cercar tots aquells expedients que cumpleixen una sèrie de criteris de filtratge, informats a la petició.

La cerca es realitzarà aplicant tots aquests criteris de filtratge de manera conjuntiva (logical AND). No es suporta la realització de cerques aplicant els criteris de manera disjuntiva (logical OR) o la construcció de consultes complexes combinant ambdues lògiques.

El paràmetre _**modality**_ indica si la cerca ha de retornar únicament les metadades dels expedients o si també ha de generar les URL pre-signades necessàries per a poder descarregar el contingut dels fitxers associats a aquests (per a aquells documents amb _**contingut**_ = 1).

Amb la finalitat de garantir el rendiment i protegir el servei davant de sobrecàrregues _**no es retornaran més de 100 resultats**_ per cerca.

La URL corresponent a aquesta operació de l'API és:

```javascript
https://{{host}}/expedient/search?codiServei={{codiServei}}&codiINE={{codiINE}}&modality={{modalitat}}
```

### Petició <a name="peticio-cerca-expedients" id="peticio-cerca-expedients"></a>

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Observacions** |
| --- | --- | --- | --- | --- |
| codiINE | Query String | Si | Text | Codi d'organisme del requeridor |
| codiServei | Query String | Si | Text | Codi de servei del requeridor |
| modality | Query String | Si | Numèric | <ul><li>1 = només metadades</li><li>2 = metadades i URL pre-signades</li></ul> |
| codiINE | Body | No | Text | -- |
| codiServei | Body | No | Text | -- |
| uuidExpedient | Body | No | Text | -- |
| sensibilitatDadesCaracterPersonal | Body | No | Text | -- |
| titol | Body | No | Text | -- |
| descripcio | Body | No | Text | -- |
| interessat | Body | No | Text | -- |
| dataAlta | Body | No | Bloc | _[Veure 5.8.1](#5.8.1)_ |
| dataAlta.inici | Body | No | Numèric | -- |
| dataAlta.fi | Body | No | Numèric | -- |
| dataInici | Body | No | Bloc | _[Veure 5.8.2](#5.8.2)_ |
| dataInici.inici | Body | No | Numèric | -- |
| dataInici.fi | Body | No | Numèric | -- |
| dataFi | Body | No | Bloc | _[Veure 5.8.3](#5.8.3)_ |
| dataFi.inici | Body | No | Numèric | -- |
| dataFi.fi | Body | No | Numèric | -- |
| usuari | Body | No | Text | -- |
| unitatResponsable | Body | No | Text | -- |
| codiClassificacio | Body | No | Text | -- |
| nomClassificacio | Body | No | Text | -- |
| nivellAcces | Body | No | Text | -- |
| classificacioENS | Body | No | Text | -- |
| codiSIA | Body | No | Text | -- |
| infoAddicional | Body | No | Llista | _[Veure 5.8.4](#5.8.4)_ |
| infoAddicional[].key | Body | No | Text | -- |
| infoAddicional[].value | Body | No | Text | -- |
| estatExpedient | Body | No | Text | -- |
| versioNTI | Body | No | Text | -- |
| identificador | Body | No | Text | -- |
| organ | Body | No | Text | -- |
| identificadorDesal | Body | No | Text | -- |
| documents[] | Body | No | Llista | Llista d'identificadors de documents  _[Veure 5.8.5](#5.8.5)_ |

> **_NOTA:_**  Per a la descripció dels camps dels expedients i el seu format consulteu l'apartat _[2.1](#2.1)_ d'aquest manual.

##### Rang de dates d'alta <a name="5.8.1" id="5.8.1"></a>
```json
"dataAlta": {
  "inici": 1652432260560,
  "fi": 1652432264560
},
```

##### Rang de dates d'inici <a name="5.8.2" id="5.8.2"></a>
```json
"dataInici": {
  "inici": 1652432260560,
  "fi": 1652432264560
},
```

##### Rang de dates de fi <a name="5.8.3" id="5.8.3"></a>
```json
"dataFi": {
  "inici": 1652432260560,
  "fi": 1652432264560
},
```

##### Info Addicional <a name="5.8.4" id="5.8.4"></a>
```json
"infoAddicional": [
  {
    "key": "clau_1",
    "value": "valor_1"
  }
]
```

##### Llista d'identificadors de documents <a name="5.8.5" id="5.8.5"></a>
```json
"documents": [
  "11111111-1111-1111-1111-111111111111",
  "22222222-2222-2222-2222-222222222222"
]
```

#### Exemple de petició <a name="exemple-peticio-cerca-expedients" id="exemple-peticio-cerca-expedients"></a> 
```json
{
  "codiServei": "eVALISA",
  "codiINE": "9821920002",
  "dataAlta": {
    "inici": 1658131385035,
    "fi": 1658131405035
  },
  "dataInici": {
    "inici": 1652432260560,
    "fi": 1652432264560
  },
  "dataFi": {
    "inici": 1652432250000,
    "fi": 1652432270000
  },
  "infoAddicional": [
    {
      "key": "clau_1",
    },
    {
      "value": "valor_1"
    },
    {
      "key": "clau_3",
      "value": "valor_3"
    }
  ],
  "documents": [
    "11111111-1111-1111-1111-111111111111",
    "22222222-2222-2222-2222-222222222222"
  ]
}
```
### Resposta <a name="resposta-cerca-expedients" id="resposta-cerca-expedients"></a>

| **Element** | **Tipus paràmetre** | **Tipus camps** | **Observacions** |
| --- | --- | --- | --- |
| totalResultats | Body | Text | -- |
| resultatsRecuperats | Body | Text | -- |
| codiResposta | Body | Text | -- |
| descripcioResposta | Body | Text | -- |
| expedients | Body | Llista | Llista d'expedients recuperats |

> **_NOTA:_**  Per a la descripció dels camps dels expedients i el seu format consulteu l'apartat _[2.1](#2.1)_ d'aquest manual.

#### Exemple de resposta <a name="exemple-resposta-cerca-expedients" id="exemple-resposta-cerca-expedients"></a>
```json
{
  "totalResultats": 1,
  "resultatsRecuperats": 1,
  "codiResposta": "0",
  "descripcioResposta": "Operació realitzada correctament",
  "expedients": [
    {
      "codiServei": "eVALISA",
      "codiINE": "9821920002",
      "uuidExpedient": "ef820562-9c7d-4ce6-b7a2-f6c716780739",
      "titol": "Aquest és el títol de l'expedient amb una mida de fins a 500 caràcters",
      "dataInici": 1628846943000,
      "dataFi": 1640991599000,
      "usuari": "11111111H - Usuari Peticionari Navegador",
      "unitatResponsable": "Unitat responsable de l'expedient amb una mida màxima de 250 caràcters",
      "codiClassificacio": "Codi de Classificació",
      "nomClassificacio": "Nom Classificació",
      "nivellAcces": "C",
      "sensibilitatDadesCaracterPersonal": "Basic",
      "estatExpedient": "E02",
      "interessat": [
        "82828282S",
        "X4687141V"
      ],
      "descripcio": "Aquesta és una descripció molt i molt llarga amb caràcters especials",
      "infoAddicional": [
        {
          "key": "variableçÑ€%",
          "value": "Paràmetre encoding conflictiu: çÑàa'()=?$€@ºª|!"
        },
        {
          "key": "variable1Etiqueta",
          "value": "Aquest és el literal"
        }
      ],
      "dataAlta": 1665062001619,
      "versioNTI": "http://administracionelectronica.gob.es/ENI/XSD/v1.0/documento-e",
      "identificador": "Aquest és l'identificador de l'expedient",
      "organ": "A09018933",
      "documents": [
        {
          "presentCSV": false,
          "uuidFitxer": "f48a8443-d739-491a-905e-c13e111c2920",
          "codiINE": "9821920002",
          "codiServei": "eVALISA",
          "nomNatural": "Primer document creat",
          "infoAddicional": [
            {
              "key": "Clau Document1",
              "value": "Encoding conflictiu: çÑàa'()=?$€@ºª|!"
            }
          ],
          "CSV": "9821920002061020222FD3E814B42D",
          "formatFitxer": "plain/text",
          "hash": "2CxqoTOg/CWwh/Rq1+0qMEJ3LmEuAVVx5hdT/1W6bag=",
          "hashAlgoritme": "SHA-256",
          "mida": 100,
          "nomFitxer": "Primer document.pdf",
          "dataAlta": 1665062001619,
          "dataDocument": 1627131422000,
          "contingut": "Fitxer",
          "identificadorExpedientDesal": "ef820562-9c7d-4ce6-b7a2-f6c716780739",
          "versioNTI": "http://administracionelectronica.gob.es/ENI/XSD/v1.0/documento-e",
          "identificador": "ES_9821920002_2022_FBD38E4E-E2D4-4D27-B211-80229BF170FE",
          "organ": "A09018933",
          "estatElaboracio": "EE99",
          "origen": true,
          "tipusDocumental": "TD10",
          "tipusSignatura": "TF06",
          "interessat": [
            "82828282S"
          ],
          "codiResposta": "0",
          "uuidDocument": "fbd38e4e-e2d4-4d27-b211-80229bf170fe"
        },
        {
          "presentCSV": false,
          "codiINE": "9821920002",
          "codiServei": "eVALISA",
          "nomNatural": "Segon document creat dins l'expedient amb el JSON de càrrega d'expedient",
          "sensibilitatDadesCaracterPersonal": "Alt",
          "documentEssencial": false,
          "idioma": "fr_FR",
          "codiClassificacio": "Codi de Classificació inventat per SGP amb 50 chrs",
          "nomClassificacio": "Nom Classificació inventat per SGP amb una longitud de 250",
          "codiSIA": "SIA  inventat per SGP amb longitud de 50 caràcters",
          "CSV": "9821920002061020226961679AE9B5",
          "URLDocumentExtern": "https://www.URLExternaInventadaperSGP.com/234234a",
          "dataAlta": 1665062001647,
          "dataDocument": 1626269354000,
          "contingut": "URL",
          "identificadorExpedientDesal": "ef820562-9c7d-4ce6-b7a2-f6c716780739",
          "versioNTI": "http://administracionelectronica.gob.es/ENI/XSD/v1.0/documento-e",
          "identificador": "ES_9821920002_2022_EFEA840C-5287-407A-9924-BDAD2116BA7A",
          "organ": "A09018933",
          "estatElaboracio": "EE02",
          "origen": false,
          "tipusDocumental": "TD01",
          "tipusSignatura": "TF01",
          "CSVSignatura": "CSVSIG_1d8164ea-6a13-423c-9fde-5fa3e4288229",
          "regulacioGeneracioCSVSignatura": "Sembla que la validació d'aquest camp es fa correctament. Aquest camp ha d'informar-se de forma obligatòria si el camp 'tipusSignatura' té el valor TF01.",
          "identificadorDocumentOrigen": "06ca9170-9729-449c-bbc5-fe4c86e78cd8",
          "tipusDocumentalSICRES": "03",
          "descripcio": "Aquesta és una descripció molt i molt llarga amb caràcters especials ñÑçÇàÀüÜ{}[]()/&%$€·l'#ºª|!",
          "nivellAcces": "B",
          "classificacioENS": "Baix",
          "usuari": "Nom Cognom1 Cognom2 del funcionari",
          "numeroRegistre": "E/541412123/2021",
          "codiResposta": "0",
          "uuidDocument": "efea840c-5287-407a-9924-bdad2116ba7a"
        }
      ],
      "classificacioENS": "Mig"
    }
  ]
}
```

### Codis de Resposta <a name="codis-resposta-cerca-expedients" id="codis-resposta-cerca-expedients"></a>

A continuació es detallen els possibles codis de resposta per a l'operació de cerca d'expedients:

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 4 | Error: Petició mal formada. |
| 10 | Error: no tens autorització per realitzar aquesta operació. Operació NO realitzada. |
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
| codiINE | Body | Si | Text | 10 | -- |
| codiServei | Body | Si | Taula | 10 | -- |
| nomFitxer | Body | Condicional | Text | 250 | Només s&#39;informa si contingut igual a 1 |
| nomNatural | Body | Si | Text | 500 | Nom natural (sense extensió) |
| dataDocument | Body | Si | Data i hora | -- | Format: DD/MM/AAAA HH:mm:SS |
| contingut | Body | Si | Text | -- | -- |
| interessat | Body | Si | Llista | 20 | Llista d&#39;interessats |
| usuari | Body | Si | Text | 250 | Dades identificatives qui crea el document |
| numeroRegistre | Body | Si | Text | 100 | -- |
| CSV | Body | Si | Text | 100 | -- |
| identificadorExpedientDesal | Body | Si | Text | 100 | -- |
| identificadorExpedientExtern | Body | Si | Text | 100 | -- |
| UUIDFitxer | Body | Condicional | Text | 20 | Només s&#39;informa si contingut igual a 1 |
| URLDocumentExtern | Body | Condicional | URI |   | Només s&#39;informa si contingut igual a 2 |
| identificadorDocumentExtern | Body | Condicional | Text | 100 | Només s&#39;informa si contingut igual a 3 |
| infoAddicional | Body | No | Llista | -- | Llista d&#39;elements clau/valor |

![image](https://user-images.githubusercontent.com/32306731/156006549-311b9c95-86d1-42e2-90a8-09be88d20bef.png)
	
### Resposta alta document basic

![image](https://user-images.githubusercontent.com/32306731/156006669-af4b4cb2-d0ce-43a7-9a1e-a0007bd70f99.png)

### Petició alta document complet

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| codiINE |  Body | Si | Text | 10 | -- |
| codiServei | Body | Si | Taula | 10 | -- |
| nomFitxer | Body | Condicional | Text | 250 | Només s&#39;informa si contingut igual a 1 |
| nomNatural | Body | Si | Text | 500 | Nom natural (sense extensió) |
| dataDocument | Body | Si | Data i hora | -- | Format: DD/MM/AAAA HH:mm:SS |
| contingut | Body | Si | Text | -- | -- |
| interessat | Body | Si | Llista | 20 | Llista d&#39;interessats |
| usuari | Body | Si | Text | 250 | Dades identificatives qui crea el document |
| numeroRegistre | Body | Si | Text | 100 | -- |
| CSV | Body | Si | Text | 100 | -- |
| identificadorExpedientDesal | Body | Si | Text | 100 | -- |
| identificadorExpedientExtern | Body | Si | Text | 100 | -- |
| UUIDFitxer | Body | Condicional | Text | 20 | Només s&#39;informa si contingut igual a 1 |
| URLDocumentExtern | Body | Condicional | URI |   | Només s&#39;informa si contingut igual a 2 |
| identificadorDocumentExtern | Body | Condicional | Text | 100 | Només s&#39;informa si contingut igual a 3 |
| infoAddicional | Body | No | Llista | -- | Llista d&#39;elements clau/valor |
| estatElaboracio | Body | Si | Text | -- | <ul><li>EE01 - Original</li><li>EE02 - Copia electrónica auténtica con cambio de formato</li><li>EE03 - Copia electrónica auténtica de documento papel</li><li>EE04 - Copia electrónica parcial auténtica</li><li>EE99 - Otros.</li></ul> |
| origen | Body | Si | boolea | -- | false= Ciutadà, true=Administració |
| tipusDocumental | Body  | Si | Text | -- | <ul><li>TD01 - Resolución</li><li>TD02 - Acuerdo</li><li>TD03 - Contrato</li><li>TD04 - Convenio</li><li>TD05 - Declaración</li><li>TD06 - Comunicación</li><li>TD07 - Notificación</li><li>TD08 - Publicación</li><li>TD09 - Acuse de recibo</li><li>TD10 - Acta</li><li>TD11 - Certificado</li><li>TD12 - Diligencia</li><li>TD13 - Informe</li><li>TD14 - Solicitud</li><li>TD15 - Denuncia</li><li>TD16 - Alegación</li><li>TD17 - Recursos</li><li>TD18 - Comunicación ciudadano</li><li>TD19 - Factura</li><li>TD20 - Otros incautados</li><li>TD51 - Ley</li><li>TD52 - Moción</li><li>TD53 - Instrucción</li><li>TD54 - Convocatoria</li><li>TD55 - Orden del día</li><li>TD56 - Informe de Ponencia</li><li>TD57 - Dictamen de Comisión</li><li>TD58 - Iniciativa legislativa</li><li>TD59 - Pregunta</li><li>TD60 - Interpelación</li><li>TD61 - Respuesta</li><li>TD62 - Proposición no de ley</li><li>TD63 - Enmienda</li><li>TD64 - Propuesta de resolución</li><li>TD65 - Comparecencia</li><li>TD66 - Solicitud de información</li><li>TD67 - Escrito</li><li>TD68 - Iniciativa legislativa</li><li>TD69 - Petición</li><li>TD99 - Otros. </li></ul>|
| tipusSignatura | Body  | Si | Text | --  | <ul><li>TF01 - CSV</li><li>TF02 - XAdES internally detached signature</li><li>TF03 - XAdES enveloped signature</li><li>TF04 - CAdES detached/explicit signature</li><li>TF05 - CAdES attached/implicit signature</li><li>TF06 - PAdES</li><li>TF07 - XAdES Manifest</li></ul> |
| CSVSignatura | Body  | Condicional | Text | 100 | S&#39;informa si TipoFirma =TF01 |
| regulacioGeneracioCSVSignatura | Body  | Condicional | Text | 500 | S&#39;informa si TipoFirma =TF01 |
| referenciaSignatura | Body  | Condicional | Text | 100 | Només cas TF03 i TF04. Referencia al fitxer que inclou la signatura (UUID - fitxer) |
| identificadorDocumentOrigen | Body  | Condicional | Text | 250 | Només si s&#39;ha indicat EE02,EE03 i EE04 a EstadoElaboracion |
| descripcio | Body  | No | Text | 500 | --  |
| nivellAcces | Body  | No | Enum | --  | <ul><li>A-Secret</li><li>B-Reservat</li><li>C-Confidencial</li><li>E-No classificat</li></ul> |
| clasificacioENS | Body  | No | Enum | -- | Baix, Mig, Alt |
| sensibilitatDadesCaracterPersonal | Body  | No | Enum | -- | Basic, Mig, Alt |
| documentEssencial | Body  | No | boolea | -- | True (si), False (NO) |
| idioma | Body  | No | Text | 50 | -- |
| codiClassificacio | Body  | No | Text | 50 | -- |
| nomClassificacio | Body  | No | Text | 250 | -- |
| codiSIA | Body  | No | Text | 50 | -- |

![image](https://user-images.githubusercontent.com/32306731/156010161-c3d01cf2-3047-4787-bdb6-60b4c864d62e.png)

### Resposta document complert

![image](https://user-images.githubusercontent.com/32306731/156010340-957feb12-9bb4-4bd0-a13f-d23301098d72.png)

### Codis de Resposta

A continuació es detallen els possibles codis de resposta per l&#39;alta de document (per al codi d&#39;error 11, XXXXXX especifica la metadada en qüestió i per al codi d&#39;error 100 XXXXXX ofereix més detalls de l&#39;error no controlat):

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 1 | El document és correcte però el fitxer encara està sent analitzat per l'antivirus. |
| 2 | Error: El contingut del fitxer encara no ha estat carregat a S3. |
| 4 | Error: Petició mal formada. |
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

![image](https://user-images.githubusercontent.com/32306731/156010604-cb2811d3-fbc6-4445-a658-5fb23ddbcaec.png)

![image](https://user-images.githubusercontent.com/32306731/156010703-bb056f29-d1c6-4d5f-90a8-d4aae8c380bd.png)

En la resposta del mètode de modificació de document, DESA&#39;L retorna totes les metadades del document tal i com han quedat després de l&#39;execució d&#39;aquest mètode.

### Petició document model complet

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| uuidDocument | PathParam | Sí | Text | -- | -- |
| codiINE | QueryParam | Sí | Text | 10 | -- |
| nomFitxer | Body | No | Text | 250 | -- |
| nomNatural | Body | No | Text | 500 | -- |
| dataDocument | Body | No | Data i hora | -- | Format: DD/MM/AAAA HH:mm:SS |
| interessat | Body | No | Text | -- | Llista d&#39;interessats |
| numeroRegistre | Body | No | Text | -- | -- |
| identificadorExpedientDesal | Body | No | Text | -- | -- |
| identificadorExpedientExtern | Body | No | Text | -- | -- |
| UUIDFitxer | Body | No | Text | -- | -- |
| URLDocumentExtern | Body | No | Text | -- | -- |
| identificadorDocumentExtern | Body | No | Text | -- | -- |
| estatElaboracio | Body | No | Text | -- | <ul><li>EE01 - Original</li><li>EE02 - Copia electrónica auténtica con cambio de formato</li><li>EE03 - Copia electrónica auténtica de documento papel</li><li>EE04 - Copia electrónica parcial auténticaEE99 - Otros.</li></ul> |
| origen | Body | No | Boolean | -- | false= Ciudadàtrue=Administració |
| tipusDocumental | Body | No | Text | -- | <ul><li>TD01 - Resolución</li><li>TD02 - Acuerdo</li><li>TD03 - Contrato</li><li>TD04 - Convenio</li><li>TD05 - Declaración</li><li>TD06 - Comunicación</li><li>TD07 - Notificación</li><li>TD08 - Publicación</li><li>TD09 - Acuse de recibo</li><li>TD10 - Acta</li><li>TD11 - Certificado</li><li>TD12 - Diligencia</li><li>TD13 - Informe</li><li>TD14 - Solicitud</li><li>TD15 - Denuncia</li><li>TD16 - Alegación</li><li>TD17 - Recursos</li><li>TD18 - Comunicación ciudadano</li><li>TD19 - Factura</li><li>TD20 - Otros incautados</li><li>TD51 - Ley</li><li>TD52 - Moción</li><li>TD53 - Instrucción</li><li>TD54 - Convocatoria</li><li>TD55 - Orden del día</li><li>TD56 - Informe de Ponencia</li><li>TD57 - Dictamen de Comisión</li><li>TD58 - Iniciativa legislativa</li><li>TD59 - Pregunta</li><li>TD60 - Interpelación</li><li>TD61 - Respuesta</li><li>TD62 - Proposición no de ley</li><li>TD63 - Enmienda</li><li>TD64 - Propuesta de resolución</li><li>TD65 - Comparecencia</li><li>TD66 - Solicitud de informaciónT</li><li>D67 - Escrito</li><li>TD68 - Iniciativa legislativa</li><li>TD69 - Petición</li><li>TD99 - Otros.</li><ul> |
| tipusSignatura | Body | No | Text | -- | <ul><li>TF01 - CSV</li><li>TF02 - XAdES internally detached signature</li><li>TF03 - XAdES enveloped signature</li><li>TF04 - CAdES detached/explicit signature</li><li>TF05 - CAdES attached/implicit signature</li><li>TF06 - PAdES</li><li>TF07 - XAdES Manifest</li></ul> |
| CSVSignatura | Body | No | Text | -- | S&#39;informa si a TipoFirma =TF01 |
| regulacioGeneracioCSVSignatura | Body | No | Text | -- | S&#39;informa si a TipoFirma =TF01 |
| referenciaSignatura | Body | No | Text | -- | Només cas TF03 i TF04. Referencia al fitxer que inclou la signatura (uuidFitxer) |
| identificadorDocumentOrigen | Body | No | Text | -- | Identificador normalizat del document origen al que correspon la copia. Només si s'ha indicat EE02,EE03 i EE04 a EstadoElaboracion |
| descripcio | Body | No | Text | -- | -- |
| nivellAcces | Body | No | Text | -- | <ul>A-Secret</li><li>B-Reservat</li><li>C-Confidencial</li><li>E-No classificat</li></ul> |
| clasificacioENS | Body | No | Text | -- | Baix, Mig, Alt |
| sensibilitatDadesCaracterPersonal | Body | No | -- | -- | Basic, Mig, Alt |
| documentEssencial | Body | No | -- | -- | True (si), False (NO) |
| codiClassificacio | Body | No | -- | -- | -- |
| nomClassificacio | Body | No | -- | -- | -- |
| codiSIA | Body | No | -- | -- | -- |
| infoAddicional | Body | No | Llista | -- | Llista d&#39;elements clau/valor |

![image](https://user-images.githubusercontent.com/32306731/156012337-af4b1748-268c-44e7-bfca-5663ba265001.png)

### Resposta

![image](https://user-images.githubusercontent.com/32306731/156012614-25feb10c-73bc-47e6-acf7-26d4e703edd8.png)

### Codis de resposta

A continuació es detallen els possibles codis de resposta per la modificació del document (per al codi d&#39;error 11, XXXXXX especifica la metadada en qüestió i per al codi d&#39;error 100 XXXXXX ofereix més detalls de l&#39;error no controlat):

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 1 | El document és correcte però el fitxer encara està sent analitzat per l'antivirus
| 2 | Error: No s'ha fet el put del fitxer a S3 (URL-Presigned)
| 4 | Error: Petició mal formada
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

El següent diagrama mostra les 2 possibilitats amb les que es pot trobar DESA&#39;L en el moment d&#39;eliminar el document si aquest està associat amb un fitxer a través de la metadada _**UUIDFitxer**_:

![image](https://user-images.githubusercontent.com/32306731/156012806-1f53e86f-c025-4fed-8a89-c89197aba8f3.png)

### Petició

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| uuidDocument | PathParam | Sí | Text | -- | -- |
| codiINE | QueryParam | Sí | Text | 10 | -- |
| codiServei | QueryParam | Sí | Text | 10 | -- |

![image](https://user-images.githubusercontent.com/32306731/156012971-745a44a1-613a-4071-a1df-fe43310691af.png)

### Resposta

![image](https://user-images.githubusercontent.com/32306731/156013045-461b0bd7-a072-4fa4-a726-1d8c57464de7.png)

### Codis de resposta

A continuació es detallen els possibles codis de resposta per l&#39;eliminació de document (per al codi d&#39;error 11, XXXXXX especifica la metadada en qüestió i per al codi d&#39;error 100 XXXXXX ofereix més detalls de l&#39;error no controlat):

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 4 | Error: Petició mal formada. |
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
| uuidDocument | PathParam | Sí | Text | -- | -- |
| codiServei | QueryParam | Sí | Text | 10 | --|
| codiINE | QueryParam | Sí | Text | 10 | -- |
| Modalitat | QueryParam | Sí | Número | 1 | Posar &quot;1&quot; per a modalitat 1 |

![image](https://user-images.githubusercontent.com/32306731/156013205-594427d4-079e-4dc1-98e3-aa28a70a345f.png)

### Resposta

![image](https://user-images.githubusercontent.com/32306731/156013374-529e26ba-3813-4889-9a41-b47e8ef1be10.png)

### Petició Modalitat 2: Descarrega Document i contingut (fitxer)

**Important:** Si l’antivirus no ha pogut finalitzar l’anàlisi d’algun dels fitxers, la descàrrega de l’expedient fallarà amb un codi d’error 1 - El contingut del fitxer està esperant a ser analitzat pel antivirus.

La modalitat 2 només es pot executar si el document té un contingut igual 1 (fitxer).

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| uuidDocument | PathParam | Sí | Text | -- | -- |
| codiServei | QueryParam | Sí | Text | 10 | -- |
| codiINE | QueryParam | Sí | Text | 10 | -- |
| Modalitat | QueryParam | Sí | Número | 1 | Posar &quot;2&quot; per a modalitat 2 |

![image](https://user-images.githubusercontent.com/32306731/156013703-a65f5209-8c05-4ea3-9043-01bd7817f09f.png)

### Resposta

![image](https://user-images.githubusercontent.com/32306731/156013838-eef71872-9204-4a49-ba09-5b92dd4b5a54.png)
	
### Codis de resposta

A continuació es detallen els possibles codis de resposta per a la descàrrega del document (per al codi d&#39;error 100 XXXXXX ofereix més detalls de l&#39;error no controlat):

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 1 | Error: El contingut del fitxer està esperant a ser analitzat pel antivirus. |
| 4 | Error: Petició mal formada. |
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
| uuidDocument | PathParam | Sí | Text | -- | -- |
| codiINE | QueryParam | Sí | Text | 10 | -- |
| codiServei | QueryParam | Sí | Text | 10 | -- |

![image](https://user-images.githubusercontent.com/32306731/156014155-0cac96b2-0e21-4517-9092-641defb8ae9c.png)

### Resposta

![image](https://user-images.githubusercontent.com/32306731/156014253-69baa29e-1f76-47b6-8adf-8b259aa89b4b.png)

### Codis de resposta

A continuació es detallen els possibles codis de resposta per a la descàrrega del document en format ENI:

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 1 | Error: El contingut del fitxer està esperant a ser analitzat pel antivirus. |
| 4 | Error: Petició mal formada. |
| 10 | Error: no tens autorització per realitzar aquesta operació. Operació NO realitzada. |
| 11 | Error: la petició no és correcta. Operació NO realitzada. |
| 12 | Error: l&#39;expedient indicat no existeix en el servei i organisme indicats. Operació NO realitzada. |
| 100 | Error no controlat: XXXXXX. Si us plau, reintenti l&#39;operació en uns minuts. Operació NO realitzada. |

## 6.6 Cerca de Documents <a name="cerca-documents" id="cerca-documents"></a>

Aquest mètode de l'API permet cercar tots aquells documents que cumpleixen una sèrie de criteris de filtratge, informats a la petició.

La cerca es realitzarà aplicant tots aquests criteris de filtratge de manera conjuntiva (logical AND). No es suporta la realització de cerques aplicant els criteris de manera disjuntiva (logical OR) o la construcció de consultes complexes combinant ambdues lògiques.

El paràmetre _**modality**_ indica si la cerca ha de retornar únicament les metadades dels documents o si per contra també ha de generar les URL pre-signades per a poder descarregar el contingut dels fitxers associats als documents (per a aquells documents amb tipus de _**contingut**_=1).

Amb la finalitat de garantir el rendiment i protegir el servei davant de sobrecàrregues _**no es retornaran més de 100 resultats**_ per cerca.

La URL corresponent a aquesta operació de l'API és:

```javascript
https://{{host}}/document/search?codiServei={{codiServei}}&codiINE={{codiINE}}&modality={{modalitat}}
```

### Petició <a name="peticio-cerca-doc" id="peticio-cerca-doc"></a>

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Observacions** |
| --- | --- | --- | --- | --- |
| codiINE | Query String | Si | Text | Codi d'organisme del requeridor |
| codiServei | Query String | Si | Text | Codi de servei del requeridor |
| modality | Query String | Si | Numèric | <ul><li>1 = només metadades</li><li>2 = metadades i URL pre-signades</li></ul> |
| codiINE | Body | No | Text | -- |
| codiServei | Body | No | Text | -- |
| uuidDocument | Body | No | Text | -- |
| sensibilitatDadesCaracterPersonal | Body | No | Text | -- |
| documentEssencial | Body | No | Booleà | -- |
| idioma | Body | No | Text | -- |
| codiClassificacio | Body | No | Text | -- |
| nomClassificacio | Body | No | Text | -- |
| codiSIA | Body | No | Text | -- |
| nomNatural | Body | No | Text | -- |
| infoAddicional | Body | No | Llista | _[Veure 6.6.1](#6.6.1)_ |
| infoAddicional[].key | Body | No | Text | -- |
| infoAddicional[].value | Body | No | Text | -- |
| CSV | Body | No | Text | -- |
| formatFitxer | Body | No | Text | -- |
| hash | Body | No | Base64 | -- |
| hashAlgoritme | Body | No | Text | -- |
| mida | Body | No | Bloc | _[Veure 6.6.2](#6.6.2)_ |
| mida.de | Body | No | Numèric | -- |
| mida.fins | Body | No | Numèric | -- |
| nomFitxer | Body | No | Text | -- |
| uuidFitxer | Body | No | Text | -- |
| URLDocumentExtern | Body | No | Text | -- |
| dataAlta | Body | No | Bloc | _[Veure 6.6.3](#6.6.3)_ |
| dataAlta.inici | Body | No | Numèric | -- |
| dataAlta.fi | Body | No | Numèric | -- |
| dataDocument | Body | No | Bloc | _[Veure 6.6.4](#6.6.4)_ |
| dataDocument.inici | Body | No | Numèric | -- |
| dataDocument.fi | Body | No | Numèric | -- |
| identificadorExpedientDesal | Body | No | Text | -- |
| identificadorExpedientExtern | Body | No | Text | -- |
| versioNTI | Body | No | Text | -- |
| identificador | Body | No | Text | -- |
| organ | Body | No | Text | -- |
| estatElaboracio | Body | No | Text | -- |
| origen | Body | No | Booleà | -- |
| tipusDocumental | Body | No | Text | -- |
| tipusSignatura | Body | No | Text | -- |
| CSVSignatura | Body | No | Text | -- |
| regulacioGeneracioCSVSignatura | Body | No | Text | -- |
| referenciaSignatura | Body | No | Text | -- |
| identificadorDocumentOrigen | Body | No | Text | -- |
| tipusDocumentalSICRES | Body | No | Text | -- |
| descripcio | Body | No | Text | -- |
| nivellAcces | Body | No | Text | -- |
| classificacioENS | Body | No | Text | -- |
| identificadorDocumentExtern | Body | No | Text | -- |
| interessat | Body | No | Text | -- |
| usuari | Body | No | Text | -- |
| numeroRegistre | Body | No | Text | -- |
| contingut | Body | No | Text | -- |

> **_NOTA:_**  Per a la descripció dels camps dels documents i el seu format consulteu l'apartat _[2.2](#2.2)_ d'aquest manual.

##### Info Addicional <a name="6.6.1" id="6.6.1"></a>
```json
"infoAddicional": [
  {
    "key": "clau_1",
    "value": "valor_1"
  }
]
```

##### Rang numèric <a name="6.6.2" id="6.6.2"></a>
```json
"mida": {
  "de": 370000,
  "fins": 375000
}
```

##### Rang de dates d'alta <a name="6.6.3" id="6.6.3"></a>
```json
"dataAlta": {
  "inici": 1652432260560,
  "fi": 1652432264560
},
```

##### Rang de dates de document <a name="6.6.4" id="6.6.4"></a>
```json
"dataDocument": {
  "inici": 1652432260560,
  "fi": 1652432264560
},
```

#### Exemple de petició <a name="exemple-peticio-cerca-documents" id="exemple-peticio-cerca-documents"></a>
```json
{
  "codiServei": "SERVEI",
  "codiINE": "9821920002",
  "interessat": "22222222R",
  "nomNatural": "natural",
  "dataAlta": {
    "inici": 1652432260560,
    "fi": 1652432264560
  },
  "dataDocument": {
    "inici": 1652432250000,
    "fi": 1652432270000
  },
  "infoAddicional": [
    {
      "key": "clau_1",
      "value": "valor_1"
    }
  ],
  "numeroRegistre": "E/999999-2022",
  "CSVSignatura": "CSVSIG-1652432261048",
  "CSV": "CSVFTX-1652432260985",
  "identificadorExpedientExtern": "EXP/9999999/2022",
  "uuidFitxer": "11111111-1111-1111-1111-111111111111",
  "uuidDocument": "11111111-1111-1111-1111-111111111111"
}
```

### Resposta <a name="resposta-cerca-documents" id="resposta-cerca-documents"></a>

| **Element** | **Tipus paràmetre** | **Tipus camps** | **Observacions** |
| --- | --- | --- | --- |
| totalResultats | Body | Text | -- |
| resultatsRecuperats | Body | Text | -- |
| codiResposta | Body | Text | -- |
| descripcioResposta | Body | Text | -- |
| documents | Body | Llista | Llista de documents recuperats |

> **_NOTA:_**  Per a la descripció dels camps dels documents i el seu format consulteu l'apartat _[2.2](#2.2)_ d'aquest manual.

#### Exemple de resposta <a name="exemple-resposta-cerca-documents" id="exemple-resposta-cerca-documents"></a>
```json
{
  "totalResultats": 2,
  "resultatsRecuperats": 2,
  "codiResposta": "0",
  "descripcioResposta": "Operació realitzada correctament",
  "documents": [
    {
      "uuidDocument": "11111111-1111-1111-1111-111111111111",
      "uuidFitxer": "22222222-2222-2222-2222-222222222222",
      "codiINE": "9610420002",
      "codiServei": "eVALISA",
      "nomNatural": "curs_prevencio_riscos",
      "documentEssencial": false,
      "idioma": "ca_ES",
      "CSV": "961042000222022022C261HF1KRL8",
      "formatFitxer": "application/pdf",
      "hash": "AtCnNoXBWaHQtRuXtkYce1lgKUu+cMFDHdyJjHLaNMA=",
      "hashAlgoritme": "SHA-256",
      "mida": 346778,
      "nomFitxer": "curs_prevencio_riscos.pdf",
      "dataAlta": 1645529469000,
      "dataDocument": 1645525800000,
      "contingut": "1",
      "identificadorExpedientDesal": "99999999-9999-9999-9999-999999999999",
      "versioNTI": "http://administracionelectronica.gob.es/ENI/XSD/v1.0/documento-e",
      "identificador": "ES_9610420002_2022_11111111-1111-1111-1111-111111111111",
      "organ": "A09018799",
      "estatElaboracio": "EE01",
      "origen": true,
      "tipusDocumental": "TD99",
      "tipusSignatura": "TF01",
      "CSVSignatura": "961042000222022022C261HF1KRL8",
      "regulacioGeneracioCSVSignatura": "Resolució sobre l'ús del sistema de codi segur de verificació del Consorci AOC",
      "tipusDocumentalSICRES": "02",
      "nivellAcces": "E",
      "codiResposta": "0",
      "interessat": [],
      "usuari": "66666667V"
    },
    {
      "uuidDocument": "22222222-2222-2222-2222-222222222222",
      "uuidFitxer": "33333333-3333-3333-3333-333333333333",
      "codiINE": "9610420002",
      "codiServei": "eVALISA",
      "nomNatural": "curs_prevencio_riscos",
      "documentEssencial": false,
      "idioma": "ca_ES",
      "infoAddicional": [],
      "CSV": "9610420002220220227S3708IDS7CK",
      "formatFitxer": "application/pdf",
      "hash": "AtCnNoXBWaHQtRuXtkYce1lgKUu+cMFDHdyJjHLaNMA=",
      "hashAlgoritme": "SHA-256",
      "mida": 346778,
      "nomFitxer": "curs_prevencio_riscos.pdf",
      "dataAlta": 1645528888000,
      "dataDocument": 1645525260000,
      "contingut": "1",
      "identificadorExpedientDesal": "99999999-9999-9999-9999-999999999999",
      "versioNTI": "http://administracionelectronica.gob.es/ENI/XSD/v1.0/documento-e",
      "identificador": "ES_9610420002_2022_22222222-2222-2222-2222-222222222222",
      "organ": "A09018799",
      "estatElaboracio": "EE01",
      "origen": true,
      "tipusDocumental": "TD99",
      "tipusSignatura": "TF01",
      "CSVSignatura": "9610420002220220227S3708IDS7CK",
      "regulacioGeneracioCSVSignatura": "Resolució sobre l'ús del sistema de codi segur de verificació del Consorci AOC",
      "tipusDocumentalSICRES": "02",
      "nivellAcces": "E",
      "codiResposta": "0",
      "interessat": ["11111111H"],
      "usuari": "33333334D"
    }
  ]
}
```

### Codis de Resposta <a name="codis-resposta-cerca-documents" id="codis-resposta-cerca-documents"></a>

A continuació es detallen els possibles codis de resposta per a l'operació de cerca de documents:

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 4 | Error: Petició mal formada. |
| 10 | Error: no tens autorització per realitzar aquesta operació. Operació NO realitzada. |
| 100 | Error no controlat: XXXXXX. Si us plau, reintenti l&#39;operació en uns minuts. Operació NO realitzada. |

## 6.7 Eliminació de Documents <a name="eliminacio-documents" id="eliminacio-documents"></a>

Aquest mètode permet eliminar diversos documents, i en cascada, el propi fitxer associat si aquest només està referenciat per un únic document.

**Important:** Si el servei integrador elimina un document i aquest està associat a un fitxer a través de la metadada UUIDFitxer, DESA&#39;L comprovarà si hi ha algun altre document que referenciï a aquest fitxer. En cas contrari, eliminarà el fitxer de forma irreversible.

El següent diagrama mostra les 2 possibilitats amb les que es pot trobar DESA&#39;L en el moment d&#39;eliminar un document si aquest està associat amb un fitxer a través de la metadada _**UUIDFitxer**_:

![image](https://user-images.githubusercontent.com/32306731/156012806-1f53e86f-c025-4fed-8a89-c89197aba8f3.png)

### Petició <a name="peticio-eliminacio-documents" id="peticio-eliminacio-documents"></a>

| **Element** | **Tipus paràmetre** | **Obligatori** | **Tipus camps** | **Mida màxima** | **Observacions** |
| --- | --- | --- | --- | --- | --- |
| uuidDocument | Body | Sí | Llista | -- | -- |
| codiINE | QueryParam | Sí | Text | 10 | -- |
| codiServei | QueryParam | Sí | Text | 10 | -- |

La URL corresponent a aquesta operació de l'API és:

```javascript
https://{{host}}/document/deleteDocuments?codiServei={{codiServei}}&codiINE={{codiINE}}
```

El contingut de la petició quedaria: 

```json
{
"uuidDocument": ["1a6648d1-0e98-463f-93c4-cc468dbcd1e8","b6815ee4-b83f-4218-8240-54eae6be1d67"]
}
```

### Resposta <a name="resposta-eliminacio-documents" id="resposta-eliminacio-documents"></a>

```json
{
    "codiResposta": "0",
    "descripcioResposta": "Operació realitzada correctament"
}
```

### Codis de resposta <a name="codis-resposta-eliminacio-documents" id="codis-resposta-eliminacio-documents"></a>

A continuació es detallen els possibles codis de resposta per l&#39;eliminació de documents (per al codi d&#39;error 11, XXXXXX especifica la metadada en qüestió i per al codi d&#39;error 100 XXXXXX ofereix més detalls de l&#39;error no controlat):

| **Codi** | **Missatge** |
| --- | --- |
| 0 | Operació realitzada correctament. |
| 4 | Error: Petició mal formada. |
| 10 | Error: no tens autorització per realitzar aquesta operació. Operació NO realitzada. |
| 11 | Error: la petició no és correcta. Hi ha metadades obligatòries sense informar o metadades informades no vàlides (XXXXXX). Operació NO realitzada. |
| 12 | Error: el número d&#39;expedient indicat no existeix en el servei i organisme indicats. Operació NO realitzada. |
| 13 | Error: el fitxer físic indicat no existeix. Operació NO realitzada. |
| 14 | Error: el fitxer físic conté virus i ha estat eliminat. Operació NO realitzada. |
| 100 | Error no controlat: XXXXXX. Si us plau, reintenti l&#39;operació en uns minuts. Operació NO realitzada. |
| 101 | Error: el document físic indicat està en procés de validació. Si us plau, reintenta l&#39;operació en uns minuts. Operació NO realitzada. |
