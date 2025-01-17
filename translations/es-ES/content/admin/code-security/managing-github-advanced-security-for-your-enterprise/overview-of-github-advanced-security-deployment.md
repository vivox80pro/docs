---
title: Resumen del despliegue de la Seguridad Avanzada de GitHub
intro: Ayuda a tu compañía para que se prepare con éxito para adoptar la {% data variables.product.prodname_GH_advanced_security %} (GHAS) revisando y entendiendo estas mejores prácticas, ejemplos de implementación y nuestro acercamiento gradual probado en empresas.
product: '{% data variables.product.prodname_GH_advanced_security %} is a set of security features designed to make enterprise code more secure. It is available for {% data variables.product.prodname_ghe_server %} 3.0 or higher, {% data variables.product.prodname_ghe_cloud %}, and open source repositories. To learn more about the features, included in {% data variables.product.prodname_GH_advanced_security %}, see "[About GitHub Advanced Security](/get-started/learning-about-github/about-github-advanced-security)."'
redirect_from:
- /admin/advanced-security/overview-of-github-advanced-security-deployment
miniTocMaxHeadingLevel: 3
versions:
  ghes: '*'
  ghec: '*'
type: how_to
topics:
- Advanced Security
- Code scanning
- Enterprise
- Security
ms.openlocfilehash: 9c58cc8cca76a19ccc1aa36770e4cafcf4c9fcc7
ms.sourcegitcommit: 22d665055b1bee7a5df630385e734e3a149fc720
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/13/2022
ms.locfileid: "145120857"
---
La {% data variables.product.prodname_GH_advanced_security %} (GHAS) ayuda a los equipos a crear código más seguro de forma más rápida utilizando las herramientas integradas, tales como CodeQL, el motor de análisis de código semántico más avanzado del mundo. La GHAS es una suite de herramientas que requiere una participación activa de los desarrolladores en toda tu empresa. Para realizar el mejor retorno de inversión para tu empresa, debes aprender cómo utilizar, aplicar y mantener la GHAS para proteger tu código verdaderamente.

Uno de los retos más grandes en abordar el software nuevo para una compañía puede ser el proceso de implementación y despliegue, así como traer el cambio cultural para impulsar la participación organizacional necesaria para que dicha implementación tenga éxito.

Para ayudar a que tu compañía entienda y se prepare mejor para este proceso con la GHAS, este resumen se enfoca en:
  - Proporcionar información general del aspecto que tendría un lanzamiento de GHAS para la empresa.
  - Ayudarte a preparar tu compañía para esta implementación.
  - Compartir los principales procedimientos recomendados para ayudarle a incrementar el éxito del lanzamiento de la empresa.

Para comprender las características de seguridad disponibles mediante {% data variables.product.prodname_GH_advanced_security %}, vea "[Características de seguridad de {% data variables.product.prodname_dotcom %}](/code-security/getting-started/github-security-features)".

## <a name="recommended-phased-approach-for-ghas-rollouts"></a>Método gradual recomendado para las implementaciones de la GHAS

Creamos un enfoque gradual para las implementaciones de la GHAS que se desarrolla con las mejores prácticas de la industria y de GitHub. Puedes utilizar este enfoque para tu implementación, ya sea en asociación con {% data variables.product.prodname_professional_services %} o independientemente.

Si bien se recomienda el enfoque gradual, los ajustes pueden realizarse con base en las necesidades de tu compañía. También te sugerimos crear y apegarte a una línea de tiempo para tu implementación y despliegue. Conforme comienzas tu planeación, podemos trabajar en conjunto para identificar el enfoque y línea de tiempo ideales que funcionen mejor para tu compañía.

![Diagrama en el que se muestran las tres fases de lanzamiento e implementación de la Seguridad avanzada de GitHub, incluyendo la Fase 0: Planificación y puesta en marcha, Fase 1: Proyectos piloto, Fase 2: Participación de la organización e implementación para usuarios pioneros, y Fase 3: Implementación completa de la organización y administración de cambios](/assets/images/enterprise/security/advanced-security-phased-approach-diagram.png)


