---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: 4dbddf7e78297acc3f12f69dd2a44f9698f7b891
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909514"
---
# <span data-ttu-id="a3730-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a3730-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="a3730-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a3730-102">SYNOPSIS</span></span>
<span data-ttu-id="a3730-103">Удаление канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a3730-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a3730-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a3730-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3730-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3730-105">DESCRIPTION</span></span>
<span data-ttu-id="a3730-106">Командлет **Remove-AzExpressRouteCircuit** удаляет канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a3730-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a3730-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a3730-107">EXAMPLES</span></span>

### <span data-ttu-id="a3730-108">Пример 1: удаление канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="a3730-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="a3730-109">Пример 2: удаление канала ExpressRoute с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="a3730-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="a3730-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a3730-110">PARAMETERS</span></span>

### <span data-ttu-id="a3730-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3730-111">-AsJob</span></span>
<span data-ttu-id="a3730-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a3730-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3730-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3730-113">-DefaultProfile</span></span>
<span data-ttu-id="a3730-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3730-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3730-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a3730-115">-Force</span></span>
<span data-ttu-id="a3730-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a3730-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a3730-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a3730-117">-Name</span></span>
<span data-ttu-id="a3730-118">Имя удаляемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a3730-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="a3730-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3730-119">-PassThru</span></span>
<span data-ttu-id="a3730-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="a3730-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="a3730-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a3730-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a3730-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3730-122">-ResourceGroupName</span></span>
<span data-ttu-id="a3730-123">Указывает имя группы ресурсов, которой принадлежит эта цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a3730-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="a3730-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3730-124">-Confirm</span></span>
<span data-ttu-id="a3730-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a3730-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3730-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3730-126">-WhatIf</span></span>
<span data-ttu-id="a3730-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a3730-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3730-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a3730-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3730-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3730-129">CommonParameters</span></span>
<span data-ttu-id="a3730-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a3730-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3730-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3730-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3730-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a3730-132">INPUTS</span></span>

## <span data-ttu-id="a3730-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3730-133">OUTPUTS</span></span>

## <span data-ttu-id="a3730-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="a3730-134">NOTES</span></span>

## <span data-ttu-id="a3730-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3730-135">RELATED LINKS</span></span>

[<span data-ttu-id="a3730-136">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a3730-136">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a3730-137">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a3730-137">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="a3730-138">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a3730-138">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="a3730-139">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a3730-139">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
