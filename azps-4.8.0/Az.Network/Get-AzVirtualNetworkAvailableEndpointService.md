---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 79517dc748a0599fca588e18d18a9d1e41f5e7fa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235509"
---
# <span data-ttu-id="7973b-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="7973b-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="7973b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7973b-102">SYNOPSIS</span></span>
<span data-ttu-id="7973b-103">Список доступных служб конечных точек для местоположения.</span><span class="sxs-lookup"><span data-stu-id="7973b-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="7973b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7973b-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7973b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7973b-105">DESCRIPTION</span></span>
<span data-ttu-id="7973b-106">Get-AzVirtualNetworkAvailableEndpointService список доступных служб конечных точек в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="7973b-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="7973b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7973b-107">EXAMPLES</span></span>

### <span data-ttu-id="7973b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7973b-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="7973b-109">Получает доступные службы конечных точек в westus области.</span><span class="sxs-lookup"><span data-stu-id="7973b-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="7973b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7973b-110">PARAMETERS</span></span>

### <span data-ttu-id="7973b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7973b-111">-DefaultProfile</span></span>
<span data-ttu-id="7973b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7973b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7973b-113">-Location</span><span class="sxs-lookup"><span data-stu-id="7973b-113">-Location</span></span>
<span data-ttu-id="7973b-114">Расположение, из которого нужно извлечь службы конечной точки.</span><span class="sxs-lookup"><span data-stu-id="7973b-114">The location to retrieve the endpoint services from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7973b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7973b-115">CommonParameters</span></span>
<span data-ttu-id="7973b-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7973b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7973b-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7973b-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7973b-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7973b-118">INPUTS</span></span>

### <span data-ttu-id="7973b-119">System. String</span><span class="sxs-lookup"><span data-stu-id="7973b-119">System.String</span></span>

## <span data-ttu-id="7973b-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7973b-120">OUTPUTS</span></span>

### <span data-ttu-id="7973b-121">Microsoft. Azure. Commands. Network. Models. PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="7973b-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="7973b-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="7973b-122">NOTES</span></span>

## <span data-ttu-id="7973b-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7973b-123">RELATED LINKS</span></span>
