---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 38c7bfe31faa8b4f167a14ede75f92055919ba55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569984"
---
# <span data-ttu-id="273e8-101">Get-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="273e8-101">Get-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="273e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="273e8-102">SYNOPSIS</span></span>
<span data-ttu-id="273e8-103">Получает состояние установки Operations Management Suite (OMS) в кластере.</span><span class="sxs-lookup"><span data-stu-id="273e8-103">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="273e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="273e8-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="273e8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="273e8-105">DESCRIPTION</span></span>
<span data-ttu-id="273e8-106">Командлет **Get-AzureRmHDInsightOperationsManagementSuite** получает состояние установки OMS в кластере HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="273e8-106">The **Get-AzureRmHDInsightOperationsManagementSuite** cmdlet gets the status of OMS installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="273e8-107">Если включена поддержка OMS, она также будет возвращать идентификатор рабочей области OMS.</span><span class="sxs-lookup"><span data-stu-id="273e8-107">If OMS is enabled then it will also return the OMS workspace id.</span></span>

## <span data-ttu-id="273e8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="273e8-108">EXAMPLES</span></span>

### <span data-ttu-id="273e8-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="273e8-109">Example 1</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="273e8-110">В кластере включена поддержка Operations Management Suite (OMS), так как свойство ClusterMonitoringEnabled имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="273e8-110">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="273e8-111">Идентификатор рабочей области OMS, в которой находятся журналы, 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="273e8-111">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="273e8-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="273e8-112">Example 2</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="273e8-113">В кластере включена поддержка Operations Management Suite (OMS), так как свойство ClusterMonitoringEnabled имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="273e8-113">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="273e8-114">Идентификатор рабочей области OMS, в которой находятся журналы, 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="273e8-114">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="273e8-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="273e8-115">Example 3</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="273e8-116">Набор Operations Management Suite (OMS) в кластере отключен, так как свойство ClusterMonitoringEnabled имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="273e8-116">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="273e8-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="273e8-117">Example 4</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="273e8-118">Набор Operations Management Suite (OMS) в кластере отключен, так как свойство ClusterMonitoringEnabled имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="273e8-118">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="273e8-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="273e8-119">PARAMETERS</span></span>

### <span data-ttu-id="273e8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="273e8-120">-DefaultProfile</span></span>
<span data-ttu-id="273e8-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="273e8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273e8-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="273e8-122">-Name</span></span>
<span data-ttu-id="273e8-123">Имя кластера, которое получает состояние набора Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="273e8-123">The name of the cluster to get the status of Operations Management Suite(OMS).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="273e8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="273e8-124">-ResourceGroupName</span></span>
<span data-ttu-id="273e8-125">Группа ресурсов кластера.</span><span class="sxs-lookup"><span data-stu-id="273e8-125">The resource group of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="273e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="273e8-126">CommonParameters</span></span>
<span data-ttu-id="273e8-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="273e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="273e8-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="273e8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="273e8-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="273e8-129">INPUTS</span></span>

### <span data-ttu-id="273e8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="273e8-130">System.String</span></span>

## <span data-ttu-id="273e8-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="273e8-131">OUTPUTS</span></span>

### <span data-ttu-id="273e8-132">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="273e8-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightOMS</span></span>

## <span data-ttu-id="273e8-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="273e8-133">NOTES</span></span>

## <span data-ttu-id="273e8-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="273e8-134">RELATED LINKS</span></span>

