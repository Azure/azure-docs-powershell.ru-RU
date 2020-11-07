---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3ad784757210273cd2e456069c8d3a759e973a0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907109"
---
# <span data-ttu-id="79b0d-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="79b0d-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="79b0d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79b0d-102">SYNOPSIS</span></span>
<span data-ttu-id="79b0d-103">Восстанавливает узел кластера.</span><span class="sxs-lookup"><span data-stu-id="79b0d-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="79b0d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79b0d-104">SYNTAX</span></span>

### <span data-ttu-id="79b0d-105">Восстановление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="79b0d-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79b0d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="79b0d-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79b0d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79b0d-107">DESCRIPTION</span></span>
<span data-ttu-id="79b0d-108">Восстанавливает узел кластера.</span><span class="sxs-lookup"><span data-stu-id="79b0d-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="79b0d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79b0d-109">EXAMPLES</span></span>

### <span data-ttu-id="79b0d-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="79b0d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="79b0d-111">Восстановите узел масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="79b0d-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="79b0d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79b0d-112">PARAMETERS</span></span>

### <span data-ttu-id="79b0d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79b0d-113">-AsJob</span></span>
<span data-ttu-id="79b0d-114">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="79b0d-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="79b0d-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="79b0d-115">-BMCIPv4Address</span></span>
<span data-ttu-id="79b0d-116">BMC адрес физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="79b0d-116">BMC address of the physical machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79b0d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="79b0d-117">-Force</span></span>
<span data-ttu-id="79b0d-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="79b0d-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="79b0d-119">-Location</span><span class="sxs-lookup"><span data-stu-id="79b0d-119">-Location</span></span>
<span data-ttu-id="79b0d-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="79b0d-120">Location of the resource.</span></span>

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

### <span data-ttu-id="79b0d-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="79b0d-121">-Name</span></span>
<span data-ttu-id="79b0d-122">Имя узла единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="79b0d-122">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="79b0d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79b0d-123">-ResourceGroupName</span></span>
<span data-ttu-id="79b0d-124">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="79b0d-124">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="79b0d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79b0d-125">-ResourceId</span></span>
<span data-ttu-id="79b0d-126">Идентификатор ресурса узла единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="79b0d-126">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="79b0d-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79b0d-127">-Confirm</span></span>
<span data-ttu-id="79b0d-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="79b0d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79b0d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79b0d-129">-WhatIf</span></span>
<span data-ttu-id="79b0d-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="79b0d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79b0d-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="79b0d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79b0d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b0d-132">CommonParameters</span></span>
<span data-ttu-id="79b0d-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79b0d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b0d-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79b0d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b0d-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79b0d-135">INPUTS</span></span>

## <span data-ttu-id="79b0d-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79b0d-136">OUTPUTS</span></span>

## <span data-ttu-id="79b0d-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="79b0d-137">NOTES</span></span>

## <span data-ttu-id="79b0d-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79b0d-138">RELATED LINKS</span></span>

