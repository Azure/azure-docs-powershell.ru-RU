---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4406dc4cadecd1945e82b8a90e9937df2183b4da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556008"
---
# <span data-ttu-id="8ae5f-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="8ae5f-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="8ae5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ae5f-102">SYNOPSIS</span></span>
<span data-ttu-id="8ae5f-103">Применение определенного обновления на расположении обновления.</span><span class="sxs-lookup"><span data-stu-id="8ae5f-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="8ae5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ae5f-104">SYNTAX</span></span>

### <span data-ttu-id="8ae5f-105">Apply (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ae5f-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ae5f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ae5f-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ae5f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ae5f-107">DESCRIPTION</span></span>
<span data-ttu-id="8ae5f-108">Применение определенного обновления на расположении обновления.</span><span class="sxs-lookup"><span data-stu-id="8ae5f-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="8ae5f-109">После вызова Get-AzsUpdateRun можно использовать для изменения хода выполнения обновления.</span><span class="sxs-lookup"><span data-stu-id="8ae5f-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="8ae5f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ae5f-110">EXAMPLES</span></span>

### <span data-ttu-id="8ae5f-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8ae5f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="8ae5f-112">Применение определенного обновления на расположении обновления.</span><span class="sxs-lookup"><span data-stu-id="8ae5f-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="8ae5f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ae5f-113">PARAMETERS</span></span>

### <span data-ttu-id="8ae5f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ae5f-114">-AsJob</span></span>
<span data-ttu-id="8ae5f-115">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="8ae5f-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="8ae5f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8ae5f-116">-Force</span></span>
<span data-ttu-id="8ae5f-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="8ae5f-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8ae5f-118">-Location</span><span class="sxs-lookup"><span data-stu-id="8ae5f-118">-Location</span></span>
<span data-ttu-id="8ae5f-119">Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="8ae5f-119">The name of the update location.</span></span>

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

### <span data-ttu-id="8ae5f-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8ae5f-120">-Name</span></span>
<span data-ttu-id="8ae5f-121">Имя обновления.</span><span class="sxs-lookup"><span data-stu-id="8ae5f-121">Name of the update.</span></span>

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

### <span data-ttu-id="8ae5f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ae5f-122">-ResourceGroupName</span></span>
<span data-ttu-id="8ae5f-123">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="8ae5f-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="8ae5f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ae5f-124">-ResourceId</span></span>
<span data-ttu-id="8ae5f-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="8ae5f-125">The resource id.</span></span>

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

### <span data-ttu-id="8ae5f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ae5f-126">-Confirm</span></span>
<span data-ttu-id="8ae5f-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8ae5f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ae5f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ae5f-128">-WhatIf</span></span>
<span data-ttu-id="8ae5f-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8ae5f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ae5f-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8ae5f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ae5f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ae5f-131">CommonParameters</span></span>
<span data-ttu-id="8ae5f-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ae5f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ae5f-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ae5f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ae5f-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ae5f-134">INPUTS</span></span>

## <span data-ttu-id="8ae5f-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ae5f-135">OUTPUTS</span></span>

### <span data-ttu-id="8ae5f-136">Microsoft. AzureStack. Management. Update. admin. Model. Update</span><span class="sxs-lookup"><span data-stu-id="8ae5f-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="8ae5f-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ae5f-137">NOTES</span></span>

## <span data-ttu-id="8ae5f-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ae5f-138">RELATED LINKS</span></span>

