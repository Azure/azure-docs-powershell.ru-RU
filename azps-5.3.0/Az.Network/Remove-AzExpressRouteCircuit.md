---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: bc77c5d133561984f388e378f13595b3a72af785
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506072"
---
# <span data-ttu-id="1de16-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1de16-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="1de16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1de16-102">SYNOPSIS</span></span>
<span data-ttu-id="1de16-103">Удаляет канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1de16-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="1de16-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1de16-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1de16-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1de16-105">DESCRIPTION</span></span>
<span data-ttu-id="1de16-106">Для **удаления каналов ExpressRoute удаляется cmdlet Remove-AzExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="1de16-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="1de16-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1de16-107">EXAMPLES</span></span>

### <span data-ttu-id="1de16-108">Пример 1. Удаление схемы ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="1de16-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="1de16-109">Пример 2. Удаление каналов ExpressRoute с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="1de16-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="1de16-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1de16-110">PARAMETERS</span></span>

### <span data-ttu-id="1de16-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1de16-111">-AsJob</span></span>
<span data-ttu-id="1de16-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1de16-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1de16-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1de16-113">-DefaultProfile</span></span>
<span data-ttu-id="1de16-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1de16-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1de16-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1de16-115">-Force</span></span>
<span data-ttu-id="1de16-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1de16-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1de16-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1de16-117">-Name</span></span>
<span data-ttu-id="1de16-118">Имя удаляемого контура ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1de16-118">The name of the ExpressRoute circuit to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de16-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1de16-119">-PassThru</span></span>
<span data-ttu-id="1de16-120">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="1de16-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="1de16-121">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1de16-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1de16-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1de16-122">-ResourceGroupName</span></span>
<span data-ttu-id="1de16-123">Имя группы ресурсов, к которой принадлежит этот канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1de16-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de16-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1de16-124">-Confirm</span></span>
<span data-ttu-id="1de16-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1de16-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de16-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1de16-126">-WhatIf</span></span>
<span data-ttu-id="1de16-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1de16-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1de16-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1de16-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de16-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1de16-129">CommonParameters</span></span>
<span data-ttu-id="1de16-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1de16-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1de16-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1de16-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1de16-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1de16-132">INPUTS</span></span>

### <span data-ttu-id="1de16-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1de16-133">System.String</span></span>

## <span data-ttu-id="1de16-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1de16-134">OUTPUTS</span></span>

### <span data-ttu-id="1de16-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1de16-135">System.Boolean</span></span>

## <span data-ttu-id="1de16-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1de16-136">NOTES</span></span>

## <span data-ttu-id="1de16-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1de16-137">RELATED LINKS</span></span>

[<span data-ttu-id="1de16-138">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1de16-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="1de16-139">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1de16-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="1de16-140">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1de16-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="1de16-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1de16-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
