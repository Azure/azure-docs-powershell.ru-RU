---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 72c57f8310aaffdbe3c4afa38564c10132539749
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065106"
---
# <span data-ttu-id="4ce96-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="4ce96-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="4ce96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ce96-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce96-103">Назначьте подписку определением чертежей.</span><span class="sxs-lookup"><span data-stu-id="4ce96-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="4ce96-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ce96-104">SYNTAX</span></span>

### <span data-ttu-id="4ce96-105">CreateBlueprintAssignment (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ce96-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ce96-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="4ce96-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ce96-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ce96-107">DESCRIPTION</span></span>
<span data-ttu-id="4ce96-108">Назначьте подписку определением чертежей.</span><span class="sxs-lookup"><span data-stu-id="4ce96-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="4ce96-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ce96-109">EXAMPLES</span></span>

### <span data-ttu-id="4ce96-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4ce96-110">Example 1</span></span>
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

<span data-ttu-id="4ce96-111">Создание нового назначения для определения плана `$blueprintObject` в указанной подписке с помощью определенного параметра и словаря группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4ce96-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="4ce96-112">Использует присвоенное системой удостоверение.</span><span class="sxs-lookup"><span data-stu-id="4ce96-112">Uses system-assigned identity.</span></span> <span data-ttu-id="4ce96-113">Расположение определяет регион для создания управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="4ce96-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="4ce96-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4ce96-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="4ce96-115">Создание нового назначения для определения схемы `$blueprintObject` в указанной подписке с помощью определенного параметра и словаря группы ресурсов, а также Настройка блокировки ресурсов на **AllResources**.</span><span class="sxs-lookup"><span data-stu-id="4ce96-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="4ce96-116">По умолчанию используется идентификатор, назначенный системой.</span><span class="sxs-lookup"><span data-stu-id="4ce96-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="4ce96-117">Расположение определяет регион для создания управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="4ce96-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="4ce96-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4ce96-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="4ce96-119">Создание нового назначения для определения плана `$blueprintObject` в указанной подписке с помощью определенного параметра и словаря группы ресурсов с указанным пользовательским идентификатором удостоверения.</span><span class="sxs-lookup"><span data-stu-id="4ce96-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="4ce96-120">Пример 4</span><span class="sxs-lookup"><span data-stu-id="4ce96-120">Example 4</span></span>
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

<span data-ttu-id="4ce96-121">Создавайте задания с помощью файла подборки.</span><span class="sxs-lookup"><span data-stu-id="4ce96-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="4ce96-122">Формат файла подборки можно найти в образцах запросов и ответов по адресу: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="4ce96-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="4ce96-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ce96-123">PARAMETERS</span></span>

### <span data-ttu-id="4ce96-124">-Чертеж</span><span class="sxs-lookup"><span data-stu-id="4ce96-124">-Blueprint</span></span>
<span data-ttu-id="4ce96-125">Объект определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="4ce96-125">Blueprint definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce96-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce96-126">-DefaultProfile</span></span>
<span data-ttu-id="4ce96-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ce96-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ce96-128">-Location</span><span class="sxs-lookup"><span data-stu-id="4ce96-128">-Location</span></span>
<span data-ttu-id="4ce96-129">Регион для создания управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="4ce96-129">Region for managed identity to be created in.</span></span>
<span data-ttu-id="4ce96-130">Дополнительные сведения по адресу aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="4ce96-130">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce96-131">-Lock</span><span class="sxs-lookup"><span data-stu-id="4ce96-131">-Lock</span></span>
<span data-ttu-id="4ce96-132">Блокировка ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4ce96-132">Lock resources.</span></span>
<span data-ttu-id="4ce96-133">Дополнительные сведения по адресу aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="4ce96-133">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: (All)
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ce96-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4ce96-134">-Name</span></span>
<span data-ttu-id="4ce96-135">Имя назначения для схемы.</span><span class="sxs-lookup"><span data-stu-id="4ce96-135">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce96-136">-Параметр</span><span class="sxs-lookup"><span data-stu-id="4ce96-136">-Parameter</span></span>
<span data-ttu-id="4ce96-137">Параметры артефактов.</span><span class="sxs-lookup"><span data-stu-id="4ce96-137">Artifact parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce96-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="4ce96-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="4ce96-139">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="4ce96-139">{{Fill ResourceGroupParameter Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce96-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="4ce96-140">-SecureStringParameter</span></span>
<span data-ttu-id="4ce96-141">Параметр Secure String для идентификатора ресурса KeyVault, имени и версии.</span><span class="sxs-lookup"><span data-stu-id="4ce96-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ce96-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ce96-142">-SubscriptionId</span></span>
<span data-ttu-id="4ce96-143">Идентификатор подписки, с помощью которой можно назначить определение чертежа.</span><span class="sxs-lookup"><span data-stu-id="4ce96-143">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="4ce96-144">Может быть списком из строк subscriptionId, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="4ce96-144">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce96-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4ce96-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="4ce96-146">Система присвоила идентификатор (MSI) для развертывания артефактов.</span><span class="sxs-lookup"><span data-stu-id="4ce96-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="4ce96-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4ce96-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="4ce96-148">Идентификатор (MSI), назначенный пользователю для развертывания артефактов.</span><span class="sxs-lookup"><span data-stu-id="4ce96-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="4ce96-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ce96-149">-Confirm</span></span>
<span data-ttu-id="4ce96-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4ce96-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ce96-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ce96-151">-WhatIf</span></span>
<span data-ttu-id="4ce96-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4ce96-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ce96-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4ce96-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ce96-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce96-154">CommonParameters</span></span>
<span data-ttu-id="4ce96-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ce96-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce96-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ce96-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce96-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ce96-157">INPUTS</span></span>

### <span data-ttu-id="4ce96-158">System. String</span><span class="sxs-lookup"><span data-stu-id="4ce96-158">System.String</span></span>

### <span data-ttu-id="4ce96-159">Microsoft. Azure. Commands. чертеж. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="4ce96-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="4ce96-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="4ce96-160">System.String[]</span></span>

### <span data-ttu-id="4ce96-161">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4ce96-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4ce96-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ce96-162">OUTPUTS</span></span>

### <span data-ttu-id="4ce96-163">System. Object</span><span class="sxs-lookup"><span data-stu-id="4ce96-163">System.Object</span></span>
## <span data-ttu-id="4ce96-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ce96-164">NOTES</span></span>

## <span data-ttu-id="4ce96-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ce96-165">RELATED LINKS</span></span>
