---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: a3e1561feb470708420015bac1e2f0688f182896
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414719"
---
# <span data-ttu-id="9bdd4-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="9bdd4-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="9bdd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bdd4-102">SYNOPSIS</span></span>
<span data-ttu-id="9bdd4-103">Обновив кластер "Кусто".</span><span class="sxs-lookup"><span data-stu-id="9bdd4-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="9bdd4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9bdd4-104">SYNTAX</span></span>

### <span data-ttu-id="9bdd4-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9bdd4-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9bdd4-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9bdd4-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9bdd4-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bdd4-107">DESCRIPTION</span></span>
<span data-ttu-id="9bdd4-108">Обновив кластер "Кусто".</span><span class="sxs-lookup"><span data-stu-id="9bdd4-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="9bdd4-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9bdd4-109">EXAMPLES</span></span>

### <span data-ttu-id="9bdd4-110">Пример 1. Обновление существующего кластера по имени</span><span class="sxs-lookup"><span data-stu-id="9bdd4-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="9bdd4-111">С этой командой обновляется sku кластера кусто "testnewkustocluster", найденный в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="9bdd4-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="9bdd4-112">Пример 2. Обновление существующего кластера по имени</span><span class="sxs-lookup"><span data-stu-id="9bdd4-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="9bdd4-113">Она обновляет кластер testnewkustocluster, который находится в группе ресурсов Testrg, с помощью управляемого клиентом ключа.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="9bdd4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bdd4-114">PARAMETERS</span></span>

### <span data-ttu-id="9bdd4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9bdd4-115">-AsJob</span></span>
<span data-ttu-id="9bdd4-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="9bdd4-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9bdd4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bdd4-117">-DefaultProfile</span></span>
<span data-ttu-id="9bdd4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bdd4-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="9bdd4-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="9bdd4-120">Boolean value that indicates if the cluster's disks are encrypted.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="9bdd4-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="9bdd4-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="9bdd4-122">Boolean value that indicates if double encryption is enabled.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="9bdd4-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="9bdd4-123">-EnablePurge</span></span>
<span data-ttu-id="9bdd4-124">Boolean value that indicates if the purge operations are enabled.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="9bdd4-125">-EnableStreamingingest</span><span class="sxs-lookup"><span data-stu-id="9bdd4-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="9bdd4-126">Boolean value that indicates if the streaming ingest is enabled.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="9bdd4-127">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="9bdd4-127">-IdentityType</span></span>
<span data-ttu-id="9bdd4-128">Тип удостоверения.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-128">The identity type.</span></span>

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

### <span data-ttu-id="9bdd4-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9bdd4-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="9bdd4-130">Список удостоверений пользователей, связанных с кластером Кусто.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="9bdd4-131">Ссылки на ключ словаря удостоверений пользователей будут ARM идентификаторами ресурсов в форме: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="9bdd4-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bdd4-132">-InputObject</span></span>
<span data-ttu-id="9bdd4-133">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9bdd4-134">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="9bdd4-134">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="9bdd4-135">Имя ключа сейфа.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-135">The name of the key vault key.</span></span>

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

### <span data-ttu-id="9bdd4-136">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="9bdd4-136">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="9bdd4-137">Uri хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-137">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="9bdd4-138">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="9bdd4-138">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="9bdd4-139">Версия ключа ключа сейфа.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-139">The version of the key vault key.</span></span>

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

### <span data-ttu-id="9bdd4-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="9bdd4-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="9bdd4-141">Список языковых расширений.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-141">The list of language extensions.</span></span>
<span data-ttu-id="9bdd4-142">Чтобы создать новую таблицу, см. раздел "ЗАМЕТКИ" для свойств LANGUAGEEXTENSIONVALUE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bdd4-143">-Location</span><span class="sxs-lookup"><span data-stu-id="9bdd4-143">-Location</span></span>
<span data-ttu-id="9bdd4-144">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-144">Resource location.</span></span>

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

