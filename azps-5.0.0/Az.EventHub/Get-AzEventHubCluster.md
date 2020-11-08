---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
ms.openlocfilehash: 4e2657d6a4af26b96a2e7a97a56b735838610005
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248698"
---
# <span data-ttu-id="34b3d-101">Get-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="34b3d-101">Get-AzEventHubCluster</span></span>

## <span data-ttu-id="34b3d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="34b3d-103">Получает сведения об одном кластере центра событий или получает список кластеров концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="34b3d-103">Gets the details of a single Event Hub Cluster , or gets a list of Event Hub Clusters.</span></span>

## <span data-ttu-id="34b3d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34b3d-104">SYNTAX</span></span>

```
Get-AzEventHubCluster [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34b3d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34b3d-105">DESCRIPTION</span></span>
<span data-ttu-id="34b3d-106">Командлет Get-AzEventHubCluster возвращает либо сведения о кластере центра событий, либо список всех кластеров концентраторов событий в данной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="34b3d-106">The Get-AzEventHubCluster cmdlet returns either the details of an Event Hub Cluster, or a list of all Event Hub Clusters in given resource group.</span></span>
<span data-ttu-id="34b3d-107">Если указано имя кластера, возвращаются сведения об одном кластере.</span><span class="sxs-lookup"><span data-stu-id="34b3d-107">If the cluster name is provided, the details of a single cluster are returned.</span></span>
<span data-ttu-id="34b3d-108">Если имя кластера не указано, возвращается список всех кластеров в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="34b3d-108">If an cluster name is not provided, a list of all clusters in the specified resource group is returned.</span></span>

## <span data-ttu-id="34b3d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34b3d-109">EXAMPLES</span></span>

### <span data-ttu-id="34b3d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="34b3d-110">Example 1</span></span>
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

<span data-ttu-id="34b3d-111">Возвращает detials кластера "Eventhub-Cluster-5557" из группы ресурсов "RSG-Cluster27651"</span><span class="sxs-lookup"><span data-stu-id="34b3d-111">Returns the detials of cluster 'Eventhub-Cluster-5557' from the resource group 'RSG-Cluster27651'</span></span>

## <span data-ttu-id="34b3d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34b3d-112">PARAMETERS</span></span>

### <span data-ttu-id="34b3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34b3d-113">-DefaultProfile</span></span>
<span data-ttu-id="34b3d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34b3d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34b3d-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="34b3d-115">-Name</span></span>
<span data-ttu-id="34b3d-116">Имя кластера</span><span class="sxs-lookup"><span data-stu-id="34b3d-116">Cluster Name</span></span>

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

### <span data-ttu-id="34b3d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34b3d-117">-ResourceGroupName</span></span>
<span data-ttu-id="34b3d-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="34b3d-118">Resource Group Name</span></span>

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

### <span data-ttu-id="34b3d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34b3d-119">CommonParameters</span></span>
<span data-ttu-id="34b3d-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34b3d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34b3d-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34b3d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34b3d-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34b3d-122">INPUTS</span></span>

### <span data-ttu-id="34b3d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="34b3d-123">System.String</span></span>

## <span data-ttu-id="34b3d-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34b3d-124">OUTPUTS</span></span>

### <span data-ttu-id="34b3d-125">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="34b3d-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="34b3d-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="34b3d-126">NOTES</span></span>

## <span data-ttu-id="34b3d-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34b3d-127">RELATED LINKS</span></span>
