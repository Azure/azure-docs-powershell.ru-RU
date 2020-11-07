---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94609250696a99a337153e9e0d3a1d092e380c40
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909069"
---
# <span data-ttu-id="b8e11-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="b8e11-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="b8e11-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8e11-102">SYNOPSIS</span></span>
<span data-ttu-id="b8e11-103">Удаление квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="b8e11-103">Delete a quota by name.</span></span>

## <span data-ttu-id="b8e11-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8e11-104">SYNTAX</span></span>

### <span data-ttu-id="b8e11-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b8e11-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8e11-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8e11-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8e11-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8e11-107">DESCRIPTION</span></span>
<span data-ttu-id="b8e11-108">Удаление квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="b8e11-108">Delete a quota by name.</span></span>

## <span data-ttu-id="b8e11-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8e11-109">EXAMPLES</span></span>

### <span data-ttu-id="b8e11-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="b8e11-110">EXAMPLE 1</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="b8e11-111">Удаление сетевой квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="b8e11-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="b8e11-112">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="b8e11-112">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="b8e11-113">Удалите сетевую квоту, используя канал.</span><span class="sxs-lookup"><span data-stu-id="b8e11-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="b8e11-114">ПРИМЕР 3</span><span class="sxs-lookup"><span data-stu-id="b8e11-114">EXAMPLE 3</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="b8e11-115">Удалите сетевые квоты.</span><span class="sxs-lookup"><span data-stu-id="b8e11-115">Remove a network quota.</span></span>

## <span data-ttu-id="b8e11-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8e11-116">PARAMETERS</span></span>

### <span data-ttu-id="b8e11-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8e11-117">-Name</span></span>
<span data-ttu-id="b8e11-118">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8e11-118">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e11-119">-Location</span><span class="sxs-lookup"><span data-stu-id="b8e11-119">-Location</span></span>
<span data-ttu-id="b8e11-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8e11-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e11-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8e11-121">-ResourceId</span></span>
<span data-ttu-id="b8e11-122">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8e11-122">The resource id.</span></span>

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

### <span data-ttu-id="b8e11-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8e11-123">-AsJob</span></span>
<span data-ttu-id="b8e11-124">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="b8e11-124">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="b8e11-125">-Force</span><span class="sxs-lookup"><span data-stu-id="b8e11-125">-Force</span></span>
<span data-ttu-id="b8e11-126">Параметр переключить на запрос подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b8e11-126">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="b8e11-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8e11-127">-WhatIf</span></span>
<span data-ttu-id="b8e11-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b8e11-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8e11-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b8e11-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8e11-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8e11-130">-Confirm</span></span>
<span data-ttu-id="b8e11-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b8e11-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8e11-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8e11-132">CommonParameters</span></span>
<span data-ttu-id="b8e11-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8e11-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8e11-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8e11-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8e11-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8e11-135">INPUTS</span></span>

## <span data-ttu-id="b8e11-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8e11-136">OUTPUTS</span></span>

## <span data-ttu-id="b8e11-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8e11-137">NOTES</span></span>

## <span data-ttu-id="b8e11-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8e11-138">RELATED LINKS</span></span>
