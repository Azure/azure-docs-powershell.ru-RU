---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: 4b2963d77d2182821bb4950907ef278950e410f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958152"
---
# Resize-AzVirtualNetworkGateway

## SYNOPSIS
Resizes an existing virtual network gateway.

## СИНТАКСИС

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Командлет **Resize-AzVirtualNetworkGateway** позволяет изменить единицы управления акциями для виртуального сетевого шлюза.
Номера номеров sk определяют возможности шлюза, в том числе пропускную способность и максимально допустимое количество разрешенных IP-туннельов.
Azure поддерживает базовые, стандартные, высокоскоростные, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (также называются небольшие, средние и большие СКА).
Подробные сведения о возможностях каждого типа SKU см. в https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .
Помните о том, что цены и возможности СКАЙФ различаются.
Дополнительные сведения https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ см. в .

## ПРИМЕРЫ

### Пример 1. Изменение размера виртуального сетевого шлюза
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

В этом примере изменяется размер виртуального сетевого шлюза с именем ContosoVirtualGateway.
Первая команда создает ссылку на объект ContosoVirtualGateway; эта ссылка на объект хранится в переменной с именем $Gateway.
Вторая команда затем использует командлет **Resize-AzVirtualNetworkGateway** для свойства *GatewaySku* Basic.

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

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

### -GatewaySku
Указывает новый тип SKU шлюза.
Допустимые значения этого параметра:
- Базовая
- Стандартный
- Высокая производительность
- VpnGw1
- VpnGw2
- VpnGw3
- VpnGw1AZ 
- VpnGw2AZ 
- VpnGw3AZ 
- ErGw1AZ 
- ErGw2AZ 
- ErGw3AZ 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Указывает ссылку на объект виртуального сетевого шлюза, который нужно размеризировать.
Эту ссылку на объект можно создать, указав Get-AzVirtualNetworkGateway имя шлюза.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## ПРИМЕЧАНИЯ
С обычных, стандартных и highPerformance на новые СКАйп VpnGw1/VpnGw2/VpnGw3 нельзя 399999999. Возможность дальнейшего перенамерки не разрешена для VPNGw1AZ/VpnGw2AZ/VpnGw3AZ или ErGw1AZ/ErGw2AZ/ErGw3AZ. Размер, допустимый только в рядах SKU, например, размер VPNGw1AZ можно использовать в vpnGw2AZ/VpnGw3AZ и ErGw1AZ, а также в ErGw2AZ/ErGw3AZ. См. https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpngateways инструкции.

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[New-AzVirtualNetworkGateway](./New-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGateway](./Remove-AzVirtualNetworkGateway.md)

[Reset-AzVirtualNetworkGateway](./Reset-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGateway](./Set-AzVirtualNetworkGateway.md)

[Get-AzVpnClientPackage](./Get-AzVpnClientPackage.md)

[Set-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)
