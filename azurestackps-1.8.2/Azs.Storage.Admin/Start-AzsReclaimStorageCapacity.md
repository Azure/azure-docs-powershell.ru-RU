---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7256c6ffa7dc3b8a227b516faad9482eb44242d5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076952"
---
# <span data-ttu-id="bbb17-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="bbb17-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="bbb17-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bbb17-102">SYNOPSIS</span></span>
<span data-ttu-id="bbb17-103">Начните сбор мусора для удаленных объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="bbb17-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="bbb17-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bbb17-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbb17-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbb17-105">DESCRIPTION</span></span>
<span data-ttu-id="bbb17-106">Начните сбор мусора для удаленных объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="bbb17-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="bbb17-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bbb17-107">EXAMPLES</span></span>

### <span data-ttu-id="bbb17-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="bbb17-108">EXAMPLE 1</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="bbb17-109">Начните сбор мусора.</span><span class="sxs-lookup"><span data-stu-id="bbb17-109">Start garbage collection.</span></span>

## <span data-ttu-id="bbb17-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bbb17-110">PARAMETERS</span></span>

### <span data-ttu-id="bbb17-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbb17-111">-ResourceGroupName</span></span>
<span data-ttu-id="bbb17-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bbb17-112">Resource group name.</span></span>

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

### <span data-ttu-id="bbb17-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="bbb17-113">-FarmName</span></span>
<span data-ttu-id="bbb17-114">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="bbb17-114">Farm Id.</span></span>

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

### <span data-ttu-id="bbb17-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbb17-115">-AsJob</span></span>
<span data-ttu-id="bbb17-116">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="bbb17-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="bbb17-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bbb17-117">-Force</span></span>
<span data-ttu-id="bbb17-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="bbb17-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bbb17-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbb17-119">-WhatIf</span></span>
<span data-ttu-id="bbb17-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bbb17-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbb17-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bbb17-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbb17-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbb17-122">-Confirm</span></span>
<span data-ttu-id="bbb17-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bbb17-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbb17-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbb17-124">CommonParameters</span></span>
<span data-ttu-id="bbb17-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bbb17-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbb17-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbb17-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbb17-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bbb17-127">INPUTS</span></span>

## <span data-ttu-id="bbb17-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbb17-128">OUTPUTS</span></span>

## <span data-ttu-id="bbb17-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="bbb17-129">NOTES</span></span>

## <span data-ttu-id="bbb17-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbb17-130">RELATED LINKS</span></span>
