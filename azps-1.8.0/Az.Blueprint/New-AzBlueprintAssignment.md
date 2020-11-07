---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 43689de5ae2431db8bc523369700f32dba0206bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901477"
---
# <span data-ttu-id="e2462-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="e2462-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="e2462-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2462-102">SYNOPSIS</span></span>
<span data-ttu-id="e2462-103">Назначьте подписку определением чертежей.</span><span class="sxs-lookup"><span data-stu-id="e2462-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="e2462-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2462-104">SYNTAX</span></span>

```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2462-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2462-105">DESCRIPTION</span></span>
<span data-ttu-id="e2462-106">Назначьте подписку определением чертежей.</span><span class="sxs-lookup"><span data-stu-id="e2462-106">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="e2462-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2462-107">EXAMPLES</span></span>

### <span data-ttu-id="e2462-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e2462-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameters $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="e2462-109">Создание нового назначения для определения плана `$blueprintObject` в указанной подписке с помощью определенного параметра и словаря группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2462-109">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="e2462-110">Использует присвоенное системой удостоверение.</span><span class="sxs-lookup"><span data-stu-id="e2462-110">Uses system-assigned identity.</span></span> <span data-ttu-id="e2462-111">Расположение определяет регион для создания управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="e2462-111">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="e2462-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e2462-112">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="e2462-113">Создание нового назначения для определения схемы `$blueprintObject` в указанной подписке с помощью определенного параметра и словаря группы ресурсов, а также Настройка блокировки ресурсов на **AllResources**.</span><span class="sxs-lookup"><span data-stu-id="e2462-113">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="e2462-114">По умолчанию используется идентификатор, назначенный системой.</span><span class="sxs-lookup"><span data-stu-id="e2462-114">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="e2462-115">Расположение определяет регион для создания управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="e2462-115">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="e2462-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e2462-116">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="e2462-117">Создание нового назначения для определения плана `$blueprintObject` в указанной подписке с помощью определенного параметра и словаря группы ресурсов с указанным пользовательским идентификатором удостоверения.</span><span class="sxs-lookup"><span data-stu-id="e2462-117">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

## <span data-ttu-id="e2462-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2462-118">PARAMETERS</span></span>

### <span data-ttu-id="e2462-119">-Чертеж</span><span class="sxs-lookup"><span data-stu-id="e2462-119">-Blueprint</span></span>
<span data-ttu-id="e2462-120">Объект определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="e2462-120">Blueprint definition object.</span></span>

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

### <span data-ttu-id="e2462-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2462-121">-DefaultProfile</span></span>
<span data-ttu-id="e2462-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2462-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2462-123">-Location</span><span class="sxs-lookup"><span data-stu-id="e2462-123">-Location</span></span>
<span data-ttu-id="e2462-124">Регион для создания управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="e2462-124">Region for managed identity to be created in.</span></span>
<span data-ttu-id="e2462-125">Дополнительные сведения по адресу aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="e2462-125">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="e2462-126">-Lock</span><span class="sxs-lookup"><span data-stu-id="e2462-126">-Lock</span></span>
<span data-ttu-id="e2462-127">Блокировка ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2462-127">Lock resources.</span></span>
<span data-ttu-id="e2462-128">Дополнительные сведения по адресу aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="e2462-128">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="e2462-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e2462-129">-Name</span></span>
<span data-ttu-id="e2462-130">Имя назначения для схемы.</span><span class="sxs-lookup"><span data-stu-id="e2462-130">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="e2462-131">-Параметр</span><span class="sxs-lookup"><span data-stu-id="e2462-131">-Parameter</span></span>
<span data-ttu-id="e2462-132">Параметры артефактов.</span><span class="sxs-lookup"><span data-stu-id="e2462-132">Artifact parameters.</span></span>

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

### <span data-ttu-id="e2462-133">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="e2462-133">-ResourceGroupParameter</span></span>
<span data-ttu-id="e2462-134">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="e2462-134">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="e2462-135">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="e2462-135">-SecureStringParameter</span></span>
<span data-ttu-id="e2462-136">Параметр Secure String для идентификатора ресурса KeyVault, имени и версии.</span><span class="sxs-lookup"><span data-stu-id="e2462-136">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="e2462-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2462-137">-SubscriptionId</span></span>
<span data-ttu-id="e2462-138">Идентификатор подписки, с помощью которой можно назначить определение чертежа.</span><span class="sxs-lookup"><span data-stu-id="e2462-138">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="e2462-139">Может быть списком из строк subscriptionId, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="e2462-139">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="e2462-140">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e2462-140">-SystemAssignedIdentity</span></span>
<span data-ttu-id="e2462-141">Система присвоила идентификатор (MSI) для развертывания артефактов.</span><span class="sxs-lookup"><span data-stu-id="e2462-141">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="e2462-142">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e2462-142">-UserAssignedIdentity</span></span>
<span data-ttu-id="e2462-143">Идентификатор (MSI), назначенный пользователю для развертывания артефактов.</span><span class="sxs-lookup"><span data-stu-id="e2462-143">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="e2462-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2462-144">-Confirm</span></span>
<span data-ttu-id="e2462-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e2462-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2462-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2462-146">-WhatIf</span></span>
<span data-ttu-id="e2462-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e2462-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2462-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e2462-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2462-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2462-149">CommonParameters</span></span>
<span data-ttu-id="e2462-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2462-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2462-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2462-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2462-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2462-152">INPUTS</span></span>

### <span data-ttu-id="e2462-153">System. String</span><span class="sxs-lookup"><span data-stu-id="e2462-153">System.String</span></span>

### <span data-ttu-id="e2462-154">Microsoft. Azure. Commands. чертеж. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="e2462-154">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="e2462-155">System. String []</span><span class="sxs-lookup"><span data-stu-id="e2462-155">System.String[]</span></span>

### <span data-ttu-id="e2462-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e2462-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e2462-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2462-157">OUTPUTS</span></span>

### <span data-ttu-id="e2462-158">System. Object</span><span class="sxs-lookup"><span data-stu-id="e2462-158">System.Object</span></span>
## <span data-ttu-id="e2462-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2462-159">NOTES</span></span>

## <span data-ttu-id="e2462-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2462-160">RELATED LINKS</span></span>
