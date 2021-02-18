---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 712e9274eabe27bbe5f4a8acce704926e1e895fe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230409"
---
# <span data-ttu-id="42ab4-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="42ab4-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="42ab4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42ab4-102">SYNOPSIS</span></span>
<span data-ttu-id="42ab4-103">Подробные сведения о кластере Естройка или списке кластеров в данной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="42ab4-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="42ab4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="42ab4-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42ab4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42ab4-105">DESCRIPTION</span></span>
<span data-ttu-id="42ab4-106">Список Get-AzEventHubClustersAvailableRegion, в которых можно создать выделенные области.</span><span class="sxs-lookup"><span data-stu-id="42ab4-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="42ab4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="42ab4-107">EXAMPLES</span></span>

### <span data-ttu-id="42ab4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="42ab4-108">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubClustersAvailableRegion

Location
--------
northcentralus
westeurope
uksouth
westcentralus
australiasoutheast
ukwest
brazilsouth
centralus
australiaeast
eastus
southcentralus
japaneast
northeurope
eastus2
southeastasia
eastasia
westus
westus2
```

<span data-ttu-id="42ab4-109">Возвращается список регионов, где</span><span class="sxs-lookup"><span data-stu-id="42ab4-109">List of regions is returned where</span></span>

## <span data-ttu-id="42ab4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42ab4-110">PARAMETERS</span></span>

### <span data-ttu-id="42ab4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42ab4-111">-DefaultProfile</span></span>
<span data-ttu-id="42ab4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42ab4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42ab4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ab4-113">CommonParameters</span></span>
<span data-ttu-id="42ab4-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42ab4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ab4-115">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42ab4-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ab4-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="42ab4-116">INPUTS</span></span>

### <span data-ttu-id="42ab4-117">Нет</span><span class="sxs-lookup"><span data-stu-id="42ab4-117">None</span></span>

## <span data-ttu-id="42ab4-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="42ab4-118">OUTPUTS</span></span>

### <span data-ttu-id="42ab4-119">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="42ab4-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="42ab4-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="42ab4-120">NOTES</span></span>

## <span data-ttu-id="42ab4-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42ab4-121">RELATED LINKS</span></span>
