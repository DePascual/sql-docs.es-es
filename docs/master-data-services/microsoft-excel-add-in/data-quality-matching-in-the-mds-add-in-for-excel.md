---
title: Coincidencia de calidad de datos en el Complemento MDS para Excel | Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: mds
ms.component: microsoft-excel-add-in
ms.reviewer: ''
ms.suite: sql
ms.technology:
- master-data-services
ms.tgt_pltfrm: ''
ms.topic: conceptual
ms.assetid: be78d051-0d56-46d3-bb89-327e218dadd6
caps.latest.revision: 9
author: leolimsft
ms.author: lle
manager: craigg
ms.openlocfilehash: b6e7f3b94682397465de4ddc70aedb78d8d92f08
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/03/2018
---
# <a name="data-quality-matching-in-the-mds-add-in-for-excel"></a>Coincidencia de calidad de datos en el Complemento MDS para Excel

[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md-winonly](../../includes/appliesto-ss-xxxx-xxxx-xxx-md-winonly.md)]

  Con el tiempo, le interesará agregar más datos al repositorio MDS. Antes de agregar datos, puede ser útil comparar los nuevos datos con los datos que ya se administran en MDS, para asegurarse de que no se agregan datos duplicados o imprecisos.  
  
 MDS [!INCLUDE[ssMDSXLS](../../includes/ssmdsxls-md.md)] usa la característica Data Quality Services (DQS) de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] para que coincidan los datos similares. Si usa la funcionalidad de coincidencia en el complemento, los registros similares se agrupan y se muestra una puntuación que representa la precisión del resultado. Para obtener más información acerca de la funcionalidad de coincidencia que proporciona DQS, vea [Data Matching](../../data-quality-services/data-matching.md).  
  
## <a name="workflow-for-data-quality-matching"></a>Flujo de trabajo de la coincidencia de calidad de datos  
 Al usar DQS con MDS [!INCLUDE[ssMDSXLS](../../includes/ssmdsxls-md.md)], use el siguiente flujo de trabajo:  
  
1.  Recupere una lista de los datos administrados con MDS y combínelos con una lista que no se administre en MDS. Para obtener más información, consulte [Combinar datos &#40;Complemento MDS para Excel&#41;](../../master-data-services/microsoft-excel-add-in/combine-data-mds-add-in-for-excel.md).  
  
2.  Use el conocimiento de DQS para comparar los datos de la lista combinada. Para obtener más información, consulte [Coincidir datos similares &#40;Complemento MDS para Excel&#41;](../../master-data-services/microsoft-excel-add-in/match-similar-data-mds-add-in-for-excel.md).  
  
3.  Para ver más detalles sobre las similitudes encontradas por DQS, muestre las columnas de detalles.  
  
4.  Pase a los resultados y determine qué datos se deben agregar al repositorio MDS y qué datos se duplican.  
  
5.  Publique los datos nuevos y/o actualizados en el repositorio MDS.  
  
## <a name="knowledge-bases"></a>Bases de conocimiento  
 Los resultados de la coincidencia que se proporcionan en el complemento se basan en una base de conocimiento DQS.  
  
-   La base de conocimiento predeterminada (DQS Data) se crea al instalar DQS. Si elige utilizar la base de conocimiento predeterminada (sin agregar una directiva correspondiente a la base de conocimiento predeterminada en Data Quality Client), debe asignar columnas en la hoja de cálculo en los dominios de la base de conocimiento y asignar después un valor de ponderación a los dominios que elija.  
  
-   Puede utilizar Data Quality Client para crear una base de conocimiento nueva con una directiva correspondiente o agregar una directiva correspondiente a la base de conocimiento predeterminada. En este caso, los valores de ponderación se determinan mediante la directiva de coincidencia que creó previamente y solo tiene que asignar las columnas a los dominios. Para más información, consulte [Create a Matching Policy](../../data-quality-services/create-a-matching-policy.md).  
  
 Para obtener más información acerca de las bases de conocimiento, vea [DQS Knowledge Bases and Domains](../../data-quality-services/dqs-knowledge-bases-and-domains.md).  
  
## <a name="related-tasks"></a>Related Tasks  
  
|Descripción de la tarea|Tema|  
|----------------------|-----------|  
|Combinar los datos externos con los datos administrados con MDS en preparación para compararlos.|[Combinar datos &#40;Complemento MDS para Excel&#41;](../../master-data-services/microsoft-excel-add-in/combine-data-mds-add-in-for-excel.md)|  
|Use el conocimiento de DQS para buscar similitudes en los datos.|[Coincidir datos similares &#40;Complemento MDS para Excel&#41;](../../master-data-services/microsoft-excel-add-in/match-similar-data-mds-add-in-for-excel.md)|  
  
## <a name="related-content"></a>Contenido relacionado  
  
-   [Información general: Importación de datos desde Excel &#40;complemento MDS para Excel&#41;](../../master-data-services/microsoft-excel-add-in/overview-importing-data-from-excel-mds-add-in-for-excel.md)  
  
-   [Data Matching](../../data-quality-services/data-matching.md)  
  
  
