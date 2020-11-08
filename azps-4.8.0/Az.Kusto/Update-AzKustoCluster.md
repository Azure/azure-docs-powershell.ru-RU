---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: a3e1561feb470708420015bac1e2f0688f182896
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244491"
---
# <span data-ttu-id="1dd61-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="1dd61-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="1dd61-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1dd61-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd61-103">Обновите кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="1dd61-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="1dd61-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1dd61-104">SYNTAX</span></span>

### <span data-ttu-id="1dd61-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1dd61-105">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="1dd61-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1dd61-106">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="1dd61-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1dd61-107">DESCRIPTION</span></span>
<span data-ttu-id="1dd61-108">Обновите кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="1dd61-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="1dd61-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1dd61-109">EXAMPLES</span></span>

### <span data-ttu-id="1dd61-110">Пример 1: обновление существующего кластера по имени</span><span class="sxs-lookup"><span data-stu-id="1dd61-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="1dd61-111">Приведенная выше команда обновляет SKU кластера Kusto "testnewkustocluster", который находится в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="1dd61-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="1dd61-112">Пример 2: обновление существующего кластера по имени</span><span class="sxs-lookup"><span data-stu-id="1dd61-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="1dd61-113">Приведенная выше команда обновляет кластер "testnewkustocluster", который находится в группе ресурсов "testrg" с помощью ключа, управляемого клиентом.</span><span class="sxs-lookup"><span data-stu-id="1dd61-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="1dd61-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1dd61-114">PARAMETERS</span></span>

### <span data-ttu-id="1dd61-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dd61-115">-AsJob</span></span>
<span data-ttu-id="1dd61-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="1dd61-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1dd61-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd61-117">-DefaultProfile</span></span>
<span data-ttu-id="1dd61-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1dd61-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dd61-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="1dd61-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="1dd61-120">Логическое значение, указывающее, зашифрованы ли диски кластера.</span><span class="sxs-lookup"><span data-stu-id="1dd61-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="1dd61-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="1dd61-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="1dd61-122">Логическое значение, указывающее, включено ли двойное шифрование.</span><span class="sxs-lookup"><span data-stu-id="1dd61-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="1dd61-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="1dd61-123">-EnablePurge</span></span>
<span data-ttu-id="1dd61-124">Логическое значение, указывающее, включены ли операции очистки.</span><span class="sxs-lookup"><span data-stu-id="1dd61-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="1dd61-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="1dd61-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="1dd61-126">Логическое значение, указывающее, включена ли потоковая передача.</span><span class="sxs-lookup"><span data-stu-id="1dd61-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="1dd61-127">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="1dd61-127">-IdentityType</span></span>
<span data-ttu-id="1dd61-128">Тип удостоверения.</span><span class="sxs-lookup"><span data-stu-id="1dd61-128">The identity type.</span></span>

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

### <span data-ttu-id="1dd61-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1dd61-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="1dd61-130">Список удостоверений пользователей, связанных с кластером Kusto.</span><span class="sxs-lookup"><span data-stu-id="1dd61-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="1dd61-131">Ссылки на ключи словаря удостоверения пользователя будут идентификаторами ресурсов ARM в форме: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="1dd61-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="1dd61-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dd61-132">-InputObject</span></span>
<span data-ttu-id="1dd61-133">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="1dd61-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1dd61-134">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="1dd61-134">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="1dd61-135">Имя ключа хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1dd61-135">The name of the key vault key.</span></span>

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

### <span data-ttu-id="1dd61-136">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="1dd61-136">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="1dd61-137">URI хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1dd61-137">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="1dd61-138">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="1dd61-138">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="1dd61-139">Версия ключа хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1dd61-139">The version of the key vault key.</span></span>

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

### <span data-ttu-id="1dd61-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="1dd61-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="1dd61-141">Список расширений языка.</span><span class="sxs-lookup"><span data-stu-id="1dd61-141">The list of language extensions.</span></span>
<span data-ttu-id="1dd61-142">Для конструирования ознакомьтесь с разделом "Заметки" для свойств LANGUAGEEXTENSIONVALUE и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="1dd61-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="1dd61-143">-Location</span><span class="sxs-lookup"><span data-stu-id="1dd61-143">-Location</span></span>
<span data-ttu-id="1dd61-144">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="1dd61-144">Resource location.</span></span>

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

