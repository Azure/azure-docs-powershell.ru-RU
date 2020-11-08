---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b8b6c11da622b7fa0ee67dc418f2055dd72c1d13
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243553"
---
# <span data-ttu-id="3a57a-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="3a57a-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="3a57a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a57a-102">SYNOPSIS</span></span>
<span data-ttu-id="3a57a-103">Создайте или обновите кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="3a57a-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="3a57a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a57a-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3a57a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a57a-105">DESCRIPTION</span></span>
<span data-ttu-id="3a57a-106">Создайте или обновите кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="3a57a-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="3a57a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a57a-107">EXAMPLES</span></span>

### <span data-ttu-id="3a57a-108">Пример 1: создание нового кластера Kusto</span><span class="sxs-lookup"><span data-stu-id="3a57a-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="3a57a-109">В приведенной выше команде создается новый кластер Kusto с именем "testnewkustocluster" в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="3a57a-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="3a57a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a57a-110">PARAMETERS</span></span>

### <span data-ttu-id="3a57a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a57a-111">-AsJob</span></span>
<span data-ttu-id="3a57a-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="3a57a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="3a57a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a57a-113">-DefaultProfile</span></span>
<span data-ttu-id="3a57a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a57a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a57a-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="3a57a-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="3a57a-116">Логическое значение, указывающее, зашифрованы ли диски кластера.</span><span class="sxs-lookup"><span data-stu-id="3a57a-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="3a57a-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="3a57a-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="3a57a-118">Логическое значение, указывающее, включено ли двойное шифрование.</span><span class="sxs-lookup"><span data-stu-id="3a57a-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="3a57a-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="3a57a-119">-EnablePurge</span></span>
<span data-ttu-id="3a57a-120">Логическое значение, указывающее, включены ли операции очистки.</span><span class="sxs-lookup"><span data-stu-id="3a57a-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="3a57a-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="3a57a-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="3a57a-122">Логическое значение, указывающее, включена ли потоковая передача.</span><span class="sxs-lookup"><span data-stu-id="3a57a-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="3a57a-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="3a57a-123">-IdentityType</span></span>
<span data-ttu-id="3a57a-124">Тип удостоверения.</span><span class="sxs-lookup"><span data-stu-id="3a57a-124">The identity type.</span></span>

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

### <span data-ttu-id="3a57a-125">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3a57a-125">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="3a57a-126">Список удостоверений пользователей, связанных с кластером Kusto.</span><span class="sxs-lookup"><span data-stu-id="3a57a-126">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="3a57a-127">Ссылки на ключи словаря удостоверения пользователя будут идентификаторами ресурсов ARM в форме: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="3a57a-127">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="3a57a-128">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="3a57a-128">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="3a57a-129">Имя ключа хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3a57a-129">The name of the key vault key.</span></span>

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

### <span data-ttu-id="3a57a-130">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="3a57a-130">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="3a57a-131">URI хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3a57a-131">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="3a57a-132">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="3a57a-132">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="3a57a-133">Версия ключа хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3a57a-133">The version of the key vault key.</span></span>

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

### <span data-ttu-id="3a57a-134">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="3a57a-134">-LanguageExtensionValue</span></span>
<span data-ttu-id="3a57a-135">Список расширений языка.</span><span class="sxs-lookup"><span data-stu-id="3a57a-135">The list of language extensions.</span></span>
<span data-ttu-id="3a57a-136">Для конструирования ознакомьтесь с разделом "Заметки" для свойств LANGUAGEEXTENSIONVALUE и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3a57a-136">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="3a57a-137">-Location</span><span class="sxs-lookup"><span data-stu-id="3a57a-137">-Location</span></span>
<span data-ttu-id="3a57a-138">Географическое расположение, в котором находится ресурс</span><span class="sxs-lookup"><span data-stu-id="3a57a-138">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="3a57a-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3a57a-139">-Name</span></span>
<span data-ttu-id="3a57a-140">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="3a57a-140">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="3a57a-141">-Wait</span><span class="sxs-lookup"><span data-stu-id="3a57a-141">-NoWait</span></span>
<span data-ttu-id="3a57a-142">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="3a57a-142">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3a57a-143">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="3a57a-143">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="3a57a-144">Логическое значение, определяющее, включена ли Оптимизированная функция автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="3a57a-144">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="3a57a-145">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="3a57a-145">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="3a57a-146">Максимальное количество разрешенных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="3a57a-146">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="3a57a-147">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="3a57a-147">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="3a57a-148">Минимальное количество разрешенных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="3a57a-148">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="3a57a-149">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="3a57a-149">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="3a57a-150">Версия шаблона, определенная для экземпляра 1.</span><span class="sxs-lookup"><span data-stu-id="3a57a-150">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="3a57a-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a57a-151">-ResourceGroupName</span></span>
<span data-ttu-id="3a57a-152">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="3a57a-152">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="3a57a-153">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="3a57a-153">-SkuCapacity</span></span>
<span data-ttu-id="3a57a-154">Количество экземпляров кластера.</span><span class="sxs-lookup"><span data-stu-id="3a57a-154">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="3a57a-155">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3a57a-155">-SkuName</span></span>
<span data-ttu-id="3a57a-156">Название SKU.</span><span class="sxs-lookup"><span data-stu-id="3a57a-156">SKU name.</span></span>

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

