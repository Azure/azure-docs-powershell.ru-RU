---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/export-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 1e50bba7c00c94daac983511f6fcea0ed1319759
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217852"
---
# <span data-ttu-id="81106-101">Export-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="81106-101">Export-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="81106-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81106-102">SYNOPSIS</span></span>
<span data-ttu-id="81106-103">Экспорт файла базы данных из целевой базы данных.</span><span class="sxs-lookup"><span data-stu-id="81106-103">Exports a database file from target database.</span></span>

## <span data-ttu-id="81106-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="81106-104">SYNTAX</span></span>

```
Export-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="81106-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81106-105">DESCRIPTION</span></span>
<span data-ttu-id="81106-106">Экспорт файла базы данных из целевой базы данных.</span><span class="sxs-lookup"><span data-stu-id="81106-106">Exports a database file from target database.</span></span>

## <span data-ttu-id="81106-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="81106-107">EXAMPLES</span></span>

### <span data-ttu-id="81106-108">Пример 1. Экспорт базы данных</span><span class="sxs-lookup"><span data-stu-id="81106-108">Example 1: Export database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Export-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="81106-109">Эта команда экспортирует базу данных кэша Redis Enterprise под названием MyCache в файл базы данных.</span><span class="sxs-lookup"><span data-stu-id="81106-109">This command exports the database of the Redis Enterprise Cache named MyCache to a database file.</span></span>

## <span data-ttu-id="81106-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81106-110">PARAMETERS</span></span>

### <span data-ttu-id="81106-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81106-111">-AsJob</span></span>
<span data-ttu-id="81106-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="81106-112">Run the command as a job</span></span>

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

### <span data-ttu-id="81106-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="81106-113">-ClusterName</span></span>
<span data-ttu-id="81106-114">Название кластера RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="81106-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="81106-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81106-115">-DefaultProfile</span></span>
<span data-ttu-id="81106-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81106-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81106-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="81106-117">-NoWait</span></span>
<span data-ttu-id="81106-118">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="81106-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="81106-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81106-119">-PassThru</span></span>
<span data-ttu-id="81106-120">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="81106-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="81106-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81106-121">-ResourceGroupName</span></span>
<span data-ttu-id="81106-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="81106-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="81106-123">-SasUri</span><span class="sxs-lookup"><span data-stu-id="81106-123">-SasUri</span></span>
<span data-ttu-id="81106-124">Uri SAS для целевого каталога, в который нужно экспортировать</span><span class="sxs-lookup"><span data-stu-id="81106-124">SAS Uri for the target directory to export to</span></span>

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

### <span data-ttu-id="81106-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81106-125">-SubscriptionId</span></span>
<span data-ttu-id="81106-126">Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="81106-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="81106-127">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="81106-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="81106-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81106-128">-Confirm</span></span>
<span data-ttu-id="81106-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="81106-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81106-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81106-130">-WhatIf</span></span>
<span data-ttu-id="81106-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81106-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81106-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="81106-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81106-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81106-133">CommonParameters</span></span>
<span data-ttu-id="81106-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81106-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81106-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81106-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81106-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81106-136">INPUTS</span></span>

## <span data-ttu-id="81106-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="81106-137">OUTPUTS</span></span>

### <span data-ttu-id="81106-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="81106-138">System.Boolean</span></span>

## <span data-ttu-id="81106-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="81106-139">NOTES</span></span>

<span data-ttu-id="81106-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="81106-140">ALIASES</span></span>

## <span data-ttu-id="81106-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81106-141">RELATED LINKS</span></span>

