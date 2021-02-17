---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionArpTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionArpTable.md
ms.openlocfilehash: 8dac5f65599ead696416eaf33f8773415a5631cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221265"
---
# <span data-ttu-id="945bb-101">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="945bb-101">Get-AzExpressRouteCrossConnectionArpTable</span></span>

## <span data-ttu-id="945bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="945bb-102">SYNOPSIS</span></span>
<span data-ttu-id="945bb-103">Получает таблицу ARP из перекрестного подключения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="945bb-103">Gets the ARP table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="945bb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="945bb-104">SYNTAX</span></span>

### <span data-ttu-id="945bb-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="945bb-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="945bb-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="945bb-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="945bb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="945bb-107">DESCRIPTION</span></span>
<span data-ttu-id="945bb-108">С помощью cmdlet **Get-AzExpressRouteCrossConnectionARPTable** можно извлечь таблицу ARP из обоих интерфейсов перекрестного подключения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="945bb-108">The **Get-AzExpressRouteCrossConnectionARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute cross connection.</span></span> <span data-ttu-id="945bb-109">Таблица "ARP" содержит сопоставление IPv4-адреса с MAC-адресом для определенного пиринга.</span><span class="sxs-lookup"><span data-stu-id="945bb-109">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="945bb-110">Таблицу ARP можно использовать для проверки конфигурации и подключения уровня 2.</span><span class="sxs-lookup"><span data-stu-id="945bb-110">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="945bb-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="945bb-111">EXAMPLES</span></span>

### <span data-ttu-id="945bb-112">Пример 1. Отображение таблицы ARP для одноранговой сети ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="945bb-112">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCrossConnectionARPTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="945bb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="945bb-113">PARAMETERS</span></span>

### <span data-ttu-id="945bb-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="945bb-114">-CrossConnectionName</span></span>
<span data-ttu-id="945bb-115">Имя перекрестного подключения Express Route</span><span class="sxs-lookup"><span data-stu-id="945bb-115">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="945bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="945bb-116">-DefaultProfile</span></span>
<span data-ttu-id="945bb-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="945bb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="945bb-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="945bb-118">-DevicePath</span></span>
<span data-ttu-id="945bb-119">Допустимыми значениями для этого параметра являются: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="945bb-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945bb-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="945bb-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="945bb-121">Перекрестное подключение Express Route</span><span class="sxs-lookup"><span data-stu-id="945bb-121">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="945bb-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="945bb-122">-PeeringType</span></span>
<span data-ttu-id="945bb-123">Допустимыми значениями для этого параметра являются: `AzurePrivatePeering` `AzurePublicPeering` , и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="945bb-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945bb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="945bb-124">-ResourceGroupName</span></span>
<span data-ttu-id="945bb-125">Имя группы ресурсов, содержащей перекрестное подключение ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="945bb-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="945bb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="945bb-126">CommonParameters</span></span>
<span data-ttu-id="945bb-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="945bb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="945bb-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="945bb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="945bb-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="945bb-129">INPUTS</span></span>

### <span data-ttu-id="945bb-130">Нет</span><span class="sxs-lookup"><span data-stu-id="945bb-130">None</span></span>
<span data-ttu-id="945bb-131">Этот cmdlet не принимает входные данные.</span><span class="sxs-lookup"><span data-stu-id="945bb-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="945bb-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="945bb-132">OUTPUTS</span></span>

### <span data-ttu-id="945bb-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="945bb-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="945bb-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="945bb-134">NOTES</span></span>

## <span data-ttu-id="945bb-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="945bb-135">RELATED LINKS</span></span>

[<span data-ttu-id="945bb-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="945bb-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)

[<span data-ttu-id="945bb-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="945bb-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
