---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 8b17767f31683acb0228fbef52fd1de32d49ba6c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008115"
---
# <span data-ttu-id="89657-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="89657-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="89657-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89657-102">SYNOPSIS</span></span>
<span data-ttu-id="89657-103">Назначьте определение схемы подписке или группе управления.</span><span class="sxs-lookup"><span data-stu-id="89657-103">Assign a blueprint definition to a subscription or a management group.</span></span>

## <span data-ttu-id="89657-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="89657-104">SYNTAX</span></span>

### <span data-ttu-id="89657-105">CreateBlueprintAssignment (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89657-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89657-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="89657-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89657-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89657-107">DESCRIPTION</span></span>
<span data-ttu-id="89657-108">Назначьте определение схемы подписке.</span><span class="sxs-lookup"><span data-stu-id="89657-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="89657-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="89657-109">EXAMPLES</span></span>

### <span data-ttu-id="89657-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="89657-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{mySecureStringParam=@{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameter $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="89657-111">Создайте новый чертеж определения в указанной подписке, используя словарь определенных параметров `$blueprintObject` и групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89657-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="89657-112">Используется удостоверение, назначенное системе.</span><span class="sxs-lookup"><span data-stu-id="89657-112">Uses system-assigned identity.</span></span> <span data-ttu-id="89657-113">Расположение определяет регион для создания управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="89657-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="89657-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="89657-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="89657-115">Создайте новый чертеж определения схемы в указанной подписке, используя словарь определенных параметров и групп ресурсов и настроив блокировку ресурсов для `$blueprintObject` **AllResources.**</span><span class="sxs-lookup"><span data-stu-id="89657-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="89657-116">Используется по умолчанию для использования системных удостоверений.</span><span class="sxs-lookup"><span data-stu-id="89657-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="89657-117">Расположение определяет регион для создания управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="89657-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="89657-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="89657-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="89657-119">Создайте новый чертеж определения схемы в указанной подписке, используя определенный словарь параметров и групп ресурсов с использованием указанного идентификатора, назначенного `$blueprintObject` пользователю.</span><span class="sxs-lookup"><span data-stu-id="89657-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="89657-120">Пример 4</span><span class="sxs-lookup"><span data-stu-id="89657-120">Example 4</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="89657-121">Создайте чертеж с помощью файла задания.</span><span class="sxs-lookup"><span data-stu-id="89657-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="89657-122">Формат файла задания можно найти в примерах запросов и ответов: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="89657-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="89657-123">Пример 5</span><span class="sxs-lookup"><span data-stu-id="89657-123">Example 5</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "myManagementGroup" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="89657-124">Создайте новый чертеж, определяющий указанную подписку в указанной группе управления, с использованием `$blueprintObject` указанного параметра.</span><span class="sxs-lookup"><span data-stu-id="89657-124">Create a new blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="89657-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89657-125">PARAMETERS</span></span>

### <span data-ttu-id="89657-126">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="89657-126">-AssignmentFile</span></span>
<span data-ttu-id="89657-127">Расположение файла назначения в формате JSON на диске.</span><span class="sxs-lookup"><span data-stu-id="89657-127">Location of the assignment file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89657-128">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="89657-128">-Blueprint</span></span>
<span data-ttu-id="89657-129">Объект определения схемы.</span><span class="sxs-lookup"><span data-stu-id="89657-129">Blueprint definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89657-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89657-130">-DefaultProfile</span></span>
<span data-ttu-id="89657-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89657-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89657-132">-Location</span><span class="sxs-lookup"><span data-stu-id="89657-132">-Location</span></span>
<span data-ttu-id="89657-133">Регион для создания управляемых удостоверений.</span><span class="sxs-lookup"><span data-stu-id="89657-133">Region for managed identity to be created in.</span></span>
<span data-ttu-id="89657-134">Дополнительные дополнительные aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="89657-134">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89657-135">-Lock</span><span class="sxs-lookup"><span data-stu-id="89657-135">-Lock</span></span>
<span data-ttu-id="89657-136">Заблокировать ресурсы.</span><span class="sxs-lookup"><span data-stu-id="89657-136">Lock resources.</span></span>
<span data-ttu-id="89657-137">Дополнительные дополнительные aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="89657-137">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: CreateBlueprintAssignment
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89657-138">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="89657-138">-ManagementGroupId</span></span>
<span data-ttu-id="89657-139">ИД группы управления, в которой сохраняются назначения Blueprint.</span><span class="sxs-lookup"><span data-stu-id="89657-139">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89657-140">-Name</span><span class="sxs-lookup"><span data-stu-id="89657-140">-Name</span></span>
<span data-ttu-id="89657-141">Название задания «Чертеж».</span><span class="sxs-lookup"><span data-stu-id="89657-141">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89657-142">-Parameter</span><span class="sxs-lookup"><span data-stu-id="89657-142">-Parameter</span></span>
<span data-ttu-id="89657-143">Параметры артефакта.</span><span class="sxs-lookup"><span data-stu-id="89657-143">Artifact parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89657-144">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="89657-144">-ResourceGroupParameter</span></span>
<span data-ttu-id="89657-145">Возможность передавать параметры в артефакт группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89657-145">Hashtable of parameters to pass to the resource group artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89657-146">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="89657-146">-SecureStringParameter</span></span>
<span data-ttu-id="89657-147">Параметр Secure String для ИД ресурса KeyVault, имени и версии.</span><span class="sxs-lookup"><span data-stu-id="89657-147">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89657-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="89657-148">-SubscriptionId</span></span>
<span data-ttu-id="89657-149">ИД подписки, чтобы назначить определение схемы.</span><span class="sxs-lookup"><span data-stu-id="89657-149">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="89657-150">Может быть списком строк SubscriptionId, который является запятой.</span><span class="sxs-lookup"><span data-stu-id="89657-150">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89657-151">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="89657-151">-SystemAssignedIdentity</span></span>
<span data-ttu-id="89657-152">Системные удостоверения (MSI) для развертывания артефактов.</span><span class="sxs-lookup"><span data-stu-id="89657-152">System assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89657-153">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="89657-153">-UserAssignedIdentity</span></span>
<span data-ttu-id="89657-154">Удостоверение, назначенное пользователем (MSI) для развертывания артефактов.</span><span class="sxs-lookup"><span data-stu-id="89657-154">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89657-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89657-155">-Confirm</span></span>
<span data-ttu-id="89657-156">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89657-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89657-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89657-157">-WhatIf</span></span>
<span data-ttu-id="89657-158">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89657-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89657-159">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="89657-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89657-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89657-160">CommonParameters</span></span>
<span data-ttu-id="89657-161">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89657-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89657-162">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89657-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89657-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89657-163">INPUTS</span></span>

### <span data-ttu-id="89657-164">System.String</span><span class="sxs-lookup"><span data-stu-id="89657-164">System.String</span></span>

### <span data-ttu-id="89657-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="89657-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="89657-166">System.String[]</span><span class="sxs-lookup"><span data-stu-id="89657-166">System.String[]</span></span>

### <span data-ttu-id="89657-167">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="89657-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="89657-168">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89657-168">OUTPUTS</span></span>

### <span data-ttu-id="89657-169">System.Object</span><span class="sxs-lookup"><span data-stu-id="89657-169">System.Object</span></span>
## <span data-ttu-id="89657-170">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="89657-170">NOTES</span></span>

## <span data-ttu-id="89657-171">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89657-171">RELATED LINKS</span></span>
