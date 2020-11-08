---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 295e70d91af0c6c06ac913c10bfe5a9e265523c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246101"
---
# <span data-ttu-id="e0af3-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="e0af3-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="e0af3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0af3-102">SYNOPSIS</span></span>
<span data-ttu-id="e0af3-103">Назначение определения плана подписке или группе управления.</span><span class="sxs-lookup"><span data-stu-id="e0af3-103">Assign a blueprint definition to a subscription or a management group.</span></span>

## <span data-ttu-id="e0af3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0af3-104">SYNTAX</span></span>

### <span data-ttu-id="e0af3-105">CreateBlueprintAssignment (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e0af3-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0af3-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="e0af3-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0af3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0af3-107">DESCRIPTION</span></span>
<span data-ttu-id="e0af3-108">Назначьте подписку определением чертежей.</span><span class="sxs-lookup"><span data-stu-id="e0af3-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="e0af3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0af3-109">EXAMPLES</span></span>

### <span data-ttu-id="e0af3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e0af3-110">Example 1</span></span>
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

<span data-ttu-id="e0af3-111">Создание нового назначения для определения плана `$blueprintObject` в указанной подписке с помощью определенного параметра и словаря группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e0af3-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="e0af3-112">Использует присвоенное системой удостоверение.</span><span class="sxs-lookup"><span data-stu-id="e0af3-112">Uses system-assigned identity.</span></span> <span data-ttu-id="e0af3-113">Расположение определяет регион для создания управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="e0af3-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="e0af3-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e0af3-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="e0af3-115">Создание нового назначения для определения схемы `$blueprintObject` в указанной подписке с помощью определенного параметра и словаря группы ресурсов, а также Настройка блокировки ресурсов на **AllResources**.</span><span class="sxs-lookup"><span data-stu-id="e0af3-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="e0af3-116">По умолчанию используется идентификатор, назначенный системой.</span><span class="sxs-lookup"><span data-stu-id="e0af3-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="e0af3-117">Расположение определяет регион для создания управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="e0af3-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="e0af3-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e0af3-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="e0af3-119">Создание нового назначения для определения плана `$blueprintObject` в указанной подписке с помощью определенного параметра и словаря группы ресурсов с указанным пользовательским идентификатором удостоверения.</span><span class="sxs-lookup"><span data-stu-id="e0af3-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="e0af3-120">Пример 4</span><span class="sxs-lookup"><span data-stu-id="e0af3-120">Example 4</span></span>
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

<span data-ttu-id="e0af3-121">Создавайте задания с помощью файла подборки.</span><span class="sxs-lookup"><span data-stu-id="e0af3-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="e0af3-122">Формат файла подборки можно найти в образцах запросов и ответов по адресу: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="e0af3-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="e0af3-123">Пример 5</span><span class="sxs-lookup"><span data-stu-id="e0af3-123">Example 5</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "myManagementGroup" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="e0af3-124">Создание нового назначения для определения `$blueprintObject` плана, ориентированного на определенную подписку в указанной группе управления, с помощью определенного параметра.</span><span class="sxs-lookup"><span data-stu-id="e0af3-124">Create a new blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="e0af3-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0af3-125">PARAMETERS</span></span>

### <span data-ttu-id="e0af3-126">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="e0af3-126">-AssignmentFile</span></span>
<span data-ttu-id="e0af3-127">Расположение файла назначения в формате JSON на диске.</span><span class="sxs-lookup"><span data-stu-id="e0af3-127">Location of the assignment file in JSON format on disk.</span></span>

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

### <span data-ttu-id="e0af3-128">-Чертеж</span><span class="sxs-lookup"><span data-stu-id="e0af3-128">-Blueprint</span></span>
<span data-ttu-id="e0af3-129">Объект определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="e0af3-129">Blueprint definition object.</span></span>

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

