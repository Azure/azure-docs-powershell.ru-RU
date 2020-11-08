---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab432625ab6af4a8fbd23895cb82e1d9f83954c8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076931"
---
# <span data-ttu-id="b74a1-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="b74a1-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="b74a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b74a1-102">SYNOPSIS</span></span>
<span data-ttu-id="b74a1-103">Применение определенного обновления на расположении обновления.</span><span class="sxs-lookup"><span data-stu-id="b74a1-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="b74a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b74a1-104">SYNTAX</span></span>

### <span data-ttu-id="b74a1-105">Apply (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b74a1-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b74a1-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b74a1-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b74a1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b74a1-107">DESCRIPTION</span></span>
<span data-ttu-id="b74a1-108">Применение определенного обновления на расположении обновления.</span><span class="sxs-lookup"><span data-stu-id="b74a1-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="b74a1-109">После вызова Get-AzsUpdateRun можно использовать для изменения хода выполнения обновления.</span><span class="sxs-lookup"><span data-stu-id="b74a1-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="b74a1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b74a1-110">EXAMPLES</span></span>

### <span data-ttu-id="b74a1-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="b74a1-111">EXAMPLE 1</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="b74a1-112">Применение определенного обновления на расположении обновления.</span><span class="sxs-lookup"><span data-stu-id="b74a1-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="b74a1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b74a1-113">PARAMETERS</span></span>

### <span data-ttu-id="b74a1-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b74a1-114">-Name</span></span>
<span data-ttu-id="b74a1-115">Имя обновления.</span><span class="sxs-lookup"><span data-stu-id="b74a1-115">Name of the update.</span></span>

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

### <span data-ttu-id="b74a1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b74a1-116">-ResourceGroupName</span></span>
<span data-ttu-id="b74a1-117">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="b74a1-117">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="b74a1-118">-Location</span><span class="sxs-lookup"><span data-stu-id="b74a1-118">-Location</span></span>
<span data-ttu-id="b74a1-119">Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="b74a1-119">The name of the update location.</span></span>

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

### <span data-ttu-id="b74a1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b74a1-120">-AsJob</span></span>
<span data-ttu-id="b74a1-121">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="b74a1-121">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="b74a1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b74a1-122">-ResourceId</span></span>
<span data-ttu-id="b74a1-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="b74a1-123">The resource id.</span></span>

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

### <span data-ttu-id="b74a1-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b74a1-124">-Force</span></span>
<span data-ttu-id="b74a1-125">Пометка для удаления элемента без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b74a1-125">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="b74a1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b74a1-126">-WhatIf</span></span>
<span data-ttu-id="b74a1-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b74a1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b74a1-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b74a1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b74a1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b74a1-129">-Confirm</span></span>
<span data-ttu-id="b74a1-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b74a1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b74a1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b74a1-131">CommonParameters</span></span>
<span data-ttu-id="b74a1-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b74a1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b74a1-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b74a1-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b74a1-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b74a1-134">INPUTS</span></span>

## <span data-ttu-id="b74a1-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b74a1-135">OUTPUTS</span></span>

### <span data-ttu-id="b74a1-136">Microsoft. AzureStack. Management. Update. admin. Model. Update</span><span class="sxs-lookup"><span data-stu-id="b74a1-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="b74a1-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="b74a1-137">NOTES</span></span>

## <span data-ttu-id="b74a1-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b74a1-138">RELATED LINKS</span></span>
