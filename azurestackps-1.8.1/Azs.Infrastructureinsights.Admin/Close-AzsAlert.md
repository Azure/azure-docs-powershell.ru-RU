---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14885871139eaed1c901312b9540a90d385795e5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909114"
---
# <span data-ttu-id="28084-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="28084-101">Close-AzsAlert</span></span>

## <span data-ttu-id="28084-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28084-102">SYNOPSIS</span></span>
<span data-ttu-id="28084-103">Закрывает заданное оповещение.</span><span class="sxs-lookup"><span data-stu-id="28084-103">Closes the given alert.</span></span>

## <span data-ttu-id="28084-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28084-104">SYNTAX</span></span>

### <span data-ttu-id="28084-105">Закрыть (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="28084-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28084-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="28084-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28084-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="28084-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28084-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28084-108">DESCRIPTION</span></span>
<span data-ttu-id="28084-109">Закрывает заданное оповещение.</span><span class="sxs-lookup"><span data-stu-id="28084-109">Closes the given alert.</span></span>

## <span data-ttu-id="28084-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28084-110">EXAMPLES</span></span>

### <span data-ttu-id="28084-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="28084-111">EXAMPLE 1</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="28084-112">Закрыть оповещение по имени.</span><span class="sxs-lookup"><span data-stu-id="28084-112">Close an alert by Name.</span></span>

### <span data-ttu-id="28084-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="28084-113">EXAMPLE 2</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="28084-114">Закрывайте оповещение с помощью трубопроводов.</span><span class="sxs-lookup"><span data-stu-id="28084-114">Close an alert through piping.</span></span>

## <span data-ttu-id="28084-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28084-115">PARAMETERS</span></span>

### <span data-ttu-id="28084-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="28084-116">-Name</span></span>
<span data-ttu-id="28084-117">Идентификатор оповещения.</span><span class="sxs-lookup"><span data-stu-id="28084-117">The alert identifier.</span></span>

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

### <span data-ttu-id="28084-118">-Location</span><span class="sxs-lookup"><span data-stu-id="28084-118">-Location</span></span>
<span data-ttu-id="28084-119">Название местоположения.</span><span class="sxs-lookup"><span data-stu-id="28084-119">Name of the location.</span></span>

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

### <span data-ttu-id="28084-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28084-120">-ResourceGroupName</span></span>
<span data-ttu-id="28084-121">Имя группы ресурсов для оповещения.</span><span class="sxs-lookup"><span data-stu-id="28084-121">Resource group name of the alert.</span></span>

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

### <span data-ttu-id="28084-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28084-122">-InputObject</span></span>
<span data-ttu-id="28084-123">Оповещение, возвращенное из Get-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="28084-123">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="28084-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28084-124">-ResourceId</span></span>
<span data-ttu-id="28084-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="28084-125">The resource id.</span></span>

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

### <span data-ttu-id="28084-126">-Force</span><span class="sxs-lookup"><span data-stu-id="28084-126">-Force</span></span>
<span data-ttu-id="28084-127">Параметр переключить на запрос подтверждения.</span><span class="sxs-lookup"><span data-stu-id="28084-127">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="28084-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28084-128">-WhatIf</span></span>
<span data-ttu-id="28084-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="28084-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28084-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="28084-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28084-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28084-131">-Confirm</span></span>
<span data-ttu-id="28084-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="28084-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28084-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28084-133">CommonParameters</span></span>
<span data-ttu-id="28084-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28084-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28084-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28084-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28084-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28084-136">INPUTS</span></span>

## <span data-ttu-id="28084-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28084-137">OUTPUTS</span></span>

### <span data-ttu-id="28084-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. Alert</span><span class="sxs-lookup"><span data-stu-id="28084-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="28084-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="28084-139">NOTES</span></span>

## <span data-ttu-id="28084-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28084-140">RELATED LINKS</span></span>