### <span data-ttu-id="e0af3-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0af3-130">-DefaultProfile</span></span>
<span data-ttu-id="e0af3-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0af3-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0af3-132">-Location</span><span class="sxs-lookup"><span data-stu-id="e0af3-132">-Location</span></span>
<span data-ttu-id="e0af3-133">Регион для создания управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="e0af3-133">Region for managed identity to be created in.</span></span>
<span data-ttu-id="e0af3-134">Дополнительные сведения по адресу aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="e0af3-134">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="e0af3-135">-Lock</span><span class="sxs-lookup"><span data-stu-id="e0af3-135">-Lock</span></span>
<span data-ttu-id="e0af3-136">Блокировка ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e0af3-136">Lock resources.</span></span>
<span data-ttu-id="e0af3-137">Дополнительные сведения по адресу aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="e0af3-137">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="e0af3-138">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="e0af3-138">-ManagementGroupId</span></span>
<span data-ttu-id="e0af3-139">Идентификатор группы управления, в которой будут сохранены назначения для чертежей.</span><span class="sxs-lookup"><span data-stu-id="e0af3-139">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

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

### <span data-ttu-id="e0af3-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e0af3-140">-Name</span></span>
<span data-ttu-id="e0af3-141">Имя назначения для схемы.</span><span class="sxs-lookup"><span data-stu-id="e0af3-141">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="e0af3-142">-Параметр</span><span class="sxs-lookup"><span data-stu-id="e0af3-142">-Parameter</span></span>
<span data-ttu-id="e0af3-143">Параметры артефактов.</span><span class="sxs-lookup"><span data-stu-id="e0af3-143">Artifact parameters.</span></span>

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

### <span data-ttu-id="e0af3-144">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="e0af3-144">-ResourceGroupParameter</span></span>
<span data-ttu-id="e0af3-145">Хэш-таблица параметров для передачи артефакту группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e0af3-145">Hashtable of parameters to pass to the resource group artifact.</span></span>

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

### <span data-ttu-id="e0af3-146">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="e0af3-146">-SecureStringParameter</span></span>
<span data-ttu-id="e0af3-147">Параметр Secure String для идентификатора ресурса KeyVault, имени и версии.</span><span class="sxs-lookup"><span data-stu-id="e0af3-147">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="e0af3-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0af3-148">-SubscriptionId</span></span>
<span data-ttu-id="e0af3-149">Идентификатор подписки, с помощью которой можно назначить определение чертежа.</span><span class="sxs-lookup"><span data-stu-id="e0af3-149">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="e0af3-150">Может быть списком из строк subscriptionId, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="e0af3-150">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="e0af3-151">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e0af3-151">-SystemAssignedIdentity</span></span>
<span data-ttu-id="e0af3-152">Система присвоила идентификатор (MSI) для развертывания артефактов.</span><span class="sxs-lookup"><span data-stu-id="e0af3-152">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="e0af3-153">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e0af3-153">-UserAssignedIdentity</span></span>
<span data-ttu-id="e0af3-154">Идентификатор (MSI), назначенный пользователю для развертывания артефактов.</span><span class="sxs-lookup"><span data-stu-id="e0af3-154">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="e0af3-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0af3-155">-Confirm</span></span>
<span data-ttu-id="e0af3-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e0af3-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0af3-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0af3-157">-WhatIf</span></span>
<span data-ttu-id="e0af3-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e0af3-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0af3-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e0af3-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0af3-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0af3-160">CommonParameters</span></span>
<span data-ttu-id="e0af3-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0af3-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0af3-162">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0af3-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0af3-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0af3-163">INPUTS</span></span>

### <span data-ttu-id="e0af3-164">System. String</span><span class="sxs-lookup"><span data-stu-id="e0af3-164">System.String</span></span>

### <span data-ttu-id="e0af3-165">Microsoft. Azure. Commands. чертеж. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="e0af3-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="e0af3-166">System. String []</span><span class="sxs-lookup"><span data-stu-id="e0af3-166">System.String[]</span></span>

### <span data-ttu-id="e0af3-167">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e0af3-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e0af3-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0af3-168">OUTPUTS</span></span>

### <span data-ttu-id="e0af3-169">System. Object</span><span class="sxs-lookup"><span data-stu-id="e0af3-169">System.Object</span></span>
## <span data-ttu-id="e0af3-170">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0af3-170">NOTES</span></span>

## <span data-ttu-id="e0af3-171">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0af3-171">RELATED LINKS</span></span>
