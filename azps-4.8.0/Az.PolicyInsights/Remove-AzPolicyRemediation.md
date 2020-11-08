---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/remove-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
ms.openlocfilehash: 969b764be302231f33dda00b32afb79ec04a324e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244714"
---
# <span data-ttu-id="389ad-101">Remove-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="389ad-101">Remove-AzPolicyRemediation</span></span>

## <span data-ttu-id="389ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="389ad-102">SYNOPSIS</span></span>
<span data-ttu-id="389ad-103">Удаление исправления политики.</span><span class="sxs-lookup"><span data-stu-id="389ad-103">Deletes a policy remediation.</span></span>

## <span data-ttu-id="389ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="389ad-104">SYNTAX</span></span>

### <span data-ttu-id="389ad-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="389ad-105">ByName (Default)</span></span>
```
Remove-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="389ad-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="389ad-106">ByResourceId</span></span>
```
Remove-AzPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="389ad-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="389ad-107">ByInputObject</span></span>
```
Remove-AzPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="389ad-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="389ad-108">DESCRIPTION</span></span>
<span data-ttu-id="389ad-109">Командлет **remediation-AzPolicyRemediation** удаляет исправление политики.</span><span class="sxs-lookup"><span data-stu-id="389ad-109">The **Remove-AzPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="389ad-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="389ad-110">EXAMPLES</span></span>

### <span data-ttu-id="389ad-111">Пример 1: Удаление исправления политики на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="389ad-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="389ad-112">Эта команда удаляет исправление с именем "remediation1" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="389ad-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="389ad-113">Пример 2: Удаление исправления группы управления с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="389ad-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzPolicyRemediation -Confirm
```

<span data-ttu-id="389ad-114">Эта команда удаляет исправление с именем "remediation1" из группы управления "MG1".</span><span class="sxs-lookup"><span data-stu-id="389ad-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="389ad-115">Перед удалением ресурса появится запрос подтверждения.</span><span class="sxs-lookup"><span data-stu-id="389ad-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="389ad-116">Пример 3: Отмена и удаление исправления политики</span><span class="sxs-lookup"><span data-stu-id="389ad-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="389ad-117">Эта команда удаляет исправление с именем "remediation1" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="389ad-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="389ad-118">Если исправление пройдет, оно будет отменено перед удалением.</span><span class="sxs-lookup"><span data-stu-id="389ad-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="389ad-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="389ad-119">PARAMETERS</span></span>

### <span data-ttu-id="389ad-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="389ad-120">-AllowStop</span></span>
<span data-ttu-id="389ad-121">Разрешение отмены исправления, если оно выполняется.</span><span class="sxs-lookup"><span data-stu-id="389ad-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="389ad-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="389ad-122">-AsJob</span></span>
<span data-ttu-id="389ad-123">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="389ad-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="389ad-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="389ad-124">-DefaultProfile</span></span>
<span data-ttu-id="389ad-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="389ad-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="389ad-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="389ad-126">-InputObject</span></span>
<span data-ttu-id="389ad-127">Объект исправления.</span><span class="sxs-lookup"><span data-stu-id="389ad-127">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="389ad-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="389ad-128">-ManagementGroupName</span></span>
<span data-ttu-id="389ad-129">Идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="389ad-129">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="389ad-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="389ad-130">-Name</span></span>
<span data-ttu-id="389ad-131">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="389ad-131">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="389ad-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="389ad-132">-PassThru</span></span>
<span data-ttu-id="389ad-133">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="389ad-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="389ad-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="389ad-134">-ResourceGroupName</span></span>
<span data-ttu-id="389ad-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="389ad-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="389ad-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="389ad-136">-ResourceId</span></span>
<span data-ttu-id="389ad-137">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="389ad-137">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="389ad-138">-Scope</span><span class="sxs-lookup"><span data-stu-id="389ad-138">-Scope</span></span>
<span data-ttu-id="389ad-139">Область действия ресурса.</span><span class="sxs-lookup"><span data-stu-id="389ad-139">Scope of the resource.</span></span>
<span data-ttu-id="389ad-140">Сокращен.</span><span class="sxs-lookup"><span data-stu-id="389ad-140">E.g.</span></span>
<span data-ttu-id="389ad-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="389ad-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="389ad-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="389ad-142">-Confirm</span></span>
<span data-ttu-id="389ad-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="389ad-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="389ad-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="389ad-144">-WhatIf</span></span>
<span data-ttu-id="389ad-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="389ad-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="389ad-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="389ad-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="389ad-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="389ad-147">CommonParameters</span></span>
<span data-ttu-id="389ad-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="389ad-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="389ad-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="389ad-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="389ad-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="389ad-150">INPUTS</span></span>

### <span data-ttu-id="389ad-151">System. String</span><span class="sxs-lookup"><span data-stu-id="389ad-151">System.String</span></span>

### <span data-ttu-id="389ad-152">Microsoft. Azure. Commands. PolicyInsights. Models. unисправление. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="389ad-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="389ad-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="389ad-153">OUTPUTS</span></span>

### <span data-ttu-id="389ad-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="389ad-154">System.Boolean</span></span>

## <span data-ttu-id="389ad-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="389ad-155">NOTES</span></span>

## <span data-ttu-id="389ad-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="389ad-156">RELATED LINKS</span></span>