### <span data-ttu-id="3a57a-157">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="3a57a-157">-SkuTier</span></span>
<span data-ttu-id="3a57a-158">Уровень SKU.</span><span class="sxs-lookup"><span data-stu-id="3a57a-158">SKU tier.</span></span>

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

### <span data-ttu-id="3a57a-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a57a-159">-SubscriptionId</span></span>
<span data-ttu-id="3a57a-160">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3a57a-160">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3a57a-161">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="3a57a-161">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3a57a-162">-Тег</span><span class="sxs-lookup"><span data-stu-id="3a57a-162">-Tag</span></span>
<span data-ttu-id="3a57a-163">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3a57a-163">Resource tags.</span></span>

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

### <span data-ttu-id="3a57a-164">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="3a57a-164">-TrustedExternalTenant</span></span>
<span data-ttu-id="3a57a-165">Внешние клиенты кластера.</span><span class="sxs-lookup"><span data-stu-id="3a57a-165">The cluster's external tenants.</span></span>
<span data-ttu-id="3a57a-166">Для конструирования ознакомьтесь с разделом "Заметки" для свойств TRUSTEDEXTERNALTENANT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3a57a-166">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3a57a-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="3a57a-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="3a57a-168">Идентификатор ресурса общедоступного IP-адреса службы управления данными.</span><span class="sxs-lookup"><span data-stu-id="3a57a-168">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="3a57a-169">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="3a57a-169">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="3a57a-170">Идентификатор ресурса общедоступного IP-адреса службы модуля.</span><span class="sxs-lookup"><span data-stu-id="3a57a-170">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="3a57a-171">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="3a57a-171">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="3a57a-172">Идентификатор ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="3a57a-172">The subnet resource id.</span></span>

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

### <span data-ttu-id="3a57a-173">-Zone</span><span class="sxs-lookup"><span data-stu-id="3a57a-173">-Zone</span></span>
<span data-ttu-id="3a57a-174">Зоны доступности кластера.</span><span class="sxs-lookup"><span data-stu-id="3a57a-174">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="3a57a-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a57a-175">-Confirm</span></span>
<span data-ttu-id="3a57a-176">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3a57a-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a57a-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a57a-177">-WhatIf</span></span>
<span data-ttu-id="3a57a-178">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3a57a-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a57a-179">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3a57a-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a57a-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a57a-180">CommonParameters</span></span>
<span data-ttu-id="3a57a-181">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a57a-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a57a-182">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a57a-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a57a-183">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a57a-183">INPUTS</span></span>

## <span data-ttu-id="3a57a-184">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a57a-184">OUTPUTS</span></span>

### <span data-ttu-id="3a57a-185">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="3a57a-185">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="3a57a-186">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a57a-186">NOTES</span></span>

<span data-ttu-id="3a57a-187">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="3a57a-187">ALIASES</span></span>

<span data-ttu-id="3a57a-188">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="3a57a-188">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3a57a-189">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3a57a-189">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3a57a-190">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3a57a-190">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3a57a-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: список расширений языка.</span><span class="sxs-lookup"><span data-stu-id="3a57a-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="3a57a-192">`[Name <LanguageExtensionName?>]`: Имя расширения языка.</span><span class="sxs-lookup"><span data-stu-id="3a57a-192">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="3a57a-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: внешние клиенты кластера.</span><span class="sxs-lookup"><span data-stu-id="3a57a-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="3a57a-194">`[Value <String>]`: GUID, представляющий внешний клиент.</span><span class="sxs-lookup"><span data-stu-id="3a57a-194">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="3a57a-195">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a57a-195">RELATED LINKS</span></span>

