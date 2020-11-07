---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c7ec31ce2af23a4376f8b5f94deca302345e81
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908266"
---
# <span data-ttu-id="514c1-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="514c1-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="514c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="514c1-102">SYNOPSIS</span></span>
<span data-ttu-id="514c1-103">Начните сбор мусора для удаленных объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="514c1-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="514c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="514c1-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="514c1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="514c1-105">DESCRIPTION</span></span>
<span data-ttu-id="514c1-106">Начните сбор мусора для удаленных объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="514c1-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="514c1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="514c1-107">EXAMPLES</span></span>

### <span data-ttu-id="514c1-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="514c1-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="514c1-109">Начните сбор мусора.</span><span class="sxs-lookup"><span data-stu-id="514c1-109">Start garbage collection.</span></span>

## <span data-ttu-id="514c1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="514c1-110">PARAMETERS</span></span>

### <span data-ttu-id="514c1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="514c1-111">-AsJob</span></span>
<span data-ttu-id="514c1-112">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="514c1-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="514c1-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="514c1-113">-FarmName</span></span>
<span data-ttu-id="514c1-114">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="514c1-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="514c1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="514c1-115">-Force</span></span>
<span data-ttu-id="514c1-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="514c1-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="514c1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="514c1-117">-ResourceGroupName</span></span>
<span data-ttu-id="514c1-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="514c1-118">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="514c1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="514c1-119">-Confirm</span></span>
<span data-ttu-id="514c1-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="514c1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="514c1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="514c1-121">-WhatIf</span></span>
<span data-ttu-id="514c1-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="514c1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="514c1-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="514c1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="514c1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="514c1-124">CommonParameters</span></span>
<span data-ttu-id="514c1-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="514c1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="514c1-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="514c1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="514c1-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="514c1-127">INPUTS</span></span>

## <span data-ttu-id="514c1-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="514c1-128">OUTPUTS</span></span>

## <span data-ttu-id="514c1-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="514c1-129">NOTES</span></span>

## <span data-ttu-id="514c1-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="514c1-130">RELATED LINKS</span></span>

