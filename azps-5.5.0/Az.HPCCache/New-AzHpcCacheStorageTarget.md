---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: eee07c01b0c9e0e2b072787d0d37a6a868fbf150
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243445"
---
# <span data-ttu-id="ab05d-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="ab05d-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="ab05d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab05d-102">SYNOPSIS</span></span>
<span data-ttu-id="ab05d-103">Создает целевое хранилище.</span><span class="sxs-lookup"><span data-stu-id="ab05d-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="ab05d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ab05d-104">SYNTAX</span></span>

### <span data-ttu-id="ab05d-105">ClfsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ab05d-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab05d-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab05d-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab05d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab05d-107">DESCRIPTION</span></span>
<span data-ttu-id="ab05d-108">Этот **cmdlet добавляет** целевой объект хранилища в кэш HPC Azure.</span><span class="sxs-lookup"><span data-stu-id="ab05d-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="ab05d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ab05d-109">EXAMPLES</span></span>

### <span data-ttu-id="ab05d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ab05d-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="ab05d-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ab05d-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="ab05d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab05d-112">PARAMETERS</span></span>

### <span data-ttu-id="ab05d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab05d-113">-AsJob</span></span>
<span data-ttu-id="ab05d-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ab05d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab05d-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="ab05d-115">-CacheName</span></span>
<span data-ttu-id="ab05d-116">Имя кэша.</span><span class="sxs-lookup"><span data-stu-id="ab05d-116">Name of cache.</span></span>

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

### <span data-ttu-id="ab05d-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="ab05d-117">-CLFS</span></span>
<span data-ttu-id="ab05d-118">Обновление целевого типа хранилища CLFS.</span><span class="sxs-lookup"><span data-stu-id="ab05d-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="ab05d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab05d-119">-DefaultProfile</span></span>
<span data-ttu-id="ab05d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab05d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab05d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ab05d-121">-Force</span></span>
<span data-ttu-id="ab05d-122">Указывает на то, что при этом не будет предложено подтвердить запрос.</span><span class="sxs-lookup"><span data-stu-id="ab05d-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="ab05d-123">По умолчанию этот cmdlet запросит подтверждение очистки кэша.</span><span class="sxs-lookup"><span data-stu-id="ab05d-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="ab05d-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="ab05d-124">-HostName</span></span>
<span data-ttu-id="ab05d-125">Имя хоста NFS.</span><span class="sxs-lookup"><span data-stu-id="ab05d-125">NFS host name.</span></span>

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

### <span data-ttu-id="ab05d-126">-Junction</span><span class="sxs-lookup"><span data-stu-id="ab05d-126">-Junction</span></span>
<span data-ttu-id="ab05d-127">"Соединения".</span><span class="sxs-lookup"><span data-stu-id="ab05d-127">Junction.</span></span>

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

### <span data-ttu-id="ab05d-128">-Name</span><span class="sxs-lookup"><span data-stu-id="ab05d-128">-Name</span></span>
<span data-ttu-id="ab05d-129">Имя целевого хранилища.</span><span class="sxs-lookup"><span data-stu-id="ab05d-129">Name of storage target.</span></span>

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

### <span data-ttu-id="ab05d-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="ab05d-130">-NFS</span></span>
<span data-ttu-id="ab05d-131">Обновление целевого типа хранилища NFS.</span><span class="sxs-lookup"><span data-stu-id="ab05d-131">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="ab05d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab05d-132">-ResourceGroupName</span></span>
<span data-ttu-id="ab05d-133">"Имя группы ресурсов, для которой вы хотите создать целевую хранилищу для заданного кэша.</span><span class="sxs-lookup"><span data-stu-id="ab05d-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

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

### <span data-ttu-id="ab05d-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="ab05d-134">-StorageContainerID</span></span>
<span data-ttu-id="ab05d-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="ab05d-135">StorageContainerID</span></span>

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

### <span data-ttu-id="ab05d-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="ab05d-136">-UsageModel</span></span>
<span data-ttu-id="ab05d-137">Модель использования NFS.</span><span class="sxs-lookup"><span data-stu-id="ab05d-137">NFS usage model.</span></span>

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

### <span data-ttu-id="ab05d-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab05d-138">-Confirm</span></span>
<span data-ttu-id="ab05d-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab05d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab05d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab05d-140">-WhatIf</span></span>
<span data-ttu-id="ab05d-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab05d-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab05d-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ab05d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab05d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab05d-143">CommonParameters</span></span>
<span data-ttu-id="ab05d-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab05d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab05d-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab05d-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab05d-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab05d-146">INPUTS</span></span>

### <span data-ttu-id="ab05d-147">System.String</span><span class="sxs-lookup"><span data-stu-id="ab05d-147">System.String</span></span>

## <span data-ttu-id="ab05d-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ab05d-148">OUTPUTS</span></span>

### <span data-ttu-id="ab05d-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="ab05d-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="ab05d-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ab05d-150">NOTES</span></span>

## <span data-ttu-id="ab05d-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab05d-151">RELATED LINKS</span></span>
