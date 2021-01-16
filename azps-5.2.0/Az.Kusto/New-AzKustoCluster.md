---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b8b6c11da622b7fa0ee67dc418f2055dd72c1d13
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410231"
---
# <span data-ttu-id="fd111-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="fd111-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="fd111-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd111-102">SYNOPSIS</span></span>
<span data-ttu-id="fd111-103">Создайте или обновйте кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="fd111-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="fd111-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fd111-104">SYNTAX</span></span>

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

## <span data-ttu-id="fd111-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd111-105">DESCRIPTION</span></span>
<span data-ttu-id="fd111-106">Создайте или обновйте кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="fd111-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="fd111-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fd111-107">EXAMPLES</span></span>

### <span data-ttu-id="fd111-108">Пример 1. Создание кластера "Кузто"</span><span class="sxs-lookup"><span data-stu-id="fd111-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="fd111-109">С этой командой создается новый кластер "Кузто" с именем "testnewkustocluster" в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="fd111-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="fd111-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd111-110">PARAMETERS</span></span>

### <span data-ttu-id="fd111-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd111-111">-AsJob</span></span>
<span data-ttu-id="fd111-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="fd111-112">Run the command as a job</span></span>

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

### <span data-ttu-id="fd111-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd111-113">-DefaultProfile</span></span>
<span data-ttu-id="fd111-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd111-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd111-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="fd111-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="fd111-116">Boolean value that indicates if the cluster's disks are encrypted.</span><span class="sxs-lookup"><span data-stu-id="fd111-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="fd111-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="fd111-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="fd111-118">Boolean value that indicates if double encryption is enabled.</span><span class="sxs-lookup"><span data-stu-id="fd111-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="fd111-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="fd111-119">-EnablePurge</span></span>
<span data-ttu-id="fd111-120">Boolean value that indicates if the purge operations are enabled.</span><span class="sxs-lookup"><span data-stu-id="fd111-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="fd111-121">-EnableStreamingingest</span><span class="sxs-lookup"><span data-stu-id="fd111-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="fd111-122">Boolean value that indicates if the streaming ingest is enabled.</span><span class="sxs-lookup"><span data-stu-id="fd111-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="fd111-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="fd111-123">-IdentityType</span></span>
<span data-ttu-id="fd111-124">Тип удостоверения.</span><span class="sxs-lookup"><span data-stu-id="fd111-124">The identity type.</span></span>

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

### <span data-ttu-id="fd111-125">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="fd111-125">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="fd111-126">Список удостоверений пользователей, связанных с кластером Кусто.</span><span class="sxs-lookup"><span data-stu-id="fd111-126">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="fd111-127">Ссылки на ключ словаря удостоверений пользователей будут ARM идентификаторами ресурсов в форме: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="fd111-127">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="fd111-128">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="fd111-128">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="fd111-129">Имя ключа сейфа.</span><span class="sxs-lookup"><span data-stu-id="fd111-129">The name of the key vault key.</span></span>

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

### <span data-ttu-id="fd111-130">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="fd111-130">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="fd111-131">Uri хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="fd111-131">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="fd111-132">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="fd111-132">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="fd111-133">Версия ключа ключа сейфа.</span><span class="sxs-lookup"><span data-stu-id="fd111-133">The version of the key vault key.</span></span>

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

### <span data-ttu-id="fd111-134">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="fd111-134">-LanguageExtensionValue</span></span>
<span data-ttu-id="fd111-135">Список языковых расширений.</span><span class="sxs-lookup"><span data-stu-id="fd111-135">The list of language extensions.</span></span>
<span data-ttu-id="fd111-136">Чтобы создать новую таблицу, см. раздел "ЗАМЕТКИ" для свойств LANGUAGEEXTENSIONVALUE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="fd111-136">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="fd111-137">-Location</span><span class="sxs-lookup"><span data-stu-id="fd111-137">-Location</span></span>
<span data-ttu-id="fd111-138">Географическое расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="fd111-138">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="fd111-139">-Name</span><span class="sxs-lookup"><span data-stu-id="fd111-139">-Name</span></span>
<span data-ttu-id="fd111-140">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="fd111-140">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="fd111-141">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fd111-141">-NoWait</span></span>
<span data-ttu-id="fd111-142">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="fd111-142">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fd111-143">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="fd111-143">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="fd111-144">Boolean value that indicate if the optimized autoscale feature is enabled or not.</span><span class="sxs-lookup"><span data-stu-id="fd111-144">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="fd111-145">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="fd111-145">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="fd111-146">Максимальное количество разрешенных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="fd111-146">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="fd111-147">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="fd111-147">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="fd111-148">Количество экземпляров, разрешенных как минимум.</span><span class="sxs-lookup"><span data-stu-id="fd111-148">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="fd111-149">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="fd111-149">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="fd111-150">Версия определенного шаблона, например 1.</span><span class="sxs-lookup"><span data-stu-id="fd111-150">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="fd111-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd111-151">-ResourceGroupName</span></span>
<span data-ttu-id="fd111-152">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="fd111-152">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="fd111-153">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="fd111-153">-SkuCapacity</span></span>
<span data-ttu-id="fd111-154">Количество экземпляров кластера.</span><span class="sxs-lookup"><span data-stu-id="fd111-154">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="fd111-155">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fd111-155">-SkuName</span></span>
<span data-ttu-id="fd111-156">Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="fd111-156">SKU name.</span></span>

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