Con base en nuestra experiencia ayudando a los clientes a tener un despliegue exitoso de la {% data variables.product.prodname_GH_advanced_security %}, esperamos que la mayoría de ellos estén dispuestos a seguir estas fases. Dependiendo de las necesidades de tu compañía, podrías necesitar modificar este enfoque y modificar o eliminar algunas fases o pasos.

Para obtener una guía detallada sobre cómo implementar cada una de estas fases, vea "[Implementación de {% data variables.product.prodname_GH_advanced_security %} en la empresa](/admin/advanced-security/deploying-github-advanced-security-in-your-enterprise)". La siguiente sección te proporciona un resumen de alto nivel de cada una de estas fases.

###  <a name="-octicon-milestone-aria-labelthe-milestone-icon--phase-0-planning--kickoff"></a>{% octicon "milestone" aria-label="The milestone icon" %} Fase 0: Planificación e inicio

Durante esta fase, la meta general es planear y prepararte para la implementación, garantizando que tienes lista a la gente, procesos y tecnologías y que estás listo para llevarla a cabo. También debes considerar qué criterios de éxito se utilizarán para medir la adopción de la GHAS y su uso por parte de todos tus equipos.

### <a name="-octicon-milestone-aria-labelthe-milestone-icon---phase-1-pilot-projects"></a>{% octicon "milestone" aria-label="The milestone icon" %}  Fase1: Proyecto(s) piloto

Para comenzar a implementar la GHAS, te recomendamos comenzar con unos cuantos equipos/proyectos de alto impacto con los cuales puedas hacer un piloto de la implementación inicial. Esto permitirá que un grupo inicial dentro de tu compañía se familiarice con la GHAS, aprenda cómo habilitarla y configurarla y cree bases sólidas en ella antes de implementarla con el resto de tu compañía.

### <a name="-octicon-milestone-aria-labelthe-milestone-icon---phase-2-organizational-buy-in--rollout-preparation"></a>{% octicon "milestone" aria-label="The milestone icon" %} Fase 2: Participación de la organización y preparación para el lanzamiento

La Fase 2 es una recapitulación de las fases previas y una preparación para una implementación mayor a lo largo del resto de la compañía. En esta fase, la participación organizacional puede referirse a la decisión de tu compañía para avanzar después del (los) proyecto(s) piloto o del uso y adopción de la GHAS en la compañía con el tiempo (esto es lo más común). Si tu compañía decide adoptar la GHAS con el tiempo, entonces la fase 2 puede seguir con la fase 3 y posterior.

### <a name="-octicon-milestone-aria-labelthe-milestone-icon---phase-3-full-organizational-rollout--change-management"></a>{% octicon "milestone" aria-label="The milestone icon" %} Fase 3: Lanzamiento completo de la organización y administración de cambios

Una vez que tu compañía se alinee, puedes comenzar a implementar la GHAS en el resto de ella con base en tu plan de implementación. Durante esta fase, es crucial asegurarse de que se haya hecho un plan para abordar cualquier cambio organizacional que necesite hacerse durante tu implementación de GHAS y garantizar que los equipos entiendan la necesidad, valor e impacto de dicho cambio en los flujos de trabajo actuales.

## <a name="best-practices-for-a-successful-ghas-rollout"></a>Mejores prácticas para una implementación exitosa de la GHAS

Hemos visto que las compañías que completan implementaciones exitosas de la GHAS tienen varias características similares que les permiten impulsar su éxito. Para ayudar a tu compañía a incrementar el éxito de la implementación de la GHAS, revisa estas mejores prácticas.

### <a name="-octicon-checklist-aria-labelthe-checklist-icon--set-clear-goals-for-your-companys-rollout"></a>{% octicon "checklist" aria-label="The checklist icon" %} Establece metas claras para la implementación en tu compañía

El establecer metas podría verse como algo obvio, pero hemos visto que algunas compañías que comienzan su implementación de la GHAS no las tienen en mente. Es más difícil que estas compañías obtengan una verdadera participación organizacional, la cual se requiere para completar el proceso de implementación y comprender el valor de la GHAS en ellas.

