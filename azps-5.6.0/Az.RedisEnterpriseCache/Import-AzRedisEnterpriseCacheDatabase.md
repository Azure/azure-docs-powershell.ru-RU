---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/import-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: b7258c552d14a9c7cdeafae5c23908321b0705c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000776"
---
# <span data-ttu-id="4a6ba-101">Import-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="4a6ba-101">Import-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="4a6ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a6ba-102">SYNOPSIS</span></span>
<span data-ttu-id="4a6ba-103">Импорт файла базы данных в целевую базу данных.</span><span class="sxs-lookup"><span data-stu-id="4a6ba-103">Imports a database file to target database.</span></span>

## <span data-ttu-id="4a6ba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4a6ba-104">SYNTAX</span></span>

```
Import-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4a6ba-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a6ba-105">DESCRIPTION</span></span>
<span data-ttu-id="4a6ba-106">Импорт файла базы данных в целевую базу данных.</span><span class="sxs-lookup"><span data-stu-id="4a6ba-106">Imports a database file to target database.</span></span>

## <span data-ttu-id="4a6ba-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4a6ba-107">EXAMPLES</span></span>

### <span data-ttu-id="4a6ba-108">Пример 1. Импорт базы данных</span><span class="sxs-lookup"><span data-stu-id="4a6ba-108">Example 1: Import database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/myfilename?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="4a6ba-109">Эта команда импортирует файл базы данных в базу данных кэша Redis Enterprise под названием MyCache.</span><span class="sxs-lookup"><span data-stu-id="4a6ba-109">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="4a6ba-110">Пример 2. Импорт базы данных (с использованием имени файла примера)</span><span class="sxs-lookup"><span data-stu-id="4a6ba-110">Example 2: Import database (using example filename)</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/bk20201130-223654-1-db-1_of_1-2-0-16383.rdb.gz?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="4a6ba-111">Эта команда импортирует файл базы данных в базу данных кэша Redis Enterprise под названием MyCache.</span><span class="sxs-lookup"><span data-stu-id="4a6ba-111">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="4a6ba-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a6ba-112">PARAMETERS</span></span>

### <span data-ttu-id="4a6ba-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a6ba-113">-AsJob</span></span>
<span data-ttu-id="4a6ba-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="4a6ba-114">Run the command as a job</span></span>

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

### <span data-ttu-id="4a6ba-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4a6ba-115">-ClusterName</span></span>
<span data-ttu-id="4a6ba-116">Название кластера RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="4a6ba-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="4a6ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a6ba-117">-DefaultProfile</span></span>
<span data-ttu-id="4a6ba-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a6ba-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a6ba-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4a6ba-119">-NoWait</span></span>
<span data-ttu-id="4a6ba-120">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="4a6ba-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4a6ba-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a6ba-121">-PassThru</span></span>
<span data-ttu-id="4a6ba-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="4a6ba-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4a6ba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a6ba-123">-ResourceGroupName</span></span>
<span data-ttu-id="4a6ba-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a6ba-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="4a6ba-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="4a6ba-125">-SasUri</span></span>
<span data-ttu-id="4a6ba-126">Uri SAS для целевого BLOB-объектов, из</span><span class="sxs-lookup"><span data-stu-id="4a6ba-126">SAS Uri for the target blob to import from</span></span>

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

### <span data-ttu-id="4a6ba-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a6ba-127">-SubscriptionId</span></span>
<span data-ttu-id="4a6ba-128">Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4a6ba-128">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4a6ba-129">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="4a6ba-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4a6ba-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a6ba-130">-Confirm</span></span>
<span data-ttu-id="4a6ba-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a6ba-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a6ba-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a6ba-132">-WhatIf</span></span>
<span data-ttu-id="4a6ba-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a6ba-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a6ba-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4a6ba-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a6ba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a6ba-135">CommonParameters</span></span>
<span data-ttu-id="4a6ba-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a6ba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a6ba-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a6ba-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a6ba-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a6ba-138">INPUTS</span></span>

## <span data-ttu-id="4a6ba-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4a6ba-139">OUTPUTS</span></span>

### <span data-ttu-id="4a6ba-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4a6ba-140">System.Boolean</span></span>

## <span data-ttu-id="4a6ba-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4a6ba-141">NOTES</span></span>

<span data-ttu-id="4a6ba-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4a6ba-142">ALIASES</span></span>

## <span data-ttu-id="4a6ba-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a6ba-143">RELATED LINKS</span></span>

