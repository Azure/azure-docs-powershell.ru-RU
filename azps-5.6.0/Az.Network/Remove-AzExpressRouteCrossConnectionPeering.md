---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 26e924bc94258480e0ae91f30d61c9cfd2adb72c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993782"
---
# <span data-ttu-id="d62cc-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="d62cc-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="d62cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d62cc-102">SYNOPSIS</span></span>
<span data-ttu-id="d62cc-103">Удаляет пиринг перекрестного подключения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d62cc-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="d62cc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d62cc-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d62cc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d62cc-105">DESCRIPTION</span></span>
<span data-ttu-id="d62cc-106">Для удаления конфигурации пиринга перекрестного подключения ExpressRoute удаляется cmdlet **Remove-AzExpressRouteCrossConnectionPeering.**</span><span class="sxs-lookup"><span data-stu-id="d62cc-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="d62cc-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d62cc-107">EXAMPLES</span></span>

### <span data-ttu-id="d62cc-108">Пример 1. Удаление конфигурации пиринга из перекрестного подключения ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="d62cc-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="d62cc-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d62cc-109">PARAMETERS</span></span>

### <span data-ttu-id="d62cc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d62cc-110">-DefaultProfile</span></span>
<span data-ttu-id="d62cc-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d62cc-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d62cc-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d62cc-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="d62cc-113">Перекрестное подключение ExpressRoute, содержащее удаляемую конфигурацию пиринга.</span><span class="sxs-lookup"><span data-stu-id="d62cc-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="d62cc-114">-Force</span><span class="sxs-lookup"><span data-stu-id="d62cc-114">-Force</span></span>
<span data-ttu-id="d62cc-115">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="d62cc-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d62cc-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d62cc-116">-Name</span></span>
<span data-ttu-id="d62cc-117">Имя удаляемой конфигурации пиринга.</span><span class="sxs-lookup"><span data-stu-id="d62cc-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="d62cc-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="d62cc-118">-PeerAddressType</span></span>
<span data-ttu-id="d62cc-119">Семейство адресов пиринга</span><span class="sxs-lookup"><span data-stu-id="d62cc-119">The Address family of the peering</span></span>

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

### <span data-ttu-id="d62cc-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d62cc-120">-Confirm</span></span>
<span data-ttu-id="d62cc-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d62cc-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d62cc-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d62cc-122">-WhatIf</span></span>
<span data-ttu-id="d62cc-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d62cc-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d62cc-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d62cc-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d62cc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d62cc-125">CommonParameters</span></span>
<span data-ttu-id="d62cc-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d62cc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d62cc-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d62cc-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d62cc-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d62cc-128">INPUTS</span></span>

### <span data-ttu-id="d62cc-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d62cc-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="d62cc-130">Параметр "ExpressRouteCrossConnection" принимает значение типа PSExpressRouteCrossConnection из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d62cc-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="d62cc-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d62cc-131">OUTPUTS</span></span>

### <span data-ttu-id="d62cc-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d62cc-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="d62cc-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d62cc-133">NOTES</span></span>

## <span data-ttu-id="d62cc-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d62cc-134">RELATED LINKS</span></span>

[<span data-ttu-id="d62cc-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="d62cc-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="d62cc-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="d62cc-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](./Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="d62cc-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d62cc-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="d62cc-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d62cc-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