Conforme comienzas a planear tu implementación y despliegue, comienza a definir las metas para la GHAS dentro de tu compañía y asegúrate de que estas se le comuniquen a tu equipo. Tus metas pueden tener mucho detalle o ser simples, en tanto exista un punto inicial y un alineamiento. Esto ayudará a crear bases para la dirección de la implementación de tu compañía y para crear un plan para conseguirlo. Si necesitas ayuda para establecer tus metas, {% data variables.product.prodname_professional_services %} puede ayudarte dándote recomendaciones con base en nuestra experiencia con tu compañía y con las interacciones que hemos tenido con otros clientes.

Aquí tienes algunos ejemplos de alto nivel de cómo podrían verse tus metas para implementar la GHAS:
  - **Reducción del número de vulnerabilidades:** esto puede ser general o porque la empresa se haya visto afectada recientemente por alguna vulnerabilidad significativa, que considere que se podría haber evitado con una herramienta como GHAS.
  - **Identificación de los repositorios de riesgo algo:** es posible que algunas empresas solo quieran centrarse en repositorios que contengan el mayor riesgo, listos para comenzar a corregir las vulnerabilidades y reducir los riesgos.
  -  **Aumento de las tasas de corrección:** esto se puede lograr mediante el impulso de la adopción de los hallazgos de los desarrolladores y garantizando que estas vulnerabilidades se corrigen de forma oportuna, a fin de evitar que se acumule la deuda de seguridad.  
  - **Satisfacción de los requisitos de cumplimiento:** puede ser tan simple como crear requisitos de cumplimiento o algo más específico. Hemos visto que muchas compañías del sector salud utilizan la GHAS para prevenir la divulgación de la PHI (Información Personal sobre la Salud, por sus siglas en inglés).
  - **Prevenir la fuga de secretos:** este suele ser el objetivo de las empresas que han sufrido (o quieren evitar) la fuga de información como claves de software, datos financieros o del cliente, etc.
  - **Administración de dependencias:** este suele ser el objetivo de las empresas que han sido víctimas de ataques desde dependencias sin revisar, o bien de las que buscan impedir este tipo de ataques mediante la actualización de las dependencias vulnerables.  

### <a name="-octicon-checklist-aria-labelthe-checklist-icon--establish-clear-communication-and-alignment-between-your-teams"></a>{% octicon "checklist" aria-label="The checklist icon" %} Establecer un alineamiento y comunicación clara entre tus equipos

La comunicación clara y el alineamiento son críticos para el éxito de cualquier proyecto y la implementación de la GHAS no es la exepción. Hemos visto que las compañías que tienen comunicaciones claras y que se alinean entre sus grupos de desarrollo y seguridad, así como con su patrocinador ejecutivo (ya sea el CISO o VP) desde la compra de GHAS hasta su implementación suelen tener más éxito en dichas implementaciones.

Adicionalmente a garantizar que estos grupos se encuentran alineados a lo largo de tu implementación de la GHAS, hay algunas áreas específicas en las que recomendamos te enfoques.

#### <a name="rollout-planning"></a>Planeación de la implementación

¿Cómo implementarás la GHAS en tu compañía? Lo más seguro es que se presenten muchas ideas y opiniones. Aquí tienes algunas preguntas que deberías considerar responder y con las cuales deberías alinearte antes de seguir:
  - ¿Qué equipos se incluirán en el piloto?
  - ¿Qué proyectos están enfocados en el piloto?
  - ¿Cómo deberían priorizarse los proyectos para la implementación?
  - ¿Cómo planeas medir el éxito del piloto y después de este?
  - ¿Cuál es el nivel de cambio diario que experimentarán tus equipos? ¿Cómo se comunicará esto?
  - ¿Cómo se comunicarán tus planes de implementación en toda la compañía?
  - ¿Cómo planeas capacitar a tus equipos?
  - ¿Cómo planeas administrar los resultados de escaneo inicialmente? (Para obtener más información, consulta la siguiente sección enfocada en el "Procesamiento de resultados")

#### <a name="processing-results"></a>Procesar resultados

