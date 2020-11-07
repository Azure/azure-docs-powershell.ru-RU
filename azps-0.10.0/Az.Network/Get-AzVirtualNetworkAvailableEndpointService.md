---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: bcd4ba14a14fdacdcdaa0ea85ec8059d2639bdc6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909873"
---
# <span data-ttu-id="44669-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="44669-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="44669-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44669-102">SYNOPSIS</span></span>
<span data-ttu-id="44669-103">Список доступных служб конечных точек для местоположения.</span><span class="sxs-lookup"><span data-stu-id="44669-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="44669-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44669-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44669-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44669-105">DESCRIPTION</span></span>
<span data-ttu-id="44669-106">Get-AzVirtualNetworkAvailableEndpointService список доступных служб конечных точек в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="44669-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="44669-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44669-107">EXAMPLES</span></span>

### <span data-ttu-id="44669-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="44669-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="44669-109">Получает доступные службы конечных точек в westus области.</span><span class="sxs-lookup"><span data-stu-id="44669-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="44669-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44669-110">PARAMETERS</span></span>

### <span data-ttu-id="44669-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44669-111">-DefaultProfile</span></span>
<span data-ttu-id="44669-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44669-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44669-113">-Location</span><span class="sxs-lookup"><span data-stu-id="44669-113">-Location</span></span>
<span data-ttu-id="44669-114">Расположение, из которого нужно извлечь службы конечной точки.</span><span class="sxs-lookup"><span data-stu-id="44669-114">The location to retrieve the endpoint services from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44669-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44669-115">CommonParameters</span></span>
<span data-ttu-id="44669-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44669-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44669-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44669-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44669-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44669-118">INPUTS</span></span>

### <span data-ttu-id="44669-119">System. String</span><span class="sxs-lookup"><span data-stu-id="44669-119">System.String</span></span>

## <span data-ttu-id="44669-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44669-120">OUTPUTS</span></span>

### <span data-ttu-id="44669-121">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSEndpointServiceResult, Microsoft. Azure. Commands. Network, Version = 4.2.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="44669-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult, Microsoft.Azure.Commands.Network, Version=4.2.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="44669-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="44669-122">NOTES</span></span>

## <span data-ttu-id="44669-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44669-123">RELATED LINKS</span></span>

