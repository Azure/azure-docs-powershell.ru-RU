---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 4d9442ba87ba46704aaa93b31f41f111519c980b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568887"
---
# <span data-ttu-id="7c155-101">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7c155-101">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="7c155-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c155-102">SYNOPSIS</span></span>
<span data-ttu-id="7c155-103">Получает конфигурацию подключения к каналу ExpressRoute, связанную с частным одноранговым подключением ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="7c155-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c155-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c155-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c155-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c155-105">DESCRIPTION</span></span>
<span data-ttu-id="7c155-106">Командлет **Get-AzureRmExpressRouteCircuitConnectionConfig** извлекает конфигурацию подключения к каналу, связанного с частным одноранговым соединением для канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7c155-106">The **Get-AzureRmExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="7c155-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c155-107">EXAMPLES</span></span>

### <span data-ttu-id="7c155-108">Пример 1: отображение конфигурации подключения к каналу для канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="7c155-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="7c155-109">Пример 2: получение ресурса подключения к каналу, связанного с цепью ExpressRoute с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="7c155-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="7c155-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c155-110">PARAMETERS</span></span>

### <span data-ttu-id="7c155-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c155-111">-DefaultProfile</span></span>
<span data-ttu-id="7c155-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c155-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c155-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7c155-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="7c155-114">Объект цепи ExpressRoute, который содержит конфигурацию подключения к каналу.</span><span class="sxs-lookup"><span data-stu-id="7c155-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c155-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7c155-115">-Name</span></span>
<span data-ttu-id="7c155-116">Имя конфигурации подключения к каналу, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="7c155-116">The name of the circuit connection configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c155-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c155-117">CommonParameters</span></span>
<span data-ttu-id="7c155-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c155-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c155-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c155-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c155-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c155-120">INPUTS</span></span>

### <span data-ttu-id="7c155-121">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7c155-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="7c155-122">Параметры: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7c155-122">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="7c155-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c155-123">OUTPUTS</span></span>

### <span data-ttu-id="7c155-124">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="7c155-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="7c155-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c155-125">NOTES</span></span>

## <span data-ttu-id="7c155-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c155-126">RELATED LINKS</span></span>

[<span data-ttu-id="7c155-127">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7c155-127">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="7c155-128">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7c155-128">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7c155-129">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7c155-129">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7c155-130">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7c155-130">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7c155-131">New-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7c155-131">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)