Antes de implementar la GHAS en tus equipos, debería de haber un alineamiento claro en cómo se deben administrar los resultados con el paso del tiempo. Te recomendamos ver los resultados inicialmente, conforme sean más informativos, y sin bloquear. Es probable que tu compañía tenga un mapa completo de IC/DC, así que recomendamos este enfoque para evitar bloquear sus procesos. Conforme te acostumbres a procesar estos resultados, podrás incrementar gradualmente el nivel de restricción hasta un punto en el que se sienta más adecuado para tu compañía.

### <a name="-octicon-checklist-aria-labelthe-checklist-icon---lead-your-rollout-with-both-your-security-and-development-groups"></a>{% octicon "checklist" aria-label="The checklist icon" %}  Dirigir tu implementación tanto con tu equipo de seguridad como con los grupos de desarrllo

Muchas compañías dirigen su implementación de la GHAS con su grupo de seguridad. A menudo, no se incluye a los equipos de desarrollo en el proceso de implementación sino hasta que concluye el piloto. Sin embargo, nos hemos dado cuenta de que las compañías que dirigen sus implementaciones tanto con su equipo de seguridad como con el de desarrollo suelen tener más éxito con la implementación de su GHAS.

¿Por qué? La GHAS lleva un enfoque centrado en los desarrolladores para abordar la seguridad del software, integrándose fácilmente en el flujo de trabajo de estos. El no tener una representación clave de tu grupo de desarrollo en las fases tempranas del proceso incrementará el riesgo de la implementación y creará una pendiente para la participación organizacional.

Cuando se involucra tempranamente a los grupos de desarrollo (idealmente, desde la compra), tanto estos como los de seguridad pueden lograr un alineamiento temprano en el proceso. Esto ayuda a eliminar brechas entre ambos grupos, crea fortaleza en sus relaciones laborales y ayuda a evitar la mentalidad común de "aventar las cosas a la pared". Todo esto ayuda a apoyar la meta general de ayudar a las compañías a cambiar y comenzar a utilizar la GHAS para abordar las preocupaciones de seguridad de forma más temprana en el proceso de desarrollo.

#### <a name="-octicon-people-aria-labelthe-people-icon--recommended-key-roles-for-your-rollout-team"></a>{% octicon "people" aria-label="The people icon" %} Roles clave recomendados para tu equipo de desarrollo

Te recomendamos algunos roles clave para que los tengas en tu equipo y así te asegures de que tus grupos están bien representados a lo largo de la planeación y ejecución de tu implementación y despliegue.

Te recomendamos ampliamente que tu equipo de implementación incluya estos roles:
- **Patrocinador ejecutivo:** suele ser el CISO, CIO, vicepresidente de seguridad o vicepresidente de ingeniería.
- **Jefe de seguridad técnica:** el jefe de seguridad técnica proporciona soporte técnico en nombre del equipo de seguridad a lo largo del proceso de implementación.
- **Jefe de desarrollo técnico:** el jefe de desarrollo técnico proporciona soporte técnico y probablemente dirigirá el esfuerzo de implementación con el equipo de desarrollo.  

También te recomendamos que tu equipo de implementación incluya estos roles:
- **Jefe de proyecto:** se ha comprobado que cuanto antes participe el jefe de proyecto en el proceso de implementación, mayor serán las probabilidades de éxito.  
- **Ingeniero de control de calidad:** la inclusión de un miembro del equipo de control de calidad de la empresa ayuda a garantizar que los cambios del proceso se tienen en cuenta para el equipo de control de calidad.

### <a name="-octicon-checklist-aria-labelthe-checklist-icon--understand-key-ghas-facts-to-prevent-common-misconceptions"></a>{% octicon "checklist" aria-label="The checklist icon" %} Entender hechos clave de la GHAS para prevenir malentendidos comunes

Cuando se inicia una implementación de la GHAS, es importante entender algunos hechos clave básicos sobre qué es la GHAS y qué puede hacer y así prevenir muchos malentendidos comunes que tienen las compañías al iniciar sus implementaciones de la GHAS.

{% note %}

