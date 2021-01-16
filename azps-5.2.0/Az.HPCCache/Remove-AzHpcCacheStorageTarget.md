---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: a3603a1884318f567908937ab880182e0df5ee57
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412527"
---
# <span data-ttu-id="67d3b-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="67d3b-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="67d3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="67d3b-103">Удаляет целевое хранилище.</span><span class="sxs-lookup"><span data-stu-id="67d3b-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="67d3b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="67d3b-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67d3b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67d3b-105">DESCRIPTION</span></span>
<span data-ttu-id="67d3b-106">При этом из кэша HPC Azure удаляется целевой объект хранилища **AzHpcCacheStorageTarget.**</span><span class="sxs-lookup"><span data-stu-id="67d3b-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="67d3b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="67d3b-107">EXAMPLES</span></span>

### <span data-ttu-id="67d3b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="67d3b-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="67d3b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67d3b-109">PARAMETERS</span></span>

### <span data-ttu-id="67d3b-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67d3b-110">-AsJob</span></span>
<span data-ttu-id="67d3b-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="67d3b-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67d3b-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="67d3b-112">-CacheName</span></span>
<span data-ttu-id="67d3b-113">Имя кэша.</span><span class="sxs-lookup"><span data-stu-id="67d3b-113">Name of cache.</span></span>

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

### <span data-ttu-id="67d3b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d3b-114">-DefaultProfile</span></span>
<span data-ttu-id="67d3b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67d3b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67d3b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="67d3b-116">-Force</span></span>
<span data-ttu-id="67d3b-117">Указывает на то, что при этом не будет предложено подтвердить запрос.</span><span class="sxs-lookup"><span data-stu-id="67d3b-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="67d3b-118">По умолчанию при этом вам будет предложено подтвердить удаление целевого хранилища.</span><span class="sxs-lookup"><span data-stu-id="67d3b-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="67d3b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="67d3b-119">-Name</span></span>
<span data-ttu-id="67d3b-120">Имя целевого хранилища.</span><span class="sxs-lookup"><span data-stu-id="67d3b-120">Name of storage target.</span></span>

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

### <span data-ttu-id="67d3b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67d3b-121">-PassThru</span></span>
<span data-ttu-id="67d3b-122">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="67d3b-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="67d3b-123">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="67d3b-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="67d3b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67d3b-124">-ResourceGroupName</span></span>
<span data-ttu-id="67d3b-125">Имя группы ресурсов, для которой вы хотите удалить целевой объект хранилища из кэша.</span><span class="sxs-lookup"><span data-stu-id="67d3b-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="67d3b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67d3b-126">-Confirm</span></span>
<span data-ttu-id="67d3b-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67d3b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67d3b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67d3b-128">-WhatIf</span></span>
<span data-ttu-id="67d3b-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67d3b-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67d3b-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="67d3b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67d3b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d3b-131">CommonParameters</span></span>
<span data-ttu-id="67d3b-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67d3b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d3b-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67d3b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d3b-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67d3b-134">INPUTS</span></span>

### <span data-ttu-id="67d3b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="67d3b-135">System.String</span></span>

## <span data-ttu-id="67d3b-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67d3b-136">OUTPUTS</span></span>

## <span data-ttu-id="67d3b-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="67d3b-137">NOTES</span></span>

## <span data-ttu-id="67d3b-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67d3b-138">RELATED LINKS</span></span>
