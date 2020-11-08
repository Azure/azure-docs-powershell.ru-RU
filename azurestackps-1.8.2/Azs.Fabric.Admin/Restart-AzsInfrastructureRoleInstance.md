---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03dfddb3ec666df5096184c5e00692862e091626
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076680"
---
# <span data-ttu-id="6db56-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="6db56-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="6db56-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6db56-102">SYNOPSIS</span></span>
<span data-ttu-id="6db56-103">Перезагрузите экземпляр роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="6db56-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="6db56-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6db56-104">SYNTAX</span></span>

### <span data-ttu-id="6db56-105">Перезагрузка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6db56-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6db56-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6db56-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6db56-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6db56-107">DESCRIPTION</span></span>
<span data-ttu-id="6db56-108">Перезагрузите экземпляр роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="6db56-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="6db56-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6db56-109">EXAMPLES</span></span>

### <span data-ttu-id="6db56-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="6db56-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="6db56-111">Перезагрузите экземпляр роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="6db56-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="6db56-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6db56-112">PARAMETERS</span></span>

### <span data-ttu-id="6db56-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6db56-113">-Name</span></span>
<span data-ttu-id="6db56-114">Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="6db56-114">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="6db56-115">-Location</span><span class="sxs-lookup"><span data-stu-id="6db56-115">-Location</span></span>
<span data-ttu-id="6db56-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="6db56-116">Location of the resource.</span></span>

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

### <span data-ttu-id="6db56-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6db56-117">-ResourceGroupName</span></span>
<span data-ttu-id="6db56-118">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6db56-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="6db56-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6db56-119">-ResourceId</span></span>
<span data-ttu-id="6db56-120">Идентификатор ресурса для экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="6db56-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="6db56-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6db56-121">-AsJob</span></span>
<span data-ttu-id="6db56-122">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="6db56-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="6db56-123">-Force</span><span class="sxs-lookup"><span data-stu-id="6db56-123">-Force</span></span>
<span data-ttu-id="6db56-124">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="6db56-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6db56-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6db56-125">-WhatIf</span></span>
<span data-ttu-id="6db56-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6db56-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6db56-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6db56-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6db56-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6db56-128">-Confirm</span></span>
<span data-ttu-id="6db56-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6db56-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6db56-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db56-130">CommonParameters</span></span>
<span data-ttu-id="6db56-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6db56-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db56-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6db56-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db56-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6db56-133">INPUTS</span></span>

## <span data-ttu-id="6db56-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6db56-134">OUTPUTS</span></span>

## <span data-ttu-id="6db56-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="6db56-135">NOTES</span></span>

## <span data-ttu-id="6db56-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6db56-136">RELATED LINKS</span></span>