**Nota:** Si le interesa obtener más información sobre GHAS, en {% data variables.product.prodname_professional_services %} se ofrecen diversas opciones educativas y de entrenamiento adicionales, incluidos temas que la empresa necesita preparar para GHAS. Estas ofertas podrían mostrarse como talleres, demostraciones y capacitaciones intensivas. Los temas pueden ir desde desplegar la GHAS y mostrar su uso básico hasta algunos más avanzados para seguir desarrollando las habilidades de tu equipo. Para más información sobre cómo trabajar con el equipo de {% data variables.product.prodname_professional_services_team %}, vea "[{% data variables.product.prodname_professional_services %}](#github-professional-services)".

{% endnote %}


#### <a name="fact-1-ghas-is-a-suite-of-security-tools-that-require-action-to-protect-your-code"></a>Hecho 1: La GHAS es una suite de herramientas de seguridad que requiere de una participación activa para proteger tu código.

No es software de seguridad que se pueda instalar y olvidar; el solo hecho de tener la GHAS no protege tu código. La GHAS es una suite de herramientas que incrementa su valor cuando la configuras, mantienes, utilizas en flujos de trabajo diariamente y la combinas con otras herramientas.

#### <a name="fact-2-ghas-will-require-adjustment-out-of-the-box"></a>Hecho 2: La GHAS necesitará ajustes tan pronto la implmementes.

Una vez que configures la GHAS en tus repositorios, habrán pasos adicionales necesarios para garantizar que funcione de acuerdo con las necesidades de tu compañía. El escaneo de código en particular necesita configurarse aún más para hacer los ajustes más específicos en tus resultados, por ejemplo, personalizar lo que marcan los escaneos para ajustar qué se escogerá en los escaneos futuros. Muchos clientes se encuentran con que los escaneos iniciales ya sea no recogen resultados, o bien, que estos resultados no son relevantes con base en el modelo de amenazas de aplicación y necesitan ajustarse de acuerdo con las necesidades de sus compañías.

#### <a name="fact-3-ghas-tools-are-most-effective-when-used-together-but-the-most-effective-appsec-programs-involve-the-use-of-additional-toolsactivities"></a>Hecho 3: Las herramientas de la GHAS tienen su mayor efectividad cuando se utilizan en conjunto, pero los programas más efectivos de AppSec involucran el uso de actividades/herramientas adicionales.

La GHAS tiene su mayor efectividad cuando se utilizan todas las herramientas en conjunto. Cuando las compañías integran la GHAS con otras herramientas y actividades, tales como pruebas de penetración y escaneos dinámicos, esta mejora aún más la efectividad del programa de AppSec. Te recomendamos que siempre utilices capas de protección múltiples.

#### <a name="fact-4-not-all-companies-will-useneed-custom--data-variablesproductprodname_codeql--queries-but-they-can--help-you-customizetarget-scan-results"></a>Hecho 4: No todas las compañías utilizarán/necesitarán consultas de {% data variables.product.prodname_codeql %} personalizadas, pero pueden ayudarte a personalizar/apuntar los resultados del escaneo.

{% data variables.product.prodname_codeql %}, el motor de análisis de código más poderoso del mundo, impulsa el escaneo de código. Si bien muchas compañías están emocionadas con la posibilidad de poder escribir consultas personalizadas, para la mayoría de ellas, el conjunto básico de consultas y las adicionales disponibles en la comunidad, son habitualmente más que suficiente. Sin embargo, muchas compañías podrían encontrar la necesidad de tener consultas personalizadas de {% data variables.product.prodname_codeql %} para ayudarles a reducir las tasas de falsos positivos en los resultados o para crear consultas nuevas para tratar los resultados que pudiera necesitar tu compañía.

Sin embargo, si tu compañía está interesada en escribir consultas personalizadas de {% data variables.product.prodname_codeql %}, te recomendamos completar tu implementación y despliegue de la GHAS antes de explorar esta opción.

{% note %}

**Nota:** Es fundamental que la empresa tenga una base sólida de GHAS antes de profundizar en procedimientos de seguridad más complejos.

{% endnote %}

Cuando tu compañía esté lista, nuestro equipo de Éxito del Cliente te ayudará a navegar a través de los requisitos que necesitan cumplirse y que pueden ayudarte a garantizar que tu compañía tenga un buen uso de casos para las consultas personalizadas.  

