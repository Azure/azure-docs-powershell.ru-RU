---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/export-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 3576cfb8185898ea7bb0fa2052a18b651d1d5cc0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000840"
---
# <span data-ttu-id="004ec-101">Export-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="004ec-101">Export-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="004ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="004ec-102">SYNOPSIS</span></span>
<span data-ttu-id="004ec-103">Экспорт файла базы данных из целевой базы данных.</span><span class="sxs-lookup"><span data-stu-id="004ec-103">Exports a database file from target database.</span></span>

## <span data-ttu-id="004ec-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="004ec-104">SYNTAX</span></span>

```
Export-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="004ec-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="004ec-105">DESCRIPTION</span></span>
<span data-ttu-id="004ec-106">Экспорт файла базы данных из целевой базы данных.</span><span class="sxs-lookup"><span data-stu-id="004ec-106">Exports a database file from target database.</span></span>

## <span data-ttu-id="004ec-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="004ec-107">EXAMPLES</span></span>

### <span data-ttu-id="004ec-108">Пример 1. Экспорт базы данных</span><span class="sxs-lookup"><span data-stu-id="004ec-108">Example 1: Export database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Export-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="004ec-109">Эта команда экспортирует базу данных кэша Redis Enterprise под названием MyCache в файл базы данных.</span><span class="sxs-lookup"><span data-stu-id="004ec-109">This command exports the database of the Redis Enterprise Cache named MyCache to a database file.</span></span>

## <span data-ttu-id="004ec-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="004ec-110">PARAMETERS</span></span>

### <span data-ttu-id="004ec-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="004ec-111">-AsJob</span></span>
<span data-ttu-id="004ec-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="004ec-112">Run the command as a job</span></span>

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

### <span data-ttu-id="004ec-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="004ec-113">-ClusterName</span></span>
<span data-ttu-id="004ec-114">Название кластера RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="004ec-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="004ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="004ec-115">-DefaultProfile</span></span>
<span data-ttu-id="004ec-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="004ec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="004ec-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="004ec-117">-NoWait</span></span>
<span data-ttu-id="004ec-118">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="004ec-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="004ec-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="004ec-119">-PassThru</span></span>
<span data-ttu-id="004ec-120">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="004ec-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="004ec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="004ec-121">-ResourceGroupName</span></span>
<span data-ttu-id="004ec-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="004ec-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="004ec-123">-SasUri</span><span class="sxs-lookup"><span data-stu-id="004ec-123">-SasUri</span></span>
<span data-ttu-id="004ec-124">Uri SAS для целевого каталога, в который нужно экспортировать</span><span class="sxs-lookup"><span data-stu-id="004ec-124">SAS Uri for the target directory to export to</span></span>

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

### <span data-ttu-id="004ec-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="004ec-125">-SubscriptionId</span></span>
<span data-ttu-id="004ec-126">Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="004ec-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="004ec-127">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="004ec-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="004ec-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="004ec-128">-Confirm</span></span>
<span data-ttu-id="004ec-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="004ec-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="004ec-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="004ec-130">-WhatIf</span></span>
<span data-ttu-id="004ec-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="004ec-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="004ec-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="004ec-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="004ec-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="004ec-133">CommonParameters</span></span>
<span data-ttu-id="004ec-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="004ec-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="004ec-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="004ec-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="004ec-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="004ec-136">INPUTS</span></span>

## <span data-ttu-id="004ec-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="004ec-137">OUTPUTS</span></span>

### <span data-ttu-id="004ec-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="004ec-138">System.Boolean</span></span>

## <span data-ttu-id="004ec-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="004ec-139">NOTES</span></span>

<span data-ttu-id="004ec-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="004ec-140">ALIASES</span></span>

## <span data-ttu-id="004ec-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="004ec-141">RELATED LINKS</span></span>

