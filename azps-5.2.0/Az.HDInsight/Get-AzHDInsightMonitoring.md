---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: 2d91c96d20797988a7def2d11d633f36b08cb8cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396612"
---
# <span data-ttu-id="0e4b0-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="0e4b0-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="0e4b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e4b0-102">SYNOPSIS</span></span>
<span data-ttu-id="0e4b0-103">Состояние мониторинга установки на кластере.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="0e4b0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0e4b0-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e4b0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e4b0-105">DESCRIPTION</span></span>
<span data-ttu-id="0e4b0-106">Для **этого можно получить** состояние мониторинга установки в кластере Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="0e4b0-107">Если мониторинг включен, возвращается также id рабочей области аналитики журнала.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="0e4b0-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0e4b0-108">EXAMPLES</span></span>

### <span data-ttu-id="0e4b0-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0e4b0-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="0e4b0-110">Мониторинг на кластере включен, поскольку свойство ClusterMonitoringEnabled имеет истинное свойство.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="0e4b0-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="0e4b0-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="0e4b0-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0e4b0-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="0e4b0-113">Мониторинг на кластере включен, поскольку свойство ClusterMonitoringEnabled имеет истинное свойство.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="0e4b0-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="0e4b0-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="0e4b0-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0e4b0-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="0e4b0-116">Мониторинг на кластере отключен, поскольку свойство ClusterMonitoringEnabled ложно.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="0e4b0-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="0e4b0-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="0e4b0-118">Мониторинг на кластере отключен, поскольку свойство ClusterMonitoringEnabled ложно.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="0e4b0-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e4b0-119">PARAMETERS</span></span>

### <span data-ttu-id="0e4b0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e4b0-120">-DefaultProfile</span></span>
<span data-ttu-id="0e4b0-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0e4b0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e4b0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0e4b0-122">-Name</span></span>
<span data-ttu-id="0e4b0-123">Название кластера для отслеживания состояния.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-123">The name of the cluster to get the status of monitoring.</span></span>

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

### <span data-ttu-id="0e4b0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e4b0-124">-ResourceGroupName</span></span>
<span data-ttu-id="0e4b0-125">Группа ресурсов в кластере.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-125">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="0e4b0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e4b0-126">CommonParameters</span></span>
<span data-ttu-id="0e4b0-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e4b0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e4b0-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e4b0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e4b0-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e4b0-129">INPUTS</span></span>

### <span data-ttu-id="0e4b0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0e4b0-130">System.String</span></span>

## <span data-ttu-id="0e4b0-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0e4b0-131">OUTPUTS</span></span>

### <span data-ttu-id="0e4b0-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="0e4b0-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="0e4b0-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0e4b0-133">NOTES</span></span>

## <span data-ttu-id="0e4b0-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e4b0-134">RELATED LINKS</span></span>
