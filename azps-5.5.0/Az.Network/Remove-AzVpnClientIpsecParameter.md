---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: cee8d5d1ca76fbf206b4695661cc8f452052e62c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225764"
---
# <span data-ttu-id="82a30-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="82a30-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="82a30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82a30-102">SYNOPSIS</span></span>
<span data-ttu-id="82a30-103">Удаляет настраиваемую политику IPSEC vpn, настроенную для ресурса виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="82a30-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="82a30-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="82a30-104">SYNTAX</span></span>

### <span data-ttu-id="82a30-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="82a30-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82a30-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="82a30-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82a30-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="82a30-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82a30-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82a30-108">DESCRIPTION</span></span>
<span data-ttu-id="82a30-109">Виртуальный сетевой шлюз — это объект, представляющий шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="82a30-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="82a30-110">Командлет **Remove-AzVpnClientIpsecParameter** удаляет настраиваемые параметры ipsec VPN, заданные для виртуального сетевого шлюза, которые, в свою очередь, настраивают политику VPN ipsec для VPN-шлюза на основе имени vpnNetworkGateway и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82a30-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="82a30-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="82a30-111">EXAMPLES</span></span>

### <span data-ttu-id="82a30-112">Пример 1. Удаляет параметры ipsec VPN, заданные на виртуальном сетевом шлюзе.</span><span class="sxs-lookup"><span data-stu-id="82a30-112">Example 1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```powershell
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="82a30-113">Удаляет vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span><span class="sxs-lookup"><span data-stu-id="82a30-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="82a30-114">Эта команда возвращает объект Bool, который показывает, успешно ли удаление было успешно или не удалось.</span><span class="sxs-lookup"><span data-stu-id="82a30-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="82a30-115">Примечание. Это приведет к настройке политики VPN IPSEC по умолчанию для виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="82a30-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="82a30-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82a30-116">PARAMETERS</span></span>

### <span data-ttu-id="82a30-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82a30-117">-DefaultProfile</span></span>
<span data-ttu-id="82a30-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82a30-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82a30-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82a30-119">-InputObject</span></span>
<span data-ttu-id="82a30-120">Объект виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="82a30-120">The virtual network gateway object</span></span>

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

### <span data-ttu-id="82a30-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82a30-121">-ResourceGroupName</span></span>
<span data-ttu-id="82a30-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82a30-122">The resource group name.</span></span>

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

### <span data-ttu-id="82a30-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82a30-123">-ResourceId</span></span>
<span data-ttu-id="82a30-124">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="82a30-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="82a30-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="82a30-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="82a30-126">Имя виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="82a30-126">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="82a30-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82a30-127">-Confirm</span></span>
<span data-ttu-id="82a30-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82a30-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82a30-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82a30-129">-WhatIf</span></span>
<span data-ttu-id="82a30-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82a30-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82a30-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="82a30-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82a30-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a30-132">CommonParameters</span></span>
<span data-ttu-id="82a30-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82a30-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a30-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82a30-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a30-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82a30-135">INPUTS</span></span>

### <span data-ttu-id="82a30-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="82a30-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="82a30-137">System.String</span><span class="sxs-lookup"><span data-stu-id="82a30-137">System.String</span></span>

## <span data-ttu-id="82a30-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="82a30-138">OUTPUTS</span></span>

### <span data-ttu-id="82a30-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="82a30-139">System.Boolean</span></span>

## <span data-ttu-id="82a30-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="82a30-140">NOTES</span></span>

## <span data-ttu-id="82a30-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82a30-141">RELATED LINKS</span></span>

[<span data-ttu-id="82a30-142">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="82a30-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="82a30-143">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="82a30-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="82a30-144">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="82a30-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
