---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/remove-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
ms.openlocfilehash: 969b764be302231f33dda00b32afb79ec04a324e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417908"
---
# <span data-ttu-id="89318-101">Remove-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="89318-101">Remove-AzPolicyRemediation</span></span>

## <span data-ttu-id="89318-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89318-102">SYNOPSIS</span></span>
<span data-ttu-id="89318-103">Удаляет исправление политики.</span><span class="sxs-lookup"><span data-stu-id="89318-103">Deletes a policy remediation.</span></span>

## <span data-ttu-id="89318-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="89318-104">SYNTAX</span></span>

### <span data-ttu-id="89318-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89318-105">ByName (Default)</span></span>
```
Remove-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89318-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="89318-106">ByResourceId</span></span>
```
Remove-AzPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89318-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="89318-107">ByInputObject</span></span>
```
Remove-AzPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89318-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89318-108">DESCRIPTION</span></span>
<span data-ttu-id="89318-109">Для удаления исправлений политики будет удалена **cmdlet Remove-AzPolicyRemediation.**</span><span class="sxs-lookup"><span data-stu-id="89318-109">The **Remove-AzPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="89318-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="89318-110">EXAMPLES</span></span>

### <span data-ttu-id="89318-111">Пример 1. Удаление исправлений политики в области группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="89318-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="89318-112">Эта команда удаляет исправление с именем "исправление1" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="89318-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="89318-113">Пример 2. Удаление исправлений для группы управления с помощью piping</span><span class="sxs-lookup"><span data-stu-id="89318-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzPolicyRemediation -Confirm
```

<span data-ttu-id="89318-114">Эта команда удаляет исправление с именем "исправление1" из группы управления "mg1".</span><span class="sxs-lookup"><span data-stu-id="89318-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="89318-115">Перед удалением ресурса будет предложено подтвердить удаление.</span><span class="sxs-lookup"><span data-stu-id="89318-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="89318-116">Пример 3. Отмена и удаление исправлений политики</span><span class="sxs-lookup"><span data-stu-id="89318-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="89318-117">Эта команда удаляет исправление с именем "исправление1" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="89318-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="89318-118">Если исправление уже идет, оно будет отменено перед удалением.</span><span class="sxs-lookup"><span data-stu-id="89318-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="89318-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89318-119">PARAMETERS</span></span>

### <span data-ttu-id="89318-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="89318-120">-AllowStop</span></span>
<span data-ttu-id="89318-121">Разрешить отмену исправлений, если она еще идет.</span><span class="sxs-lookup"><span data-stu-id="89318-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="89318-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89318-122">-AsJob</span></span>
<span data-ttu-id="89318-123">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="89318-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="89318-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89318-124">-DefaultProfile</span></span>
<span data-ttu-id="89318-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89318-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89318-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89318-126">-InputObject</span></span>
<span data-ttu-id="89318-127">Объект исправлений.</span><span class="sxs-lookup"><span data-stu-id="89318-127">The Remediation object.</span></span>

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

### <span data-ttu-id="89318-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="89318-128">-ManagementGroupName</span></span>
<span data-ttu-id="89318-129">ИД группы управления.</span><span class="sxs-lookup"><span data-stu-id="89318-129">Management group ID.</span></span>

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

### <span data-ttu-id="89318-130">-Name</span><span class="sxs-lookup"><span data-stu-id="89318-130">-Name</span></span>
<span data-ttu-id="89318-131">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="89318-131">Resource name.</span></span>

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

### <span data-ttu-id="89318-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89318-132">-PassThru</span></span>
<span data-ttu-id="89318-133">Если команда успешно завершена, возвращается "Истина".</span><span class="sxs-lookup"><span data-stu-id="89318-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="89318-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89318-134">-ResourceGroupName</span></span>
<span data-ttu-id="89318-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89318-135">Resource group name.</span></span>

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

### <span data-ttu-id="89318-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89318-136">-ResourceId</span></span>
<span data-ttu-id="89318-137">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="89318-137">Resource ID.</span></span>

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

### <span data-ttu-id="89318-138">-Scope</span><span class="sxs-lookup"><span data-stu-id="89318-138">-Scope</span></span>
<span data-ttu-id="89318-139">Область действия ресурса.</span><span class="sxs-lookup"><span data-stu-id="89318-139">Scope of the resource.</span></span>
<span data-ttu-id="89318-140">Например,</span><span class="sxs-lookup"><span data-stu-id="89318-140">E.g.</span></span>
<span data-ttu-id="89318-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="89318-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="89318-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89318-142">-Confirm</span></span>
<span data-ttu-id="89318-143">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89318-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89318-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89318-144">-WhatIf</span></span>
<span data-ttu-id="89318-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89318-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89318-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="89318-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89318-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89318-147">CommonParameters</span></span>
<span data-ttu-id="89318-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89318-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89318-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89318-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89318-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89318-150">INPUTS</span></span>

### <span data-ttu-id="89318-151">System.String</span><span class="sxs-lookup"><span data-stu-id="89318-151">System.String</span></span>

### <span data-ttu-id="89318-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="89318-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="89318-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89318-153">OUTPUTS</span></span>

### <span data-ttu-id="89318-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="89318-154">System.Boolean</span></span>

## <span data-ttu-id="89318-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="89318-155">NOTES</span></span>

## <span data-ttu-id="89318-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89318-156">RELATED LINKS</span></span>
