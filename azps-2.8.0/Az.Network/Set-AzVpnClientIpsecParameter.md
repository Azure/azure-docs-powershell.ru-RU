---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 248e932bfc2c9148122ecad924ae10b3e480fd3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904353"
---
# <span data-ttu-id="cd380-101">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cd380-101">Set-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="cd380-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd380-102">SYNOPSIS</span></span>
<span data-ttu-id="cd380-103">Задает параметры IPsec VPN для существующего шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cd380-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

## <span data-ttu-id="cd380-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd380-104">SYNTAX</span></span>

### <span data-ttu-id="cd380-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cd380-105">ByFactoryName (Default)</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd380-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cd380-106">ByFactoryObject</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd380-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cd380-107">ByResourceId</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd380-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd380-108">DESCRIPTION</span></span>
<span data-ttu-id="cd380-109">Командлет **Set-AzVpnClientIpsecParameter** задает параметры IPsec VPN для существующего шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cd380-109">The **Set-AzVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="cd380-110">После создания шлюза виртуальной сети он задает набор политик IPSec по умолчанию для шлюза VPN.</span><span class="sxs-lookup"><span data-stu-id="cd380-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="cd380-111">В случае наведите указатель мыши на сайт, чтобы использовать определенную политику IPSec для подключения к шлюзу VPN, пользователь должен сначала настроить политику IPSec в VPN-шлюзе.</span><span class="sxs-lookup"><span data-stu-id="cd380-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="cd380-112">**Set-AzVpnClientIpsecParameter** обеспечивает эти возможности.</span><span class="sxs-lookup"><span data-stu-id="cd380-112">**Set-AzVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="cd380-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd380-113">EXAMPLES</span></span>

### <span data-ttu-id="cd380-114">Пример 1: Установка настраиваемой политики IPSec VPN для существующего шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cd380-114">Example 1 : Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="cd380-115">В этом примере в качестве настраиваемой политики IPSec для VPN указан IP-адрес существующего виртуального сетевого шлюза с именем ContosoVirtualGateway из группы ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cd380-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="cd380-116">New-AzVpnClientIpsecParameter, который используется для создания объекта параметров VPN-IPSec с использованием переданных значений одного или всех параметров, которые пользователь может настроить для любого из существующих шлюзов виртуальной сети в ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cd380-116">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="cd380-117">Созданный объект VpnClientIPsecParameters передается Set-AzVpnClientIpsecParameter команде для настройки указанной настраиваемой политики IPSec VPN на виртуальном сетевом шлюзе, как показано в примере выше.</span><span class="sxs-lookup"><span data-stu-id="cd380-117">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="cd380-118">Эта команда возвращает объект VpnClientIPsecParameters, который показывает наборы параметров.</span><span class="sxs-lookup"><span data-stu-id="cd380-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="cd380-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd380-119">PARAMETERS</span></span>

### <span data-ttu-id="cd380-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd380-120">-DefaultProfile</span></span>
<span data-ttu-id="cd380-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd380-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd380-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd380-122">-InputObject</span></span>
<span data-ttu-id="cd380-123">Объект шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="cd380-123">The virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd380-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd380-124">-ResourceGroupName</span></span>
<span data-ttu-id="cd380-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cd380-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd380-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd380-126">-ResourceId</span></span>
<span data-ttu-id="cd380-127">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="cd380-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd380-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="cd380-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="cd380-129">Имя шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cd380-129">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd380-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="cd380-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="cd380-131">Параметры IPsec VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="cd380-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="cd380-132">Это значение параметра может быть создано с помощью команды PS Let: New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cd380-132">This parameter value can be constructed using PS command let:New-AzVpnClientIpsecParameter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd380-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd380-133">-Confirm</span></span>
<span data-ttu-id="cd380-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cd380-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd380-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd380-135">-WhatIf</span></span>
<span data-ttu-id="cd380-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cd380-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd380-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cd380-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd380-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd380-138">CommonParameters</span></span>
<span data-ttu-id="cd380-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd380-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd380-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd380-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd380-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd380-141">INPUTS</span></span>

### <span data-ttu-id="cd380-142">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="cd380-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

### <span data-ttu-id="cd380-143">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cd380-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="cd380-144">System. String</span><span class="sxs-lookup"><span data-stu-id="cd380-144">System.String</span></span>

## <span data-ttu-id="cd380-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd380-145">OUTPUTS</span></span>

### <span data-ttu-id="cd380-146">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="cd380-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="cd380-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd380-147">NOTES</span></span>

## <span data-ttu-id="cd380-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd380-148">RELATED LINKS</span></span>

[<span data-ttu-id="cd380-149">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cd380-149">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="cd380-150">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cd380-150">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="cd380-151">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cd380-151">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)
