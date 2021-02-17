---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
ms.openlocfilehash: fa799a05b76f9f6941b19bf171beb77318b77d39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230340"
---
# <span data-ttu-id="9c654-101">Set-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="9c654-101">Set-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="9c654-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c654-102">SYNOPSIS</span></span>
<span data-ttu-id="9c654-103">Обновляет целевую хранилищу.</span><span class="sxs-lookup"><span data-stu-id="9c654-103">Updates a Storage Target.</span></span>

## <span data-ttu-id="9c654-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9c654-104">SYNTAX</span></span>

### <span data-ttu-id="9c654-105">ClfsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c654-105">ClfsParameterSet (Default)</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c654-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c654-106">NfsParameterSet</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c654-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c654-107">DESCRIPTION</span></span>
<span data-ttu-id="9c654-108">**Cmdlet Set-AzHpcCacheStorageTarget** обновляет целевой объект хранилища, подключенный к кэше HPC Azure.</span><span class="sxs-lookup"><span data-stu-id="9c654-108">The **Set-AzHpcCacheStorageTarget** cmdlet updates a Storage Target attached to Azure HPC cache.</span></span>

## <span data-ttu-id="9c654-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9c654-109">EXAMPLES</span></span>

### <span data-ttu-id="9c654-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9c654-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="9c654-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9c654-111">Example 2</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/export"})
```

## <span data-ttu-id="9c654-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c654-112">PARAMETERS</span></span>

### <span data-ttu-id="9c654-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c654-113">-AsJob</span></span>
<span data-ttu-id="9c654-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9c654-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c654-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="9c654-115">-CacheName</span></span>
<span data-ttu-id="9c654-116">Имя кэша.</span><span class="sxs-lookup"><span data-stu-id="9c654-116">Name of cache.</span></span>

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

### <span data-ttu-id="9c654-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="9c654-117">-CLFS</span></span>
<span data-ttu-id="9c654-118">Обновление целевого типа хранилища CLFS.</span><span class="sxs-lookup"><span data-stu-id="9c654-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="9c654-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c654-119">-DefaultProfile</span></span>
<span data-ttu-id="9c654-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c654-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c654-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9c654-121">-Force</span></span>
<span data-ttu-id="9c654-122">Указывает на то, что при этом не будет предложено подтвердить запрос.</span><span class="sxs-lookup"><span data-stu-id="9c654-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="9c654-123">По умолчанию этот cmdlet запросит подтверждение очистки кэша.</span><span class="sxs-lookup"><span data-stu-id="9c654-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="9c654-124">-Junction</span><span class="sxs-lookup"><span data-stu-id="9c654-124">-Junction</span></span>
<span data-ttu-id="9c654-125">"Соединения".</span><span class="sxs-lookup"><span data-stu-id="9c654-125">Junction.</span></span>

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

### <span data-ttu-id="9c654-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9c654-126">-Name</span></span>
<span data-ttu-id="9c654-127">Имя целевого хранилища.</span><span class="sxs-lookup"><span data-stu-id="9c654-127">Name of storage target.</span></span>

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

### <span data-ttu-id="9c654-128">-NFS</span><span class="sxs-lookup"><span data-stu-id="9c654-128">-NFS</span></span>
<span data-ttu-id="9c654-129">Обновление целевого типа хранилища NFS.</span><span class="sxs-lookup"><span data-stu-id="9c654-129">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="9c654-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c654-130">-ResourceGroupName</span></span>
<span data-ttu-id="9c654-131">Имя группы ресурсов, для которой вы хотите обновить целевое хранилище.</span><span class="sxs-lookup"><span data-stu-id="9c654-131">Name of resource group under which you want to update storage target.</span></span>

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

### <span data-ttu-id="9c654-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c654-132">-Confirm</span></span>
<span data-ttu-id="9c654-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c654-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c654-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c654-134">-WhatIf</span></span>
<span data-ttu-id="9c654-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c654-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c654-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9c654-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c654-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c654-137">CommonParameters</span></span>
<span data-ttu-id="9c654-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c654-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c654-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c654-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c654-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c654-140">INPUTS</span></span>

### <span data-ttu-id="9c654-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9c654-141">System.String</span></span>

## <span data-ttu-id="9c654-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9c654-142">OUTPUTS</span></span>

### <span data-ttu-id="9c654-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="9c654-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="9c654-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9c654-144">NOTES</span></span>

## <span data-ttu-id="9c654-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c654-145">RELATED LINKS</span></span>
