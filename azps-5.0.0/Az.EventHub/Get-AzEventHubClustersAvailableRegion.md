---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 712e9274eabe27bbe5f4a8acce704926e1e895fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248695"
---
# <span data-ttu-id="1f975-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="1f975-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="1f975-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f975-102">SYNOPSIS</span></span>
<span data-ttu-id="1f975-103">Получение сведений об одном кластере Eventhub или списке кластеров в заданной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="1f975-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="1f975-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f975-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f975-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f975-105">DESCRIPTION</span></span>
<span data-ttu-id="1f975-106">Список командлетов Get-AzEventHubClustersAvailableRegion, в которых можно создать выделенные области.</span><span class="sxs-lookup"><span data-stu-id="1f975-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="1f975-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f975-107">EXAMPLES</span></span>

### <span data-ttu-id="1f975-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1f975-108">Example 1</span></span>
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

<span data-ttu-id="1f975-109">Возвращается список областей, где</span><span class="sxs-lookup"><span data-stu-id="1f975-109">List of regions is returned where</span></span>

## <span data-ttu-id="1f975-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f975-110">PARAMETERS</span></span>

### <span data-ttu-id="1f975-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f975-111">-DefaultProfile</span></span>
<span data-ttu-id="1f975-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f975-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f975-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f975-113">CommonParameters</span></span>
<span data-ttu-id="1f975-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f975-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f975-115">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f975-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f975-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f975-116">INPUTS</span></span>

### <span data-ttu-id="1f975-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="1f975-117">None</span></span>

## <span data-ttu-id="1f975-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f975-118">OUTPUTS</span></span>

### <span data-ttu-id="1f975-119">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. EventHub. EventHub. PSEventHubsAvailableCluster, Microsoft. Azure. PowerShell. командлеты, версия = 1.5.0.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="1f975-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1f975-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f975-120">NOTES</span></span>

## <span data-ttu-id="1f975-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f975-121">RELATED LINKS</span></span>
