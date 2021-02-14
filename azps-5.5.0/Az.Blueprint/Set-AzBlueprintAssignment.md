---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: b8913ead9844a55190a6117f57f01d243e004fde
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234961"
---
# <span data-ttu-id="a08f5-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="a08f5-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="a08f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a08f5-102">SYNOPSIS</span></span>
<span data-ttu-id="a08f5-103">Обновим существующее задание чертежа.</span><span class="sxs-lookup"><span data-stu-id="a08f5-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="a08f5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a08f5-104">SYNTAX</span></span>

### <span data-ttu-id="a08f5-105">UpdateBlueprintAssignment (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a08f5-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a08f5-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="a08f5-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a08f5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a08f5-107">DESCRIPTION</span></span>
<span data-ttu-id="a08f5-108">Обновим существующее задание чертежа.</span><span class="sxs-lookup"><span data-stu-id="a08f5-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="a08f5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a08f5-109">EXAMPLES</span></span>

### <span data-ttu-id="a08f5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a08f5-110">Example 1</span></span>
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

<span data-ttu-id="a08f5-111">Обновив существующее определение схемы в указанной `$blueprintObject` подписке, обновив параметры.</span><span class="sxs-lookup"><span data-stu-id="a08f5-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="a08f5-112">Используется удостоверение, назначенное системе.</span><span class="sxs-lookup"><span data-stu-id="a08f5-112">Uses system-assigned identity.</span></span> <span data-ttu-id="a08f5-113">Расположение определяет регион для создания управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="a08f5-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="a08f5-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a08f5-114">Example 2</span></span>
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

<span data-ttu-id="a08f5-115">Обновив существующее задание с помощью файла задания.</span><span class="sxs-lookup"><span data-stu-id="a08f5-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="a08f5-116">Формат файла задания можно найти в примерах запросов и ответов: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="a08f5-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="a08f5-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a08f5-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="a08f5-118">Обновив существующее определение схемы, определяющую указанную подписку в указанной группе управления, используя `$blueprintObject` определенный параметр.</span><span class="sxs-lookup"><span data-stu-id="a08f5-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="a08f5-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a08f5-119">PARAMETERS</span></span>

### <span data-ttu-id="a08f5-120">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="a08f5-120">-AssignmentFile</span></span>
<span data-ttu-id="a08f5-121">Расположение файла назначения в формате JSON на диске.</span><span class="sxs-lookup"><span data-stu-id="a08f5-121">Location of the assignment file in JSON format on disk.</span></span>

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

### <span data-ttu-id="a08f5-122">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="a08f5-122">-Blueprint</span></span>
<span data-ttu-id="a08f5-123">Объект Blueprint.</span><span class="sxs-lookup"><span data-stu-id="a08f5-123">Blueprint object.</span></span>

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

### <span data-ttu-id="a08f5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a08f5-124">-DefaultProfile</span></span>
<span data-ttu-id="a08f5-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a08f5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a08f5-126">-Location</span><span class="sxs-lookup"><span data-stu-id="a08f5-126">-Location</span></span>
<span data-ttu-id="a08f5-127">Регион для создания управляемых удостоверений.</span><span class="sxs-lookup"><span data-stu-id="a08f5-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="a08f5-128">Дополнительные дополнительные aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="a08f5-128">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="a08f5-129">-Lock</span><span class="sxs-lookup"><span data-stu-id="a08f5-129">-Lock</span></span>
<span data-ttu-id="a08f5-130">Заблокировать ресурсы.</span><span class="sxs-lookup"><span data-stu-id="a08f5-130">Lock resources.</span></span>
<span data-ttu-id="a08f5-131">Дополнительные дополнительные aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="a08f5-131">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="a08f5-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="a08f5-132">-ManagementGroupId</span></span>
<span data-ttu-id="a08f5-133">ИД группы управления, в которой сохраняются назначения Blueprint.</span><span class="sxs-lookup"><span data-stu-id="a08f5-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

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

### <span data-ttu-id="a08f5-134">-Name</span><span class="sxs-lookup"><span data-stu-id="a08f5-134">-Name</span></span>
<span data-ttu-id="a08f5-135">Название задания «Чертеж».</span><span class="sxs-lookup"><span data-stu-id="a08f5-135">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="a08f5-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="a08f5-136">-Parameter</span></span>
<span data-ttu-id="a08f5-137">Параметр артефакта.</span><span class="sxs-lookup"><span data-stu-id="a08f5-137">Artifact parameter.</span></span>

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

### <span data-ttu-id="a08f5-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="a08f5-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="a08f5-139">Возможность передавать параметры в артефакт группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a08f5-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

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

### <span data-ttu-id="a08f5-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="a08f5-140">-SecureStringParameter</span></span>
<span data-ttu-id="a08f5-141">Параметр Secure String для ИД ресурса KeyVault, имени и версии.</span><span class="sxs-lookup"><span data-stu-id="a08f5-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="a08f5-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a08f5-142">-SubscriptionId</span></span>
<span data-ttu-id="a08f5-143">SubscriptionId, чтобы назначить "Чертеж".</span><span class="sxs-lookup"><span data-stu-id="a08f5-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="a08f5-144">Может быть списком строк SubscriptionId, который является запятой.</span><span class="sxs-lookup"><span data-stu-id="a08f5-144">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="a08f5-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a08f5-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="a08f5-146">Системные удостоверения(MSI) для развертывания артефактов.</span><span class="sxs-lookup"><span data-stu-id="a08f5-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="a08f5-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a08f5-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="a08f5-148">Удостоверение, назначенное пользователем (MSI) для развертывания артефактов.</span><span class="sxs-lookup"><span data-stu-id="a08f5-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="a08f5-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a08f5-149">-Confirm</span></span>
<span data-ttu-id="a08f5-150">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a08f5-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a08f5-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a08f5-151">-WhatIf</span></span>
<span data-ttu-id="a08f5-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a08f5-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a08f5-153">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a08f5-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a08f5-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a08f5-154">CommonParameters</span></span>
<span data-ttu-id="a08f5-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a08f5-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a08f5-156">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a08f5-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a08f5-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a08f5-157">INPUTS</span></span>

### <span data-ttu-id="a08f5-158">System.String</span><span class="sxs-lookup"><span data-stu-id="a08f5-158">System.String</span></span>

### <span data-ttu-id="a08f5-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="a08f5-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="a08f5-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a08f5-160">System.String[]</span></span>

### <span data-ttu-id="a08f5-161">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a08f5-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a08f5-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a08f5-162">OUTPUTS</span></span>

### <span data-ttu-id="a08f5-163">System.Object</span><span class="sxs-lookup"><span data-stu-id="a08f5-163">System.Object</span></span>
## <span data-ttu-id="a08f5-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a08f5-164">NOTES</span></span>

## <span data-ttu-id="a08f5-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a08f5-165">RELATED LINKS</span></span>
