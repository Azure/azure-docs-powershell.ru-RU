---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: bc77c5d133561984f388e378f13595b3a72af785
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244794"
---
# <span data-ttu-id="fb1e0-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fb1e0-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="fb1e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb1e0-102">SYNOPSIS</span></span>
<span data-ttu-id="fb1e0-103">Удаление канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fb1e0-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="fb1e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb1e0-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb1e0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb1e0-105">DESCRIPTION</span></span>
<span data-ttu-id="fb1e0-106">Командлет **Remove-AzExpressRouteCircuit** удаляет канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fb1e0-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="fb1e0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb1e0-107">EXAMPLES</span></span>

### <span data-ttu-id="fb1e0-108">Пример 1: удаление канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="fb1e0-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="fb1e0-109">Пример 2: удаление канала ExpressRoute с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="fb1e0-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="fb1e0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb1e0-110">PARAMETERS</span></span>

### <span data-ttu-id="fb1e0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb1e0-111">-AsJob</span></span>
<span data-ttu-id="fb1e0-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fb1e0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb1e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb1e0-113">-DefaultProfile</span></span>
<span data-ttu-id="fb1e0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb1e0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb1e0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fb1e0-115">-Force</span></span>
<span data-ttu-id="fb1e0-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="fb1e0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fb1e0-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fb1e0-117">-Name</span></span>
<span data-ttu-id="fb1e0-118">Имя удаляемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fb1e0-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="fb1e0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb1e0-119">-PassThru</span></span>
<span data-ttu-id="fb1e0-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="fb1e0-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="fb1e0-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="fb1e0-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fb1e0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb1e0-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb1e0-123">Указывает имя группы ресурсов, которой принадлежит эта цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fb1e0-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="fb1e0-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb1e0-124">-Confirm</span></span>
<span data-ttu-id="fb1e0-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fb1e0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb1e0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb1e0-126">-WhatIf</span></span>
<span data-ttu-id="fb1e0-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fb1e0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb1e0-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fb1e0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb1e0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb1e0-129">CommonParameters</span></span>
<span data-ttu-id="fb1e0-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb1e0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb1e0-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb1e0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb1e0-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb1e0-132">INPUTS</span></span>

### <span data-ttu-id="fb1e0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fb1e0-133">System.String</span></span>

## <span data-ttu-id="fb1e0-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb1e0-134">OUTPUTS</span></span>

### <span data-ttu-id="fb1e0-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb1e0-135">System.Boolean</span></span>

## <span data-ttu-id="fb1e0-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb1e0-136">NOTES</span></span>

## <span data-ttu-id="fb1e0-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb1e0-137">RELATED LINKS</span></span>

[<span data-ttu-id="fb1e0-138">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fb1e0-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="fb1e0-139">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fb1e0-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="fb1e0-140">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fb1e0-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="fb1e0-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fb1e0-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
