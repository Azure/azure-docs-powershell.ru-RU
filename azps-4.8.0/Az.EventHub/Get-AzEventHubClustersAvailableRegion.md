---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 712e9274eabe27bbe5f4a8acce704926e1e895fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244534"
---
# <span data-ttu-id="c8a3a-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="c8a3a-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="c8a3a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8a3a-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a3a-103">Получение сведений об одном кластере Eventhub или списке кластеров в заданной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="c8a3a-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="c8a3a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8a3a-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8a3a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8a3a-105">DESCRIPTION</span></span>
<span data-ttu-id="c8a3a-106">Список командлетов Get-AzEventHubClustersAvailableRegion, в которых можно создать выделенные области.</span><span class="sxs-lookup"><span data-stu-id="c8a3a-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="c8a3a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8a3a-107">EXAMPLES</span></span>

### <span data-ttu-id="c8a3a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c8a3a-108">Example 1</span></span>
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

<span data-ttu-id="c8a3a-109">Возвращается список областей, где</span><span class="sxs-lookup"><span data-stu-id="c8a3a-109">List of regions is returned where</span></span>

## <span data-ttu-id="c8a3a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8a3a-110">PARAMETERS</span></span>

### <span data-ttu-id="c8a3a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a3a-111">-DefaultProfile</span></span>
<span data-ttu-id="c8a3a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a3a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8a3a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a3a-113">CommonParameters</span></span>
<span data-ttu-id="c8a3a-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8a3a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a3a-115">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8a3a-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a3a-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8a3a-116">INPUTS</span></span>

### <span data-ttu-id="c8a3a-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="c8a3a-117">None</span></span>

## <span data-ttu-id="c8a3a-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8a3a-118">OUTPUTS</span></span>

### <span data-ttu-id="c8a3a-119">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. EventHub. EventHub. PSEventHubsAvailableCluster, Microsoft. Azure. PowerShell. командлеты, версия = 1.5.0.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="c8a3a-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c8a3a-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8a3a-120">NOTES</span></span>

## <span data-ttu-id="c8a3a-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8a3a-121">RELATED LINKS</span></span>
