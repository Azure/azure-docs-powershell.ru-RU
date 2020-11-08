---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: b8913ead9844a55190a6117f57f01d243e004fde
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249222"
---
# <span data-ttu-id="d2026-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="d2026-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="d2026-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2026-102">SYNOPSIS</span></span>
<span data-ttu-id="d2026-103">Обновление существующего задания в виде чертежей.</span><span class="sxs-lookup"><span data-stu-id="d2026-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="d2026-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2026-104">SYNTAX</span></span>

### <span data-ttu-id="d2026-105">UpdateBlueprintAssignment (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2026-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2026-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="d2026-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2026-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2026-107">DESCRIPTION</span></span>
<span data-ttu-id="d2026-108">Обновление существующего задания в виде чертежей.</span><span class="sxs-lookup"><span data-stu-id="d2026-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="d2026-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2026-109">EXAMPLES</span></span>

### <span data-ttu-id="d2026-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d2026-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="d2026-111">Обновите существующее назначение для определения плана `$blueprintObject` в указанной подписке, обновив параметры.</span><span class="sxs-lookup"><span data-stu-id="d2026-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="d2026-112">Использует присвоенное системой удостоверение.</span><span class="sxs-lookup"><span data-stu-id="d2026-112">Uses system-assigned identity.</span></span> <span data-ttu-id="d2026-113">Расположение определяет регион для создания управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="d2026-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="d2026-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d2026-114">Example 2</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="d2026-115">Обновление существующего задания из схемы с помощью файла подборки.</span><span class="sxs-lookup"><span data-stu-id="d2026-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="d2026-116">Формат файла подборки можно найти в образцах запросов и ответов по адресу: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="d2026-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="d2026-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d2026-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="d2026-118">Обновите существующее назначение для определения `$blueprintObject` плана, предназначенного для указанной подписки в указанной группе управления, с помощью определенного параметра.</span><span class="sxs-lookup"><span data-stu-id="d2026-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="d2026-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2026-119">PARAMETERS</span></span>

### <span data-ttu-id="d2026-120">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="d2026-120">-AssignmentFile</span></span>
<span data-ttu-id="d2026-121">Расположение файла назначения в формате JSON на диске.</span><span class="sxs-lookup"><span data-stu-id="d2026-121">Location of the assignment file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2026-122">-Чертеж</span><span class="sxs-lookup"><span data-stu-id="d2026-122">-Blueprint</span></span>
<span data-ttu-id="d2026-123">Объект чертежа.</span><span class="sxs-lookup"><span data-stu-id="d2026-123">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2026-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2026-124">-DefaultProfile</span></span>
<span data-ttu-id="d2026-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2026-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2026-126">-Location</span><span class="sxs-lookup"><span data-stu-id="d2026-126">-Location</span></span>
<span data-ttu-id="d2026-127">Регион для создания управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="d2026-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="d2026-128">Дополнительные сведения по адресу aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="d2026-128">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2026-129">-Lock</span><span class="sxs-lookup"><span data-stu-id="d2026-129">-Lock</span></span>
<span data-ttu-id="d2026-130">Блокировка ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2026-130">Lock resources.</span></span>
<span data-ttu-id="d2026-131">Дополнительные сведения по адресу aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="d2026-131">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: UpdateBlueprintAssignment
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2026-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d2026-132">-ManagementGroupId</span></span>
<span data-ttu-id="d2026-133">Идентификатор группы управления, в которой будут сохранены назначения для чертежей.</span><span class="sxs-lookup"><span data-stu-id="d2026-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2026-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d2026-134">-Name</span></span>
<span data-ttu-id="d2026-135">Имя назначения для схемы.</span><span class="sxs-lookup"><span data-stu-id="d2026-135">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2026-136">-Параметр</span><span class="sxs-lookup"><span data-stu-id="d2026-136">-Parameter</span></span>
<span data-ttu-id="d2026-137">Параметр артефакта.</span><span class="sxs-lookup"><span data-stu-id="d2026-137">Artifact parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2026-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="d2026-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="d2026-139">Хэш-таблица параметров для передачи артефакту группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2026-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2026-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="d2026-140">-SecureStringParameter</span></span>
<span data-ttu-id="d2026-141">Параметр Secure String для идентификатора ресурса KeyVault, имени и версии.</span><span class="sxs-lookup"><span data-stu-id="d2026-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2026-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2026-142">-SubscriptionId</span></span>
<span data-ttu-id="d2026-143">SubscriptionId, чтобы назначить проект.</span><span class="sxs-lookup"><span data-stu-id="d2026-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="d2026-144">Может быть списком из строк subscriptionId, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="d2026-144">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2026-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d2026-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="d2026-146">Система присвоила идентификатор (MSI) для развертывания артефактов.</span><span class="sxs-lookup"><span data-stu-id="d2026-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2026-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d2026-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="d2026-148">Идентификатор (MSI), назначенный пользователю для развертывания артефактов.</span><span class="sxs-lookup"><span data-stu-id="d2026-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2026-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2026-149">-Confirm</span></span>
<span data-ttu-id="d2026-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d2026-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2026-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2026-151">-WhatIf</span></span>
<span data-ttu-id="d2026-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d2026-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2026-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d2026-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2026-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2026-154">CommonParameters</span></span>
<span data-ttu-id="d2026-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2026-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2026-156">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2026-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2026-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2026-157">INPUTS</span></span>

### <span data-ttu-id="d2026-158">System. String</span><span class="sxs-lookup"><span data-stu-id="d2026-158">System.String</span></span>

### <span data-ttu-id="d2026-159">Microsoft. Azure. Commands. чертеж. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="d2026-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="d2026-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="d2026-160">System.String[]</span></span>

### <span data-ttu-id="d2026-161">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d2026-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d2026-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2026-162">OUTPUTS</span></span>

### <span data-ttu-id="d2026-163">System. Object</span><span class="sxs-lookup"><span data-stu-id="d2026-163">System.Object</span></span>
## <span data-ttu-id="d2026-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2026-164">NOTES</span></span>

## <span data-ttu-id="d2026-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2026-165">RELATED LINKS</span></span>
