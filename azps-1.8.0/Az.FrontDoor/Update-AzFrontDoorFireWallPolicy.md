---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/update-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: 3e0502d3503bdbf95fb81c779829b73e896b150f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900569"
---
# <span data-ttu-id="5659c-101">Update-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="5659c-101">Update-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="5659c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5659c-102">SYNOPSIS</span></span>
<span data-ttu-id="5659c-103">Обновление политики WAF</span><span class="sxs-lookup"><span data-stu-id="5659c-103">Update WAF policy</span></span>

## <span data-ttu-id="5659c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5659c-104">SYNTAX</span></span>

### <span data-ttu-id="5659c-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5659c-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5659c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5659c-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorFireWallPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5659c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5659c-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorFireWallPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5659c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5659c-108">DESCRIPTION</span></span>
<span data-ttu-id="5659c-109">Командлет **Update-AzFrontDoorFireWallPolicy** обновляет СУЩЕСТВУЮЩУЮ политику WAF.</span><span class="sxs-lookup"><span data-stu-id="5659c-109">The **Update-AzFrontDoorFireWallPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="5659c-110">Если входные параметры не предоставлены, будут использоваться старые параметры существующей политики WAF.</span><span class="sxs-lookup"><span data-stu-id="5659c-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="5659c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5659c-111">EXAMPLES</span></span>

### <span data-ttu-id="5659c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5659c-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="5659c-113">Обновление существующего кода состояния WAF политики.</span><span class="sxs-lookup"><span data-stu-id="5659c-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="5659c-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5659c-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="5659c-115">Обновите существующий режим политики WAF.</span><span class="sxs-lookup"><span data-stu-id="5659c-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="5659c-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5659c-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="5659c-117">Обновление состояния и режима действующей политики WAF.</span><span class="sxs-lookup"><span data-stu-id="5659c-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="5659c-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="5659c-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorFireWallPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="5659c-119">Обновление всех политик WAF в $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5659c-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="5659c-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5659c-120">PARAMETERS</span></span>

### <span data-ttu-id="5659c-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="5659c-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="5659c-122">Настраиваемый текст ответа</span><span class="sxs-lookup"><span data-stu-id="5659c-122">Custom Response Body</span></span>

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

### <span data-ttu-id="5659c-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="5659c-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="5659c-124">Код состояния настраиваемого ответа</span><span class="sxs-lookup"><span data-stu-id="5659c-124">Custom Response Status Code</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5659c-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="5659c-125">-Customrule</span></span>
<span data-ttu-id="5659c-126">Пользовательские правила в политике</span><span class="sxs-lookup"><span data-stu-id="5659c-126">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="5659c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5659c-127">-DefaultProfile</span></span>
<span data-ttu-id="5659c-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5659c-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5659c-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="5659c-129">-EnabledState</span></span>
<span data-ttu-id="5659c-130">Состояние политики: включено или отключено.</span><span class="sxs-lookup"><span data-stu-id="5659c-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="5659c-131">Возможные значения: "отключено", "включено"</span><span class="sxs-lookup"><span data-stu-id="5659c-131">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="5659c-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5659c-132">-InputObject</span></span>
<span data-ttu-id="5659c-133">Объект FireWallPolicy, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="5659c-133">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="5659c-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="5659c-134">-ManagedRule</span></span>
<span data-ttu-id="5659c-135">Управляемые правила в политике</span><span class="sxs-lookup"><span data-stu-id="5659c-135">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="5659c-136">Режим</span><span class="sxs-lookup"><span data-stu-id="5659c-136">-Mode</span></span>
<span data-ttu-id="5659c-137">Описывает, находится ли этот режим в режиме обнаружения или защиты на уровне политики.</span><span class="sxs-lookup"><span data-stu-id="5659c-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="5659c-138">Возможные значения: "Защита", "Обнаружение"</span><span class="sxs-lookup"><span data-stu-id="5659c-138">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="5659c-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5659c-139">-Name</span></span>
<span data-ttu-id="5659c-140">Имя FireWallPolicy для обновления.</span><span class="sxs-lookup"><span data-stu-id="5659c-140">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="5659c-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="5659c-141">-RedirectUrl</span></span>
<span data-ttu-id="5659c-142">URL-адрес перенаправления</span><span class="sxs-lookup"><span data-stu-id="5659c-142">Redirect URL</span></span>

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

### <span data-ttu-id="5659c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5659c-143">-ResourceGroupName</span></span>
<span data-ttu-id="5659c-144">Группа ресурсов, к которой принадлежит FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="5659c-144">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="5659c-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5659c-145">-ResourceId</span></span>
<span data-ttu-id="5659c-146">ИД ресурса обновляемого FireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="5659c-146">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5659c-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5659c-147">-Confirm</span></span>
<span data-ttu-id="5659c-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5659c-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5659c-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5659c-149">-WhatIf</span></span>
<span data-ttu-id="5659c-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5659c-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5659c-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5659c-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5659c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5659c-152">CommonParameters</span></span>
<span data-ttu-id="5659c-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5659c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5659c-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5659c-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5659c-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5659c-155">INPUTS</span></span>

### <span data-ttu-id="5659c-156">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="5659c-156">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="5659c-157">System. String</span><span class="sxs-lookup"><span data-stu-id="5659c-157">System.String</span></span>

## <span data-ttu-id="5659c-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5659c-158">OUTPUTS</span></span>

### <span data-ttu-id="5659c-159">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="5659c-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="5659c-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="5659c-160">NOTES</span></span>

## <span data-ttu-id="5659c-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5659c-161">RELATED LINKS</span></span>

<span data-ttu-id="5659c-162">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md) 
 [New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md) 
 [New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="5659c-162">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md)
[New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span></span>
