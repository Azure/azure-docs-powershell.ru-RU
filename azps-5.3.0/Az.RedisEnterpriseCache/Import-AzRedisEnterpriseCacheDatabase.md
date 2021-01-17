---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/import-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 6ab4babd894a3c639db6e41e6088653604072c7e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421196"
---
# <span data-ttu-id="7287b-101">Import-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="7287b-101">Import-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="7287b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7287b-102">SYNOPSIS</span></span>
<span data-ttu-id="7287b-103">Импорт файла базы данных в целевую базу данных.</span><span class="sxs-lookup"><span data-stu-id="7287b-103">Imports a database file to target database.</span></span>

## <span data-ttu-id="7287b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7287b-104">SYNTAX</span></span>

```
Import-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7287b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7287b-105">DESCRIPTION</span></span>
<span data-ttu-id="7287b-106">Импорт файла базы данных в целевую базу данных.</span><span class="sxs-lookup"><span data-stu-id="7287b-106">Imports a database file to target database.</span></span>

## <span data-ttu-id="7287b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7287b-107">EXAMPLES</span></span>

### <span data-ttu-id="7287b-108">Пример 1. Импорт базы данных</span><span class="sxs-lookup"><span data-stu-id="7287b-108">Example 1: Import database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/myfilename?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="7287b-109">Эта команда импортирует файл базы данных в базу данных кэша Redis Enterprise под названием MyCache.</span><span class="sxs-lookup"><span data-stu-id="7287b-109">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="7287b-110">Пример 2. Импорт базы данных (с использованием имени файла примера)</span><span class="sxs-lookup"><span data-stu-id="7287b-110">Example 2: Import database (using example filename)</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/bk20201130-223654-1-db-1_of_1-2-0-16383.rdb.gz?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="7287b-111">Эта команда импортирует файл базы данных в базу данных кэша Redis Enterprise под названием MyCache.</span><span class="sxs-lookup"><span data-stu-id="7287b-111">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="7287b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7287b-112">PARAMETERS</span></span>

### <span data-ttu-id="7287b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7287b-113">-AsJob</span></span>
<span data-ttu-id="7287b-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="7287b-114">Run the command as a job</span></span>

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

### <span data-ttu-id="7287b-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7287b-115">-ClusterName</span></span>
<span data-ttu-id="7287b-116">Название кластера RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="7287b-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="7287b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7287b-117">-DefaultProfile</span></span>
<span data-ttu-id="7287b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7287b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7287b-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7287b-119">-NoWait</span></span>
<span data-ttu-id="7287b-120">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="7287b-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7287b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7287b-121">-PassThru</span></span>
<span data-ttu-id="7287b-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="7287b-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7287b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7287b-123">-ResourceGroupName</span></span>
<span data-ttu-id="7287b-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7287b-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="7287b-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="7287b-125">-SasUri</span></span>
<span data-ttu-id="7287b-126">Uri SAS для целевого BLOB-объектов, из</span><span class="sxs-lookup"><span data-stu-id="7287b-126">SAS Uri for the target blob to import from</span></span>

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

### <span data-ttu-id="7287b-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7287b-127">-SubscriptionId</span></span>
<span data-ttu-id="7287b-128">Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7287b-128">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7287b-129">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="7287b-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7287b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7287b-130">-Confirm</span></span>
<span data-ttu-id="7287b-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7287b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7287b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7287b-132">-WhatIf</span></span>
<span data-ttu-id="7287b-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7287b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7287b-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7287b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7287b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7287b-135">CommonParameters</span></span>
<span data-ttu-id="7287b-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7287b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7287b-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7287b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7287b-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7287b-138">INPUTS</span></span>

## <span data-ttu-id="7287b-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7287b-139">OUTPUTS</span></span>

### <span data-ttu-id="7287b-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7287b-140">System.Boolean</span></span>

## <span data-ttu-id="7287b-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7287b-141">NOTES</span></span>

<span data-ttu-id="7287b-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7287b-142">ALIASES</span></span>

## <span data-ttu-id="7287b-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7287b-143">RELATED LINKS</span></span>