#### <a name="fact-5--data-variablesproductprodname_codeql--scans-the-whole-code-base-not-just-the-changes-made-in-a-pull-request"></a>Hecho 5: El {% data variables.product.prodname_codeql %} escaneo toda la base de código, no únicamente los cambios que se hacen en una solicitud de cambios.

Cuando el escaneo de código se ejecuta desde una solicitud de cambios, este incluirá a toda la base de código y no solo a los cambios que se realizan en la solicitud de cambios. Si bien esto podría verse como innecesario en algunas ocasiones, es un paso importante para garantizar que los cambios se revisaron contra todas las interacciones en la base de código.

## <a name="examples-of-successful--data-variablesproductprodname_gh_advanced_security--rollouts"></a>Ejemplos de implementaciones exitosas de la {% data variables.product.prodname_GH_advanced_security %}

Ahora que tienes un mejor entendimiento de cuáles son algunas de las claves para tener una implementación y despliegue exitosas de la GHAS, aquí tienes algunos ejemplos de cómo nuestros clientes realizaron su implementación exitosamente. Incluso si tu compañía se encuentra en un lugar diferente, {% data variables.product.prodname_dotcom %} puede ayudarte a crear una ruta personalizada que satisfaga las necesidades de tu implementación.

### <a name="example-rollout-for-a-mid-sized-healthcare-technology-company"></a>Implementación de ejemplo para una compañía de tecnología en el sector salud de tamaño medio  

Una compañía de tecnología en el sector salud de tamaño medio basada en San Francisco completó su proceso de implementación de la GHAS exitosamente. Si bien podrían no haber tenido una cantidad grande de repositorios que necesitan habilitarse, estas claves del éxito de la compañía incluyen tener un equipo alineado y bien organizado para la implementación, con un contacto clave bien establecido para trabajar con {% data variables.product.prodname_dotcom %} y para solucionar cualquier problema durante el proceso. Esto le permitió completar su implementación en dos meses.

Adicionalmente, el haber incluido a su equipo de desarrollo le permitió tener equipos que utilizaron el escaneo de código a nivel de las solicitudes de cambio después de haber completado su implementación.

### <a name="example-rollout-for-a-mid-sized-data-platform-company"></a>Implementación de ejemplo para una compañía mediana de plataforma de datos

Una compañía global de plataforma de datos tuvo un gran éxito con la GHAS hasta el momento. Completaron su implementación inicial y actualmente están progresando a través del resto de este proceso. Esta compañía tiene una buena madurez en su postura y herramientas de seguridad y está bien alineada como compañía. Esto les permite operar de forma muy autosuficiente y les permitió moverse rápida y eficazmente a lo largo de la implementación.

El alineamiento fuerte, operaciones eficientes y madurez de las herramientas de seguridad de esta compañía les permitió implementar la GHAS rápidamente y construir bases fuertes para el {% data variables.product.prodname_codeql %}. Desde su implementación, ahora pueden habilitar el {% data variables.product.prodname_codeql %} automáticamente a lo largo de los diversos repositorios.

Adicionalmente a su madurez técnica y de seguridad, otra clave crítica en el éxito de esta compañía es tener un propietario del proyecto y un punto de contacto único en su equipo para impulsarlo. No solo fue crucial contar con este contacto clave, sino que presentaron habilidades e ingenio increíbles que contribuyeron directamente con el éxito de la implementación.

## <a name="prerequisites-for-your-company-before-rolling-out-ghas"></a>Prerrequisitos para tu compañía antes de implementar la GHAS

Los {% data variables.product.prodname_professional_services %} pueden ayudarte a proporcionar apoyo adicional para ayudar a que tu compañía sintetice y entienda estos prerrequisitos y te ayudará a prepararte para el proceso de implementación de la GHAS.

 ### <a name="cicd-systems-and-process"></a>Sistemas y procesos de CI/CD

Si tu compañía aún no ha invertido o implementado en sistemas y procesos de integración y despliegue contínuos (IC/DC), te recomendamos tomar este paso en conjunto con la implementación de la GHAS. Esto podría representar un cambio importante para tu compañía: podemos trabajar contigo para proporcionar recomendaciones y orientación para implementar un sistema de IC/DC, así como proporcionar apoyo con cualquier capacitación que pudiera necesitarse.

