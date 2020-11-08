---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 498374f19f83befc5697395eb58bb191555b10ca
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076763"
---
# <span data-ttu-id="9a0fa-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="9a0fa-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="9a0fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a0fa-102">SYNOPSIS</span></span>
<span data-ttu-id="9a0fa-103">Восстанавливает узел кластера.</span><span class="sxs-lookup"><span data-stu-id="9a0fa-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="9a0fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a0fa-104">SYNTAX</span></span>

### <span data-ttu-id="9a0fa-105">Восстановление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a0fa-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a0fa-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a0fa-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a0fa-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a0fa-107">DESCRIPTION</span></span>
<span data-ttu-id="9a0fa-108">Восстанавливает узел кластера.</span><span class="sxs-lookup"><span data-stu-id="9a0fa-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="9a0fa-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a0fa-109">EXAMPLES</span></span>

### <span data-ttu-id="9a0fa-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="9a0fa-110">EXAMPLE 1</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="9a0fa-111">Восстановите узел масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="9a0fa-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="9a0fa-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a0fa-112">PARAMETERS</span></span>

### <span data-ttu-id="9a0fa-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9a0fa-113">-Name</span></span>
<span data-ttu-id="9a0fa-114">Имя узла единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="9a0fa-114">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="9a0fa-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="9a0fa-115">-BMCIPv4Address</span></span>
<span data-ttu-id="9a0fa-116">BMC адрес физического компьютера.</span><span class="sxs-lookup"><span data-stu-id="9a0fa-116">BMC address of the physical machine.</span></span>

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

### <span data-ttu-id="9a0fa-117">-Location</span><span class="sxs-lookup"><span data-stu-id="9a0fa-117">-Location</span></span>
<span data-ttu-id="9a0fa-118">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="9a0fa-118">Location of the resource.</span></span>

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

### <span data-ttu-id="9a0fa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a0fa-119">-ResourceGroupName</span></span>
<span data-ttu-id="9a0fa-120">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9a0fa-120">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="9a0fa-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a0fa-121">-ResourceId</span></span>
<span data-ttu-id="9a0fa-122">Идентификатор ресурса узла единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="9a0fa-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="9a0fa-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a0fa-123">-AsJob</span></span>
<span data-ttu-id="9a0fa-124">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="9a0fa-124">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="9a0fa-125">-Force</span><span class="sxs-lookup"><span data-stu-id="9a0fa-125">-Force</span></span>
<span data-ttu-id="9a0fa-126">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9a0fa-126">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="9a0fa-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a0fa-127">-WhatIf</span></span>
<span data-ttu-id="9a0fa-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9a0fa-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a0fa-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9a0fa-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a0fa-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a0fa-130">-Confirm</span></span>
<span data-ttu-id="9a0fa-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9a0fa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a0fa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a0fa-132">CommonParameters</span></span>
<span data-ttu-id="9a0fa-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a0fa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a0fa-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a0fa-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a0fa-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a0fa-135">INPUTS</span></span>

## <span data-ttu-id="9a0fa-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a0fa-136">OUTPUTS</span></span>

## <span data-ttu-id="9a0fa-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a0fa-137">NOTES</span></span>

## <span data-ttu-id="9a0fa-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a0fa-138">RELATED LINKS</span></span>
