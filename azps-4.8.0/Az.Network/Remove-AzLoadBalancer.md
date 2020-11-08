---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: 271033c39e049a423a15228968ad20c985b57036
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234955"
---
# <span data-ttu-id="506a1-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="506a1-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="506a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="506a1-102">SYNOPSIS</span></span>
<span data-ttu-id="506a1-103">Удаляет подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="506a1-103">Removes a load balancer.</span></span>

## <span data-ttu-id="506a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="506a1-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="506a1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="506a1-105">DESCRIPTION</span></span>
<span data-ttu-id="506a1-106">Командлет **Remove-AzLoadBalancer** Удаляет службу балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="506a1-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="506a1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="506a1-107">EXAMPLES</span></span>

### <span data-ttu-id="506a1-108">Пример 1: Удаление подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="506a1-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="506a1-109">Эта команда удаляет подсистему балансировки нагрузки с именем MyLoadBalancer в группе ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="506a1-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="506a1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="506a1-110">PARAMETERS</span></span>

### <span data-ttu-id="506a1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="506a1-111">-AsJob</span></span>
<span data-ttu-id="506a1-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="506a1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="506a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="506a1-113">-DefaultProfile</span></span>
<span data-ttu-id="506a1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="506a1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="506a1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="506a1-115">-Force</span></span>
<span data-ttu-id="506a1-116">Указывает на то, что этот командлет удаляет подсистему балансировки нагрузки независимо от того, назначены ли ему ресурсы.</span><span class="sxs-lookup"><span data-stu-id="506a1-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="506a1-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="506a1-117">-Name</span></span>
<span data-ttu-id="506a1-118">Указывает имя подсистемы балансировки нагрузки, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="506a1-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="506a1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="506a1-119">-PassThru</span></span>
<span data-ttu-id="506a1-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="506a1-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="506a1-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="506a1-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="506a1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="506a1-122">-ResourceGroupName</span></span>
<span data-ttu-id="506a1-123">Указывает имя группы ресурсов, содержащей подсистему балансировки нагрузки, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="506a1-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="506a1-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="506a1-124">-Confirm</span></span>
<span data-ttu-id="506a1-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="506a1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="506a1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="506a1-126">-WhatIf</span></span>
<span data-ttu-id="506a1-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="506a1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="506a1-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="506a1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="506a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="506a1-129">CommonParameters</span></span>
<span data-ttu-id="506a1-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="506a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="506a1-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="506a1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="506a1-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="506a1-132">INPUTS</span></span>

### <span data-ttu-id="506a1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="506a1-133">System.String</span></span>

## <span data-ttu-id="506a1-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="506a1-134">OUTPUTS</span></span>

### <span data-ttu-id="506a1-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="506a1-135">System.Boolean</span></span>

## <span data-ttu-id="506a1-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="506a1-136">NOTES</span></span>

## <span data-ttu-id="506a1-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="506a1-137">RELATED LINKS</span></span>

[<span data-ttu-id="506a1-138">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="506a1-138">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="506a1-139">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="506a1-139">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="506a1-140">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="506a1-140">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


