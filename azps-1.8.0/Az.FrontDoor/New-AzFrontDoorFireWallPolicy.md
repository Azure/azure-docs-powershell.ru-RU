---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: 9b1339d138087207b84a7f515c66bd9964420dcd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401493"
---
# <span data-ttu-id="43e8a-101">New-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="43e8a-101">New-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="43e8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="43e8a-103">Создание политики WAF</span><span class="sxs-lookup"><span data-stu-id="43e8a-103">Create WAF policy</span></span>

## <span data-ttu-id="43e8a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="43e8a-104">SYNTAX</span></span>

```
New-AzFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43e8a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43e8a-105">DESCRIPTION</span></span>
<span data-ttu-id="43e8a-106">С **помощью cmdlet New-AzFrontDoorFireWallPolicy** в указанной группе ресурсов в текущей подписке создается новая политика Azure WAF.</span><span class="sxs-lookup"><span data-stu-id="43e8a-106">The **New-AzFrontDoorFireWallPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="43e8a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="43e8a-107">EXAMPLES</span></span>

### <span data-ttu-id="43e8a-108">Пример 1. Создание политики WAF</span><span class="sxs-lookup"><span data-stu-id="43e8a-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="43e8a-109">Создание политики WAF</span><span class="sxs-lookup"><span data-stu-id="43e8a-109">Create WAF policy</span></span>

## <span data-ttu-id="43e8a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43e8a-110">PARAMETERS</span></span>

### <span data-ttu-id="43e8a-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="43e8a-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="43e8a-112">Настраиваемый тело ответа</span><span class="sxs-lookup"><span data-stu-id="43e8a-112">Custom Response Body</span></span>

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

### <span data-ttu-id="43e8a-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="43e8a-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="43e8a-114">Пользовательский код состояния ответа</span><span class="sxs-lookup"><span data-stu-id="43e8a-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="43e8a-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="43e8a-115">-Customrule</span></span>
<span data-ttu-id="43e8a-116">Настраиваемые правила в политике</span><span class="sxs-lookup"><span data-stu-id="43e8a-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="43e8a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43e8a-117">-DefaultProfile</span></span>
<span data-ttu-id="43e8a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43e8a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43e8a-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="43e8a-119">-EnabledState</span></span>
<span data-ttu-id="43e8a-120">Состояние политики (включена или отключена).</span><span class="sxs-lookup"><span data-stu-id="43e8a-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="43e8a-121">Возможные значения: "Отключено", "Включено"</span><span class="sxs-lookup"><span data-stu-id="43e8a-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="43e8a-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="43e8a-122">-ManagedRule</span></span>
<span data-ttu-id="43e8a-123">Управляемые правила в политике</span><span class="sxs-lookup"><span data-stu-id="43e8a-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="43e8a-124">-Mode</span><span class="sxs-lookup"><span data-stu-id="43e8a-124">-Mode</span></span>
<span data-ttu-id="43e8a-125">В нем описывается, находится ли он в режиме обнаружения или режиме предотвращения на уровне политики.</span><span class="sxs-lookup"><span data-stu-id="43e8a-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="43e8a-126">Возможные значения: 'Prevention', 'Detection'</span><span class="sxs-lookup"><span data-stu-id="43e8a-126">Possible values include:'Prevention', 'Detection'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMode
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e8a-127">-Name</span><span class="sxs-lookup"><span data-stu-id="43e8a-127">-Name</span></span>
<span data-ttu-id="43e8a-128">Имя WebApplicationFireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="43e8a-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="43e8a-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="43e8a-129">-RedirectUrl</span></span>
<span data-ttu-id="43e8a-130">URL-адрес перенаправления</span><span class="sxs-lookup"><span data-stu-id="43e8a-130">Redirect URL</span></span>

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

### <span data-ttu-id="43e8a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43e8a-131">-ResourceGroupName</span></span>
<span data-ttu-id="43e8a-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="43e8a-132">The resource group name</span></span>

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

### <span data-ttu-id="43e8a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43e8a-133">-Confirm</span></span>
<span data-ttu-id="43e8a-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="43e8a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43e8a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43e8a-135">-WhatIf</span></span>
<span data-ttu-id="43e8a-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43e8a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43e8a-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="43e8a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43e8a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43e8a-138">CommonParameters</span></span>
<span data-ttu-id="43e8a-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43e8a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43e8a-140">Дополнительные сведения см. [в about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43e8a-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43e8a-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43e8a-141">INPUTS</span></span>

### <span data-ttu-id="43e8a-142">Нет</span><span class="sxs-lookup"><span data-stu-id="43e8a-142">None</span></span>

## <span data-ttu-id="43e8a-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="43e8a-143">OUTPUTS</span></span>

### <span data-ttu-id="43e8a-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="43e8a-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="43e8a-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="43e8a-145">NOTES</span></span>

## <span data-ttu-id="43e8a-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43e8a-146">RELATED LINKS</span></span>

<span data-ttu-id="43e8a-147">[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md) 
 [Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md) 
 [Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md) 
 [New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md) 
 [New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="43e8a-147">[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)
[Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md)
[New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span></span>
