---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: b991b26d8d6fc7a7cfd33ab051619b7192ae0aec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730175"
---
# <span data-ttu-id="41bbb-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="41bbb-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="41bbb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="41bbb-103">Удаляет конфигурацию пиринга перекрестного соединения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="41bbb-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="41bbb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41bbb-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41bbb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41bbb-105">DESCRIPTION</span></span>
<span data-ttu-id="41bbb-106">Командлет **Remove-AzExpressRouteCrossConnectionPeering** удаляет конфигурацию пиринга перекрестного подключения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="41bbb-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="41bbb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41bbb-107">EXAMPLES</span></span>

### <span data-ttu-id="41bbb-108">Пример 1: Удаление конфигурации пиринга из перекрестного соединения ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="41bbb-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="41bbb-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41bbb-109">PARAMETERS</span></span>

### <span data-ttu-id="41bbb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41bbb-110">-DefaultProfile</span></span>
<span data-ttu-id="41bbb-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41bbb-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41bbb-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="41bbb-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="41bbb-113">Перекрестное соединение ExpressRoute, содержащее конфигурацию пиринга, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="41bbb-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="41bbb-114">-Force</span><span class="sxs-lookup"><span data-stu-id="41bbb-114">-Force</span></span>
<span data-ttu-id="41bbb-115">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="41bbb-115">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="41bbb-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="41bbb-116">-Name</span></span>
<span data-ttu-id="41bbb-117">Имя конфигурации пиринга, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="41bbb-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="41bbb-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="41bbb-118">-PeerAddressType</span></span>
<span data-ttu-id="41bbb-119">Семейство адресов пиринга</span><span class="sxs-lookup"><span data-stu-id="41bbb-119">The Address family of the peering</span></span>

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

### <span data-ttu-id="41bbb-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41bbb-120">-Confirm</span></span>
<span data-ttu-id="41bbb-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="41bbb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41bbb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41bbb-122">-WhatIf</span></span>
<span data-ttu-id="41bbb-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="41bbb-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41bbb-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="41bbb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41bbb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41bbb-125">CommonParameters</span></span>
<span data-ttu-id="41bbb-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41bbb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41bbb-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41bbb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41bbb-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41bbb-128">INPUTS</span></span>

### <span data-ttu-id="41bbb-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="41bbb-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="41bbb-130">Параметр "ExpressRouteCrossConnection" принимает значение типа "PSExpressRouteCrossConnection" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="41bbb-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="41bbb-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41bbb-131">OUTPUTS</span></span>

### <span data-ttu-id="41bbb-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="41bbb-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="41bbb-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="41bbb-133">NOTES</span></span>

## <span data-ttu-id="41bbb-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41bbb-134">RELATED LINKS</span></span>

[<span data-ttu-id="41bbb-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="41bbb-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="41bbb-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="41bbb-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](New-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="41bbb-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="41bbb-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="41bbb-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="41bbb-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
