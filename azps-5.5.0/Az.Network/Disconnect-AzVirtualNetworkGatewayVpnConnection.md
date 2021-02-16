---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: b14d7f0ac4f70268175948b41abaa1fee564a383
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223996"
---
# <span data-ttu-id="dad8c-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="dad8c-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="dad8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dad8c-102">SYNOPSIS</span></span> 
<span data-ttu-id="dad8c-103">Отключите подключенные vpn-клиентские подключения к заданным виртуальным сетевым шлюзам.</span><span class="sxs-lookup"><span data-stu-id="dad8c-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="dad8c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dad8c-104">SYNTAX</span></span>
### <span data-ttu-id="dad8c-105">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dad8c-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="dad8c-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="dad8c-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="dad8c-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="dad8c-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="dad8c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dad8c-108">DESCRIPTION</span></span>
<span data-ttu-id="dad8c-109">Командлет **Disconnect-AzVirtualNetworkGatewayVpnConnection** позволяет отключить подключенное VPN-подключение.</span><span class="sxs-lookup"><span data-stu-id="dad8c-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="dad8c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dad8c-110">EXAMPLES</span></span>

### <span data-ttu-id="dad8c-111">Пример</span><span class="sxs-lookup"><span data-stu-id="dad8c-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="dad8c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dad8c-112">PARAMETERS</span></span>

### <span data-ttu-id="dad8c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dad8c-113">-ResourceGroupName</span></span>
<span data-ttu-id="dad8c-114">Имя группы ресурсов виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="dad8c-114">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="dad8c-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="dad8c-115">-ResourceName</span></span>
<span data-ttu-id="dad8c-116">Имя виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="dad8c-116">Virtual network gateway name</span></span>

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

### <span data-ttu-id="dad8c-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dad8c-117">-ResourceId</span></span>
<span data-ttu-id="dad8c-118">ИД ресурса виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="dad8c-118">Virtual network gateway resource Id</span></span>

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

### <span data-ttu-id="dad8c-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="dad8c-119">-VpnConnectionId</span></span>
<span data-ttu-id="dad8c-120">Vpn Connection Ids</span><span class="sxs-lookup"><span data-stu-id="dad8c-120">Vpn Connection Ids</span></span>

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

### <span data-ttu-id="dad8c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dad8c-121">-InputObject</span></span>
<span data-ttu-id="dad8c-122">Объект виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="dad8c-122">Virtual network gateway object</span></span>

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

### <span data-ttu-id="dad8c-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dad8c-123">-AsJob</span></span>
<span data-ttu-id="dad8c-124">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="dad8c-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dad8c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad8c-125">CommonParameters</span></span>
<span data-ttu-id="dad8c-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dad8c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad8c-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dad8c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad8c-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dad8c-128">INPUTS</span></span>

### <span data-ttu-id="dad8c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="dad8c-129">System.String</span></span>

## <span data-ttu-id="dad8c-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dad8c-130">OUTPUTS</span></span>

### <span data-ttu-id="dad8c-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dad8c-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="dad8c-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dad8c-132">NOTES</span></span>

## <span data-ttu-id="dad8c-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dad8c-133">RELATED LINKS</span></span>
