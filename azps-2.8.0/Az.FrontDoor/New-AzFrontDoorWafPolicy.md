---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 0612f8bddf69e36fe8084bf27dbb44635059ee1a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408922"
---
# <span data-ttu-id="60649-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="60649-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="60649-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60649-102">SYNOPSIS</span></span>
<span data-ttu-id="60649-103">Создание политики WAF</span><span class="sxs-lookup"><span data-stu-id="60649-103">Create WAF policy</span></span>

## <span data-ttu-id="60649-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="60649-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60649-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60649-105">DESCRIPTION</span></span>
<span data-ttu-id="60649-106">Для создания политики Azure WAF в указанной группе ресурсов в текущей подписке будет создаваться новый cmdlet **AzFrontDoorWafPolicy.**</span><span class="sxs-lookup"><span data-stu-id="60649-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="60649-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="60649-107">EXAMPLES</span></span>

### <span data-ttu-id="60649-108">Пример 1. Создание политики WAF</span><span class="sxs-lookup"><span data-stu-id="60649-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="60649-109">Создание политики WAF</span><span class="sxs-lookup"><span data-stu-id="60649-109">Create WAF policy</span></span>

## <span data-ttu-id="60649-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60649-110">PARAMETERS</span></span>

### <span data-ttu-id="60649-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="60649-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="60649-112">Настраиваемый тело ответа</span><span class="sxs-lookup"><span data-stu-id="60649-112">Custom Response Body</span></span>

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

### <span data-ttu-id="60649-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="60649-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="60649-114">Пользовательский код состояния ответа</span><span class="sxs-lookup"><span data-stu-id="60649-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="60649-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="60649-115">-Customrule</span></span>
<span data-ttu-id="60649-116">Настраиваемые правила в политике</span><span class="sxs-lookup"><span data-stu-id="60649-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="60649-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60649-117">-DefaultProfile</span></span>
<span data-ttu-id="60649-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60649-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60649-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="60649-119">-EnabledState</span></span>
<span data-ttu-id="60649-120">Состояние политики (включена или отключена).</span><span class="sxs-lookup"><span data-stu-id="60649-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="60649-121">Возможные значения: "Отключено", "Включено"</span><span class="sxs-lookup"><span data-stu-id="60649-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="60649-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="60649-122">-ManagedRule</span></span>
<span data-ttu-id="60649-123">Управляемые правила в политике</span><span class="sxs-lookup"><span data-stu-id="60649-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="60649-124">-Mode</span><span class="sxs-lookup"><span data-stu-id="60649-124">-Mode</span></span>
<span data-ttu-id="60649-125">В нем описывается, находится ли он в режиме обнаружения или режиме предотвращения на уровне политики.</span><span class="sxs-lookup"><span data-stu-id="60649-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="60649-126">Возможные значения: 'Prevention', 'Detection'</span><span class="sxs-lookup"><span data-stu-id="60649-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="60649-127">-Name</span><span class="sxs-lookup"><span data-stu-id="60649-127">-Name</span></span>
<span data-ttu-id="60649-128">Имя WebApplicationFireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="60649-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="60649-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="60649-129">-RedirectUrl</span></span>
<span data-ttu-id="60649-130">URL-адрес перенаправления</span><span class="sxs-lookup"><span data-stu-id="60649-130">Redirect URL</span></span>

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

### <span data-ttu-id="60649-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60649-131">-ResourceGroupName</span></span>
<span data-ttu-id="60649-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="60649-132">The resource group name</span></span>

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

### <span data-ttu-id="60649-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60649-133">-Confirm</span></span>
<span data-ttu-id="60649-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="60649-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60649-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60649-135">-WhatIf</span></span>
<span data-ttu-id="60649-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60649-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60649-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="60649-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60649-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60649-138">CommonParameters</span></span>
<span data-ttu-id="60649-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60649-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60649-140">Дополнительные сведения см. [в about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60649-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60649-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60649-141">INPUTS</span></span>

### <span data-ttu-id="60649-142">Нет</span><span class="sxs-lookup"><span data-stu-id="60649-142">None</span></span>

## <span data-ttu-id="60649-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="60649-143">OUTPUTS</span></span>

### <span data-ttu-id="60649-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="60649-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="60649-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="60649-145">NOTES</span></span>

## <span data-ttu-id="60649-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60649-146">RELATED LINKS</span></span>

<span data-ttu-id="60649-147">[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="60649-147">[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
