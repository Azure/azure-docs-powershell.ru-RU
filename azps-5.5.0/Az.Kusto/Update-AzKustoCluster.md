---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 7cc359b230bc3e4480b1cc6a03db768c17ebf60c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214489"
---
# <span data-ttu-id="b95e1-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="b95e1-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="b95e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b95e1-102">SYNOPSIS</span></span>
<span data-ttu-id="b95e1-103">Обновив кластер "Кусто".</span><span class="sxs-lookup"><span data-stu-id="b95e1-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="b95e1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b95e1-104">SYNTAX</span></span>

### <span data-ttu-id="b95e1-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b95e1-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-EngineType <EngineType>] [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-KeyVaultPropertyUserIdentity <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b95e1-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b95e1-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-Location <String>] [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>]
 [-OptimizedAutoscaleMinimum <Int32>] [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>]
 [-SkuName <AzureSkuName>] [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b95e1-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b95e1-107">DESCRIPTION</span></span>
<span data-ttu-id="b95e1-108">Обновив кластер "Кусто".</span><span class="sxs-lookup"><span data-stu-id="b95e1-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="b95e1-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b95e1-109">EXAMPLES</span></span>

### <span data-ttu-id="b95e1-110">Пример 1. Обновление существующего кластера по имени</span><span class="sxs-lookup"><span data-stu-id="b95e1-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="b95e1-111">С этой командой обновляется sku кластера кусто "testnewkustocluster", найденный в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="b95e1-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="b95e1-112">Пример 2. Обновление существующего кластера по имени</span><span class="sxs-lookup"><span data-stu-id="b95e1-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="b95e1-113">Она обновляет кластер testnewkustocluster, который находится в группе ресурсов Testrg, с помощью управляемого клиентом ключа.</span><span class="sxs-lookup"><span data-stu-id="b95e1-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="b95e1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b95e1-114">PARAMETERS</span></span>

### <span data-ttu-id="b95e1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b95e1-115">-AsJob</span></span>
<span data-ttu-id="b95e1-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="b95e1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b95e1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b95e1-117">-DefaultProfile</span></span>
<span data-ttu-id="b95e1-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b95e1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95e1-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="b95e1-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="b95e1-120">Boolean value that indicates if the cluster's disks are encrypted.</span><span class="sxs-lookup"><span data-stu-id="b95e1-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="b95e1-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="b95e1-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="b95e1-122">Boolean value that indicates if double encryption is enabled.</span><span class="sxs-lookup"><span data-stu-id="b95e1-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="b95e1-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="b95e1-123">-EnablePurge</span></span>
<span data-ttu-id="b95e1-124">Boolean value that indicates if the purge operations are enabled.</span><span class="sxs-lookup"><span data-stu-id="b95e1-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="b95e1-125">-EnableStreamingingest</span><span class="sxs-lookup"><span data-stu-id="b95e1-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="b95e1-126">Boolean value that indicates if the streaming ingest is enabled.</span><span class="sxs-lookup"><span data-stu-id="b95e1-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="b95e1-127">-EngineType</span><span class="sxs-lookup"><span data-stu-id="b95e1-127">-EngineType</span></span>
<span data-ttu-id="b95e1-128">Тип движка</span><span class="sxs-lookup"><span data-stu-id="b95e1-128">The engine type</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EngineType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95e1-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="b95e1-129">-IdentityType</span></span>
<span data-ttu-id="b95e1-130">Тип используемых управляемых удостоверений.</span><span class="sxs-lookup"><span data-stu-id="b95e1-130">The type of managed identity used.</span></span>
<span data-ttu-id="b95e1-131">Тип "SystemAssigned, UserAssigned" включает неявное созданное удостоверение и набор удостоверений, которые назначены пользователю.</span><span class="sxs-lookup"><span data-stu-id="b95e1-131">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="b95e1-132">При типе "Нет" будут удаляться все удостоверения.</span><span class="sxs-lookup"><span data-stu-id="b95e1-132">The type 'None' will remove all identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95e1-133">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="b95e1-133">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="b95e1-134">Список удостоверений пользователей, связанных с кластером Кусто.</span><span class="sxs-lookup"><span data-stu-id="b95e1-134">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="b95e1-135">Ссылки на ключ словаря удостоверений пользователей будут ARM идентификаторами ресурсов в форме: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="b95e1-135">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="b95e1-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b95e1-136">-InputObject</span></span>
<span data-ttu-id="b95e1-137">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="b95e1-137">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b95e1-138">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="b95e1-138">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="b95e1-139">Имя ключа сейфа.</span><span class="sxs-lookup"><span data-stu-id="b95e1-139">The name of the key vault key.</span></span>

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

### <span data-ttu-id="b95e1-140">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="b95e1-140">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="b95e1-141">Uri хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="b95e1-141">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="b95e1-142">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="b95e1-142">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="b95e1-143">Версия ключа ключа сейфа.</span><span class="sxs-lookup"><span data-stu-id="b95e1-143">The version of the key vault key.</span></span>

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

### <span data-ttu-id="b95e1-144">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="b95e1-144">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="b95e1-145">Удостоверение, назначенное пользователем (ARM ресурса), которое имеет доступ к ключу.</span><span class="sxs-lookup"><span data-stu-id="b95e1-145">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="b95e1-146">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="b95e1-146">-LanguageExtensionValue</span></span>
<span data-ttu-id="b95e1-147">Список языковых расширений.</span><span class="sxs-lookup"><span data-stu-id="b95e1-147">The list of language extensions.</span></span>
<span data-ttu-id="b95e1-148">Чтобы создать новую таблицу, см. раздел "ЗАМЕТКИ" для свойств LANGUAGEEXTENSIONVALUE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="b95e1-148">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95e1-149">-Location</span><span class="sxs-lookup"><span data-stu-id="b95e1-149">-Location</span></span>
<span data-ttu-id="b95e1-150">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="b95e1-150">Resource location.</span></span>

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

### <span data-ttu-id="b95e1-151">-Name</span><span class="sxs-lookup"><span data-stu-id="b95e1-151">-Name</span></span>
<span data-ttu-id="b95e1-152">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="b95e1-152">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95e1-153">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b95e1-153">-NoWait</span></span>
<span data-ttu-id="b95e1-154">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="b95e1-154">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b95e1-155">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="b95e1-155">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="b95e1-156">Boolean value that indicate if the optimized autoscale feature is enabled or not.</span><span class="sxs-lookup"><span data-stu-id="b95e1-156">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="b95e1-157">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="b95e1-157">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="b95e1-158">Максимальное количество разрешенных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="b95e1-158">Maximum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95e1-159">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="b95e1-159">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="b95e1-160">Количество экземпляров, разрешенных как минимум.</span><span class="sxs-lookup"><span data-stu-id="b95e1-160">Minimum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95e1-161">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="b95e1-161">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="b95e1-162">Версия определенного шаблона, например 1.</span><span class="sxs-lookup"><span data-stu-id="b95e1-162">The version of the template defined, for instance 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95e1-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b95e1-163">-ResourceGroupName</span></span>
<span data-ttu-id="b95e1-164">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="b95e1-164">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95e1-165">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="b95e1-165">-SkuCapacity</span></span>
<span data-ttu-id="b95e1-166">Количество экземпляров кластера.</span><span class="sxs-lookup"><span data-stu-id="b95e1-166">The number of instances of the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95e1-167">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b95e1-167">-SkuName</span></span>
<span data-ttu-id="b95e1-168">Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="b95e1-168">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95e1-169">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b95e1-169">-SkuTier</span></span>
<span data-ttu-id="b95e1-170">Уровень SKU.</span><span class="sxs-lookup"><span data-stu-id="b95e1-170">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95e1-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b95e1-171">-SubscriptionId</span></span>
<span data-ttu-id="b95e1-172">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b95e1-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b95e1-173">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="b95e1-173">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95e1-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="b95e1-174">-Tag</span></span>
<span data-ttu-id="b95e1-175">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b95e1-175">Resource tags.</span></span>

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

### <span data-ttu-id="b95e1-176">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="b95e1-176">-TrustedExternalTenant</span></span>
<span data-ttu-id="b95e1-177">Внешние клиенты кластера.</span><span class="sxs-lookup"><span data-stu-id="b95e1-177">The cluster's external tenants.</span></span>
<span data-ttu-id="b95e1-178">Чтобы построить таблицу, см. раздел "ЗАМЕТКи" для свойств TRUSTEDEXTERNALTENANT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="b95e1-178">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95e1-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="b95e1-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="b95e1-180">ИД ресурса общедоступных IP-адресов службы управления данными.</span><span class="sxs-lookup"><span data-stu-id="b95e1-180">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="b95e1-181">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="b95e1-181">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="b95e1-182">ИД ресурса общедоступных IP-адресов службы Engine.</span><span class="sxs-lookup"><span data-stu-id="b95e1-182">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="b95e1-183">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="b95e1-183">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="b95e1-184">ИД ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="b95e1-184">The subnet resource id.</span></span>

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

### <span data-ttu-id="b95e1-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b95e1-185">-Confirm</span></span>
<span data-ttu-id="b95e1-186">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b95e1-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b95e1-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b95e1-187">-WhatIf</span></span>
<span data-ttu-id="b95e1-188">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b95e1-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b95e1-189">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b95e1-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b95e1-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b95e1-190">CommonParameters</span></span>
<span data-ttu-id="b95e1-191">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b95e1-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b95e1-192">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b95e1-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b95e1-193">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b95e1-193">INPUTS</span></span>

### <span data-ttu-id="b95e1-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="b95e1-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="b95e1-195">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b95e1-195">OUTPUTS</span></span>

### <span data-ttu-id="b95e1-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="b95e1-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="b95e1-197">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b95e1-197">NOTES</span></span>

<span data-ttu-id="b95e1-198">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b95e1-198">ALIASES</span></span>

<span data-ttu-id="b95e1-199">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="b95e1-199">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b95e1-200">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="b95e1-200">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b95e1-201">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b95e1-201">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b95e1-202">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="b95e1-202">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b95e1-203">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="b95e1-203">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="b95e1-204">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="b95e1-204">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="b95e1-205">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="b95e1-205">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="b95e1-206">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="b95e1-206">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="b95e1-207">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="b95e1-207">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b95e1-208">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="b95e1-208">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="b95e1-209">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="b95e1-209">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="b95e1-210">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="b95e1-210">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="b95e1-211">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b95e1-211">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b95e1-212">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="b95e1-212">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="b95e1-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: список языковых расширений.</span><span class="sxs-lookup"><span data-stu-id="b95e1-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="b95e1-214">`[Name <LanguageExtensionName?>]`: имя расширения языка.</span><span class="sxs-lookup"><span data-stu-id="b95e1-214">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="b95e1-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: внешние клиенты кластера.</span><span class="sxs-lookup"><span data-stu-id="b95e1-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="b95e1-216">`[Value <String>]`: GUID, представляющий внешний клиент.</span><span class="sxs-lookup"><span data-stu-id="b95e1-216">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="b95e1-217">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b95e1-217">RELATED LINKS</span></span>

