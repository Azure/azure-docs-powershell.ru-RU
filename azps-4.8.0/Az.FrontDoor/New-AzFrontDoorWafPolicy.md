---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 441e47b4ef2a796fcdf5ee802cba83f0fce7e352
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077752"
---
# <span data-ttu-id="8b9ce-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="8b9ce-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="8b9ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b9ce-102">SYNOPSIS</span></span>
<span data-ttu-id="8b9ce-103">Создание политики WAF</span><span class="sxs-lookup"><span data-stu-id="8b9ce-103">Create WAF policy</span></span>

## <span data-ttu-id="8b9ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b9ce-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b9ce-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b9ce-105">DESCRIPTION</span></span>
<span data-ttu-id="8b9ce-106">Командлет **New-AzFrontDoorWafPolicy** создает новую политику WAF Azure в указанной группе ресурсов в разделе текущая подписка</span><span class="sxs-lookup"><span data-stu-id="8b9ce-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="8b9ce-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b9ce-107">EXAMPLES</span></span>

### <span data-ttu-id="8b9ce-108">Пример 1: Создание политики WAF</span><span class="sxs-lookup"><span data-stu-id="8b9ce-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="8b9ce-109">Создание политики WAF</span><span class="sxs-lookup"><span data-stu-id="8b9ce-109">Create WAF policy</span></span>

## <span data-ttu-id="8b9ce-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b9ce-110">PARAMETERS</span></span>

### <span data-ttu-id="8b9ce-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="8b9ce-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="8b9ce-112">Настраиваемый текст ответа</span><span class="sxs-lookup"><span data-stu-id="8b9ce-112">Custom Response Body</span></span>

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

### <span data-ttu-id="8b9ce-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="8b9ce-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="8b9ce-114">Код состояния настраиваемого ответа</span><span class="sxs-lookup"><span data-stu-id="8b9ce-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="8b9ce-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="8b9ce-115">-Customrule</span></span>
<span data-ttu-id="8b9ce-116">Пользовательские правила в политике</span><span class="sxs-lookup"><span data-stu-id="8b9ce-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="8b9ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b9ce-117">-DefaultProfile</span></span>
<span data-ttu-id="8b9ce-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b9ce-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b9ce-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="8b9ce-119">-EnabledState</span></span>
<span data-ttu-id="8b9ce-120">Состояние политики: включено или отключено.</span><span class="sxs-lookup"><span data-stu-id="8b9ce-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="8b9ce-121">Возможные значения: "отключено", "включено"</span><span class="sxs-lookup"><span data-stu-id="8b9ce-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="8b9ce-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="8b9ce-122">-ManagedRule</span></span>
<span data-ttu-id="8b9ce-123">Управляемые правила в политике</span><span class="sxs-lookup"><span data-stu-id="8b9ce-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="8b9ce-124">Режим</span><span class="sxs-lookup"><span data-stu-id="8b9ce-124">-Mode</span></span>
<span data-ttu-id="8b9ce-125">Описывает, находится ли этот режим в режиме обнаружения или защиты на уровне политики.</span><span class="sxs-lookup"><span data-stu-id="8b9ce-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="8b9ce-126">Возможные значения: "Защита", "Обнаружение"</span><span class="sxs-lookup"><span data-stu-id="8b9ce-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="8b9ce-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8b9ce-127">-Name</span></span>
<span data-ttu-id="8b9ce-128">WebApplicationFireWallPolicy имя.</span><span class="sxs-lookup"><span data-stu-id="8b9ce-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="8b9ce-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="8b9ce-129">-RedirectUrl</span></span>
<span data-ttu-id="8b9ce-130">URL-адрес перенаправления</span><span class="sxs-lookup"><span data-stu-id="8b9ce-130">Redirect URL</span></span>

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

### <span data-ttu-id="8b9ce-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b9ce-131">-ResourceGroupName</span></span>
<span data-ttu-id="8b9ce-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8b9ce-132">The resource group name</span></span>

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

### <span data-ttu-id="8b9ce-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b9ce-133">-Confirm</span></span>
<span data-ttu-id="8b9ce-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8b9ce-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b9ce-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b9ce-135">-WhatIf</span></span>
<span data-ttu-id="8b9ce-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8b9ce-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b9ce-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8b9ce-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b9ce-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b9ce-138">CommonParameters</span></span>
<span data-ttu-id="8b9ce-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b9ce-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b9ce-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b9ce-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b9ce-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b9ce-141">INPUTS</span></span>

### <span data-ttu-id="8b9ce-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="8b9ce-142">None</span></span>

## <span data-ttu-id="8b9ce-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b9ce-143">OUTPUTS</span></span>

### <span data-ttu-id="8b9ce-144">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="8b9ce-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="8b9ce-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b9ce-145">NOTES</span></span>

## <span data-ttu-id="8b9ce-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b9ce-146">RELATED LINKS</span></span>

<span data-ttu-id="8b9ce-147">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="8b9ce-147">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
