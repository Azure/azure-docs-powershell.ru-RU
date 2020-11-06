---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ce97fe1fc7e21f166b1bb86db52bc8ad6e29e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555840"
---
# <span data-ttu-id="fbc98-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="fbc98-101">Close-AzsAlert</span></span>

## <span data-ttu-id="fbc98-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fbc98-102">SYNOPSIS</span></span>
<span data-ttu-id="fbc98-103">Закрывает заданное оповещение.</span><span class="sxs-lookup"><span data-stu-id="fbc98-103">Closes the given alert.</span></span>

## <span data-ttu-id="fbc98-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fbc98-104">SYNTAX</span></span>

### <span data-ttu-id="fbc98-105">Закрыть (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fbc98-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fbc98-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fbc98-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbc98-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbc98-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbc98-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbc98-108">DESCRIPTION</span></span>
<span data-ttu-id="fbc98-109">Закрывает заданное оповещение.</span><span class="sxs-lookup"><span data-stu-id="fbc98-109">Closes the given alert.</span></span>

## <span data-ttu-id="fbc98-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fbc98-110">EXAMPLES</span></span>

### <span data-ttu-id="fbc98-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fbc98-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="fbc98-112">Закрыть оповещение по имени.</span><span class="sxs-lookup"><span data-stu-id="fbc98-112">Close an alert by Name.</span></span>

### <span data-ttu-id="fbc98-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="fbc98-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="fbc98-114">Закрывайте оповещение с помощью трубопроводов.</span><span class="sxs-lookup"><span data-stu-id="fbc98-114">Close an alert through piping.</span></span>

## <span data-ttu-id="fbc98-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fbc98-115">PARAMETERS</span></span>

### <span data-ttu-id="fbc98-116">-Force</span><span class="sxs-lookup"><span data-stu-id="fbc98-116">-Force</span></span>
<span data-ttu-id="fbc98-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="fbc98-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="fbc98-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbc98-118">-InputObject</span></span>
<span data-ttu-id="fbc98-119">Оповещение, возвращенное из Get-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="fbc98-119">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="fbc98-120">-Location</span><span class="sxs-lookup"><span data-stu-id="fbc98-120">-Location</span></span>
<span data-ttu-id="fbc98-121">Название местоположения.</span><span class="sxs-lookup"><span data-stu-id="fbc98-121">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbc98-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fbc98-122">-Name</span></span>
<span data-ttu-id="fbc98-123">Идентификатор оповещения.</span><span class="sxs-lookup"><span data-stu-id="fbc98-123">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbc98-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbc98-124">-ResourceGroupName</span></span>
<span data-ttu-id="fbc98-125">Имя группы ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="fbc98-125">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbc98-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbc98-126">-ResourceId</span></span>
<span data-ttu-id="fbc98-127">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="fbc98-127">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbc98-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbc98-128">-Confirm</span></span>
<span data-ttu-id="fbc98-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fbc98-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbc98-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbc98-130">-WhatIf</span></span>
<span data-ttu-id="fbc98-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fbc98-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbc98-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fbc98-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbc98-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbc98-133">CommonParameters</span></span>
<span data-ttu-id="fbc98-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fbc98-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbc98-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbc98-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbc98-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fbc98-136">INPUTS</span></span>

## <span data-ttu-id="fbc98-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbc98-137">OUTPUTS</span></span>

### <span data-ttu-id="fbc98-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. Alert</span><span class="sxs-lookup"><span data-stu-id="fbc98-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="fbc98-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="fbc98-139">NOTES</span></span>

## <span data-ttu-id="fbc98-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbc98-140">RELATED LINKS</span></span>

