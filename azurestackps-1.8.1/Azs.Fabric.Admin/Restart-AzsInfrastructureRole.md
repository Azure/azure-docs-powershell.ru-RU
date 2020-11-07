---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 781b920bf955a84554b9152f54c9847a00a8b160
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908802"
---
# <span data-ttu-id="44b5f-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="44b5f-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="44b5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44b5f-102">SYNOPSIS</span></span>
<span data-ttu-id="44b5f-103">Перезапускает запрашиваемую роль инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="44b5f-103">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="44b5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44b5f-104">SYNTAX</span></span>

### <span data-ttu-id="44b5f-105">Перезагрузка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="44b5f-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44b5f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="44b5f-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44b5f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44b5f-107">DESCRIPTION</span></span>
<span data-ttu-id="44b5f-108">Перезапускает запрашиваемую роль инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="44b5f-108">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="44b5f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44b5f-109">EXAMPLES</span></span>

### <span data-ttu-id="44b5f-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="44b5f-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="44b5f-111">Перезапустите роль инфраструктуры, которая завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="44b5f-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="44b5f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44b5f-112">PARAMETERS</span></span>

### <span data-ttu-id="44b5f-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="44b5f-113">-Name</span></span>
<span data-ttu-id="44b5f-114">Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="44b5f-114">Infrastructure role name.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b5f-115">-Location</span><span class="sxs-lookup"><span data-stu-id="44b5f-115">-Location</span></span>
<span data-ttu-id="44b5f-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="44b5f-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b5f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44b5f-117">-ResourceGroupName</span></span>
<span data-ttu-id="44b5f-118">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="44b5f-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b5f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44b5f-119">-ResourceId</span></span>
<span data-ttu-id="44b5f-120">Идентификатор ресурса роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="44b5f-120">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="44b5f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44b5f-121">-AsJob</span></span>
<span data-ttu-id="44b5f-122">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="44b5f-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="44b5f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="44b5f-123">-Force</span></span>
<span data-ttu-id="44b5f-124">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="44b5f-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="44b5f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44b5f-125">-WhatIf</span></span>
<span data-ttu-id="44b5f-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="44b5f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44b5f-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="44b5f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44b5f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44b5f-128">-Confirm</span></span>
<span data-ttu-id="44b5f-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="44b5f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44b5f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44b5f-130">CommonParameters</span></span>
<span data-ttu-id="44b5f-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44b5f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44b5f-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44b5f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44b5f-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44b5f-133">INPUTS</span></span>

## <span data-ttu-id="44b5f-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44b5f-134">OUTPUTS</span></span>

## <span data-ttu-id="44b5f-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="44b5f-135">NOTES</span></span>

## <span data-ttu-id="44b5f-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44b5f-136">RELATED LINKS</span></span>
