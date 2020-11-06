---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b06ae4189b427686f4237c1a6eae841fcaba5c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555828"
---
# <span data-ttu-id="ec71f-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="ec71f-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="ec71f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ec71f-102">SYNOPSIS</span></span>
<span data-ttu-id="ec71f-103">Восстанавливает данное оповещение.</span><span class="sxs-lookup"><span data-stu-id="ec71f-103">Repairs the given alert.</span></span>

## <span data-ttu-id="ec71f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ec71f-104">SYNTAX</span></span>

### <span data-ttu-id="ec71f-105">Восстановление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ec71f-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec71f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ec71f-106">InputObject</span></span>
```
Repair-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec71f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec71f-107">DESCRIPTION</span></span>
<span data-ttu-id="ec71f-108">Восстанавливает данное оповещение.</span><span class="sxs-lookup"><span data-stu-id="ec71f-108">Repairs the given alert.</span></span>

## <span data-ttu-id="ec71f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ec71f-109">EXAMPLES</span></span>

### <span data-ttu-id="ec71f-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ec71f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="ec71f-111">Восстанавливает оповещение по имени.</span><span class="sxs-lookup"><span data-stu-id="ec71f-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="ec71f-112">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ec71f-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="ec71f-113">Восстанавливает оповещение с помощью трубопроводов.</span><span class="sxs-lookup"><span data-stu-id="ec71f-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="ec71f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ec71f-114">PARAMETERS</span></span>

### <span data-ttu-id="ec71f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ec71f-115">-Force</span></span>
<span data-ttu-id="ec71f-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ec71f-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ec71f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec71f-117">-InputObject</span></span>
<span data-ttu-id="ec71f-118">Оповещение, возвращенное из Get-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="ec71f-118">An alert returned from Get-AzsAlert.</span></span>

```yaml
Type: Alert
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec71f-119">-Location</span><span class="sxs-lookup"><span data-stu-id="ec71f-119">-Location</span></span>
<span data-ttu-id="ec71f-120">Название местоположения.</span><span class="sxs-lookup"><span data-stu-id="ec71f-120">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec71f-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ec71f-121">-Name</span></span>
<span data-ttu-id="ec71f-122">Идентификатор оповещения.</span><span class="sxs-lookup"><span data-stu-id="ec71f-122">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec71f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec71f-123">-ResourceGroupName</span></span>
<span data-ttu-id="ec71f-124">Имя группы ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="ec71f-124">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec71f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec71f-125">-Confirm</span></span>
<span data-ttu-id="ec71f-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ec71f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec71f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec71f-127">-WhatIf</span></span>
<span data-ttu-id="ec71f-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ec71f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec71f-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ec71f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec71f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec71f-130">CommonParameters</span></span>
<span data-ttu-id="ec71f-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ec71f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec71f-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec71f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec71f-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ec71f-133">INPUTS</span></span>

## <span data-ttu-id="ec71f-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec71f-134">OUTPUTS</span></span>

## <span data-ttu-id="ec71f-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="ec71f-135">NOTES</span></span>

## <span data-ttu-id="ec71f-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec71f-136">RELATED LINKS</span></span>

