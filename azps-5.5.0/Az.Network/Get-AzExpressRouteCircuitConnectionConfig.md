---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0ef2870592411ce64847f8a4a58dabdebcc8235f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414719"
---
# <span data-ttu-id="e32a2-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e32a2-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="e32a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e32a2-102">SYNOPSIS</span></span>
<span data-ttu-id="e32a2-103">Возвращает конфигурацию подключения к каналу ExpressRoute, связанную с частным пирингом ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="e32a2-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="e32a2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e32a2-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e32a2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e32a2-105">DESCRIPTION</span></span>
<span data-ttu-id="e32a2-106">Cmdlet **Get-AzExpressRouteCircuitConnectionConfig** извлекает конфигурацию подключения к каналу, связанному с частным пирингом для схемы ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e32a2-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="e32a2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e32a2-107">EXAMPLES</span></span>

### <span data-ttu-id="e32a2-108">Пример 1. Отображение конфигурации подключения к каналу ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="e32a2-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="e32a2-109">Пример 2. Подключение к каналу, связанному с каналом ExpressRoute, с помощью piping</span><span class="sxs-lookup"><span data-stu-id="e32a2-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="e32a2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e32a2-110">PARAMETERS</span></span>

### <span data-ttu-id="e32a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e32a2-111">-DefaultProfile</span></span>
<span data-ttu-id="e32a2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e32a2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e32a2-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e32a2-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="e32a2-114">Объект схемы ExpressRoute, содержащий конфигурацию подключения к каналу.</span><span class="sxs-lookup"><span data-stu-id="e32a2-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="e32a2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e32a2-115">-Name</span></span>
<span data-ttu-id="e32a2-116">Имя извлечения конфигурации подключения к каналу.</span><span class="sxs-lookup"><span data-stu-id="e32a2-116">The name of the circuit connection configuration to be retrieved.</span></span>

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

### <span data-ttu-id="e32a2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e32a2-117">CommonParameters</span></span>
<span data-ttu-id="e32a2-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e32a2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e32a2-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e32a2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e32a2-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e32a2-120">INPUTS</span></span>

### <span data-ttu-id="e32a2-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e32a2-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e32a2-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e32a2-122">OUTPUTS</span></span>

### <span data-ttu-id="e32a2-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="e32a2-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="e32a2-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e32a2-124">NOTES</span></span>

## <span data-ttu-id="e32a2-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e32a2-125">RELATED LINKS</span></span>

[<span data-ttu-id="e32a2-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e32a2-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="e32a2-127">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e32a2-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="e32a2-128">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e32a2-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="e32a2-129">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e32a2-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)


