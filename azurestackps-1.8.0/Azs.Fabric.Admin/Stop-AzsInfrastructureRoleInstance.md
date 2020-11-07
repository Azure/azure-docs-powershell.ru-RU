---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47e4c38d3ccd98350721d358cb98eec55341ba97
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908094"
---
# <span data-ttu-id="9e8cb-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="9e8cb-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="9e8cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e8cb-102">SYNOPSIS</span></span>
<span data-ttu-id="9e8cb-103">Выключите экземпляр роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9e8cb-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="9e8cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e8cb-104">SYNTAX</span></span>

### <span data-ttu-id="9e8cb-105">PowerOff (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e8cb-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e8cb-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e8cb-106">ResourceId</span></span>
```
Stop-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e8cb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e8cb-107">DESCRIPTION</span></span>
<span data-ttu-id="9e8cb-108">Выключите экземпляр роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9e8cb-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="9e8cb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e8cb-109">EXAMPLES</span></span>

### <span data-ttu-id="9e8cb-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="9e8cb-110">EXAMPLE 1</span></span>
```
Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"
```

<span data-ttu-id="9e8cb-111">Выключите экземпляр роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9e8cb-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="9e8cb-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e8cb-112">PARAMETERS</span></span>

### <span data-ttu-id="9e8cb-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9e8cb-113">-Name</span></span>
<span data-ttu-id="9e8cb-114">Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9e8cb-114">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e8cb-115">-Location</span><span class="sxs-lookup"><span data-stu-id="9e8cb-115">-Location</span></span>
<span data-ttu-id="9e8cb-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="9e8cb-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e8cb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e8cb-117">-ResourceGroupName</span></span>
<span data-ttu-id="9e8cb-118">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e8cb-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e8cb-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e8cb-119">-ResourceId</span></span>
<span data-ttu-id="9e8cb-120">Идентификатор ресурса для экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9e8cb-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="9e8cb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e8cb-121">-AsJob</span></span>
<span data-ttu-id="9e8cb-122">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="9e8cb-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="9e8cb-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9e8cb-123">-Force</span></span>
<span data-ttu-id="9e8cb-124">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9e8cb-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="9e8cb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e8cb-125">-WhatIf</span></span>
<span data-ttu-id="9e8cb-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9e8cb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e8cb-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9e8cb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e8cb-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e8cb-128">-Confirm</span></span>
<span data-ttu-id="9e8cb-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9e8cb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e8cb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e8cb-130">CommonParameters</span></span>
<span data-ttu-id="9e8cb-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e8cb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e8cb-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e8cb-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e8cb-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e8cb-133">INPUTS</span></span>

## <span data-ttu-id="9e8cb-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e8cb-134">OUTPUTS</span></span>

## <span data-ttu-id="9e8cb-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e8cb-135">NOTES</span></span>

## <span data-ttu-id="9e8cb-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e8cb-136">RELATED LINKS</span></span>
