---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 38dcfdb1188a810b0f154dfed31f8a1ef3206247
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565848"
---
# <span data-ttu-id="db4b1-101">Set-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="db4b1-101">Set-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="db4b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db4b1-102">SYNOPSIS</span></span>
<span data-ttu-id="db4b1-103">Задает параметры IPsec VPN для существующего шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="db4b1-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db4b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db4b1-104">SYNTAX</span></span>

### <span data-ttu-id="db4b1-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="db4b1-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db4b1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="db4b1-106">ByFactoryObject</span></span>
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db4b1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="db4b1-107">ByResourceId</span></span>
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db4b1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db4b1-108">DESCRIPTION</span></span>
<span data-ttu-id="db4b1-109">Командлет **Set-AzureRmVpnClientIpsecParameter** задает параметры IPsec VPN для существующего шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="db4b1-109">The **Set-AzureRmVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="db4b1-110">После создания шлюза виртуальной сети он задает набор политик IPSec по умолчанию для шлюза VPN.</span><span class="sxs-lookup"><span data-stu-id="db4b1-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="db4b1-111">В случае наведите указатель мыши на сайт, чтобы использовать определенную политику IPSec для подключения к шлюзу VPN, пользователь должен сначала настроить политику IPSec в VPN-шлюзе.</span><span class="sxs-lookup"><span data-stu-id="db4b1-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="db4b1-112">**Set-AzureRmVpnClientIpsecParameter** обеспечивает эти возможности.</span><span class="sxs-lookup"><span data-stu-id="db4b1-112">**Set-AzureRmVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="db4b1-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db4b1-113">EXAMPLES</span></span>

### <span data-ttu-id="db4b1-114">Пример 1: Установка настраиваемой политики IPSec VPN для существующего шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="db4b1-114">Example 1 : Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzureRmVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="db4b1-115">В этом примере в качестве настраиваемой политики IPSec для VPN указан IP-адрес существующего виртуального сетевого шлюза с именем ContosoVirtualGateway из группы ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="db4b1-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="db4b1-116">New-AzureRmVpnClientIpsecParameter, который используется для создания объекта параметров VPN-IPSec с использованием переданных значений одного или всех параметров, которые пользователь может настроить для любого из существующих шлюзов виртуальной сети в ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="db4b1-116">New-AzureRmVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="db4b1-117">Созданный объект VpnClientIPsecParameters передается Set-AzureRmVpnClientIpsecParameter команде для настройки указанной настраиваемой политики IPSec VPN на виртуальном сетевом шлюзе, как показано в примере выше.</span><span class="sxs-lookup"><span data-stu-id="db4b1-117">This created VpnClientIPsecParameters object is passed to Set-AzureRmVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="db4b1-118">Эта команда возвращает объект VpnClientIPsecParameters, который показывает наборы параметров.</span><span class="sxs-lookup"><span data-stu-id="db4b1-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="db4b1-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db4b1-119">PARAMETERS</span></span>

### <span data-ttu-id="db4b1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db4b1-120">-DefaultProfile</span></span>
<span data-ttu-id="db4b1-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db4b1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db4b1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db4b1-122">-InputObject</span></span>
<span data-ttu-id="db4b1-123">Объект Gateaway виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="db4b1-123">The virtual network gateaway object</span></span>

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

### <span data-ttu-id="db4b1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db4b1-124">-ResourceGroupName</span></span>
<span data-ttu-id="db4b1-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="db4b1-125">The resource group name.</span></span>

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

### <span data-ttu-id="db4b1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db4b1-126">-ResourceId</span></span>
<span data-ttu-id="db4b1-127">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="db4b1-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="db4b1-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="db4b1-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="db4b1-129">Имя шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="db4b1-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="db4b1-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="db4b1-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="db4b1-131">Параметры IPsec VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="db4b1-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="db4b1-132">Это значение параметра может быть создано с помощью команды PS Let: New-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="db4b1-132">This parameter value can be constructed using PS command let:New-AzureRmVpnClientIpsecParameter</span></span>

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

### <span data-ttu-id="db4b1-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db4b1-133">-Confirm</span></span>
<span data-ttu-id="db4b1-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="db4b1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db4b1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db4b1-135">-WhatIf</span></span>
<span data-ttu-id="db4b1-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="db4b1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db4b1-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="db4b1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db4b1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db4b1-138">CommonParameters</span></span>
<span data-ttu-id="db4b1-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db4b1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db4b1-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db4b1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db4b1-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db4b1-141">INPUTS</span></span>

### <span data-ttu-id="db4b1-142">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="db4b1-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>
<span data-ttu-id="db4b1-143">Параметры: VpnClientIPsecParameter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="db4b1-143">Parameters: VpnClientIPsecParameter (ByValue)</span></span>

### <span data-ttu-id="db4b1-144">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="db4b1-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="db4b1-145">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="db4b1-145">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="db4b1-146">System. String</span><span class="sxs-lookup"><span data-stu-id="db4b1-146">System.String</span></span>

## <span data-ttu-id="db4b1-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db4b1-147">OUTPUTS</span></span>

### <span data-ttu-id="db4b1-148">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="db4b1-148">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="db4b1-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="db4b1-149">NOTES</span></span>

## <span data-ttu-id="db4b1-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db4b1-150">RELATED LINKS</span></span>

[<span data-ttu-id="db4b1-151">New-AzureRmVpnClientIpsecParameters</span><span class="sxs-lookup"><span data-stu-id="db4b1-151">New-AzureRmVpnClientIpsecParameters</span></span>](./New-AzureRmVpnClientIpsecParameters.md)
