---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04b011279d88f294e1caf95519e29a8368b08546
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908334"
---
# <span data-ttu-id="45174-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="45174-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="45174-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45174-102">SYNOPSIS</span></span>
<span data-ttu-id="45174-103">Завершите работу экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="45174-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="45174-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45174-104">SYNTAX</span></span>

### <span data-ttu-id="45174-105">Завершение работы (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45174-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45174-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="45174-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45174-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45174-107">DESCRIPTION</span></span>
<span data-ttu-id="45174-108">Завершите работу экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="45174-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="45174-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45174-109">EXAMPLES</span></span>

### <span data-ttu-id="45174-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="45174-110">EXAMPLE 1</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="45174-111">Завершите работу экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="45174-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="45174-112">При возникновении ошибки возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="45174-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="45174-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45174-113">PARAMETERS</span></span>

### <span data-ttu-id="45174-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="45174-114">-Name</span></span>
<span data-ttu-id="45174-115">Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="45174-115">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45174-116">-Location</span><span class="sxs-lookup"><span data-stu-id="45174-116">-Location</span></span>
<span data-ttu-id="45174-117">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="45174-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45174-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45174-118">-ResourceGroupName</span></span>
<span data-ttu-id="45174-119">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45174-119">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45174-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45174-120">-ResourceId</span></span>
<span data-ttu-id="45174-121">Идентификатор ресурса для экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="45174-121">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="45174-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45174-122">-AsJob</span></span>
<span data-ttu-id="45174-123">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="45174-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="45174-124">-Force</span><span class="sxs-lookup"><span data-stu-id="45174-124">-Force</span></span>
<span data-ttu-id="45174-125">Не запрашивать подтверждение</span><span class="sxs-lookup"><span data-stu-id="45174-125">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="45174-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45174-126">-WhatIf</span></span>
<span data-ttu-id="45174-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="45174-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45174-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="45174-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45174-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45174-129">-Confirm</span></span>
<span data-ttu-id="45174-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="45174-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45174-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45174-131">CommonParameters</span></span>
<span data-ttu-id="45174-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45174-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45174-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45174-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45174-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45174-134">INPUTS</span></span>

## <span data-ttu-id="45174-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45174-135">OUTPUTS</span></span>

## <span data-ttu-id="45174-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="45174-136">NOTES</span></span>

## <span data-ttu-id="45174-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45174-137">RELATED LINKS</span></span>
