---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: b14d7f0ac4f70268175948b41abaa1fee564a383
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079519"
---
# <span data-ttu-id="7b137-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7b137-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="7b137-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7b137-102">SYNOPSIS</span></span> 
<span data-ttu-id="7b137-103">Отключите подключение к подключенным VPN-клиентам с использованием заданного шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7b137-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="7b137-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7b137-104">SYNTAX</span></span>
### <span data-ttu-id="7b137-105">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7b137-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="7b137-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7b137-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="7b137-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7b137-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="7b137-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b137-108">DESCRIPTION</span></span>
<span data-ttu-id="7b137-109">Командлет **Disconnect-AzVirtualNetworkGatewayVpnConnection** позволяет отключить подключение к подключенному клиенту VPN.</span><span class="sxs-lookup"><span data-stu-id="7b137-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="7b137-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7b137-110">EXAMPLES</span></span>

### <span data-ttu-id="7b137-111">Образом</span><span class="sxs-lookup"><span data-stu-id="7b137-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="7b137-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7b137-112">PARAMETERS</span></span>

### <span data-ttu-id="7b137-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b137-113">-ResourceGroupName</span></span>
<span data-ttu-id="7b137-114">Имя группы ресурсов шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="7b137-114">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="7b137-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7b137-115">-ResourceName</span></span>
<span data-ttu-id="7b137-116">Имя шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="7b137-116">Virtual network gateway name</span></span>

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

### <span data-ttu-id="7b137-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b137-117">-ResourceId</span></span>
<span data-ttu-id="7b137-118">Идентификатор ресурса шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="7b137-118">Virtual network gateway resource Id</span></span>

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

### <span data-ttu-id="7b137-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="7b137-119">-VpnConnectionId</span></span>
<span data-ttu-id="7b137-120">Коды VPN-подключений</span><span class="sxs-lookup"><span data-stu-id="7b137-120">Vpn Connection Ids</span></span>

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

### <span data-ttu-id="7b137-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b137-121">-InputObject</span></span>
<span data-ttu-id="7b137-122">Объект шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="7b137-122">Virtual network gateway object</span></span>

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

### <span data-ttu-id="7b137-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b137-123">-AsJob</span></span>
<span data-ttu-id="7b137-124">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7b137-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b137-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b137-125">CommonParameters</span></span>
<span data-ttu-id="7b137-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7b137-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b137-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b137-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b137-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7b137-128">INPUTS</span></span>

### <span data-ttu-id="7b137-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7b137-129">System.String</span></span>

## <span data-ttu-id="7b137-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b137-130">OUTPUTS</span></span>

### <span data-ttu-id="7b137-131">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7b137-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7b137-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="7b137-132">NOTES</span></span>

## <span data-ttu-id="7b137-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b137-133">RELATED LINKS</span></span>