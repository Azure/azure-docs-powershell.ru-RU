---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 2e78b132019b19725a5261d58a760b3eb9988bb2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074355"
---
# <span data-ttu-id="e3eaa-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="e3eaa-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="e3eaa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="e3eaa-103">Создание политики WAF</span><span class="sxs-lookup"><span data-stu-id="e3eaa-103">Create WAF policy</span></span>

## <span data-ttu-id="e3eaa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3eaa-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3eaa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3eaa-105">DESCRIPTION</span></span>
<span data-ttu-id="e3eaa-106">Командлет **New-AzFrontDoorWafPolicy** создает новую политику WAF Azure в указанной группе ресурсов в разделе текущая подписка</span><span class="sxs-lookup"><span data-stu-id="e3eaa-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="e3eaa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3eaa-107">EXAMPLES</span></span>

### <span data-ttu-id="e3eaa-108">Пример 1: Создание политики WAF</span><span class="sxs-lookup"><span data-stu-id="e3eaa-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="e3eaa-109">Создание политики WAF</span><span class="sxs-lookup"><span data-stu-id="e3eaa-109">Create WAF policy</span></span>

## <span data-ttu-id="e3eaa-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3eaa-110">PARAMETERS</span></span>

### <span data-ttu-id="e3eaa-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="e3eaa-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="e3eaa-112">Настраиваемый текст ответа</span><span class="sxs-lookup"><span data-stu-id="e3eaa-112">Custom Response Body</span></span>

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

### <span data-ttu-id="e3eaa-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="e3eaa-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="e3eaa-114">Код состояния настраиваемого ответа</span><span class="sxs-lookup"><span data-stu-id="e3eaa-114">Custom Response Status Code</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3eaa-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="e3eaa-115">-Customrule</span></span>
<span data-ttu-id="e3eaa-116">Пользовательские правила в политике</span><span class="sxs-lookup"><span data-stu-id="e3eaa-116">Custom rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3eaa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3eaa-117">-DefaultProfile</span></span>
<span data-ttu-id="e3eaa-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3eaa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3eaa-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="e3eaa-119">-EnabledState</span></span>
<span data-ttu-id="e3eaa-120">Состояние политики: включено или отключено.</span><span class="sxs-lookup"><span data-stu-id="e3eaa-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="e3eaa-121">Возможные значения: "отключено", "включено"</span><span class="sxs-lookup"><span data-stu-id="e3eaa-121">Possible values include: 'Disabled', 'Enabled'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3eaa-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="e3eaa-122">-ManagedRule</span></span>
<span data-ttu-id="e3eaa-123">Управляемые правила в политике</span><span class="sxs-lookup"><span data-stu-id="e3eaa-123">Managed rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3eaa-124">Режим</span><span class="sxs-lookup"><span data-stu-id="e3eaa-124">-Mode</span></span>
<span data-ttu-id="e3eaa-125">Описывает, находится ли этот режим в режиме обнаружения или защиты на уровне политики.</span><span class="sxs-lookup"><span data-stu-id="e3eaa-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="e3eaa-126">Возможные значения: "Защита", "Обнаружение"</span><span class="sxs-lookup"><span data-stu-id="e3eaa-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="e3eaa-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e3eaa-127">-Name</span></span>
<span data-ttu-id="e3eaa-128">WebApplicationFireWallPolicy имя.</span><span class="sxs-lookup"><span data-stu-id="e3eaa-128">WebApplicationFireWallPolicy name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3eaa-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="e3eaa-129">-RedirectUrl</span></span>
<span data-ttu-id="e3eaa-130">URL-адрес перенаправления</span><span class="sxs-lookup"><span data-stu-id="e3eaa-130">Redirect URL</span></span>

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

### <span data-ttu-id="e3eaa-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3eaa-131">-ResourceGroupName</span></span>
<span data-ttu-id="e3eaa-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e3eaa-132">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3eaa-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3eaa-133">-Confirm</span></span>
<span data-ttu-id="e3eaa-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e3eaa-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3eaa-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3eaa-135">-WhatIf</span></span>
<span data-ttu-id="e3eaa-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e3eaa-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3eaa-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e3eaa-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3eaa-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3eaa-138">CommonParameters</span></span>
<span data-ttu-id="e3eaa-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3eaa-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3eaa-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3eaa-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3eaa-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3eaa-141">INPUTS</span></span>

### <span data-ttu-id="e3eaa-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="e3eaa-142">None</span></span>

## <span data-ttu-id="e3eaa-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3eaa-143">OUTPUTS</span></span>

### <span data-ttu-id="e3eaa-144">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="e3eaa-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="e3eaa-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3eaa-145">NOTES</span></span>

## <span data-ttu-id="e3eaa-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3eaa-146">RELATED LINKS</span></span>

<span data-ttu-id="e3eaa-147">[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="e3eaa-147">[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