### <span data-ttu-id="1dd61-145">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1dd61-145">-Name</span></span>
<span data-ttu-id="1dd61-146">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="1dd61-146">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="1dd61-147">-Wait</span><span class="sxs-lookup"><span data-stu-id="1dd61-147">-NoWait</span></span>
<span data-ttu-id="1dd61-148">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="1dd61-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1dd61-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="1dd61-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="1dd61-150">Логическое значение, определяющее, включена ли Оптимизированная функция автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="1dd61-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="1dd61-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="1dd61-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="1dd61-152">Максимальное количество разрешенных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="1dd61-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="1dd61-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="1dd61-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="1dd61-154">Минимальное количество разрешенных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="1dd61-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="1dd61-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="1dd61-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="1dd61-156">Версия шаблона, определенная для экземпляра 1.</span><span class="sxs-lookup"><span data-stu-id="1dd61-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="1dd61-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dd61-157">-ResourceGroupName</span></span>
<span data-ttu-id="1dd61-158">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="1dd61-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="1dd61-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="1dd61-159">-SkuCapacity</span></span>
<span data-ttu-id="1dd61-160">Количество экземпляров кластера.</span><span class="sxs-lookup"><span data-stu-id="1dd61-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="1dd61-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1dd61-161">-SkuName</span></span>
<span data-ttu-id="1dd61-162">Название SKU.</span><span class="sxs-lookup"><span data-stu-id="1dd61-162">SKU name.</span></span>

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

### <span data-ttu-id="1dd61-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="1dd61-163">-SkuTier</span></span>
<span data-ttu-id="1dd61-164">Уровень SKU.</span><span class="sxs-lookup"><span data-stu-id="1dd61-164">SKU tier.</span></span>

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

### <span data-ttu-id="1dd61-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1dd61-165">-SubscriptionId</span></span>
<span data-ttu-id="1dd61-166">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1dd61-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1dd61-167">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="1dd61-167">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1dd61-168">-Тег</span><span class="sxs-lookup"><span data-stu-id="1dd61-168">-Tag</span></span>
<span data-ttu-id="1dd61-169">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1dd61-169">Resource tags.</span></span>

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

### <span data-ttu-id="1dd61-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="1dd61-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="1dd61-171">Внешние клиенты кластера.</span><span class="sxs-lookup"><span data-stu-id="1dd61-171">The cluster's external tenants.</span></span>
<span data-ttu-id="1dd61-172">Для конструирования ознакомьтесь с разделом "Заметки" для свойств TRUSTEDEXTERNALTENANT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="1dd61-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1dd61-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="1dd61-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="1dd61-174">Идентификатор ресурса общедоступного IP-адреса службы управления данными.</span><span class="sxs-lookup"><span data-stu-id="1dd61-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="1dd61-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="1dd61-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="1dd61-176">Идентификатор ресурса общедоступного IP-адреса службы модуля.</span><span class="sxs-lookup"><span data-stu-id="1dd61-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="1dd61-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="1dd61-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="1dd61-178">Идентификатор ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="1dd61-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="1dd61-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1dd61-179">-Confirm</span></span>
<span data-ttu-id="1dd61-180">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1dd61-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dd61-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dd61-181">-WhatIf</span></span>
<span data-ttu-id="1dd61-182">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1dd61-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dd61-183">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1dd61-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dd61-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd61-184">CommonParameters</span></span>
<span data-ttu-id="1dd61-185">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1dd61-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd61-186">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1dd61-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd61-187">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1dd61-187">INPUTS</span></span>

### <span data-ttu-id="1dd61-188">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="1dd61-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="1dd61-189">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1dd61-189">OUTPUTS</span></span>

### <span data-ttu-id="1dd61-190">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="1dd61-190">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="1dd61-191">Пуск</span><span class="sxs-lookup"><span data-stu-id="1dd61-191">NOTES</span></span>

<span data-ttu-id="1dd61-192">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="1dd61-192">ALIASES</span></span>

<span data-ttu-id="1dd61-193">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="1dd61-193">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1dd61-194">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1dd61-194">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1dd61-195">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1dd61-195">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1dd61-196">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="1dd61-196">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1dd61-197">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="1dd61-197">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="1dd61-198">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="1dd61-198">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="1dd61-199">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="1dd61-199">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="1dd61-200">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="1dd61-200">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="1dd61-201">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="1dd61-201">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1dd61-202">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="1dd61-202">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="1dd61-203">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="1dd61-203">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="1dd61-204">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="1dd61-204">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="1dd61-205">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1dd61-205">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1dd61-206">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="1dd61-206">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="1dd61-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: список расширений языка.</span><span class="sxs-lookup"><span data-stu-id="1dd61-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="1dd61-208">`[Name <LanguageExtensionName?>]`: Имя расширения языка.</span><span class="sxs-lookup"><span data-stu-id="1dd61-208">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="1dd61-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: внешние клиенты кластера.</span><span class="sxs-lookup"><span data-stu-id="1dd61-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="1dd61-210">`[Value <String>]`: GUID, представляющий внешний клиент.</span><span class="sxs-lookup"><span data-stu-id="1dd61-210">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="1dd61-211">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1dd61-211">RELATED LINKS</span></span>

