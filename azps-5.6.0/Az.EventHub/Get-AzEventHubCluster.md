---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
ms.openlocfilehash: 22bbbb79f8662f1e1e70785489187e68e5b38813
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983128"
---
# <span data-ttu-id="bfd6b-101">Get-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="bfd6b-101">Get-AzEventHubCluster</span></span>

## <span data-ttu-id="bfd6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfd6b-102">SYNOPSIS</span></span>
<span data-ttu-id="bfd6b-103">Возвращает сведения об одном кластере концентраторов событий или список кластеров концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-103">Gets the details of a single Event Hub Cluster , or gets a list of Event Hub Clusters.</span></span>

## <span data-ttu-id="bfd6b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bfd6b-104">SYNTAX</span></span>

```
Get-AzEventHubCluster [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bfd6b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfd6b-105">DESCRIPTION</span></span>
<span data-ttu-id="bfd6b-106">Этот Get-AzEventHubCluster возвращает сведения о кластере концентратора событий или список всех кластеров концентраторов событий в данной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-106">The Get-AzEventHubCluster cmdlet returns either the details of an Event Hub Cluster, or a list of all Event Hub Clusters in given resource group.</span></span>
<span data-ttu-id="bfd6b-107">Если за предоставлено имя кластера, возвращаются сведения об одном кластере.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-107">If the cluster name is provided, the details of a single cluster are returned.</span></span>
<span data-ttu-id="bfd6b-108">Если имя кластера не указано, возвращается список всех кластеров в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-108">If an cluster name is not provided, a list of all clusters in the specified resource group is returned.</span></span>

## <span data-ttu-id="bfd6b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bfd6b-109">EXAMPLES</span></span>

### <span data-ttu-id="bfd6b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bfd6b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557

Id        : /subscriptions/326100e2-f69d-4268-8503-075374f62b6e/resourceGroups/RSG-Cluster27651/providers/Microsoft.Eve
            ntHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/10/2020 23:02:48
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag2, Tag4], [ClusterTag1, Tag3]}

```

<span data-ttu-id="bfd6b-111">Возвращает дедиадиалы кластера "Eventhub-Cluster-5557" из группы ресурсов "RSG-Cluster27651".</span><span class="sxs-lookup"><span data-stu-id="bfd6b-111">Returns the detials of cluster 'Eventhub-Cluster-5557' from the resource group 'RSG-Cluster27651'</span></span>

## <span data-ttu-id="bfd6b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfd6b-112">PARAMETERS</span></span>

### <span data-ttu-id="bfd6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfd6b-113">-DefaultProfile</span></span>
<span data-ttu-id="bfd6b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfd6b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bfd6b-115">-Name</span></span>
<span data-ttu-id="bfd6b-116">Название кластера</span><span class="sxs-lookup"><span data-stu-id="bfd6b-116">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfd6b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfd6b-117">-ResourceGroupName</span></span>
<span data-ttu-id="bfd6b-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="bfd6b-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfd6b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfd6b-119">CommonParameters</span></span>
<span data-ttu-id="bfd6b-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfd6b-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bfd6b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfd6b-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bfd6b-122">INPUTS</span></span>

### <span data-ttu-id="bfd6b-123">System.String</span><span class="sxs-lookup"><span data-stu-id="bfd6b-123">System.String</span></span>

## <span data-ttu-id="bfd6b-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bfd6b-124">OUTPUTS</span></span>

### <span data-ttu-id="bfd6b-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="bfd6b-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="bfd6b-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bfd6b-126">NOTES</span></span>

## <span data-ttu-id="bfd6b-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bfd6b-127">RELATED LINKS</span></span>
