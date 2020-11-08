---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 505f9eb3b2402756b14fa8b8f49cb1a9ea2a3745
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073952"
---
# <span data-ttu-id="b4575-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="b4575-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="b4575-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4575-102">SYNOPSIS</span></span>
<span data-ttu-id="b4575-103">Удаление настраиваемой политики IPSec VPN, установленной на ресурсе шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b4575-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="b4575-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4575-104">SYNTAX</span></span>

### <span data-ttu-id="b4575-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b4575-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4575-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b4575-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4575-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4575-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4575-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4575-108">DESCRIPTION</span></span>
<span data-ttu-id="b4575-109">Шлюз виртуальной сети — это объект, представляющий ваш шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="b4575-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="b4575-110">Командлет **Remove-AzVpnClientIpsecParameter** удаляет особые параметры IPsec VPN, заданные в шлюзе виртуальной сети, который в свою очередь задает политику IPSec по умолчанию для VPN-шлюза на основе имени VirtualNetworkGateway и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4575-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="b4575-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4575-111">EXAMPLES</span></span>

### <span data-ttu-id="b4575-112">1: удаление параметров VPN-IPSec, заданных для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b4575-112">1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="b4575-113">Удаляет особые параметры IPsec VPN, заданные в шлюзе виртуальной сети, с именем "myGateway" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="b4575-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="b4575-114">Эта команда возвращает логический объект, который отображается, если удаление прошло успешно или завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="b4575-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="b4575-115">Примечание. в результате будет задана политика IPSec по умолчанию для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b4575-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="b4575-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4575-116">PARAMETERS</span></span>

### <span data-ttu-id="b4575-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4575-117">-DefaultProfile</span></span>
<span data-ttu-id="b4575-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4575-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4575-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4575-119">-InputObject</span></span>
<span data-ttu-id="b4575-120">Объект шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="b4575-120">The virtual network gateway object</span></span>

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

### <span data-ttu-id="b4575-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4575-121">-ResourceGroupName</span></span>
<span data-ttu-id="b4575-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4575-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4575-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4575-123">-ResourceId</span></span>
<span data-ttu-id="b4575-124">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="b4575-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b4575-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="b4575-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="b4575-126">Имя шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b4575-126">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4575-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4575-127">-Confirm</span></span>
<span data-ttu-id="b4575-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b4575-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4575-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4575-129">-WhatIf</span></span>
<span data-ttu-id="b4575-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b4575-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4575-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b4575-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4575-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4575-132">CommonParameters</span></span>
<span data-ttu-id="b4575-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4575-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4575-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4575-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4575-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4575-135">INPUTS</span></span>

### <span data-ttu-id="b4575-136">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b4575-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="b4575-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b4575-137">System.String</span></span>

## <span data-ttu-id="b4575-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4575-138">OUTPUTS</span></span>

### <span data-ttu-id="b4575-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b4575-139">System.Boolean</span></span>

## <span data-ttu-id="b4575-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4575-140">NOTES</span></span>

## <span data-ttu-id="b4575-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4575-141">RELATED LINKS</span></span>

[<span data-ttu-id="b4575-142">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="b4575-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="b4575-143">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="b4575-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="b4575-144">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="b4575-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
