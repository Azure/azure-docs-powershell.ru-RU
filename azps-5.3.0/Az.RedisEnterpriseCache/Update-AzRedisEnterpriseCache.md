---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
ms.openlocfilehash: ef1ef3d45594b0e290a014fb3aa98d670e5681a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421159"
---
# <span data-ttu-id="35a10-101">Update-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="35a10-101">Update-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="35a10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35a10-102">SYNOPSIS</span></span>
<span data-ttu-id="35a10-103">Обновление существующего кластера RedisEnterprise</span><span class="sxs-lookup"><span data-stu-id="35a10-103">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="35a10-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35a10-104">SYNTAX</span></span>

### <span data-ttu-id="35a10-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35a10-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Capacity <Int32>] [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="35a10-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="35a10-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-Capacity <Int32>]
 [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35a10-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35a10-107">DESCRIPTION</span></span>
<span data-ttu-id="35a10-108">Обновление существующего кластера RedisEnterprise</span><span class="sxs-lookup"><span data-stu-id="35a10-108">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="35a10-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35a10-109">EXAMPLES</span></span>

### <span data-ttu-id="35a10-110">Пример 1. Обновление кэша Redis Enterprise</span><span class="sxs-lookup"><span data-stu-id="35a10-110">Example 1: Update Redis Enterprise Cache</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -MinimumTlsVersion "1.2" -Tag @{"tag" = "value"}

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="35a10-111">Эта команда обновляет минимальную версию TLS и добавляет тег в кэш Redis Enterprise с именем MyCache.</span><span class="sxs-lookup"><span data-stu-id="35a10-111">This command updates the minimum TLS version and adds a tag to the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="35a10-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35a10-112">PARAMETERS</span></span>

### <span data-ttu-id="35a10-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35a10-113">-AsJob</span></span>
<span data-ttu-id="35a10-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="35a10-114">Run the command as a job</span></span>

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

### <span data-ttu-id="35a10-115">-Capacity</span><span class="sxs-lookup"><span data-stu-id="35a10-115">-Capacity</span></span>
<span data-ttu-id="35a10-116">Размер кластера RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="35a10-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="35a10-117">Значение по умолчанию 2 или 3 в зависимости от SKU.</span><span class="sxs-lookup"><span data-stu-id="35a10-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="35a10-118">Допустимые значения ( 2, 4, 6, ...) для корпоративных skus и (3, 9, 15, ...) для flash SKUs.</span><span class="sxs-lookup"><span data-stu-id="35a10-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: SkuCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a10-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="35a10-119">-ClusterName</span></span>
<span data-ttu-id="35a10-120">Название кластера RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="35a10-120">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a10-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35a10-121">-DefaultProfile</span></span>
<span data-ttu-id="35a10-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35a10-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35a10-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35a10-123">-InputObject</span></span>
<span data-ttu-id="35a10-124">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="35a10-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35a10-125">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="35a10-125">-MinimumTlsVersion</span></span>
<span data-ttu-id="35a10-126">Минимальная поддерживаемая версия TLS для кластера, например 1.2</span><span class="sxs-lookup"><span data-stu-id="35a10-126">The minimum TLS version for the cluster to support, e.g. '1.2'</span></span>

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

### <span data-ttu-id="35a10-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="35a10-127">-NoWait</span></span>
<span data-ttu-id="35a10-128">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="35a10-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="35a10-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35a10-129">-ResourceGroupName</span></span>
<span data-ttu-id="35a10-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35a10-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="35a10-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="35a10-131">-Sku</span></span>
<span data-ttu-id="35a10-132">Тип кластера RedisEnterprise для развертывания.</span><span class="sxs-lookup"><span data-stu-id="35a10-132">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="35a10-133">Возможные значения: (Enterprise_E10, EnterpriseFlash_F300 и т. д.)</span><span class="sxs-lookup"><span data-stu-id="35a10-133">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.SkuName
Parameter Sets: (All)
Aliases: SkuName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a10-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35a10-134">-SubscriptionId</span></span>
<span data-ttu-id="35a10-135">Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="35a10-135">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="35a10-136">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="35a10-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="35a10-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="35a10-137">-Tag</span></span>
<span data-ttu-id="35a10-138">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35a10-138">Resource tags.</span></span>

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

### <span data-ttu-id="35a10-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35a10-139">-Confirm</span></span>
<span data-ttu-id="35a10-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="35a10-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35a10-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35a10-141">-WhatIf</span></span>
<span data-ttu-id="35a10-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35a10-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35a10-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="35a10-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35a10-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a10-144">CommonParameters</span></span>
<span data-ttu-id="35a10-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35a10-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a10-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35a10-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a10-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35a10-147">INPUTS</span></span>

### <span data-ttu-id="35a10-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="35a10-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="35a10-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35a10-149">OUTPUTS</span></span>

### <span data-ttu-id="35a10-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="35a10-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="35a10-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35a10-151">NOTES</span></span>

<span data-ttu-id="35a10-152">ALIASES</span><span class="sxs-lookup"><span data-stu-id="35a10-152">ALIASES</span></span>

<span data-ttu-id="35a10-153">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="35a10-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="35a10-154">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="35a10-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35a10-155">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35a10-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="35a10-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="35a10-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="35a10-157">`[ClusterName <String>]`: Название кластера RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="35a10-157">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="35a10-158">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="35a10-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="35a10-159">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="35a10-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35a10-160">`[Location <String>]`Регион, в который она веется.</span><span class="sxs-lookup"><span data-stu-id="35a10-160">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="35a10-161">`[OperationId <String>]`: уникальный идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="35a10-161">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="35a10-162">`[PrivateEndpointConnectionName <String>]`: имя подключения частной конечной точки, связанного с ресурсом Azure</span><span class="sxs-lookup"><span data-stu-id="35a10-162">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="35a10-163">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35a10-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="35a10-164">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="35a10-164">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="35a10-165">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="35a10-165">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="35a10-166">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35a10-166">RELATED LINKS</span></span>

