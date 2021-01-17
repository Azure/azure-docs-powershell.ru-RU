---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: fd01dea04043d8d68009f89823fe34f3695a6d47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328218"
---
# <span data-ttu-id="4ea39-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="4ea39-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="4ea39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ea39-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea39-103">Удаляет кэш HPC.</span><span class="sxs-lookup"><span data-stu-id="4ea39-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="4ea39-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4ea39-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ea39-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ea39-105">DESCRIPTION</span></span>
<span data-ttu-id="4ea39-106">С **его использованием удаляется** кэш HPC Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea39-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="4ea39-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4ea39-107">EXAMPLES</span></span>

### <span data-ttu-id="4ea39-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4ea39-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="4ea39-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ea39-109">PARAMETERS</span></span>

### <span data-ttu-id="4ea39-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ea39-110">-AsJob</span></span>
<span data-ttu-id="4ea39-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4ea39-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ea39-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea39-112">-DefaultProfile</span></span>
<span data-ttu-id="4ea39-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea39-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ea39-114">-Force</span><span class="sxs-lookup"><span data-stu-id="4ea39-114">-Force</span></span>
<span data-ttu-id="4ea39-115">Указывает на то, что при этом не будет предложено подтвердить запрос.</span><span class="sxs-lookup"><span data-stu-id="4ea39-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="4ea39-116">По умолчанию этот cmdlet запросит подтверждение удаления кэша.</span><span class="sxs-lookup"><span data-stu-id="4ea39-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="4ea39-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4ea39-117">-Name</span></span>
<span data-ttu-id="4ea39-118">Имя кэша.</span><span class="sxs-lookup"><span data-stu-id="4ea39-118">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea39-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ea39-119">-PassThru</span></span>
<span data-ttu-id="4ea39-120">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="4ea39-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4ea39-121">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4ea39-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4ea39-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ea39-122">-ResourceGroupName</span></span>
<span data-ttu-id="4ea39-123">Имя группы ресурсов, для которой вы хотите удалить кэш.</span><span class="sxs-lookup"><span data-stu-id="4ea39-123">Name of resource group under which you want to remove cache.</span></span>

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

### <span data-ttu-id="4ea39-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ea39-124">-Confirm</span></span>
<span data-ttu-id="4ea39-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4ea39-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ea39-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ea39-126">-WhatIf</span></span>
<span data-ttu-id="4ea39-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ea39-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ea39-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4ea39-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ea39-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea39-129">CommonParameters</span></span>
<span data-ttu-id="4ea39-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ea39-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea39-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ea39-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea39-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ea39-132">INPUTS</span></span>

### <span data-ttu-id="4ea39-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4ea39-133">System.String</span></span>

## <span data-ttu-id="4ea39-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4ea39-134">OUTPUTS</span></span>

## <span data-ttu-id="4ea39-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4ea39-135">NOTES</span></span>

## <span data-ttu-id="4ea39-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ea39-136">RELATED LINKS</span></span>
