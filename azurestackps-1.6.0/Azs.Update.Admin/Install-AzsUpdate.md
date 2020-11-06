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
ms.locfileid: "93556092"
---
# <span data-ttu-id="41143-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="41143-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="41143-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41143-102">SYNOPSIS</span></span>
<span data-ttu-id="41143-103">Применение определенного обновления на расположении обновления.</span><span class="sxs-lookup"><span data-stu-id="41143-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="41143-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41143-104">SYNTAX</span></span>

### <span data-ttu-id="41143-105">Apply (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="41143-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41143-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="41143-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41143-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41143-107">DESCRIPTION</span></span>
<span data-ttu-id="41143-108">Применение определенного обновления на расположении обновления.</span><span class="sxs-lookup"><span data-stu-id="41143-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="41143-109">После вызова Get-AzsUpdateRun можно использовать для изменения хода выполнения обновления.</span><span class="sxs-lookup"><span data-stu-id="41143-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="41143-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41143-110">EXAMPLES</span></span>

### <span data-ttu-id="41143-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="41143-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="41143-112">Применение определенного обновления на расположении обновления.</span><span class="sxs-lookup"><span data-stu-id="41143-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="41143-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41143-113">PARAMETERS</span></span>

### <span data-ttu-id="41143-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41143-114">-AsJob</span></span>
<span data-ttu-id="41143-115">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="41143-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="41143-116">-Force</span><span class="sxs-lookup"><span data-stu-id="41143-116">-Force</span></span>
<span data-ttu-id="41143-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="41143-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="41143-118">-Location</span><span class="sxs-lookup"><span data-stu-id="41143-118">-Location</span></span>
<span data-ttu-id="41143-119">Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="41143-119">The name of the update location.</span></span>

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

### <span data-ttu-id="41143-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="41143-120">-Name</span></span>
<span data-ttu-id="41143-121">Имя обновления.</span><span class="sxs-lookup"><span data-stu-id="41143-121">Name of the update.</span></span>

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

### <span data-ttu-id="41143-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41143-122">-ResourceGroupName</span></span>
<span data-ttu-id="41143-123">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="41143-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="41143-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41143-124">-ResourceId</span></span>
<span data-ttu-id="41143-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="41143-125">The resource id.</span></span>

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

### <span data-ttu-id="41143-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41143-126">-Confirm</span></span>
<span data-ttu-id="41143-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="41143-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41143-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41143-128">-WhatIf</span></span>
<span data-ttu-id="41143-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="41143-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41143-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="41143-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41143-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41143-131">CommonParameters</span></span>
<span data-ttu-id="41143-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41143-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41143-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41143-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41143-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41143-134">INPUTS</span></span>

## <span data-ttu-id="41143-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41143-135">OUTPUTS</span></span>

### <span data-ttu-id="41143-136">Microsoft. AzureStack. Management. Update. admin. Model. Update</span><span class="sxs-lookup"><span data-stu-id="41143-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="41143-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="41143-137">NOTES</span></span>

## <span data-ttu-id="41143-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41143-138">RELATED LINKS</span></span>

