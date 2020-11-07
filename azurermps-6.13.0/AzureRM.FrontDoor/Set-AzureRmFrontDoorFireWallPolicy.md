---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: a02510cc72b9e674f9d4fded1355ae5b2cadc807
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93731968"
---
# <span data-ttu-id="9e606-101">Set-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="9e606-101">Set-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="9e606-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e606-102">SYNOPSIS</span></span>
<span data-ttu-id="9e606-103">Обновление политики WAF</span><span class="sxs-lookup"><span data-stu-id="9e606-103">update WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e606-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e606-104">SYNTAX</span></span>

### <span data-ttu-id="9e606-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e606-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e606-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e606-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e606-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e606-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e606-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e606-108">DESCRIPTION</span></span>
<span data-ttu-id="9e606-109">Командлет **Set-AzureRmFrontDoor** обновляет СУЩЕСТВУЮЩУЮ политику WAF.</span><span class="sxs-lookup"><span data-stu-id="9e606-109">The **Set-AzureRmFrontDoor** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="9e606-110">Если входные параметры не предоставлены, будут использоваться старые параметры существующей политики WAF.</span><span class="sxs-lookup"><span data-stu-id="9e606-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="9e606-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e606-111">EXAMPLES</span></span>

### <span data-ttu-id="9e606-112">Пример 1: обновление существующей политики WAF</span><span class="sxs-lookup"><span data-stu-id="9e606-112">Example 1: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $node

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

<span data-ttu-id="9e606-113">Обновление существующей политики WAF</span><span class="sxs-lookup"><span data-stu-id="9e606-113">update an existing WAF policy</span></span>

### <span data-ttu-id="9e606-114">Пример 2: обновление существующей политики WAF</span><span class="sxs-lookup"><span data-stu-id="9e606-114">Example 2: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -InputObject $policy1 -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

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

<span data-ttu-id="9e606-115">Обновление существующей политики WAF</span><span class="sxs-lookup"><span data-stu-id="9e606-115">update an existing WAF policy</span></span>

### <span data-ttu-id="9e606-116">Пример 3: обновление существующей политики WAF</span><span class="sxs-lookup"><span data-stu-id="9e606-116">Example 3: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -ResourceId $resourcdId -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

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

<span data-ttu-id="9e606-117">Обновление существующей политики WAF</span><span class="sxs-lookup"><span data-stu-id="9e606-117">update an existing WAF policy</span></span>

### <span data-ttu-id="9e606-118">Пример 4: обновление всех политик WAF в $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="9e606-118">Example 4: update all WAF policies in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Set-AzureRmFrontDoorFireWallPolicy -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode
```

<span data-ttu-id="9e606-119">обновление всех политик WAF в $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="9e606-119">update all WAF policies in $resourceGroup</span></span>

## <span data-ttu-id="9e606-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e606-120">PARAMETERS</span></span>

### <span data-ttu-id="9e606-121">-Customrule</span><span class="sxs-lookup"><span data-stu-id="9e606-121">-Customrule</span></span>
<span data-ttu-id="9e606-122">Пользовательские правила в политике</span><span class="sxs-lookup"><span data-stu-id="9e606-122">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="9e606-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e606-123">-DefaultProfile</span></span>
<span data-ttu-id="9e606-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e606-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e606-125">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="9e606-125">-EnabledState</span></span>
<span data-ttu-id="9e606-126">Состояние политики: включено или отключено.</span><span class="sxs-lookup"><span data-stu-id="9e606-126">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="9e606-127">Возможные значения: "отключено", "включено"</span><span class="sxs-lookup"><span data-stu-id="9e606-127">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="9e606-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e606-128">-InputObject</span></span>
<span data-ttu-id="9e606-129">Объект FireWallPolicy, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="9e606-129">The FireWallPolicy object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e606-130">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="9e606-130">-ManagedRule</span></span>
<span data-ttu-id="9e606-131">Управляемые правила в политике</span><span class="sxs-lookup"><span data-stu-id="9e606-131">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="9e606-132">Режим</span><span class="sxs-lookup"><span data-stu-id="9e606-132">-Mode</span></span>
<span data-ttu-id="9e606-133">Описывает, находится ли этот режим в режиме обнаружения или защиты на уровне политики.</span><span class="sxs-lookup"><span data-stu-id="9e606-133">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="9e606-134">Возможные значения: "Защита", "Обнаружение"</span><span class="sxs-lookup"><span data-stu-id="9e606-134">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="9e606-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9e606-135">-Name</span></span>
<span data-ttu-id="9e606-136">Имя FireWallPolicy для обновления.</span><span class="sxs-lookup"><span data-stu-id="9e606-136">The name of the FireWallPolicy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e606-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e606-137">-ResourceGroupName</span></span>
<span data-ttu-id="9e606-138">Группа ресурсов, к которой принадлежит FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="9e606-138">The resource group to which the FireWallPolicy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e606-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e606-139">-ResourceId</span></span>
<span data-ttu-id="9e606-140">ИД ресурса обновляемого FireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="9e606-140">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e606-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e606-141">-Confirm</span></span>
<span data-ttu-id="9e606-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9e606-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e606-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e606-143">-WhatIf</span></span>
<span data-ttu-id="9e606-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9e606-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e606-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9e606-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e606-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e606-146">CommonParameters</span></span>
<span data-ttu-id="9e606-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e606-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e606-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e606-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e606-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e606-149">INPUTS</span></span>

### <span data-ttu-id="9e606-150">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="9e606-150">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="9e606-151">System. String</span><span class="sxs-lookup"><span data-stu-id="9e606-151">System.String</span></span>

## <span data-ttu-id="9e606-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e606-152">OUTPUTS</span></span>

### <span data-ttu-id="9e606-153">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="9e606-153">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="9e606-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e606-154">NOTES</span></span>

## <span data-ttu-id="9e606-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e606-155">RELATED LINKS</span></span>

<span data-ttu-id="9e606-156">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md) 
 [New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md) 
 [New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="9e606-156">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)
[New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span></span>
