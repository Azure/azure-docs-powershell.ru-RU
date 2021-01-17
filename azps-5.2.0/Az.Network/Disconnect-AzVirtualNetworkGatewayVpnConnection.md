---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: b14d7f0ac4f70268175948b41abaa1fee564a383
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407223"
---
# <span data-ttu-id="8b49e-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="8b49e-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="8b49e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b49e-102">SYNOPSIS</span></span> 
<span data-ttu-id="8b49e-103">Отключите подключенные vpn-клиентские подключения к заданным виртуальным сетевым шлюзам.</span><span class="sxs-lookup"><span data-stu-id="8b49e-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="8b49e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8b49e-104">SYNTAX</span></span>
### <span data-ttu-id="8b49e-105">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8b49e-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="8b49e-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="8b49e-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="8b49e-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="8b49e-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="8b49e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b49e-108">DESCRIPTION</span></span>
<span data-ttu-id="8b49e-109">Командлет **Disconnect-AzVirtualNetworkGatewayVpnConnection** позволяет отключить подключенное VPN-подключение.</span><span class="sxs-lookup"><span data-stu-id="8b49e-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="8b49e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8b49e-110">EXAMPLES</span></span>

### <span data-ttu-id="8b49e-111">Пример</span><span class="sxs-lookup"><span data-stu-id="8b49e-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="8b49e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b49e-112">PARAMETERS</span></span>

### <span data-ttu-id="8b49e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b49e-113">-ResourceGroupName</span></span>
<span data-ttu-id="8b49e-114">Имя группы ресурсов виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="8b49e-114">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b49e-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8b49e-115">-ResourceName</span></span>
<span data-ttu-id="8b49e-116">Имя виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="8b49e-116">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: VirtualNetworkGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b49e-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b49e-117">-ResourceId</span></span>
<span data-ttu-id="8b49e-118">ИД ресурса виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="8b49e-118">Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b49e-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="8b49e-119">-VpnConnectionId</span></span>
<span data-ttu-id="8b49e-120">Vpn-подключения ids</span><span class="sxs-lookup"><span data-stu-id="8b49e-120">Vpn Connection Ids</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b49e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b49e-121">-InputObject</span></span>
<span data-ttu-id="8b49e-122">Объект виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="8b49e-122">Virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VirtualNetworkGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b49e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b49e-123">-AsJob</span></span>
<span data-ttu-id="8b49e-124">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8b49e-124">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b49e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b49e-125">CommonParameters</span></span>
<span data-ttu-id="8b49e-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b49e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b49e-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b49e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b49e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b49e-128">INPUTS</span></span>

### <span data-ttu-id="8b49e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="8b49e-129">System.String</span></span>

## <span data-ttu-id="8b49e-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b49e-130">OUTPUTS</span></span>

### <span data-ttu-id="8b49e-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8b49e-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="8b49e-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8b49e-132">NOTES</span></span>

## <span data-ttu-id="8b49e-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b49e-133">RELATED LINKS</span></span>
