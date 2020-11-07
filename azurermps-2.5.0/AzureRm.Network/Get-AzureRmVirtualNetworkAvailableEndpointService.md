---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkavailableendpointservice
schema: 2.0.0
ms.openlocfilehash: ed33d1a683e10e0e39d0b722dec92b7f7ba11254
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913613"
---
# <span data-ttu-id="17e97-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="17e97-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="17e97-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="17e97-102">SYNOPSIS</span></span>
<span data-ttu-id="17e97-103">Список доступных служб конечных точек для местоположения.</span><span class="sxs-lookup"><span data-stu-id="17e97-103">Lists available endpoint services for location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17e97-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="17e97-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17e97-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17e97-105">DESCRIPTION</span></span>
<span data-ttu-id="17e97-106">Get-AzureRmVirtualNetworkAvailableEndpointService список доступных служб конечных точек в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="17e97-106">Get-AzureRmVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="17e97-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="17e97-107">EXAMPLES</span></span>

### <span data-ttu-id="17e97-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="17e97-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="17e97-109">Получает доступные службы конечных точек в westus области.</span><span class="sxs-lookup"><span data-stu-id="17e97-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="17e97-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="17e97-110">PARAMETERS</span></span>

### <span data-ttu-id="17e97-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17e97-111">-DefaultProfile</span></span>
<span data-ttu-id="17e97-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="17e97-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17e97-113">-Location</span><span class="sxs-lookup"><span data-stu-id="17e97-113">-Location</span></span>
<span data-ttu-id="17e97-114">Расположение, из которого нужно извлечь службы конечной точки.</span><span class="sxs-lookup"><span data-stu-id="17e97-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="17e97-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17e97-115">CommonParameters</span></span>
<span data-ttu-id="17e97-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="17e97-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17e97-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17e97-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17e97-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="17e97-118">INPUTS</span></span>

### <span data-ttu-id="17e97-119">System. String</span><span class="sxs-lookup"><span data-stu-id="17e97-119">System.String</span></span>

## <span data-ttu-id="17e97-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="17e97-120">OUTPUTS</span></span>

### <span data-ttu-id="17e97-121">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSEndpointServiceResult, Microsoft. Azure. Commands. Network, Version = 4.2.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="17e97-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult, Microsoft.Azure.Commands.Network, Version=4.2.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="17e97-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="17e97-122">NOTES</span></span>

## <span data-ttu-id="17e97-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17e97-123">RELATED LINKS</span></span>

