---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 7499c96ec887673faaf93cf2901e4705b63604b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570208"
---
# <span data-ttu-id="88c7d-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="88c7d-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="88c7d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88c7d-102">SYNOPSIS</span></span>
<span data-ttu-id="88c7d-103">Список доступных служб конечных точек для местоположения.</span><span class="sxs-lookup"><span data-stu-id="88c7d-103">Lists available endpoint services for location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88c7d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88c7d-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88c7d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88c7d-105">DESCRIPTION</span></span>
<span data-ttu-id="88c7d-106">Get-AzureRmVirtualNetworkAvailableEndpointService список доступных служб конечных точек в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="88c7d-106">Get-AzureRmVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="88c7d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88c7d-107">EXAMPLES</span></span>

### <span data-ttu-id="88c7d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="88c7d-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="88c7d-109">Получает доступные службы конечных точек в westus области.</span><span class="sxs-lookup"><span data-stu-id="88c7d-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="88c7d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88c7d-110">PARAMETERS</span></span>

### <span data-ttu-id="88c7d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88c7d-111">-DefaultProfile</span></span>
<span data-ttu-id="88c7d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88c7d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88c7d-113">-Location</span><span class="sxs-lookup"><span data-stu-id="88c7d-113">-Location</span></span>
<span data-ttu-id="88c7d-114">Расположение, из которого нужно извлечь службы конечной точки.</span><span class="sxs-lookup"><span data-stu-id="88c7d-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="88c7d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88c7d-115">CommonParameters</span></span>
<span data-ttu-id="88c7d-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88c7d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88c7d-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88c7d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88c7d-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88c7d-118">INPUTS</span></span>

### <span data-ttu-id="88c7d-119">System. String</span><span class="sxs-lookup"><span data-stu-id="88c7d-119">System.String</span></span>

## <span data-ttu-id="88c7d-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88c7d-120">OUTPUTS</span></span>

### <span data-ttu-id="88c7d-121">Microsoft. Azure. Commands. Network. Models. PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="88c7d-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="88c7d-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="88c7d-122">NOTES</span></span>

## <span data-ttu-id="88c7d-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88c7d-123">RELATED LINKS</span></span>
