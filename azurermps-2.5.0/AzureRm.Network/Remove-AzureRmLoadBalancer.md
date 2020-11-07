---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancer
schema: 2.0.0
ms.openlocfilehash: 96f6acdda93de63486f117c99572b4680fb025e6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913288"
---
# <span data-ttu-id="860bc-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="860bc-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="860bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="860bc-102">SYNOPSIS</span></span>
<span data-ttu-id="860bc-103">Удаляет подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="860bc-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="860bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="860bc-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="860bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="860bc-105">DESCRIPTION</span></span>
<span data-ttu-id="860bc-106">Командлет **Remove-AzureRmLoadBalancer** Удаляет службу балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="860bc-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="860bc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="860bc-107">EXAMPLES</span></span>

### <span data-ttu-id="860bc-108">Пример 1: Удаление подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="860bc-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="860bc-109">Эта команда удаляет подсистему балансировки нагрузки с именем MyLoadBalancer в группе ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="860bc-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="860bc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="860bc-110">PARAMETERS</span></span>

### <span data-ttu-id="860bc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="860bc-111">-AsJob</span></span>
<span data-ttu-id="860bc-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="860bc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="860bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="860bc-113">-DefaultProfile</span></span>
<span data-ttu-id="860bc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="860bc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="860bc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="860bc-115">-Force</span></span>
<span data-ttu-id="860bc-116">Указывает на то, что этот командлет удаляет подсистему балансировки нагрузки независимо от того, назначены ли ему ресурсы.</span><span class="sxs-lookup"><span data-stu-id="860bc-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="860bc-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="860bc-117">-Name</span></span>
<span data-ttu-id="860bc-118">Указывает имя подсистемы балансировки нагрузки, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="860bc-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="860bc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="860bc-119">-PassThru</span></span>
<span data-ttu-id="860bc-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="860bc-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="860bc-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="860bc-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="860bc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="860bc-122">-ResourceGroupName</span></span>
<span data-ttu-id="860bc-123">Указывает имя группы ресурсов, содержащей подсистему балансировки нагрузки, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="860bc-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="860bc-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="860bc-124">-Confirm</span></span>
<span data-ttu-id="860bc-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="860bc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="860bc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="860bc-126">-WhatIf</span></span>
<span data-ttu-id="860bc-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="860bc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="860bc-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="860bc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="860bc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="860bc-129">CommonParameters</span></span>
<span data-ttu-id="860bc-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="860bc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="860bc-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="860bc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="860bc-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="860bc-132">INPUTS</span></span>

## <span data-ttu-id="860bc-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="860bc-133">OUTPUTS</span></span>

## <span data-ttu-id="860bc-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="860bc-134">NOTES</span></span>

## <span data-ttu-id="860bc-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="860bc-135">RELATED LINKS</span></span>

[<span data-ttu-id="860bc-136">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="860bc-136">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="860bc-137">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="860bc-137">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="860bc-138">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="860bc-138">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


