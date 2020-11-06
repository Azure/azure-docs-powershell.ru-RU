---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: dd47e858132dbe77556d82ce234d41bc2c990f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565232"
---
# <span data-ttu-id="a92f8-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a92f8-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="a92f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a92f8-102">SYNOPSIS</span></span>
<span data-ttu-id="a92f8-103">Удаление канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a92f8-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a92f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a92f8-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a92f8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a92f8-105">DESCRIPTION</span></span>
<span data-ttu-id="a92f8-106">Командлет **Remove-AzureRmExpressRouteCircuit** удаляет канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a92f8-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a92f8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a92f8-107">EXAMPLES</span></span>

### <span data-ttu-id="a92f8-108">Пример 1: удаление канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="a92f8-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="a92f8-109">Пример 2: удаление канала ExpressRoute с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="a92f8-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="a92f8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a92f8-110">PARAMETERS</span></span>

### <span data-ttu-id="a92f8-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a92f8-111">-Force</span></span>
<span data-ttu-id="a92f8-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a92f8-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a92f8-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a92f8-113">-Name</span></span>
<span data-ttu-id="a92f8-114">Имя удаляемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a92f8-114">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="a92f8-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a92f8-115">-PassThru</span></span>
<span data-ttu-id="a92f8-116">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="a92f8-116">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="a92f8-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a92f8-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a92f8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a92f8-118">-ResourceGroupName</span></span>
<span data-ttu-id="a92f8-119">Указывает имя группы ресурсов, которой принадлежит эта цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a92f8-119">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="a92f8-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a92f8-120">-Confirm</span></span>
<span data-ttu-id="a92f8-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a92f8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a92f8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a92f8-122">-WhatIf</span></span>
<span data-ttu-id="a92f8-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a92f8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a92f8-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a92f8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a92f8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a92f8-125">-DefaultProfile</span></span>
<span data-ttu-id="a92f8-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a92f8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a92f8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a92f8-127">CommonParameters</span></span>
<span data-ttu-id="a92f8-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a92f8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a92f8-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a92f8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a92f8-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a92f8-130">INPUTS</span></span>

## <span data-ttu-id="a92f8-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a92f8-131">OUTPUTS</span></span>

## <span data-ttu-id="a92f8-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="a92f8-132">NOTES</span></span>

## <span data-ttu-id="a92f8-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a92f8-133">RELATED LINKS</span></span>

[<span data-ttu-id="a92f8-134">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a92f8-134">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="a92f8-135">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a92f8-135">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="a92f8-136">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a92f8-136">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="a92f8-137">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a92f8-137">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
