---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab432625ab6af4a8fbd23895cb82e1d9f83954c8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908021"
---
# <span data-ttu-id="390a3-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="390a3-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="390a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="390a3-102">SYNOPSIS</span></span>
<span data-ttu-id="390a3-103">Применение определенного обновления на расположении обновления.</span><span class="sxs-lookup"><span data-stu-id="390a3-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="390a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="390a3-104">SYNTAX</span></span>

### <span data-ttu-id="390a3-105">Apply (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="390a3-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="390a3-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="390a3-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="390a3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="390a3-107">DESCRIPTION</span></span>
<span data-ttu-id="390a3-108">Применение определенного обновления на расположении обновления.</span><span class="sxs-lookup"><span data-stu-id="390a3-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="390a3-109">После вызова Get-AzsUpdateRun можно использовать для изменения хода выполнения обновления.</span><span class="sxs-lookup"><span data-stu-id="390a3-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="390a3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="390a3-110">EXAMPLES</span></span>

### <span data-ttu-id="390a3-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="390a3-111">EXAMPLE 1</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="390a3-112">Применение определенного обновления на расположении обновления.</span><span class="sxs-lookup"><span data-stu-id="390a3-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="390a3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="390a3-113">PARAMETERS</span></span>

### <span data-ttu-id="390a3-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="390a3-114">-Name</span></span>
<span data-ttu-id="390a3-115">Имя обновления.</span><span class="sxs-lookup"><span data-stu-id="390a3-115">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="390a3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="390a3-116">-ResourceGroupName</span></span>
<span data-ttu-id="390a3-117">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="390a3-117">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="390a3-118">-Location</span><span class="sxs-lookup"><span data-stu-id="390a3-118">-Location</span></span>
<span data-ttu-id="390a3-119">Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="390a3-119">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="390a3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="390a3-120">-AsJob</span></span>
<span data-ttu-id="390a3-121">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="390a3-121">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="390a3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="390a3-122">-ResourceId</span></span>
<span data-ttu-id="390a3-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="390a3-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="390a3-124">-Force</span><span class="sxs-lookup"><span data-stu-id="390a3-124">-Force</span></span>
<span data-ttu-id="390a3-125">Пометка для удаления элемента без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="390a3-125">Flag to remove the item without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="390a3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="390a3-126">-WhatIf</span></span>
<span data-ttu-id="390a3-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="390a3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="390a3-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="390a3-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="390a3-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="390a3-129">-Confirm</span></span>
<span data-ttu-id="390a3-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="390a3-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="390a3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="390a3-131">CommonParameters</span></span>
<span data-ttu-id="390a3-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="390a3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="390a3-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="390a3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="390a3-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="390a3-134">INPUTS</span></span>

## <span data-ttu-id="390a3-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="390a3-135">OUTPUTS</span></span>

### <span data-ttu-id="390a3-136">Microsoft. AzureStack. Management. Update. admin. Model. Update</span><span class="sxs-lookup"><span data-stu-id="390a3-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="390a3-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="390a3-137">NOTES</span></span>

## <span data-ttu-id="390a3-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="390a3-138">RELATED LINKS</span></span>
