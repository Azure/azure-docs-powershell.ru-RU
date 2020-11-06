---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 3ea8e43710d9e195218cc1b96a2656af2a7e2adf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560263"
---
# <span data-ttu-id="f2360-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f2360-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="f2360-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2360-102">SYNOPSIS</span></span>
<span data-ttu-id="f2360-103">Удаление канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f2360-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2360-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2360-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2360-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2360-105">DESCRIPTION</span></span>
<span data-ttu-id="f2360-106">Командлет **Remove-AzureRmExpressRouteCircuit** удаляет канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f2360-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="f2360-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2360-107">EXAMPLES</span></span>

### <span data-ttu-id="f2360-108">Пример 1: удаление канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f2360-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="f2360-109">Пример 2: удаление канала ExpressRoute с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="f2360-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="f2360-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2360-110">PARAMETERS</span></span>

### <span data-ttu-id="f2360-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2360-111">-AsJob</span></span>
<span data-ttu-id="f2360-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f2360-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2360-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2360-113">-DefaultProfile</span></span>
<span data-ttu-id="f2360-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2360-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2360-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f2360-115">-Force</span></span>
<span data-ttu-id="f2360-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f2360-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f2360-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f2360-117">-Name</span></span>
<span data-ttu-id="f2360-118">Имя удаляемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f2360-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="f2360-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2360-119">-PassThru</span></span>
<span data-ttu-id="f2360-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f2360-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="f2360-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f2360-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f2360-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2360-122">-ResourceGroupName</span></span>
<span data-ttu-id="f2360-123">Указывает имя группы ресурсов, которой принадлежит эта цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f2360-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="f2360-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2360-124">-Confirm</span></span>
<span data-ttu-id="f2360-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f2360-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2360-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2360-126">-WhatIf</span></span>
<span data-ttu-id="f2360-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f2360-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2360-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f2360-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2360-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2360-129">CommonParameters</span></span>
<span data-ttu-id="f2360-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2360-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2360-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2360-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2360-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2360-132">INPUTS</span></span>

### <span data-ttu-id="f2360-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="f2360-133">None</span></span>
<span data-ttu-id="f2360-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f2360-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f2360-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2360-135">OUTPUTS</span></span>

## <span data-ttu-id="f2360-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2360-136">NOTES</span></span>

## <span data-ttu-id="f2360-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2360-137">RELATED LINKS</span></span>

[<span data-ttu-id="f2360-138">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f2360-138">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="f2360-139">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f2360-139">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="f2360-140">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f2360-140">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="f2360-141">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f2360-141">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
