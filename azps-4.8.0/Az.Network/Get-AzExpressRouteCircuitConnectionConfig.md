---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: f4aabb68fd1f508651406d7ccf7be91ff646d46c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235051"
---
# <span data-ttu-id="9c17c-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="9c17c-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="9c17c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c17c-102">SYNOPSIS</span></span>
<span data-ttu-id="9c17c-103">Получает конфигурацию подключения к каналу ExpressRoute, связанную с частным одноранговым подключением ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="9c17c-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="9c17c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c17c-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c17c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c17c-105">DESCRIPTION</span></span>
<span data-ttu-id="9c17c-106">Командлет **Get-AzExpressRouteCircuitConnectionConfig** извлекает конфигурацию подключения к каналу, связанного с частным одноранговым соединением для канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="9c17c-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="9c17c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c17c-107">EXAMPLES</span></span>

### <span data-ttu-id="9c17c-108">Пример 1: отображение конфигурации подключения к каналу для канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="9c17c-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="9c17c-109">Пример 2: получение ресурса подключения к каналу, связанного с цепью ExpressRoute с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="9c17c-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="9c17c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c17c-110">PARAMETERS</span></span>

### <span data-ttu-id="9c17c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c17c-111">-DefaultProfile</span></span>
<span data-ttu-id="9c17c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c17c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c17c-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9c17c-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="9c17c-114">Объект цепи ExpressRoute, который содержит конфигурацию подключения к каналу.</span><span class="sxs-lookup"><span data-stu-id="9c17c-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="9c17c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9c17c-115">-Name</span></span>
<span data-ttu-id="9c17c-116">Имя конфигурации подключения к каналу, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="9c17c-116">The name of the circuit connection configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c17c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c17c-117">CommonParameters</span></span>
<span data-ttu-id="9c17c-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c17c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c17c-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c17c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c17c-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c17c-120">INPUTS</span></span>

### <span data-ttu-id="9c17c-121">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9c17c-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="9c17c-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c17c-122">OUTPUTS</span></span>

### <span data-ttu-id="9c17c-123">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="9c17c-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="9c17c-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c17c-124">NOTES</span></span>

## <span data-ttu-id="9c17c-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c17c-125">RELATED LINKS</span></span>

[<span data-ttu-id="9c17c-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9c17c-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="9c17c-127">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="9c17c-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="9c17c-128">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="9c17c-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="9c17c-129">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="9c17c-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="9c17c-130">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="9c17c-130">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)