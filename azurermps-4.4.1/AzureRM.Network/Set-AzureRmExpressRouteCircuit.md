---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: b223cf62b536479b4c39d5852974698f2f38becf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734260"
---
# <span data-ttu-id="6d5c4-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6d5c4-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="6d5c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d5c4-102">SYNOPSIS</span></span>
<span data-ttu-id="6d5c4-103">Изменение канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6d5c4-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d5c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d5c4-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d5c4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d5c4-105">DESCRIPTION</span></span>
<span data-ttu-id="6d5c4-106">Командлет **Set-AzureRmExpressRouteCircuit** сохраняет модифицированную цепь ExpressRoute в Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c4-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="6d5c4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d5c4-107">EXAMPLES</span></span>

### <span data-ttu-id="6d5c4-108">Пример 1: изменение ServiceKeyа в канале ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="6d5c4-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="6d5c4-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d5c4-109">PARAMETERS</span></span>

### <span data-ttu-id="6d5c4-110">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6d5c4-110">-ExpressRouteCircuit</span></span>
<span data-ttu-id="6d5c4-111">Указывает объект **ExpressRouteCircuit** , который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6d5c4-111">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5c4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d5c4-112">-DefaultProfile</span></span>
<span data-ttu-id="6d5c4-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d5c4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d5c4-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d5c4-114">CommonParameters</span></span>
<span data-ttu-id="6d5c4-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d5c4-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d5c4-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d5c4-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d5c4-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d5c4-117">INPUTS</span></span>

### <span data-ttu-id="6d5c4-118">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6d5c4-118">PSExpressRouteCircuit</span></span>
<span data-ttu-id="6d5c4-119">Параметр "ExpressRouteCircuit" принимает значение типа "PSExpressRouteCircuit" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="6d5c4-119">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="6d5c4-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d5c4-120">OUTPUTS</span></span>

### <span data-ttu-id="6d5c4-121">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6d5c4-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="6d5c4-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d5c4-122">NOTES</span></span>

## <span data-ttu-id="6d5c4-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d5c4-123">RELATED LINKS</span></span>

[<span data-ttu-id="6d5c4-124">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6d5c4-124">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="6d5c4-125">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6d5c4-125">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="6d5c4-126">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6d5c4-126">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="6d5c4-127">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6d5c4-127">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)