### <a name="requirements-to-install--data-variablesproductprodname_gh_advanced_security-"></a>Requisitos para instalar la {% data variables.product.prodname_GH_advanced_security %}

Hay algunas rutas diferentes que pueden tomarse para tu instalación de la GHAS con base en las combinaciones de tecnologías que utilice tu compañía. Esta sección describe un desglose rápido de las diversas rutas que tu compañía podría necesitar tomar.

{% ifversion ghes %}

#### <a name="-data-variablesproductprodname_ghe_server-"></a>{% data variables.product.prodname_ghe_server %}

Es importante que estés utilizando una versión de {% data variables.product.prodname_ghe_server %} (GHES) que sea compatible con las necesidades de tu compañía.

Si estás utilizando una versión anterior de GHES (anterior a la 3.0) y te gustaría mejorarla, hay algunos requisitos que tendrás que cumplir antes de seguir con esta mejora. Para más información, consulte:
  - "[Actualización de {% data variables.product.prodname_ghe_server %}](/enterprise-server@2.22/admin/enterprise-management/updating-the-virtual-machine-and-physical-resources/upgrading-github-enterprise-server)"
  - "[Requisitos de actualización](/enterprise-server@2.20/admin/enterprise-management/upgrade-requirements)"

Si estás utilizando un sistema de IC/DC y quieres utilizar el {% data variables.product.prodname_code_scanning %}, asegúrate de haber descargado el {% data variables.product.prodname_codeql_cli %}. Para más información, vea "[Acerca del análisis de código de CodeQL en el sistema de CI](/code-security/code-scanning/using-codeql-code-scanning-with-your-existing-ci-system/about-codeql-code-scanning-in-your-ci-system)".

Si estás trabajando con los {% data variables.product.prodname_professional_services %} para tu implementación de la GHAS, prepárate para debatir estos elementos a detalle en tu junta de inicio.

{% endif %}

{% ifversion ghec %}

#### <a name="-data-variablesproductprodname_ghe_cloud-"></a>{% data variables.product.prodname_ghe_cloud %}

Si eres un cliente de {% data variables.product.prodname_ghe_cloud %} (GHEC), hay prerrequisitos que necesitarás cumplir dependiendo del plan de IC/DC que utilices.

Utilizar las {% data variables.product.prodname_actions %} para tu IC/DC:
- Para garantizar que el {% data variables.product.prodname_code_scanning %} puede integrarse y utilizarse de forma adecuada, debes tener un entendimiento básico de las {% data variables.product.prodname_actions %} antes de proceder con tu instalación.

Utilizar una herramienta de IC/DC de terceros:
- Para integrar el {% data variables.product.prodname_codeql_cli %}, debes tener un entendimiento básico del sistema de IC/DC, así como de *nix y Windows; particularmente, la forma en la que se ejecutan los comandos y cómo se señalan los éxitos/fallas. Para más información sobre cómo integrar una herramienta de terceros, vea "[Uso del análisis de código de CodeQL con el sistema de CI existente](/code-security/code-scanning/using-codeql-code-scanning-with-your-existing-ci-system)".

{% endif %}

## <a name="partnering-with-github-for-your-rollout"></a>Asociarte con GitHub para tu implementación

Conforme te preparas para la implementación de la GHAS, es importante considerar lo que se requerirá de tu compañía para que este proyecto tenga éxito. Nuestra implementación más exitosa de la GHAS depende de las responsabilidades compartidas entre GitHub y nuestros clientes a lo largo del proceso, con una identificación clara de los participantes del cliente al que pertenece el proyecto.

#### <a name="success-model-for-customer-and-github-responsibilities"></a>Modelo de éxito para las responsabilidades de GitHub y del cliente

**Responsabilidades del cliente**
- Completar los prerrequisitos de infraestructura y procesos
- Administrar la implementación y despliegue, incluyendo la planeación y ejecución
- Capacitación interna
- (Opcional) Colaborar con consultas de {% data variables.product.prodname_codeql %} en la comunidad de GitHub

