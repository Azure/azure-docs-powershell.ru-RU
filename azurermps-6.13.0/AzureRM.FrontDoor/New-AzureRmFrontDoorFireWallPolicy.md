---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: b18f17830dd08f95c3d887ce272ff31e080001a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568916"
---
# <span data-ttu-id="be801-101">New-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="be801-101">New-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="be801-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be801-102">SYNOPSIS</span></span>
<span data-ttu-id="be801-103">Создание политики WAF</span><span class="sxs-lookup"><span data-stu-id="be801-103">Create WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be801-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be801-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be801-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be801-105">DESCRIPTION</span></span>
<span data-ttu-id="be801-106">Командлет **New-AzureRmFrontDoorFireWallPolicy** создает новую политику WAF Azure в указанной группе ресурсов в разделе текущая подписка</span><span class="sxs-lookup"><span data-stu-id="be801-106">The **New-AzureRmFrontDoorFireWallPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="be801-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be801-107">EXAMPLES</span></span>

### <span data-ttu-id="be801-108">Пример 1: Создание политики WAF</span><span class="sxs-lookup"><span data-stu-id="be801-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorFireWallPolicy -Name $Name -ResourceGroupName $resourceGroupName -Customrule $customRule1 -ManagedRule $managedRule1 -En
abledState Enabled -Mode Prevention


PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="be801-109">Создание политики WAF</span><span class="sxs-lookup"><span data-stu-id="be801-109">Create WAF policy</span></span>

## <span data-ttu-id="be801-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be801-110">PARAMETERS</span></span>

### <span data-ttu-id="be801-111">-Customrule</span><span class="sxs-lookup"><span data-stu-id="be801-111">-Customrule</span></span>
<span data-ttu-id="be801-112">Пользовательские правила в политике</span><span class="sxs-lookup"><span data-stu-id="be801-112">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="be801-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be801-113">-DefaultProfile</span></span>
<span data-ttu-id="be801-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be801-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be801-115">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="be801-115">-EnabledState</span></span>
<span data-ttu-id="be801-116">Состояние политики: включено или отключено.</span><span class="sxs-lookup"><span data-stu-id="be801-116">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="be801-117">Возможные значения: "отключено", "включено"</span><span class="sxs-lookup"><span data-stu-id="be801-117">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="be801-118">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="be801-118">-ManagedRule</span></span>
<span data-ttu-id="be801-119">Управляемые правила в политике</span><span class="sxs-lookup"><span data-stu-id="be801-119">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="be801-120">Режим</span><span class="sxs-lookup"><span data-stu-id="be801-120">-Mode</span></span>
<span data-ttu-id="be801-121">Описывает, находится ли этот режим в режиме обнаружения или защиты на уровне политики.</span><span class="sxs-lookup"><span data-stu-id="be801-121">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="be801-122">Возможные значения: "Защита", "Обнаружение"</span><span class="sxs-lookup"><span data-stu-id="be801-122">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="be801-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="be801-123">-Name</span></span>
<span data-ttu-id="be801-124">WebApplicationFireWallPolicy имя.</span><span class="sxs-lookup"><span data-stu-id="be801-124">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="be801-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be801-125">-ResourceGroupName</span></span>
<span data-ttu-id="be801-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="be801-126">The resource group name</span></span>

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

### <span data-ttu-id="be801-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be801-127">-Confirm</span></span>
<span data-ttu-id="be801-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="be801-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be801-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be801-129">-WhatIf</span></span>
<span data-ttu-id="be801-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="be801-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be801-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="be801-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be801-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be801-132">CommonParameters</span></span>
<span data-ttu-id="be801-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be801-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be801-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be801-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be801-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be801-135">INPUTS</span></span>

### <span data-ttu-id="be801-136">System. String</span><span class="sxs-lookup"><span data-stu-id="be801-136">System.String</span></span>

## <span data-ttu-id="be801-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be801-137">OUTPUTS</span></span>

### <span data-ttu-id="be801-138">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="be801-138">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="be801-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="be801-139">NOTES</span></span>

## <span data-ttu-id="be801-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be801-140">RELATED LINKS</span></span>

<span data-ttu-id="be801-141">[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md) 
 [Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md) 
 [New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md) 
 [New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="be801-141">[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)
[Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)
[New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span></span>
