---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
ms.openlocfilehash: fa799a05b76f9f6941b19bf171beb77318b77d39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077733"
---
# <span data-ttu-id="8117d-101">Set-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="8117d-101">Set-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="8117d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8117d-102">SYNOPSIS</span></span>
<span data-ttu-id="8117d-103">Обновляет целевое хранилище.</span><span class="sxs-lookup"><span data-stu-id="8117d-103">Updates a Storage Target.</span></span>

## <span data-ttu-id="8117d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8117d-104">SYNTAX</span></span>

### <span data-ttu-id="8117d-105">ClfsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8117d-105">ClfsParameterSet (Default)</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8117d-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="8117d-106">NfsParameterSet</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8117d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8117d-107">DESCRIPTION</span></span>
<span data-ttu-id="8117d-108">Командлет **Set-AzHpcCacheStorageTarget** обновляет целевую папку хранилища, присоединенную к КЭШУ Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="8117d-108">The **Set-AzHpcCacheStorageTarget** cmdlet updates a Storage Target attached to Azure HPC cache.</span></span>

## <span data-ttu-id="8117d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8117d-109">EXAMPLES</span></span>

### <span data-ttu-id="8117d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8117d-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="8117d-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8117d-111">Example 2</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/export"})
```

## <span data-ttu-id="8117d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8117d-112">PARAMETERS</span></span>

### <span data-ttu-id="8117d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8117d-113">-AsJob</span></span>
<span data-ttu-id="8117d-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8117d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8117d-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="8117d-115">-CacheName</span></span>
<span data-ttu-id="8117d-116">Имя кэша.</span><span class="sxs-lookup"><span data-stu-id="8117d-116">Name of cache.</span></span>

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

### <span data-ttu-id="8117d-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="8117d-117">-CLFS</span></span>
<span data-ttu-id="8117d-118">Обновите тип целевого хранилища CLFS.</span><span class="sxs-lookup"><span data-stu-id="8117d-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="8117d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8117d-119">-DefaultProfile</span></span>
<span data-ttu-id="8117d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8117d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8117d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8117d-121">-Force</span></span>
<span data-ttu-id="8117d-122">Указывает на то, что командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="8117d-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="8117d-123">По умолчанию этот командлет предлагает подтвердить сброс кэша.</span><span class="sxs-lookup"><span data-stu-id="8117d-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="8117d-124">-Примыкание</span><span class="sxs-lookup"><span data-stu-id="8117d-124">-Junction</span></span>
<span data-ttu-id="8117d-125">Точки.</span><span class="sxs-lookup"><span data-stu-id="8117d-125">Junction.</span></span>

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

### <span data-ttu-id="8117d-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8117d-126">-Name</span></span>
<span data-ttu-id="8117d-127">Имя целевого объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="8117d-127">Name of storage target.</span></span>

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

### <span data-ttu-id="8117d-128">-NFS</span><span class="sxs-lookup"><span data-stu-id="8117d-128">-NFS</span></span>
<span data-ttu-id="8117d-129">Обновите тип целевого хранилища NFS.</span><span class="sxs-lookup"><span data-stu-id="8117d-129">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="8117d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8117d-130">-ResourceGroupName</span></span>
<span data-ttu-id="8117d-131">Имя группы ресурсов, в которой вы хотите обновить целевое хранилище.</span><span class="sxs-lookup"><span data-stu-id="8117d-131">Name of resource group under which you want to update storage target.</span></span>

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

### <span data-ttu-id="8117d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8117d-132">-Confirm</span></span>
<span data-ttu-id="8117d-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8117d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8117d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8117d-134">-WhatIf</span></span>
<span data-ttu-id="8117d-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8117d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8117d-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8117d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8117d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8117d-137">CommonParameters</span></span>
<span data-ttu-id="8117d-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8117d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8117d-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8117d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8117d-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8117d-140">INPUTS</span></span>

### <span data-ttu-id="8117d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8117d-141">System.String</span></span>

## <span data-ttu-id="8117d-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8117d-142">OUTPUTS</span></span>

### <span data-ttu-id="8117d-143">Microsoft. Azure. PowerShell. командлеты. HPCCache. Models. PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="8117d-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="8117d-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="8117d-144">NOTES</span></span>

## <span data-ttu-id="8117d-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8117d-145">RELATED LINKS</span></span>
