---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: e9a93b66f62f6a42ba400dd84b6890cdf9f81cec
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913291"
---
# <span data-ttu-id="e5fb4-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5fb4-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="e5fb4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="e5fb4-103">Удаление канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5fb4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5fb4-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5fb4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5fb4-105">DESCRIPTION</span></span>
<span data-ttu-id="e5fb4-106">Командлет **Remove-AzureRmExpressRouteCircuit** удаляет канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="e5fb4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5fb4-107">EXAMPLES</span></span>

### <span data-ttu-id="e5fb4-108">Пример 1: удаление канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="e5fb4-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="e5fb4-109">Пример 2: удаление канала ExpressRoute с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="e5fb4-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="e5fb4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5fb4-110">PARAMETERS</span></span>

### <span data-ttu-id="e5fb4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5fb4-111">-AsJob</span></span>
<span data-ttu-id="e5fb4-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e5fb4-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5fb4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5fb4-113">-DefaultProfile</span></span>
<span data-ttu-id="e5fb4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5fb4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e5fb4-115">-Force</span></span>
<span data-ttu-id="e5fb4-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5fb4-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e5fb4-117">-Name</span></span>
<span data-ttu-id="e5fb4-118">Имя удаляемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-118">The name of the ExpressRoute circuit to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fb4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5fb4-119">-PassThru</span></span>
<span data-ttu-id="e5fb4-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="e5fb4-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5fb4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5fb4-122">-ResourceGroupName</span></span>
<span data-ttu-id="e5fb4-123">Указывает имя группы ресурсов, которой принадлежит эта цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fb4-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5fb4-124">-Confirm</span></span>
<span data-ttu-id="e5fb4-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5fb4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5fb4-126">-WhatIf</span></span>
<span data-ttu-id="e5fb4-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5fb4-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5fb4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5fb4-129">CommonParameters</span></span>
<span data-ttu-id="e5fb4-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5fb4-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5fb4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5fb4-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5fb4-132">INPUTS</span></span>

## <span data-ttu-id="e5fb4-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5fb4-133">OUTPUTS</span></span>

## <span data-ttu-id="e5fb4-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5fb4-134">NOTES</span></span>

## <span data-ttu-id="e5fb4-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5fb4-135">RELATED LINKS</span></span>

[<span data-ttu-id="e5fb4-136">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5fb4-136">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e5fb4-137">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5fb4-137">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e5fb4-138">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5fb4-138">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e5fb4-139">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5fb4-139">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