**Responsabilidades de GitHub**

- Mantenimiento y mejoras para las características, tales como {% ifversion ghes %}{% data variables.product.prodname_ghe_server %}{% endif %}, {% data variables.product.prodname_actions %}, {% data variables.product.prodname_GH_advanced_security %}
- Proporcionar, mantener y entregar los siguientes servicios: Documentos de {% data variables.product.prodname_dotcom %}, Comunidad de {% data variables.product.prodname_dotcom %}, Soporte de {% data variables.product.prodname_dotcom %}

{% note %}

**Nota:** {% data variables.product.prodname_professional_services %} puede ayudar a complementar muchas de las responsabilidades del cliente. Para más información, vea "[Servicios y soporte técnico de GitHub](#github-services-and-support)".

{% endnote %}

## <a name="-data-variablesproductprodname_dotcom--services-and-support"></a>Soporte y servicios de {% data variables.product.prodname_dotcom %}

### <a name="-data-variablesproductprodname_dotcom--support"></a>Soporte de {% data variables.product.prodname_dotcom %}

Si se te presenta algún problema durante tu implementación, puedes buscar las soluciones en nuestra documentación más específica o contactar al Soporte de {% data variables.product.prodname_dotcom %}, el cual es un equipo de ingenieros técnicos especializados que pueden apoyarte cuando tengas problemas. Para más información, vea "[Soporte técnico de GitHub Enterprise](https://enterprise.github.com/support).

Además, también puede probar nuestros [ {% data variables.product.prodname_gcf %}](https://github.community/).

Si ha comprado un plan de soporte técnico Premium, puede enviar la incidencia en el [Portal de soporte técnico Premium](https://enterprise.github.com/support). Si no estás seguro de qué plan de soporte compraste, puedes contactar a tu representante de ventas o revisar los diferentes planes disponibles.

Para obtener más información sobre las opciones de plan de soporte Premium, consulta:
  - "[Soporte técnico Premium](https://github.com/premium-support)" {% ifversion ghec %}
  - "[Acerca del Soporte técnico Premium de GitHub para {% data variables.product.prodname_ghe_cloud %}](/github/working-with-github-support/about-github-premium-support-for-github-enterprise-cloud)"{% endif %}{% ifversion ghes %}
  - "[Acerca del Soporte técnico Premium de GitHub para {% data variables.product.prodname_ghe_server %}](/admin/enterprise-support/overview/about-github-premium-support-for-github-enterprise-server)"{% endif %}

### <a name="-data-variablesproductprodname_professional_services-"></a>{% data variables.product.prodname_professional_services %}

Nuestro equipo de {% data variables.product.prodname_professional_services_team %} puede asociarse contigo para que tengas una implementación y despliegue exitosos de la {% data variables.product.prodname_GH_advanced_security %}. Ofrecemos varias opciones para el tipo de orientación y apoyo que esperas necesitar para tu implementación. También tenemos capacitación habitual e intensiva disponible para ayudar a que tu compañía optimice el valor de la GHAS.

Si te gustaría trabajar con nuestro equipo de {% data variables.product.prodname_professional_services_team %} para tu implementación, te recomendamos que comiences a pensar en tu diseño e infraestructura de sistema, así como en la cantidad de repositorios que quieres configurar con GHAS, para comenzar con estas conversiones. Adicionalmente, comienza a pensar en las metas que te gustaría lograr con esta implementación.

La implementación es tan solo un paso en este camino de éxito impulsado por la seguridad, en donde aprenderás a utilizar la GHAS. Una vez que hayas completado tu implementación, habrá más que aprender con la implementación a lo largo de tu infraestructura y bases de código. Habla con tu representante de ventas para obtener más información sobre todas las opciones de {% data variables.product.prodname_professional_services_team %} disponibles.

Si inicialmente decidiste no adoptar nuestros servicios adicionales, pero te diste cuenta de que necesitas apoyo adicional para comenzar tu implementación, contacta a tu representante de ventas para debatir las opciones de servicio que pudieras requerir para apoyar tu implementación.
