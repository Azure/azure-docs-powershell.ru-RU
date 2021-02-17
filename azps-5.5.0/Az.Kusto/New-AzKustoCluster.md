---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b868633f0217b2048f0a83641f678e9c092d21c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243320"
---
# <span data-ttu-id="5ab95-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="5ab95-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="5ab95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ab95-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab95-103">Создайте или обновйте кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="5ab95-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="5ab95-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5ab95-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5ab95-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ab95-105">DESCRIPTION</span></span>
<span data-ttu-id="5ab95-106">Создайте или обновйте кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="5ab95-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="5ab95-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5ab95-107">EXAMPLES</span></span>

### <span data-ttu-id="5ab95-108">Пример 1. Создание кластера "Кузто"</span><span class="sxs-lookup"><span data-stu-id="5ab95-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="5ab95-109">С этой командой создается новый кластер "Кузто" с именем "testnewkustocluster" в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="5ab95-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="5ab95-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ab95-110">PARAMETERS</span></span>

### <span data-ttu-id="5ab95-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ab95-111">-AsJob</span></span>
<span data-ttu-id="5ab95-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="5ab95-112">Run the command as a job</span></span>

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

### <span data-ttu-id="5ab95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab95-113">-DefaultProfile</span></span>
<span data-ttu-id="5ab95-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ab95-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ab95-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="5ab95-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="5ab95-116">Boolean value that indicates if the cluster's disks are encrypted.</span><span class="sxs-lookup"><span data-stu-id="5ab95-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="5ab95-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="5ab95-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="5ab95-118">Boolean value that indicates if double encryption is enabled.</span><span class="sxs-lookup"><span data-stu-id="5ab95-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="5ab95-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="5ab95-119">-EnablePurge</span></span>
<span data-ttu-id="5ab95-120">Boolean value that indicates if the purge operations are enabled.</span><span class="sxs-lookup"><span data-stu-id="5ab95-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="5ab95-121">-EnableStreamingingest</span><span class="sxs-lookup"><span data-stu-id="5ab95-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="5ab95-122">Boolean value that indicates if the streaming ingest is enabled.</span><span class="sxs-lookup"><span data-stu-id="5ab95-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="5ab95-123">-EngineType</span><span class="sxs-lookup"><span data-stu-id="5ab95-123">-EngineType</span></span>
<span data-ttu-id="5ab95-124">Тип движка</span><span class="sxs-lookup"><span data-stu-id="5ab95-124">The engine type</span></span>

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

### <span data-ttu-id="5ab95-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="5ab95-125">-IdentityType</span></span>
<span data-ttu-id="5ab95-126">Тип используемых управляемых удостоверений.</span><span class="sxs-lookup"><span data-stu-id="5ab95-126">The type of managed identity used.</span></span>
<span data-ttu-id="5ab95-127">Тип "SystemAssigned, UserAssigned" включает неявное созданное удостоверение и набор удостоверений, которые назначены пользователю.</span><span class="sxs-lookup"><span data-stu-id="5ab95-127">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="5ab95-128">При типе "Нет" будут удаляться все удостоверения.</span><span class="sxs-lookup"><span data-stu-id="5ab95-128">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="5ab95-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5ab95-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="5ab95-130">Список удостоверений пользователей, связанных с кластером Кусто.</span><span class="sxs-lookup"><span data-stu-id="5ab95-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="5ab95-131">Ссылки на ключ словаря удостоверений пользователей будут ARM идентификаторами ресурсов в форме: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="5ab95-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="5ab95-132">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="5ab95-132">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="5ab95-133">Имя ключа сейфа.</span><span class="sxs-lookup"><span data-stu-id="5ab95-133">The name of the key vault key.</span></span>

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

### <span data-ttu-id="5ab95-134">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="5ab95-134">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="5ab95-135">Uri хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="5ab95-135">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="5ab95-136">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="5ab95-136">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="5ab95-137">Версия ключа ключа сейфа.</span><span class="sxs-lookup"><span data-stu-id="5ab95-137">The version of the key vault key.</span></span>

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

