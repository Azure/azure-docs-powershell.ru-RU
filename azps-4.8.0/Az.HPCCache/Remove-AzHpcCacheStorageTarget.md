---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: a3603a1884318f567908937ab880182e0df5ee57
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243383"
---
# <span data-ttu-id="f51ff-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="f51ff-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="f51ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f51ff-102">SYNOPSIS</span></span>
<span data-ttu-id="f51ff-103">Удаляет целевое хранилище.</span><span class="sxs-lookup"><span data-stu-id="f51ff-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="f51ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f51ff-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f51ff-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f51ff-105">DESCRIPTION</span></span>
<span data-ttu-id="f51ff-106">Командлет **Remove-AzHpcCacheStorageTarget** Удаляет целевое хранилище из кэша Azure HPC Cache.</span><span class="sxs-lookup"><span data-stu-id="f51ff-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="f51ff-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f51ff-107">EXAMPLES</span></span>

### <span data-ttu-id="f51ff-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f51ff-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="f51ff-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f51ff-109">PARAMETERS</span></span>

### <span data-ttu-id="f51ff-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f51ff-110">-AsJob</span></span>
<span data-ttu-id="f51ff-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f51ff-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f51ff-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="f51ff-112">-CacheName</span></span>
<span data-ttu-id="f51ff-113">Имя кэша.</span><span class="sxs-lookup"><span data-stu-id="f51ff-113">Name of cache.</span></span>

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

### <span data-ttu-id="f51ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f51ff-114">-DefaultProfile</span></span>
<span data-ttu-id="f51ff-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f51ff-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f51ff-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f51ff-116">-Force</span></span>
<span data-ttu-id="f51ff-117">Указывает на то, что командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f51ff-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="f51ff-118">По умолчанию этот командлет предлагает подтвердить необходимость удаления целевого объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="f51ff-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="f51ff-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f51ff-119">-Name</span></span>
<span data-ttu-id="f51ff-120">Имя целевого объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="f51ff-120">Name of storage target.</span></span>

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

### <span data-ttu-id="f51ff-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f51ff-121">-PassThru</span></span>
<span data-ttu-id="f51ff-122">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f51ff-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f51ff-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f51ff-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f51ff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f51ff-124">-ResourceGroupName</span></span>
<span data-ttu-id="f51ff-125">Имя группы ресурсов, в которой вы хотите удалить цель хранилища из кэша.</span><span class="sxs-lookup"><span data-stu-id="f51ff-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="f51ff-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f51ff-126">-Confirm</span></span>
<span data-ttu-id="f51ff-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f51ff-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f51ff-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f51ff-128">-WhatIf</span></span>
<span data-ttu-id="f51ff-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f51ff-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f51ff-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f51ff-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f51ff-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f51ff-131">CommonParameters</span></span>
<span data-ttu-id="f51ff-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f51ff-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f51ff-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f51ff-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f51ff-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f51ff-134">INPUTS</span></span>

### <span data-ttu-id="f51ff-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f51ff-135">System.String</span></span>

## <span data-ttu-id="f51ff-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f51ff-136">OUTPUTS</span></span>

## <span data-ttu-id="f51ff-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="f51ff-137">NOTES</span></span>

## <span data-ttu-id="f51ff-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f51ff-138">RELATED LINKS</span></span>
