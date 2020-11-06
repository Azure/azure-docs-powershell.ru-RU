---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f7f40982a4c7d24e02e7e365163cc6250ff8791
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556127"
---
# <span data-ttu-id="c330c-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="c330c-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="c330c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c330c-102">SYNOPSIS</span></span>
<span data-ttu-id="c330c-103">Удаление квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="c330c-103">Delete a quota by name.</span></span>

## <span data-ttu-id="c330c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c330c-104">SYNTAX</span></span>

### <span data-ttu-id="c330c-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c330c-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c330c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c330c-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c330c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c330c-107">DESCRIPTION</span></span>
<span data-ttu-id="c330c-108">Удаление квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="c330c-108">Delete a quota by name.</span></span>

## <span data-ttu-id="c330c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c330c-109">EXAMPLES</span></span>

### <span data-ttu-id="c330c-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c330c-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="c330c-111">Удаление сетевой квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="c330c-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="c330c-112">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c330c-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="c330c-113">Удалите сетевую квоту, используя канал.</span><span class="sxs-lookup"><span data-stu-id="c330c-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="c330c-114">--------------------------ПРИМЕР 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="c330c-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="c330c-115">Удалите сетевые квоты.</span><span class="sxs-lookup"><span data-stu-id="c330c-115">Remove a network quota.</span></span>

## <span data-ttu-id="c330c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c330c-116">PARAMETERS</span></span>

### <span data-ttu-id="c330c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c330c-117">-AsJob</span></span>
<span data-ttu-id="c330c-118">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="c330c-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c330c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c330c-119">-Force</span></span>
<span data-ttu-id="c330c-120">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c330c-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c330c-121">-Location</span><span class="sxs-lookup"><span data-stu-id="c330c-121">-Location</span></span>
<span data-ttu-id="c330c-122">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="c330c-122">Location of the resource.</span></span>

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

### <span data-ttu-id="c330c-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c330c-123">-Name</span></span>
<span data-ttu-id="c330c-124">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="c330c-124">Name of the resource.</span></span>

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

### <span data-ttu-id="c330c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c330c-125">-ResourceId</span></span>
<span data-ttu-id="c330c-126">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="c330c-126">The resource id.</span></span>

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

### <span data-ttu-id="c330c-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c330c-127">-Confirm</span></span>
<span data-ttu-id="c330c-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c330c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c330c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c330c-129">-WhatIf</span></span>
<span data-ttu-id="c330c-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c330c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c330c-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c330c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c330c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c330c-132">CommonParameters</span></span>
<span data-ttu-id="c330c-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c330c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c330c-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c330c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c330c-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c330c-135">INPUTS</span></span>

## <span data-ttu-id="c330c-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c330c-136">OUTPUTS</span></span>

## <span data-ttu-id="c330c-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="c330c-137">NOTES</span></span>

## <span data-ttu-id="c330c-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c330c-138">RELATED LINKS</span></span>

