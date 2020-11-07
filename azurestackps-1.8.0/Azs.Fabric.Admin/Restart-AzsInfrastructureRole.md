---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 781b920bf955a84554b9152f54c9847a00a8b160
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908105"
---
# <span data-ttu-id="a9e69-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="a9e69-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="a9e69-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a9e69-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e69-103">Перезапускает запрашиваемую роль инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="a9e69-103">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="a9e69-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a9e69-104">SYNTAX</span></span>

### <span data-ttu-id="a9e69-105">Перезагрузка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a9e69-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9e69-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9e69-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9e69-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9e69-107">DESCRIPTION</span></span>
<span data-ttu-id="a9e69-108">Перезапускает запрашиваемую роль инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="a9e69-108">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="a9e69-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a9e69-109">EXAMPLES</span></span>

### <span data-ttu-id="a9e69-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="a9e69-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="a9e69-111">Перезапустите роль инфраструктуры, которая завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="a9e69-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="a9e69-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a9e69-112">PARAMETERS</span></span>

### <span data-ttu-id="a9e69-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a9e69-113">-Name</span></span>
<span data-ttu-id="a9e69-114">Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="a9e69-114">Infrastructure role name.</span></span>

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

### <span data-ttu-id="a9e69-115">-Location</span><span class="sxs-lookup"><span data-stu-id="a9e69-115">-Location</span></span>
<span data-ttu-id="a9e69-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a9e69-116">Location of the resource.</span></span>

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

### <span data-ttu-id="a9e69-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9e69-117">-ResourceGroupName</span></span>
<span data-ttu-id="a9e69-118">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a9e69-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="a9e69-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9e69-119">-ResourceId</span></span>
<span data-ttu-id="a9e69-120">Идентификатор ресурса роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="a9e69-120">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="a9e69-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9e69-121">-AsJob</span></span>
<span data-ttu-id="a9e69-122">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="a9e69-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="a9e69-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a9e69-123">-Force</span></span>
<span data-ttu-id="a9e69-124">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a9e69-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a9e69-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9e69-125">-WhatIf</span></span>
<span data-ttu-id="a9e69-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a9e69-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9e69-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a9e69-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9e69-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9e69-128">-Confirm</span></span>
<span data-ttu-id="a9e69-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a9e69-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9e69-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e69-130">CommonParameters</span></span>
<span data-ttu-id="a9e69-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a9e69-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e69-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9e69-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e69-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a9e69-133">INPUTS</span></span>

## <span data-ttu-id="a9e69-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9e69-134">OUTPUTS</span></span>

## <span data-ttu-id="a9e69-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="a9e69-135">NOTES</span></span>

## <span data-ttu-id="a9e69-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9e69-136">RELATED LINKS</span></span>
