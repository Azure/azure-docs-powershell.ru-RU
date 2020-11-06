---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348582b008d50371bc937961cd76edbf1ba13762
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555852"
---
# <span data-ttu-id="efe39-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="efe39-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="efe39-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="efe39-102">SYNOPSIS</span></span>
<span data-ttu-id="efe39-103">Завершите работу экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="efe39-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="efe39-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="efe39-104">SYNTAX</span></span>

### <span data-ttu-id="efe39-105">Завершение работы (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="efe39-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efe39-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="efe39-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="efe39-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="efe39-107">DESCRIPTION</span></span>
<span data-ttu-id="efe39-108">Завершите работу экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="efe39-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="efe39-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="efe39-109">EXAMPLES</span></span>

### <span data-ttu-id="efe39-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="efe39-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="efe39-111">Завершите работу экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="efe39-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="efe39-112">При возникновении ошибки возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="efe39-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="efe39-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="efe39-113">PARAMETERS</span></span>

### <span data-ttu-id="efe39-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efe39-114">-AsJob</span></span>
<span data-ttu-id="efe39-115">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="efe39-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="efe39-116">-Force</span><span class="sxs-lookup"><span data-stu-id="efe39-116">-Force</span></span>
<span data-ttu-id="efe39-117">Не запрашивать подтверждение</span><span class="sxs-lookup"><span data-stu-id="efe39-117">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="efe39-118">-Location</span><span class="sxs-lookup"><span data-stu-id="efe39-118">-Location</span></span>
<span data-ttu-id="efe39-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="efe39-119">Location of the resource.</span></span>

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

### <span data-ttu-id="efe39-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="efe39-120">-Name</span></span>
<span data-ttu-id="efe39-121">Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="efe39-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="efe39-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efe39-122">-ResourceGroupName</span></span>
<span data-ttu-id="efe39-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="efe39-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="efe39-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efe39-124">-ResourceId</span></span>
<span data-ttu-id="efe39-125">Идентификатор ресурса для экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="efe39-125">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="efe39-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="efe39-126">-Confirm</span></span>
<span data-ttu-id="efe39-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="efe39-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efe39-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efe39-128">-WhatIf</span></span>
<span data-ttu-id="efe39-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="efe39-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efe39-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="efe39-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efe39-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efe39-131">CommonParameters</span></span>
<span data-ttu-id="efe39-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="efe39-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efe39-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efe39-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efe39-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="efe39-134">INPUTS</span></span>

## <span data-ttu-id="efe39-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="efe39-135">OUTPUTS</span></span>

## <span data-ttu-id="efe39-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="efe39-136">NOTES</span></span>

## <span data-ttu-id="efe39-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="efe39-137">RELATED LINKS</span></span>

