---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: 2d91c96d20797988a7def2d11d633f36b08cb8cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93913014"
---
# <span data-ttu-id="70a4e-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="70a4e-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="70a4e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="70a4e-102">SYNOPSIS</span></span>
<span data-ttu-id="70a4e-103">Получает состояние наблюдения за установкой на кластере.</span><span class="sxs-lookup"><span data-stu-id="70a4e-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="70a4e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="70a4e-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70a4e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70a4e-105">DESCRIPTION</span></span>
<span data-ttu-id="70a4e-106">Командлет **Get-AzHDInsightMonitoring** получает состояние установки мониторинга в кластере HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="70a4e-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="70a4e-107">Если включено наблюдение, оно также возвращает идентификатор рабочей области для анализа журналов.</span><span class="sxs-lookup"><span data-stu-id="70a4e-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="70a4e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="70a4e-108">EXAMPLES</span></span>

### <span data-ttu-id="70a4e-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="70a4e-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="70a4e-110">В кластере включена поддержка мониторинга, так как свойство ClusterMonitoringEnabled имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="70a4e-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="70a4e-111">Идентификатор рабочей области мониторинга, в которой находятся журналы, 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="70a4e-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="70a4e-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="70a4e-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="70a4e-113">В кластере включена поддержка мониторинга, так как свойство ClusterMonitoringEnabled имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="70a4e-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="70a4e-114">Идентификатор рабочей области мониторинга, в которой находятся журналы, 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="70a4e-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="70a4e-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="70a4e-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="70a4e-116">Наблюдение отключено в кластере, так как свойство ClusterMonitoringEnabled имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="70a4e-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="70a4e-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="70a4e-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="70a4e-118">Наблюдение отключено в кластере, так как свойство ClusterMonitoringEnabled имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="70a4e-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="70a4e-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="70a4e-119">PARAMETERS</span></span>

### <span data-ttu-id="70a4e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70a4e-120">-DefaultProfile</span></span>
<span data-ttu-id="70a4e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="70a4e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a4e-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="70a4e-122">-Name</span></span>
<span data-ttu-id="70a4e-123">Имя кластера, для которого нужно получить состояние наблюдения.</span><span class="sxs-lookup"><span data-stu-id="70a4e-123">The name of the cluster to get the status of monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a4e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70a4e-124">-ResourceGroupName</span></span>
<span data-ttu-id="70a4e-125">Группа ресурсов кластера.</span><span class="sxs-lookup"><span data-stu-id="70a4e-125">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a4e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70a4e-126">CommonParameters</span></span>
<span data-ttu-id="70a4e-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="70a4e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70a4e-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70a4e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70a4e-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="70a4e-129">INPUTS</span></span>

### <span data-ttu-id="70a4e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="70a4e-130">System.String</span></span>

## <span data-ttu-id="70a4e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="70a4e-131">OUTPUTS</span></span>

### <span data-ttu-id="70a4e-132">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="70a4e-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="70a4e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="70a4e-133">NOTES</span></span>

## <span data-ttu-id="70a4e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70a4e-134">RELATED LINKS</span></span>
