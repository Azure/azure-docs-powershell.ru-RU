---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: eee07c01b0c9e0e2b072787d0d37a6a868fbf150
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247810"
---
# <span data-ttu-id="4c421-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="4c421-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="4c421-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c421-102">SYNOPSIS</span></span>
<span data-ttu-id="4c421-103">Создание целевого объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="4c421-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="4c421-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c421-104">SYNTAX</span></span>

### <span data-ttu-id="4c421-105">ClfsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4c421-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c421-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c421-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c421-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c421-107">DESCRIPTION</span></span>
<span data-ttu-id="4c421-108">Командлет **New-AzHpcCacheStorageTarget** добавляет целевое хранилище в кэш Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="4c421-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="4c421-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c421-109">EXAMPLES</span></span>

### <span data-ttu-id="4c421-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4c421-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="4c421-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4c421-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="4c421-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c421-112">PARAMETERS</span></span>

### <span data-ttu-id="4c421-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c421-113">-AsJob</span></span>
<span data-ttu-id="4c421-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4c421-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c421-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="4c421-115">-CacheName</span></span>
<span data-ttu-id="4c421-116">Имя кэша.</span><span class="sxs-lookup"><span data-stu-id="4c421-116">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c421-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="4c421-117">-CLFS</span></span>
<span data-ttu-id="4c421-118">Обновите тип целевого хранилища CLFS.</span><span class="sxs-lookup"><span data-stu-id="4c421-118">Update CLFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c421-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c421-119">-DefaultProfile</span></span>
<span data-ttu-id="4c421-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c421-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c421-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4c421-121">-Force</span></span>
<span data-ttu-id="4c421-122">Указывает на то, что командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4c421-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="4c421-123">По умолчанию этот командлет предлагает подтвердить сброс кэша.</span><span class="sxs-lookup"><span data-stu-id="4c421-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="4c421-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="4c421-124">-HostName</span></span>
<span data-ttu-id="4c421-125">Имя узла NFS.</span><span class="sxs-lookup"><span data-stu-id="4c421-125">NFS host name.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c421-126">-Примыкание</span><span class="sxs-lookup"><span data-stu-id="4c421-126">-Junction</span></span>
<span data-ttu-id="4c421-127">Точки.</span><span class="sxs-lookup"><span data-stu-id="4c421-127">Junction.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c421-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4c421-128">-Name</span></span>
<span data-ttu-id="4c421-129">Имя целевого объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="4c421-129">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageTargetName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c421-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="4c421-130">-NFS</span></span>
<span data-ttu-id="4c421-131">Обновите тип целевого хранилища NFS.</span><span class="sxs-lookup"><span data-stu-id="4c421-131">Update NFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c421-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c421-132">-ResourceGroupName</span></span>
<span data-ttu-id="4c421-133">"Имя группы ресурсов, в которой вы хотите создать цель хранилища для данного кэша.</span><span class="sxs-lookup"><span data-stu-id="4c421-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c421-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="4c421-134">-StorageContainerID</span></span>
<span data-ttu-id="4c421-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="4c421-135">StorageContainerID</span></span>

```yaml
Type: System.String
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c421-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="4c421-136">-UsageModel</span></span>
<span data-ttu-id="4c421-137">Модель использования NFS.</span><span class="sxs-lookup"><span data-stu-id="4c421-137">NFS usage model.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c421-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c421-138">-Confirm</span></span>
<span data-ttu-id="4c421-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4c421-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c421-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c421-140">-WhatIf</span></span>
<span data-ttu-id="4c421-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4c421-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c421-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4c421-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c421-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c421-143">CommonParameters</span></span>
<span data-ttu-id="4c421-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c421-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c421-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c421-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c421-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c421-146">INPUTS</span></span>

### <span data-ttu-id="4c421-147">System. String</span><span class="sxs-lookup"><span data-stu-id="4c421-147">System.String</span></span>

## <span data-ttu-id="4c421-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c421-148">OUTPUTS</span></span>

### <span data-ttu-id="4c421-149">Microsoft. Azure. PowerShell. командлеты. HPCCache. Models. PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="4c421-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="4c421-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c421-150">NOTES</span></span>

## <span data-ttu-id="4c421-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c421-151">RELATED LINKS</span></span>
