---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94609250696a99a337153e9e0d3a1d092e380c40
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077170"
---
# <span data-ttu-id="dd707-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="dd707-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="dd707-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd707-102">SYNOPSIS</span></span>
<span data-ttu-id="dd707-103">Удаление квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="dd707-103">Delete a quota by name.</span></span>

## <span data-ttu-id="dd707-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd707-104">SYNTAX</span></span>

### <span data-ttu-id="dd707-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd707-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd707-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd707-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd707-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd707-107">DESCRIPTION</span></span>
<span data-ttu-id="dd707-108">Удаление квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="dd707-108">Delete a quota by name.</span></span>

## <span data-ttu-id="dd707-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd707-109">EXAMPLES</span></span>

### <span data-ttu-id="dd707-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="dd707-110">EXAMPLE 1</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="dd707-111">Удаление сетевой квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="dd707-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="dd707-112">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="dd707-112">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="dd707-113">Удалите сетевую квоту, используя канал.</span><span class="sxs-lookup"><span data-stu-id="dd707-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="dd707-114">ПРИМЕР 3</span><span class="sxs-lookup"><span data-stu-id="dd707-114">EXAMPLE 3</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="dd707-115">Удалите сетевые квоты.</span><span class="sxs-lookup"><span data-stu-id="dd707-115">Remove a network quota.</span></span>

## <span data-ttu-id="dd707-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd707-116">PARAMETERS</span></span>

### <span data-ttu-id="dd707-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dd707-117">-Name</span></span>
<span data-ttu-id="dd707-118">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd707-118">Name of the resource.</span></span>

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

### <span data-ttu-id="dd707-119">-Location</span><span class="sxs-lookup"><span data-stu-id="dd707-119">-Location</span></span>
<span data-ttu-id="dd707-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd707-120">Location of the resource.</span></span>

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

### <span data-ttu-id="dd707-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd707-121">-ResourceId</span></span>
<span data-ttu-id="dd707-122">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd707-122">The resource id.</span></span>

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

### <span data-ttu-id="dd707-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd707-123">-AsJob</span></span>
<span data-ttu-id="dd707-124">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="dd707-124">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="dd707-125">-Force</span><span class="sxs-lookup"><span data-stu-id="dd707-125">-Force</span></span>
<span data-ttu-id="dd707-126">Параметр переключить на запрос подтверждения.</span><span class="sxs-lookup"><span data-stu-id="dd707-126">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="dd707-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd707-127">-WhatIf</span></span>
<span data-ttu-id="dd707-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dd707-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd707-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dd707-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd707-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd707-130">-Confirm</span></span>
<span data-ttu-id="dd707-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dd707-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd707-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd707-132">CommonParameters</span></span>
<span data-ttu-id="dd707-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd707-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd707-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd707-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd707-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd707-135">INPUTS</span></span>

## <span data-ttu-id="dd707-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd707-136">OUTPUTS</span></span>

## <span data-ttu-id="dd707-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd707-137">NOTES</span></span>

## <span data-ttu-id="dd707-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd707-138">RELATED LINKS</span></span>