### <span data-ttu-id="9bdd4-145">-Name</span><span class="sxs-lookup"><span data-stu-id="9bdd4-145">-Name</span></span>
<span data-ttu-id="9bdd4-146">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-146">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="9bdd4-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9bdd4-147">-NoWait</span></span>
<span data-ttu-id="9bdd4-148">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="9bdd4-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9bdd4-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="9bdd4-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="9bdd4-150">Boolean value that indicate if the optimized autoscale feature is enabled or not.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="9bdd4-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="9bdd4-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="9bdd4-152">Максимальное количество разрешенных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="9bdd4-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="9bdd4-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="9bdd4-154">Количество экземпляров, разрешенных как минимум.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="9bdd4-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="9bdd4-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="9bdd4-156">Версия определенного шаблона, например 1.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="9bdd4-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bdd4-157">-ResourceGroupName</span></span>
<span data-ttu-id="9bdd4-158">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="9bdd4-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="9bdd4-159">-SkuCapacity</span></span>
<span data-ttu-id="9bdd4-160">Количество экземпляров кластера.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="9bdd4-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9bdd4-161">-SkuName</span></span>
<span data-ttu-id="9bdd4-162">Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-162">SKU name.</span></span>

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

### <span data-ttu-id="9bdd4-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="9bdd4-163">-SkuTier</span></span>
<span data-ttu-id="9bdd4-164">Уровень SKU.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-164">SKU tier.</span></span>

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

### <span data-ttu-id="9bdd4-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9bdd4-165">-SubscriptionId</span></span>
<span data-ttu-id="9bdd4-166">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9bdd4-167">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-167">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9bdd4-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="9bdd4-168">-Tag</span></span>
<span data-ttu-id="9bdd4-169">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-169">Resource tags.</span></span>

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

### <span data-ttu-id="9bdd4-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="9bdd4-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="9bdd4-171">Внешние клиенты кластера.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-171">The cluster's external tenants.</span></span>
<span data-ttu-id="9bdd4-172">Чтобы построить таблицу, см. раздел "ЗАМЕТКи" для свойств TRUSTEDEXTERNALTENANT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bdd4-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="9bdd4-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="9bdd4-174">ИД ресурса общедоступных IP-адресов службы управления данными.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="9bdd4-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="9bdd4-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="9bdd4-176">ИД ресурса общедоступных IP-адресов службы Engine.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="9bdd4-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="9bdd4-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="9bdd4-178">ИД ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="9bdd4-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9bdd4-179">-Confirm</span></span>
<span data-ttu-id="9bdd4-180">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bdd4-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bdd4-181">-WhatIf</span></span>
<span data-ttu-id="9bdd4-182">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bdd4-183">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bdd4-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bdd4-184">CommonParameters</span></span>
<span data-ttu-id="9bdd4-185">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bdd4-186">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9bdd4-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bdd4-187">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9bdd4-187">INPUTS</span></span>

### <span data-ttu-id="9bdd4-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="9bdd4-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="9bdd4-189">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9bdd4-189">OUTPUTS</span></span>

### <span data-ttu-id="9bdd4-190">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span><span class="sxs-lookup"><span data-stu-id="9bdd4-190">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="9bdd4-191">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9bdd4-191">NOTES</span></span>

<span data-ttu-id="9bdd4-192">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9bdd4-192">ALIASES</span></span>

<span data-ttu-id="9bdd4-193">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="9bdd4-193">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9bdd4-194">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-194">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9bdd4-195">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-195">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9bdd4-196">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="9bdd4-196">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9bdd4-197">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-197">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="9bdd4-198">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="9bdd4-198">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="9bdd4-199">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-199">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="9bdd4-200">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-200">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="9bdd4-201">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="9bdd4-201">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9bdd4-202">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-202">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="9bdd4-203">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="9bdd4-203">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="9bdd4-204">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-204">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="9bdd4-205">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-205">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9bdd4-206">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-206">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="9bdd4-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: список языковых расширений.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="9bdd4-208">`[Name <LanguageExtensionName?>]`: имя расширения языка.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-208">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="9bdd4-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: внешние клиенты кластера.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="9bdd4-210">`[Value <String>]`: GUID, представляющий внешний клиент.</span><span class="sxs-lookup"><span data-stu-id="9bdd4-210">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="9bdd4-211">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9bdd4-211">RELATED LINKS</span></span>

