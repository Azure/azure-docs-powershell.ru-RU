---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94609250696a99a337153e9e0d3a1d092e380c40
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908489"
---
# <span data-ttu-id="9dbc9-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="9dbc9-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="9dbc9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9dbc9-102">SYNOPSIS</span></span>
<span data-ttu-id="9dbc9-103">Удаление квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="9dbc9-103">Delete a quota by name.</span></span>

## <span data-ttu-id="9dbc9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9dbc9-104">SYNTAX</span></span>

### <span data-ttu-id="9dbc9-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9dbc9-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9dbc9-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9dbc9-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dbc9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dbc9-107">DESCRIPTION</span></span>
<span data-ttu-id="9dbc9-108">Удаление квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="9dbc9-108">Delete a quota by name.</span></span>

## <span data-ttu-id="9dbc9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9dbc9-109">EXAMPLES</span></span>

### <span data-ttu-id="9dbc9-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="9dbc9-110">EXAMPLE 1</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="9dbc9-111">Удаление сетевой квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="9dbc9-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="9dbc9-112">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="9dbc9-112">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="9dbc9-113">Удалите сетевую квоту, используя канал.</span><span class="sxs-lookup"><span data-stu-id="9dbc9-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="9dbc9-114">ПРИМЕР 3</span><span class="sxs-lookup"><span data-stu-id="9dbc9-114">EXAMPLE 3</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="9dbc9-115">Удалите сетевые квоты.</span><span class="sxs-lookup"><span data-stu-id="9dbc9-115">Remove a network quota.</span></span>

## <span data-ttu-id="9dbc9-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9dbc9-116">PARAMETERS</span></span>

### <span data-ttu-id="9dbc9-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9dbc9-117">-Name</span></span>
<span data-ttu-id="9dbc9-118">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="9dbc9-118">Name of the resource.</span></span>

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

### <span data-ttu-id="9dbc9-119">-Location</span><span class="sxs-lookup"><span data-stu-id="9dbc9-119">-Location</span></span>
<span data-ttu-id="9dbc9-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="9dbc9-120">Location of the resource.</span></span>

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

### <span data-ttu-id="9dbc9-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9dbc9-121">-ResourceId</span></span>
<span data-ttu-id="9dbc9-122">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="9dbc9-122">The resource id.</span></span>

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

### <span data-ttu-id="9dbc9-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9dbc9-123">-AsJob</span></span>
<span data-ttu-id="9dbc9-124">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="9dbc9-124">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="9dbc9-125">-Force</span><span class="sxs-lookup"><span data-stu-id="9dbc9-125">-Force</span></span>
<span data-ttu-id="9dbc9-126">Параметр переключить на запрос подтверждения.</span><span class="sxs-lookup"><span data-stu-id="9dbc9-126">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="9dbc9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dbc9-127">-WhatIf</span></span>
<span data-ttu-id="9dbc9-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9dbc9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dbc9-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9dbc9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dbc9-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9dbc9-130">-Confirm</span></span>
<span data-ttu-id="9dbc9-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9dbc9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dbc9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dbc9-132">CommonParameters</span></span>
<span data-ttu-id="9dbc9-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9dbc9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dbc9-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dbc9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dbc9-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9dbc9-135">INPUTS</span></span>

## <span data-ttu-id="9dbc9-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dbc9-136">OUTPUTS</span></span>

## <span data-ttu-id="9dbc9-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="9dbc9-137">NOTES</span></span>

## <span data-ttu-id="9dbc9-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9dbc9-138">RELATED LINKS</span></span>