### <span data-ttu-id="fd111-157">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="fd111-157">-SkuTier</span></span>
<span data-ttu-id="fd111-158">Уровень SKU.</span><span class="sxs-lookup"><span data-stu-id="fd111-158">SKU tier.</span></span>

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

### <span data-ttu-id="fd111-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fd111-159">-SubscriptionId</span></span>
<span data-ttu-id="fd111-160">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fd111-160">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fd111-161">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="fd111-161">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fd111-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="fd111-162">-Tag</span></span>
<span data-ttu-id="fd111-163">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fd111-163">Resource tags.</span></span>

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

### <span data-ttu-id="fd111-164">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="fd111-164">-TrustedExternalTenant</span></span>
<span data-ttu-id="fd111-165">Внешние клиенты кластера.</span><span class="sxs-lookup"><span data-stu-id="fd111-165">The cluster's external tenants.</span></span>
<span data-ttu-id="fd111-166">Чтобы построить таблицу, см. раздел "ЗАМЕТКи" для свойств TRUSTEDEXTERNALTENANT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="fd111-166">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fd111-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="fd111-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="fd111-168">ИД ресурса общедоступных IP-адресов службы управления данными.</span><span class="sxs-lookup"><span data-stu-id="fd111-168">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="fd111-169">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="fd111-169">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="fd111-170">ИД ресурса общедоступных IP-адресов службы Engine.</span><span class="sxs-lookup"><span data-stu-id="fd111-170">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="fd111-171">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="fd111-171">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="fd111-172">ИД ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="fd111-172">The subnet resource id.</span></span>

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

### <span data-ttu-id="fd111-173">-Zone</span><span class="sxs-lookup"><span data-stu-id="fd111-173">-Zone</span></span>
<span data-ttu-id="fd111-174">Зоны доступности кластера.</span><span class="sxs-lookup"><span data-stu-id="fd111-174">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="fd111-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd111-175">-Confirm</span></span>
<span data-ttu-id="fd111-176">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fd111-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd111-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd111-177">-WhatIf</span></span>
<span data-ttu-id="fd111-178">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd111-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd111-179">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fd111-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd111-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd111-180">CommonParameters</span></span>
<span data-ttu-id="fd111-181">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd111-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd111-182">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd111-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd111-183">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd111-183">INPUTS</span></span>

## <span data-ttu-id="fd111-184">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fd111-184">OUTPUTS</span></span>

### <span data-ttu-id="fd111-185">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span><span class="sxs-lookup"><span data-stu-id="fd111-185">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="fd111-186">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fd111-186">NOTES</span></span>

<span data-ttu-id="fd111-187">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fd111-187">ALIASES</span></span>

<span data-ttu-id="fd111-188">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="fd111-188">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fd111-189">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="fd111-189">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fd111-190">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fd111-190">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fd111-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: список языковых расширений.</span><span class="sxs-lookup"><span data-stu-id="fd111-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="fd111-192">`[Name <LanguageExtensionName?>]`: имя расширения языка.</span><span class="sxs-lookup"><span data-stu-id="fd111-192">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="fd111-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: внешние клиенты кластера.</span><span class="sxs-lookup"><span data-stu-id="fd111-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="fd111-194">`[Value <String>]`: GUID, представляющий внешний клиент.</span><span class="sxs-lookup"><span data-stu-id="fd111-194">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="fd111-195">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd111-195">RELATED LINKS</span></span>

