---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: fd01dea04043d8d68009f89823fe34f3695a6d47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247811"
---
# <span data-ttu-id="1e58b-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="1e58b-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="1e58b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e58b-102">SYNOPSIS</span></span>
<span data-ttu-id="1e58b-103">Удаление кэша HPC.</span><span class="sxs-lookup"><span data-stu-id="1e58b-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="1e58b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e58b-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e58b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e58b-105">DESCRIPTION</span></span>
<span data-ttu-id="1e58b-106">Командлет **Remove-AzHpcCache** удаляет кэш Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="1e58b-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="1e58b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e58b-107">EXAMPLES</span></span>

### <span data-ttu-id="1e58b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1e58b-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="1e58b-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e58b-109">PARAMETERS</span></span>

### <span data-ttu-id="1e58b-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e58b-110">-AsJob</span></span>
<span data-ttu-id="1e58b-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1e58b-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e58b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e58b-112">-DefaultProfile</span></span>
<span data-ttu-id="1e58b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e58b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e58b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="1e58b-114">-Force</span></span>
<span data-ttu-id="1e58b-115">Указывает на то, что командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="1e58b-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="1e58b-116">По умолчанию этот командлет предлагает подтвердить удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="1e58b-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="1e58b-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1e58b-117">-Name</span></span>
<span data-ttu-id="1e58b-118">Имя кэша.</span><span class="sxs-lookup"><span data-stu-id="1e58b-118">Name of cache.</span></span>

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

### <span data-ttu-id="1e58b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e58b-119">-PassThru</span></span>
<span data-ttu-id="1e58b-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="1e58b-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1e58b-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1e58b-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1e58b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e58b-122">-ResourceGroupName</span></span>
<span data-ttu-id="1e58b-123">Имя группы ресурсов, в которой вы хотите удалить кэш.</span><span class="sxs-lookup"><span data-stu-id="1e58b-123">Name of resource group under which you want to remove cache.</span></span>

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

### <span data-ttu-id="1e58b-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e58b-124">-Confirm</span></span>
<span data-ttu-id="1e58b-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1e58b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e58b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e58b-126">-WhatIf</span></span>
<span data-ttu-id="1e58b-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1e58b-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e58b-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1e58b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e58b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e58b-129">CommonParameters</span></span>
<span data-ttu-id="1e58b-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e58b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e58b-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e58b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e58b-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e58b-132">INPUTS</span></span>

### <span data-ttu-id="1e58b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1e58b-133">System.String</span></span>

## <span data-ttu-id="1e58b-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e58b-134">OUTPUTS</span></span>

## <span data-ttu-id="1e58b-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e58b-135">NOTES</span></span>

## <span data-ttu-id="1e58b-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e58b-136">RELATED LINKS</span></span>
