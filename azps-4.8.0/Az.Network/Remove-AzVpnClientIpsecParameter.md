---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: cee8d5d1ca76fbf206b4695661cc8f452052e62c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079440"
---
# <span data-ttu-id="8e4d6-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8e4d6-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="8e4d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e4d6-102">SYNOPSIS</span></span>
<span data-ttu-id="8e4d6-103">Удаление настраиваемой политики IPSec VPN, установленной на ресурсе шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="8e4d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e4d6-104">SYNTAX</span></span>

### <span data-ttu-id="8e4d6-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e4d6-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e4d6-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8e4d6-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e4d6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e4d6-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e4d6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e4d6-108">DESCRIPTION</span></span>
<span data-ttu-id="8e4d6-109">Шлюз виртуальной сети — это объект, представляющий ваш шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="8e4d6-110">Командлет **Remove-AzVpnClientIpsecParameter** удаляет особые параметры IPsec VPN, заданные в шлюзе виртуальной сети, который в свою очередь задает политику IPSec по умолчанию для VPN-шлюза на основе имени VirtualNetworkGateway и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="8e4d6-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e4d6-111">EXAMPLES</span></span>

### <span data-ttu-id="8e4d6-112">Пример 1: удаление параметров VPN-IPSec, заданных в шлюзе виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="8e4d6-112">Example 1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```powershell
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="8e4d6-113">Удаляет особые параметры IPsec VPN, заданные в шлюзе виртуальной сети, с именем "myGateway" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="8e4d6-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="8e4d6-114">Эта команда возвращает логический объект, который отображается, если удаление прошло успешно или завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="8e4d6-115">Примечание. в результате будет задана политика IPSec по умолчанию для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="8e4d6-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e4d6-116">PARAMETERS</span></span>

### <span data-ttu-id="8e4d6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e4d6-117">-DefaultProfile</span></span>
<span data-ttu-id="8e4d6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e4d6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e4d6-119">-InputObject</span></span>
<span data-ttu-id="8e4d6-120">Объект шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="8e4d6-120">The virtual network gateway object</span></span>

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

### <span data-ttu-id="8e4d6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e4d6-121">-ResourceGroupName</span></span>
<span data-ttu-id="8e4d6-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-122">The resource group name.</span></span>

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

### <span data-ttu-id="8e4d6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e4d6-123">-ResourceId</span></span>
<span data-ttu-id="8e4d6-124">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8e4d6-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="8e4d6-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="8e4d6-126">Имя шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-126">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="8e4d6-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e4d6-127">-Confirm</span></span>
<span data-ttu-id="8e4d6-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e4d6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e4d6-129">-WhatIf</span></span>
<span data-ttu-id="8e4d6-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e4d6-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e4d6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e4d6-132">CommonParameters</span></span>
<span data-ttu-id="8e4d6-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e4d6-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e4d6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e4d6-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e4d6-135">INPUTS</span></span>

### <span data-ttu-id="8e4d6-136">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8e4d6-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="8e4d6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8e4d6-137">System.String</span></span>

## <span data-ttu-id="8e4d6-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e4d6-138">OUTPUTS</span></span>

### <span data-ttu-id="8e4d6-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e4d6-139">System.Boolean</span></span>

## <span data-ttu-id="8e4d6-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e4d6-140">NOTES</span></span>

## <span data-ttu-id="8e4d6-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e4d6-141">RELATED LINKS</span></span>

[<span data-ttu-id="8e4d6-142">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8e4d6-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="8e4d6-143">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8e4d6-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="8e4d6-144">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8e4d6-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
