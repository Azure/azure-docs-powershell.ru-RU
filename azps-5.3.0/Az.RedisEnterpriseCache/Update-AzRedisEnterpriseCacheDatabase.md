---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 9b41dbeaa10b77ed86567a51ec5fb106648e8ebd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421151"
---
# <span data-ttu-id="3cc67-101">Update-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="3cc67-101">Update-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="3cc67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cc67-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc67-103">Обновление базы данных</span><span class="sxs-lookup"><span data-stu-id="3cc67-103">Updates a database</span></span>

## <span data-ttu-id="3cc67-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3cc67-104">SYNTAX</span></span>

### <span data-ttu-id="3cc67-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3cc67-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>]
 [-EvictionPolicy <EvictionPolicy>] [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3cc67-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3cc67-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -InputObject <IRedisEnterpriseCacheIdentity>
 [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>]
 [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3cc67-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cc67-107">DESCRIPTION</span></span>
<span data-ttu-id="3cc67-108">Обновление базы данных</span><span class="sxs-lookup"><span data-stu-id="3cc67-108">Updates a database</span></span>

## <span data-ttu-id="3cc67-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3cc67-109">EXAMPLES</span></span>

### <span data-ttu-id="3cc67-110">Пример 1. Обновление протокола клиента</span><span class="sxs-lookup"><span data-stu-id="3cc67-110">Example 1: Update client protocol</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Plaintext"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="3cc67-111">Эта команда обновляет клиентский протокол базы данных для кэша Redis Enterprise под названием MyCache.</span><span class="sxs-lookup"><span data-stu-id="3cc67-111">This command updates the client protocol of the database for the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="3cc67-112">Пример 2. Обновление протокола клиента и политики забвения</span><span class="sxs-lookup"><span data-stu-id="3cc67-112">Example 2: Update client protocol and eviction policy</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Encrypted" -EvictionPolicy "NoEviction"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="3cc67-113">Эта команда обновляет клиентский протокол и политику присоединения к базе данных для кэша Redis Enterprise под названием MyCache.</span><span class="sxs-lookup"><span data-stu-id="3cc67-113">This command updates the client protocol and eviction policy of the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="3cc67-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cc67-114">PARAMETERS</span></span>

### <span data-ttu-id="3cc67-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cc67-115">-AsJob</span></span>
<span data-ttu-id="3cc67-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="3cc67-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3cc67-117">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="3cc67-117">-ClientProtocol</span></span>
<span data-ttu-id="3cc67-118">Указывает, могут ли клиенты redis подключаться с помощью протоколов, зашифрованных по протоколу TLS или plaintext redis.</span><span class="sxs-lookup"><span data-stu-id="3cc67-118">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="3cc67-119">Значение по умолчанию — шифрование TLS.</span><span class="sxs-lookup"><span data-stu-id="3cc67-119">Default is TLS-encrypted.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.Protocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cc67-120">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="3cc67-120">-ClusteringPolicy</span></span>
<span data-ttu-id="3cc67-121">Политика кластеров — по умолчанию osSCluster.</span><span class="sxs-lookup"><span data-stu-id="3cc67-121">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="3cc67-122">Задано на момент создания.</span><span class="sxs-lookup"><span data-stu-id="3cc67-122">Specified at create time.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.ClusteringPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cc67-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3cc67-123">-ClusterName</span></span>
<span data-ttu-id="3cc67-124">Название кластера RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="3cc67-124">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="3cc67-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc67-125">-DefaultProfile</span></span>
<span data-ttu-id="3cc67-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3cc67-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cc67-127">-ВуассионПолиция</span><span class="sxs-lookup"><span data-stu-id="3cc67-127">-EvictionPolicy</span></span>
<span data-ttu-id="3cc67-128">Политика присоединения к redis — значение по умолчанию — VolatileLRU</span><span class="sxs-lookup"><span data-stu-id="3cc67-128">Redis eviction policy - default is VolatileLRU</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.EvictionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cc67-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3cc67-129">-InputObject</span></span>
<span data-ttu-id="3cc67-130">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="3cc67-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3cc67-131">-Module</span><span class="sxs-lookup"><span data-stu-id="3cc67-131">-Module</span></span>
<span data-ttu-id="3cc67-132">Необязательный набор модулей redis, которые нужно включить в эту базу данных, — модули можно добавлять только во время создания.</span><span class="sxs-lookup"><span data-stu-id="3cc67-132">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="3cc67-133">Чтобы создать новую таблицу, см. раздел "ЗАМЕТКИ" для свойств MODULE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="3cc67-133">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IModule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cc67-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3cc67-134">-NoWait</span></span>
<span data-ttu-id="3cc67-135">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="3cc67-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3cc67-136">-Port</span><span class="sxs-lookup"><span data-stu-id="3cc67-136">-Port</span></span>
<span data-ttu-id="3cc67-137">TCP-порт конечной точки базы данных.</span><span class="sxs-lookup"><span data-stu-id="3cc67-137">TCP port of the database endpoint.</span></span>
<span data-ttu-id="3cc67-138">Задано на момент создания.</span><span class="sxs-lookup"><span data-stu-id="3cc67-138">Specified at create time.</span></span>
<span data-ttu-id="3cc67-139">Значение по умолчанию для доступного порта.</span><span class="sxs-lookup"><span data-stu-id="3cc67-139">Defaults to an available port.</span></span>

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

### <span data-ttu-id="3cc67-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cc67-140">-ResourceGroupName</span></span>
<span data-ttu-id="3cc67-141">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3cc67-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="3cc67-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3cc67-142">-SubscriptionId</span></span>
<span data-ttu-id="3cc67-143">Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3cc67-143">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3cc67-144">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="3cc67-144">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3cc67-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cc67-145">-Confirm</span></span>
<span data-ttu-id="3cc67-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cc67-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cc67-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cc67-147">-WhatIf</span></span>
<span data-ttu-id="3cc67-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cc67-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cc67-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3cc67-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cc67-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc67-150">CommonParameters</span></span>
<span data-ttu-id="3cc67-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cc67-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc67-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cc67-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc67-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3cc67-153">INPUTS</span></span>

### <span data-ttu-id="3cc67-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="3cc67-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="3cc67-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3cc67-155">OUTPUTS</span></span>

### <span data-ttu-id="3cc67-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="3cc67-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="3cc67-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3cc67-157">NOTES</span></span>

<span data-ttu-id="3cc67-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3cc67-158">ALIASES</span></span>

<span data-ttu-id="3cc67-159">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="3cc67-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3cc67-160">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="3cc67-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3cc67-161">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3cc67-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3cc67-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="3cc67-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3cc67-163">`[ClusterName <String>]`: Название кластера RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="3cc67-163">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="3cc67-164">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="3cc67-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3cc67-165">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="3cc67-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3cc67-166">`[Location <String>]`Регион, в который она веется.</span><span class="sxs-lookup"><span data-stu-id="3cc67-166">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="3cc67-167">`[OperationId <String>]`: уникальный идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="3cc67-167">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="3cc67-168">`[PrivateEndpointConnectionName <String>]`: имя подключения частной конечной точки, связанного с ресурсом Azure</span><span class="sxs-lookup"><span data-stu-id="3cc67-168">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="3cc67-169">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3cc67-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="3cc67-170">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3cc67-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="3cc67-171">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="3cc67-171">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="3cc67-172">MODULE <IModule[]>: необязательный набор модулей redis, которые можно включить в этой базе данных. Модули можно добавлять только во время создания.</span><span class="sxs-lookup"><span data-stu-id="3cc67-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="3cc67-173">`Name <String>`: имя модуля, например "RedisBloom", 'RediSearch', 'RedisTimeSeries'</span><span class="sxs-lookup"><span data-stu-id="3cc67-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="3cc67-174">`[Arg <String>]`: Параметры конфигурации для модуля, например "ERROR_RATE 0,00 INITIAL_SIZE 400".</span><span class="sxs-lookup"><span data-stu-id="3cc67-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="3cc67-175">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3cc67-175">RELATED LINKS</span></span>

