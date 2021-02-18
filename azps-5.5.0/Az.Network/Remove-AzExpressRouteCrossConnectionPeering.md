---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 4309550557480211560e108489b14850672ee1f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225828"
---
# <span data-ttu-id="a7351-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="a7351-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="a7351-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7351-102">SYNOPSIS</span></span>
<span data-ttu-id="a7351-103">Удаляет пиринг перекрестного подключения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a7351-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="a7351-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a7351-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7351-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7351-105">DESCRIPTION</span></span>
<span data-ttu-id="a7351-106">Для удаления конфигурации пиринга перекрестного подключения ExpressRoute удаляется cmdlet **Remove-AzExpressRouteCrossConnectionPeering.**</span><span class="sxs-lookup"><span data-stu-id="a7351-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="a7351-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a7351-107">EXAMPLES</span></span>

### <span data-ttu-id="a7351-108">Пример 1. Удаление конфигурации пиринга из перекрестного подключения ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="a7351-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="a7351-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7351-109">PARAMETERS</span></span>

### <span data-ttu-id="a7351-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7351-110">-DefaultProfile</span></span>
<span data-ttu-id="a7351-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7351-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7351-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a7351-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="a7351-113">Перекрестное подключение ExpressRoute, содержащее удаленную конфигурацию пиринга.</span><span class="sxs-lookup"><span data-stu-id="a7351-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7351-114">-Force</span><span class="sxs-lookup"><span data-stu-id="a7351-114">-Force</span></span>
<span data-ttu-id="a7351-115">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="a7351-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a7351-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a7351-116">-Name</span></span>
<span data-ttu-id="a7351-117">Имя удаляемой конфигурации пиринга.</span><span class="sxs-lookup"><span data-stu-id="a7351-117">The name of the peering configuration to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7351-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="a7351-118">-PeerAddressType</span></span>
<span data-ttu-id="a7351-119">Семейство адресов пиринга</span><span class="sxs-lookup"><span data-stu-id="a7351-119">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7351-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7351-120">-Confirm</span></span>
<span data-ttu-id="a7351-121">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a7351-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7351-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7351-122">-WhatIf</span></span>
<span data-ttu-id="a7351-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7351-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7351-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a7351-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7351-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7351-125">CommonParameters</span></span>
<span data-ttu-id="a7351-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7351-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7351-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7351-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7351-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7351-128">INPUTS</span></span>

### <span data-ttu-id="a7351-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a7351-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="a7351-130">Параметр "ExpressRouteCrossConnection" принимает значение типа PSExpressRouteCrossConnection из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a7351-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="a7351-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7351-131">OUTPUTS</span></span>

### <span data-ttu-id="a7351-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a7351-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="a7351-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a7351-133">NOTES</span></span>

## <span data-ttu-id="a7351-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7351-134">RELATED LINKS</span></span>

[<span data-ttu-id="a7351-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="a7351-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="a7351-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="a7351-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](./Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="a7351-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a7351-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="a7351-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a7351-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
