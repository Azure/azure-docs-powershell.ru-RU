---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/remove-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Remove-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Remove-AzureRmPolicyRemediation.md
ms.openlocfilehash: ec5becd714b034789aeeb8449a63012232c99d5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732301"
---
# <span data-ttu-id="1e732-101">Remove-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="1e732-101">Remove-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="1e732-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e732-102">SYNOPSIS</span></span>
<span data-ttu-id="1e732-103">Удаление исправления политики.</span><span class="sxs-lookup"><span data-stu-id="1e732-103">Deletes a policy remediation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e732-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e732-104">SYNTAX</span></span>

### <span data-ttu-id="1e732-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1e732-105">ByName (Default)</span></span>
```
Remove-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e732-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1e732-106">ByResourceId</span></span>
```
Remove-AzureRmPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e732-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1e732-107">ByInputObject</span></span>
```
Remove-AzureRmPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e732-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e732-108">DESCRIPTION</span></span>
<span data-ttu-id="1e732-109">Командлет **remediation-AzureRmPolicyRemediation** удаляет исправление политики.</span><span class="sxs-lookup"><span data-stu-id="1e732-109">The **Remove-AzureRmPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="1e732-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e732-110">EXAMPLES</span></span>

### <span data-ttu-id="1e732-111">Пример 1: Удаление исправления политики на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1e732-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="1e732-112">Эта команда удаляет исправление с именем "remediation1" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="1e732-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="1e732-113">Пример 2: Удаление исправления группы управления с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="1e732-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzureRmPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzureRmPolicyRemediation -Confirm
```

<span data-ttu-id="1e732-114">Эта команда удаляет исправление с именем "remediation1" из группы управления "MG1".</span><span class="sxs-lookup"><span data-stu-id="1e732-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="1e732-115">Перед удалением ресурса появится запрос подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1e732-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="1e732-116">Пример 3: Отмена и удаление исправления политики</span><span class="sxs-lookup"><span data-stu-id="1e732-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="1e732-117">Эта команда удаляет исправление с именем "remediation1" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="1e732-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="1e732-118">Если исправление пройдет, оно будет отменено перед удалением.</span><span class="sxs-lookup"><span data-stu-id="1e732-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="1e732-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e732-119">PARAMETERS</span></span>

### <span data-ttu-id="1e732-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="1e732-120">-AllowStop</span></span>
<span data-ttu-id="1e732-121">Разрешение отмены исправления, если оно выполняется.</span><span class="sxs-lookup"><span data-stu-id="1e732-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="1e732-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e732-122">-AsJob</span></span>
<span data-ttu-id="1e732-123">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="1e732-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="1e732-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e732-124">-DefaultProfile</span></span>
<span data-ttu-id="1e732-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e732-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e732-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e732-126">-InputObject</span></span>
<span data-ttu-id="1e732-127">Объект исправления.</span><span class="sxs-lookup"><span data-stu-id="1e732-127">The Remediation object.</span></span>

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

### <span data-ttu-id="1e732-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="1e732-128">-ManagementGroupName</span></span>
<span data-ttu-id="1e732-129">Идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="1e732-129">Management group ID.</span></span>

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

### <span data-ttu-id="1e732-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1e732-130">-Name</span></span>
<span data-ttu-id="1e732-131">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="1e732-131">Resource name.</span></span>

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

### <span data-ttu-id="1e732-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e732-132">-PassThru</span></span>
<span data-ttu-id="1e732-133">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1e732-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="1e732-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e732-134">-ResourceGroupName</span></span>
<span data-ttu-id="1e732-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1e732-135">Resource group name.</span></span>

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

### <span data-ttu-id="1e732-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e732-136">-ResourceId</span></span>
<span data-ttu-id="1e732-137">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="1e732-137">Resource ID.</span></span>

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

### <span data-ttu-id="1e732-138">-Scope</span><span class="sxs-lookup"><span data-stu-id="1e732-138">-Scope</span></span>
<span data-ttu-id="1e732-139">Область действия ресурса.</span><span class="sxs-lookup"><span data-stu-id="1e732-139">Scope of the resource.</span></span>
<span data-ttu-id="1e732-140">Сокращен.</span><span class="sxs-lookup"><span data-stu-id="1e732-140">E.g.</span></span>
<span data-ttu-id="1e732-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="1e732-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="1e732-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e732-142">-Confirm</span></span>
<span data-ttu-id="1e732-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1e732-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e732-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e732-144">-WhatIf</span></span>
<span data-ttu-id="1e732-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1e732-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e732-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1e732-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e732-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e732-147">CommonParameters</span></span>
<span data-ttu-id="1e732-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e732-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e732-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e732-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e732-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e732-150">INPUTS</span></span>

### <span data-ttu-id="1e732-151">System. String</span><span class="sxs-lookup"><span data-stu-id="1e732-151">System.String</span></span>

### <span data-ttu-id="1e732-152">Microsoft. Azure. Commands. PolicyInsights. Models. unисправление. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="1e732-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="1e732-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e732-153">OUTPUTS</span></span>

### <span data-ttu-id="1e732-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1e732-154">System.Boolean</span></span>

## <span data-ttu-id="1e732-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e732-155">NOTES</span></span>

## <span data-ttu-id="1e732-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e732-156">RELATED LINKS</span></span>
