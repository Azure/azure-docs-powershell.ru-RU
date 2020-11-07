---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: da781ee77cb94e7bc442b72ad0655041cf23b546
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907106"
---
# <span data-ttu-id="4ffcd-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="4ffcd-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="4ffcd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ffcd-102">SYNOPSIS</span></span>
<span data-ttu-id="4ffcd-103">Перезапускает запрошенную роль инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="4ffcd-103">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="4ffcd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ffcd-104">SYNTAX</span></span>

### <span data-ttu-id="4ffcd-105">Перезагрузка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ffcd-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ffcd-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ffcd-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ffcd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ffcd-107">DESCRIPTION</span></span>
<span data-ttu-id="4ffcd-108">Перезапускает запрошенную роль инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="4ffcd-108">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="4ffcd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ffcd-109">EXAMPLES</span></span>

### <span data-ttu-id="4ffcd-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4ffcd-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restart-AzsInfrastructureRole -Name "Compute Controller"
```

<span data-ttu-id="4ffcd-111">Перезапустите роль инфраструктуры, которая завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="4ffcd-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="4ffcd-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ffcd-112">PARAMETERS</span></span>

### <span data-ttu-id="4ffcd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ffcd-113">-AsJob</span></span>
<span data-ttu-id="4ffcd-114">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="4ffcd-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="4ffcd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4ffcd-115">-Force</span></span>
<span data-ttu-id="4ffcd-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4ffcd-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4ffcd-117">-Location</span><span class="sxs-lookup"><span data-stu-id="4ffcd-117">-Location</span></span>
<span data-ttu-id="4ffcd-118">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="4ffcd-118">Location of the resource.</span></span>

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

### <span data-ttu-id="4ffcd-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4ffcd-119">-Name</span></span>
<span data-ttu-id="4ffcd-120">Имя роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="4ffcd-120">Infrastructure role name.</span></span>

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

### <span data-ttu-id="4ffcd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ffcd-121">-ResourceGroupName</span></span>
<span data-ttu-id="4ffcd-122">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4ffcd-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="4ffcd-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ffcd-123">-ResourceId</span></span>
<span data-ttu-id="4ffcd-124">Идентификатор ресурса роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="4ffcd-124">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="4ffcd-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ffcd-125">-Confirm</span></span>
<span data-ttu-id="4ffcd-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4ffcd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ffcd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ffcd-127">-WhatIf</span></span>
<span data-ttu-id="4ffcd-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4ffcd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ffcd-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4ffcd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ffcd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ffcd-130">CommonParameters</span></span>
<span data-ttu-id="4ffcd-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ffcd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ffcd-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ffcd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ffcd-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ffcd-133">INPUTS</span></span>

## <span data-ttu-id="4ffcd-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ffcd-134">OUTPUTS</span></span>

## <span data-ttu-id="4ffcd-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ffcd-135">NOTES</span></span>

## <span data-ttu-id="4ffcd-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ffcd-136">RELATED LINKS</span></span>

