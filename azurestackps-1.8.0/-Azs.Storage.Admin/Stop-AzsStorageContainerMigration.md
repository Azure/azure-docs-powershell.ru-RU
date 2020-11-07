---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81bdb6a75e10af30b6febe9bbbf0989933818aec
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908550"
---
# <span data-ttu-id="5d8a2-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="5d8a2-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="5d8a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d8a2-102">SYNOPSIS</span></span>
<span data-ttu-id="5d8a2-103">Отмена задания миграции контейнера.</span><span class="sxs-lookup"><span data-stu-id="5d8a2-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="5d8a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d8a2-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d8a2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d8a2-105">DESCRIPTION</span></span>
<span data-ttu-id="5d8a2-106">Отмена задания миграции контейнера.</span><span class="sxs-lookup"><span data-stu-id="5d8a2-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="5d8a2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d8a2-107">EXAMPLES</span></span>

### <span data-ttu-id="5d8a2-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5d8a2-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="5d8a2-109">Отмена миграции контейнеров.</span><span class="sxs-lookup"><span data-stu-id="5d8a2-109">Cancel container migration.</span></span>

## <span data-ttu-id="5d8a2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d8a2-110">PARAMETERS</span></span>

### <span data-ttu-id="5d8a2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d8a2-111">-AsJob</span></span>
<span data-ttu-id="5d8a2-112">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="5d8a2-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="5d8a2-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="5d8a2-113">-FarmName</span></span>
<span data-ttu-id="5d8a2-114">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="5d8a2-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8a2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5d8a2-115">-Force</span></span>
<span data-ttu-id="5d8a2-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="5d8a2-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5d8a2-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="5d8a2-117">-JobId</span></span>
<span data-ttu-id="5d8a2-118">Код операции.</span><span class="sxs-lookup"><span data-stu-id="5d8a2-118">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8a2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d8a2-119">-ResourceGroupName</span></span>
<span data-ttu-id="5d8a2-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d8a2-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8a2-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d8a2-121">-Confirm</span></span>
<span data-ttu-id="5d8a2-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5d8a2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d8a2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d8a2-123">-WhatIf</span></span>
<span data-ttu-id="5d8a2-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5d8a2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d8a2-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5d8a2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d8a2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d8a2-126">CommonParameters</span></span>
<span data-ttu-id="5d8a2-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d8a2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d8a2-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d8a2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d8a2-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d8a2-129">INPUTS</span></span>

## <span data-ttu-id="5d8a2-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d8a2-130">OUTPUTS</span></span>

## <span data-ttu-id="5d8a2-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d8a2-131">NOTES</span></span>

## <span data-ttu-id="5d8a2-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d8a2-132">RELATED LINKS</span></span>

