---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/new-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
ms.openlocfilehash: f2f996bc212772b3b44202796e270ec345898a11
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236033"
---
# <span data-ttu-id="5b687-101">New-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="5b687-101">New-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="5b687-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b687-102">SYNOPSIS</span></span>
<span data-ttu-id="5b687-103">Создание кластера кэша Redis Enterpise и связанной базы данных</span><span class="sxs-lookup"><span data-stu-id="5b687-103">Creates a Redis Enterpise cache cluster and an associated database</span></span>

## <span data-ttu-id="5b687-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5b687-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Capacity <Int32>] [-ClientProtocol <Protocol>]
 [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>] [-MinimumTlsVersion <String>]
 [-Module <IModule[]>] [-Port <Int32>] [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5b687-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b687-105">DESCRIPTION</span></span>
<span data-ttu-id="5b687-106">Создание или обновление существующего (переописа и повторного создания, потенциального простоя) и связанной базы данных с именем "по умолчанию"</span><span class="sxs-lookup"><span data-stu-id="5b687-106">Creates or updates an existing (overwrite/recreate, with potential downtime) cache cluster and an associated database named 'default'</span></span>

## <span data-ttu-id="5b687-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5b687-107">EXAMPLES</span></span>

### <span data-ttu-id="5b687-108">Пример 1. Создание корпоративного кэша Redis</span><span class="sxs-lookup"><span data-stu-id="5b687-108">Example 1: Create a Redis Enterprise Cache</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "West US" -Sku "Enterprise_E10"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="5b687-109">Эта команда создает кэш Redis Enterprise под названием MyCache.</span><span class="sxs-lookup"><span data-stu-id="5b687-109">This command creates a Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="5b687-110">Пример 2. Создание корпоративного кэша Redis с использованием некоторых необязательных параметров</span><span class="sxs-lookup"><span data-stu-id="5b687-110">Example 2: Create a Redis Enterprise Cache using some optional parameters</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "East US" -Sku "Enterprise_E20" -Capacity 4 -Zone "1","2","3" -Module "{name:RedisBloom, args:`"ERROR_RATE 0.00 INITIAL_SIZE 400`"}","{name:RedisTimeSeries, args:`"RETENTION_POLICY 20`"}","{name:RediSearch}" -ClientProtocol "Plaintext" -EvictionPolicy "NoEviction" -ClusteringPolicy "EnterpriseCluster" -Tag @{"tag" = "value"}

Location Name    Type                            Zone      Database
-------- ----    ----                            ----      --------
East US  MyCache Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="5b687-111">Эта команда создает кэш Redis Enterprise под названием MyCache с использованием некоторых необязательных параметров.</span><span class="sxs-lookup"><span data-stu-id="5b687-111">This command creates a Redis Enterprise Cache named MyCache using some optional parameters.</span></span>

## <span data-ttu-id="5b687-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b687-112">PARAMETERS</span></span>

### <span data-ttu-id="5b687-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b687-113">-AsJob</span></span>
<span data-ttu-id="5b687-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="5b687-114">Run the command as a job</span></span>

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

### <span data-ttu-id="5b687-115">-Capacity</span><span class="sxs-lookup"><span data-stu-id="5b687-115">-Capacity</span></span>
<span data-ttu-id="5b687-116">Размер кластера RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="5b687-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="5b687-117">Значение по умолчанию 2 или 3 в зависимости от SKU.</span><span class="sxs-lookup"><span data-stu-id="5b687-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="5b687-118">Допустимые значения ( 2, 4, 6, ...) для корпоративных skus и (3, 9, 15, ...) для flash SKUs.</span><span class="sxs-lookup"><span data-stu-id="5b687-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="5b687-119">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="5b687-119">-ClientProtocol</span></span>
<span data-ttu-id="5b687-120">Указывает, могут ли клиенты redis подключаться с помощью протоколов, зашифрованных по протоколу TLS или plaintext redis.</span><span class="sxs-lookup"><span data-stu-id="5b687-120">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="5b687-121">Значение по умолчанию — шифрование TLS.</span><span class="sxs-lookup"><span data-stu-id="5b687-121">Default is TLS-encrypted.</span></span>

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

### <span data-ttu-id="5b687-122">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="5b687-122">-ClusteringPolicy</span></span>
<span data-ttu-id="5b687-123">Политика кластеров — по умолчанию osSCluster.</span><span class="sxs-lookup"><span data-stu-id="5b687-123">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="5b687-124">Задано на момент создания.</span><span class="sxs-lookup"><span data-stu-id="5b687-124">Specified at create time.</span></span>

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

### <span data-ttu-id="5b687-125">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5b687-125">-ClusterName</span></span>
<span data-ttu-id="5b687-126">Название кластера RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="5b687-126">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b687-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b687-127">-DefaultProfile</span></span>
<span data-ttu-id="5b687-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b687-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b687-129">-ВуассионПолиция</span><span class="sxs-lookup"><span data-stu-id="5b687-129">-EvictionPolicy</span></span>
<span data-ttu-id="5b687-130">Redis уличиваемая политика (по умолчанию — VolatileLRU).</span><span class="sxs-lookup"><span data-stu-id="5b687-130">Redis eviction policy - default is VolatileLRU.</span></span>

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

### <span data-ttu-id="5b687-131">-Location</span><span class="sxs-lookup"><span data-stu-id="5b687-131">-Location</span></span>
<span data-ttu-id="5b687-132">Географическое расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="5b687-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="5b687-133">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="5b687-133">-MinimumTlsVersion</span></span>
<span data-ttu-id="5b687-134">Минимальная версия TLS для кластера для поддержки, например 1.2</span><span class="sxs-lookup"><span data-stu-id="5b687-134">The minimum TLS version for the cluster to support, e.g. 1.2</span></span>

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

### <span data-ttu-id="5b687-135">-Module</span><span class="sxs-lookup"><span data-stu-id="5b687-135">-Module</span></span>
<span data-ttu-id="5b687-136">Необязательный набор модулей redis, которые нужно включить в эту базу данных, — модули можно добавлять только во время создания.</span><span class="sxs-lookup"><span data-stu-id="5b687-136">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="5b687-137">Чтобы создать новую таблицу, см. раздел "ЗАМЕТКИ" для свойств MODULE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="5b687-137">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="5b687-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5b687-138">-NoWait</span></span>
<span data-ttu-id="5b687-139">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="5b687-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5b687-140">-Port</span><span class="sxs-lookup"><span data-stu-id="5b687-140">-Port</span></span>
<span data-ttu-id="5b687-141">TCP-порт конечной точки базы данных.</span><span class="sxs-lookup"><span data-stu-id="5b687-141">TCP port of the database endpoint.</span></span>
<span data-ttu-id="5b687-142">Задано на момент создания.</span><span class="sxs-lookup"><span data-stu-id="5b687-142">Specified at create time.</span></span>
<span data-ttu-id="5b687-143">Значение по умолчанию для доступного порта.</span><span class="sxs-lookup"><span data-stu-id="5b687-143">Defaults to an available port.</span></span>

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

### <span data-ttu-id="5b687-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b687-144">-ResourceGroupName</span></span>
<span data-ttu-id="5b687-145">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b687-145">The name of the resource group.</span></span>

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

### <span data-ttu-id="5b687-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="5b687-146">-Sku</span></span>
<span data-ttu-id="5b687-147">Тип кластера RedisEnterprise для развертывания.</span><span class="sxs-lookup"><span data-stu-id="5b687-147">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="5b687-148">Возможные значения: (Enterprise_E10, EnterpriseFlash_F300 и т. д.)</span><span class="sxs-lookup"><span data-stu-id="5b687-148">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.SkuName
Parameter Sets: (All)
Aliases: SkuName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b687-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b687-149">-SubscriptionId</span></span>
<span data-ttu-id="5b687-150">Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5b687-150">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5b687-151">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="5b687-151">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5b687-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="5b687-152">-Tag</span></span>
<span data-ttu-id="5b687-153">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b687-153">Resource tags.</span></span>

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

### <span data-ttu-id="5b687-154">-Zone</span><span class="sxs-lookup"><span data-stu-id="5b687-154">-Zone</span></span>
<span data-ttu-id="5b687-155">Зоны, в которых будет развернут этот кластер.</span><span class="sxs-lookup"><span data-stu-id="5b687-155">The zones where this cluster will be deployed.</span></span>

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

### <span data-ttu-id="5b687-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b687-156">-Confirm</span></span>
<span data-ttu-id="5b687-157">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b687-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b687-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b687-158">-WhatIf</span></span>
<span data-ttu-id="5b687-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b687-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b687-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5b687-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b687-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b687-161">CommonParameters</span></span>
<span data-ttu-id="5b687-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b687-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b687-163">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b687-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b687-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b687-164">INPUTS</span></span>

## <span data-ttu-id="5b687-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5b687-165">OUTPUTS</span></span>

### <span data-ttu-id="5b687-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="5b687-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="5b687-167">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5b687-167">NOTES</span></span>

<span data-ttu-id="5b687-168">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5b687-168">ALIASES</span></span>

<span data-ttu-id="5b687-169">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="5b687-169">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5b687-170">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="5b687-170">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5b687-171">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5b687-171">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5b687-172">MODULE <IModule[]>: необязательный набор модулей redis, которые можно включить в этой базе данных. Модули можно добавлять только во время создания.</span><span class="sxs-lookup"><span data-stu-id="5b687-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="5b687-173">`Name <String>`: имя модуля, например "RedisBloom", 'RediSearch', 'RedisTimeSeries'</span><span class="sxs-lookup"><span data-stu-id="5b687-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="5b687-174">`[Arg <String>]`: Параметры конфигурации для модуля, например "ERROR_RATE 0,00 INITIAL_SIZE 400".</span><span class="sxs-lookup"><span data-stu-id="5b687-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="5b687-175">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b687-175">RELATED LINKS</span></span>