### <span data-ttu-id="5ab95-138">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="5ab95-138">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="5ab95-139">Удостоверение, назначенное пользователем (ARM ресурса), которое имеет доступ к ключу.</span><span class="sxs-lookup"><span data-stu-id="5ab95-139">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="5ab95-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="5ab95-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="5ab95-141">Список языковых расширений.</span><span class="sxs-lookup"><span data-stu-id="5ab95-141">The list of language extensions.</span></span>
<span data-ttu-id="5ab95-142">Чтобы создать новую таблицу, см. раздел "ЗАМЕТКИ" для свойств LANGUAGEEXTENSIONVALUE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="5ab95-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="5ab95-143">-Location</span><span class="sxs-lookup"><span data-stu-id="5ab95-143">-Location</span></span>
<span data-ttu-id="5ab95-144">Географическое расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="5ab95-144">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab95-145">-Name</span><span class="sxs-lookup"><span data-stu-id="5ab95-145">-Name</span></span>
<span data-ttu-id="5ab95-146">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="5ab95-146">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab95-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5ab95-147">-NoWait</span></span>
<span data-ttu-id="5ab95-148">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="5ab95-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5ab95-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="5ab95-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="5ab95-150">Boolean value that indicate if the optimized autoscale feature is enabled or not.</span><span class="sxs-lookup"><span data-stu-id="5ab95-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="5ab95-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="5ab95-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="5ab95-152">Максимальное количество разрешенных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="5ab95-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="5ab95-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="5ab95-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="5ab95-154">Количество экземпляров, разрешенных как минимум.</span><span class="sxs-lookup"><span data-stu-id="5ab95-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="5ab95-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="5ab95-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="5ab95-156">Версия определенного шаблона, например 1.</span><span class="sxs-lookup"><span data-stu-id="5ab95-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="5ab95-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ab95-157">-ResourceGroupName</span></span>
<span data-ttu-id="5ab95-158">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="5ab95-158">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab95-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="5ab95-159">-SkuCapacity</span></span>
<span data-ttu-id="5ab95-160">Количество экземпляров кластера.</span><span class="sxs-lookup"><span data-stu-id="5ab95-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="5ab95-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5ab95-161">-SkuName</span></span>
<span data-ttu-id="5ab95-162">Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="5ab95-162">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab95-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5ab95-163">-SkuTier</span></span>
<span data-ttu-id="5ab95-164">Уровень SKU.</span><span class="sxs-lookup"><span data-stu-id="5ab95-164">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab95-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ab95-165">-SubscriptionId</span></span>
<span data-ttu-id="5ab95-166">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5ab95-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5ab95-167">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="5ab95-167">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab95-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="5ab95-168">-Tag</span></span>
<span data-ttu-id="5ab95-169">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5ab95-169">Resource tags.</span></span>

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

### <span data-ttu-id="5ab95-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="5ab95-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="5ab95-171">Внешние клиенты кластера.</span><span class="sxs-lookup"><span data-stu-id="5ab95-171">The cluster's external tenants.</span></span>
<span data-ttu-id="5ab95-172">Чтобы построить таблицу, см. раздел "ЗАМЕТКи" для свойств TRUSTEDEXTERNALTENANT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="5ab95-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5ab95-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="5ab95-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="5ab95-174">ИД ресурса общедоступных IP-адресов службы управления данными.</span><span class="sxs-lookup"><span data-stu-id="5ab95-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="5ab95-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="5ab95-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="5ab95-176">ИД ресурса общедоступных IP-адресов службы Engine.</span><span class="sxs-lookup"><span data-stu-id="5ab95-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="5ab95-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="5ab95-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="5ab95-178">ИД ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="5ab95-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="5ab95-179">-Zone</span><span class="sxs-lookup"><span data-stu-id="5ab95-179">-Zone</span></span>
<span data-ttu-id="5ab95-180">Зоны доступности кластера.</span><span class="sxs-lookup"><span data-stu-id="5ab95-180">The availability zones of the cluster.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab95-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ab95-181">-Confirm</span></span>
<span data-ttu-id="5ab95-182">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ab95-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ab95-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ab95-183">-WhatIf</span></span>
<span data-ttu-id="5ab95-184">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ab95-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ab95-185">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5ab95-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ab95-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab95-186">CommonParameters</span></span>
<span data-ttu-id="5ab95-187">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ab95-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab95-188">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ab95-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab95-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ab95-189">INPUTS</span></span>

## <span data-ttu-id="5ab95-190">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5ab95-190">OUTPUTS</span></span>

### <span data-ttu-id="5ab95-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="5ab95-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="5ab95-192">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5ab95-192">NOTES</span></span>

<span data-ttu-id="5ab95-193">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5ab95-193">ALIASES</span></span>

<span data-ttu-id="5ab95-194">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="5ab95-194">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5ab95-195">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="5ab95-195">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5ab95-196">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5ab95-196">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5ab95-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: список языковых расширений.</span><span class="sxs-lookup"><span data-stu-id="5ab95-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="5ab95-198">`[Name <LanguageExtensionName?>]`: имя расширения языка.</span><span class="sxs-lookup"><span data-stu-id="5ab95-198">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="5ab95-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: внешние клиенты кластера.</span><span class="sxs-lookup"><span data-stu-id="5ab95-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="5ab95-200">`[Value <String>]`: GUID, представляющий внешний клиент.</span><span class="sxs-lookup"><span data-stu-id="5ab95-200">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="5ab95-201">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ab95-201">RELATED LINKS</span></span>

