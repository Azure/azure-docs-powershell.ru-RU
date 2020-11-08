---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: eb90b668bf0466c44e3fde0ef0a8d6777074fb37
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074055"
---
# <span data-ttu-id="c7d82-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c7d82-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="c7d82-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7d82-102">SYNOPSIS</span></span>
<span data-ttu-id="c7d82-103">Удаляет конфигурацию пиринга перекрестного соединения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c7d82-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="c7d82-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7d82-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7d82-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7d82-105">DESCRIPTION</span></span>
<span data-ttu-id="c7d82-106">Командлет **Remove-AzExpressRouteCrossConnectionPeering** удаляет конфигурацию пиринга перекрестного подключения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c7d82-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="c7d82-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7d82-107">EXAMPLES</span></span>

### <span data-ttu-id="c7d82-108">Пример 1: Удаление конфигурации пиринга из перекрестного соединения ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="c7d82-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="c7d82-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7d82-109">PARAMETERS</span></span>

### <span data-ttu-id="c7d82-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7d82-110">-DefaultProfile</span></span>
<span data-ttu-id="c7d82-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7d82-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7d82-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c7d82-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="c7d82-113">Перекрестное соединение ExpressRoute, содержащее конфигурацию пиринга, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c7d82-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="c7d82-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c7d82-114">-Force</span></span>
<span data-ttu-id="c7d82-115">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="c7d82-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c7d82-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c7d82-116">-Name</span></span>
<span data-ttu-id="c7d82-117">Имя конфигурации пиринга, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c7d82-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="c7d82-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="c7d82-118">-PeerAddressType</span></span>
<span data-ttu-id="c7d82-119">Семейство адресов пиринга</span><span class="sxs-lookup"><span data-stu-id="c7d82-119">The Address family of the peering</span></span>

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

### <span data-ttu-id="c7d82-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7d82-120">-Confirm</span></span>
<span data-ttu-id="c7d82-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c7d82-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7d82-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7d82-122">-WhatIf</span></span>
<span data-ttu-id="c7d82-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c7d82-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7d82-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c7d82-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7d82-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7d82-125">CommonParameters</span></span>
<span data-ttu-id="c7d82-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7d82-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7d82-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7d82-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7d82-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7d82-128">INPUTS</span></span>

### <span data-ttu-id="c7d82-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c7d82-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="c7d82-130">Параметр "ExpressRouteCrossConnection" принимает значение типа "PSExpressRouteCrossConnection" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c7d82-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="c7d82-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7d82-131">OUTPUTS</span></span>

### <span data-ttu-id="c7d82-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c7d82-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="c7d82-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7d82-133">NOTES</span></span>

## <span data-ttu-id="c7d82-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7d82-134">RELATED LINKS</span></span>

[<span data-ttu-id="c7d82-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c7d82-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="c7d82-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c7d82-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](New-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="c7d82-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c7d82-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="c7d82-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c7d82-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
