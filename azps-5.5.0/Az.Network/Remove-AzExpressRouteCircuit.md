---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: bc77c5d133561984f388e378f13595b3a72af785
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236593"
---
# <span data-ttu-id="a3240-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a3240-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="a3240-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3240-102">SYNOPSIS</span></span>
<span data-ttu-id="a3240-103">Удаляет канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a3240-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a3240-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a3240-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3240-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3240-105">DESCRIPTION</span></span>
<span data-ttu-id="a3240-106">Для **удаления каналов ExpressRoute удаляется cmdlet Remove-AzExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="a3240-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a3240-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a3240-107">EXAMPLES</span></span>

### <span data-ttu-id="a3240-108">Пример 1. Удаление схемы ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="a3240-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="a3240-109">Пример 2. Удаление каналов ExpressRoute с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="a3240-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="a3240-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3240-110">PARAMETERS</span></span>

### <span data-ttu-id="a3240-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3240-111">-AsJob</span></span>
<span data-ttu-id="a3240-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a3240-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3240-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3240-113">-DefaultProfile</span></span>
<span data-ttu-id="a3240-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3240-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3240-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a3240-115">-Force</span></span>
<span data-ttu-id="a3240-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a3240-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a3240-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a3240-117">-Name</span></span>
<span data-ttu-id="a3240-118">Имя удаляемого каналов ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a3240-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="a3240-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3240-119">-PassThru</span></span>
<span data-ttu-id="a3240-120">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="a3240-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="a3240-121">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a3240-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a3240-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3240-122">-ResourceGroupName</span></span>
<span data-ttu-id="a3240-123">Имя группы ресурсов, к которой принадлежит этот канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a3240-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="a3240-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3240-124">-Confirm</span></span>
<span data-ttu-id="a3240-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a3240-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3240-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3240-126">-WhatIf</span></span>
<span data-ttu-id="a3240-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3240-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3240-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a3240-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3240-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3240-129">CommonParameters</span></span>
<span data-ttu-id="a3240-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3240-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3240-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3240-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3240-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3240-132">INPUTS</span></span>

### <span data-ttu-id="a3240-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a3240-133">System.String</span></span>

## <span data-ttu-id="a3240-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a3240-134">OUTPUTS</span></span>

### <span data-ttu-id="a3240-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a3240-135">System.Boolean</span></span>

## <span data-ttu-id="a3240-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a3240-136">NOTES</span></span>

## <span data-ttu-id="a3240-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3240-137">RELATED LINKS</span></span>

[<span data-ttu-id="a3240-138">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a3240-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a3240-139">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a3240-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="a3240-140">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a3240-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="a3240-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a3240-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
