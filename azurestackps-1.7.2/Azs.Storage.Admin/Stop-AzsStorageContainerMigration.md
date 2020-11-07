---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81bdb6a75e10af30b6febe9bbbf0989933818aec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903281"
---
# <span data-ttu-id="2d7fd-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="2d7fd-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="2d7fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d7fd-102">SYNOPSIS</span></span>
<span data-ttu-id="2d7fd-103">Отмена задания миграции контейнера.</span><span class="sxs-lookup"><span data-stu-id="2d7fd-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="2d7fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d7fd-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d7fd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d7fd-105">DESCRIPTION</span></span>
<span data-ttu-id="2d7fd-106">Отмена задания миграции контейнера.</span><span class="sxs-lookup"><span data-stu-id="2d7fd-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="2d7fd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d7fd-107">EXAMPLES</span></span>

### <span data-ttu-id="2d7fd-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2d7fd-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="2d7fd-109">Отмена миграции контейнеров.</span><span class="sxs-lookup"><span data-stu-id="2d7fd-109">Cancel container migration.</span></span>

## <span data-ttu-id="2d7fd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d7fd-110">PARAMETERS</span></span>

### <span data-ttu-id="2d7fd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d7fd-111">-AsJob</span></span>
<span data-ttu-id="2d7fd-112">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="2d7fd-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="2d7fd-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="2d7fd-113">-FarmName</span></span>
<span data-ttu-id="2d7fd-114">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="2d7fd-114">Farm Id.</span></span>

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

### <span data-ttu-id="2d7fd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2d7fd-115">-Force</span></span>
<span data-ttu-id="2d7fd-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2d7fd-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2d7fd-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="2d7fd-117">-JobId</span></span>
<span data-ttu-id="2d7fd-118">Код операции.</span><span class="sxs-lookup"><span data-stu-id="2d7fd-118">Operation Id.</span></span>

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

### <span data-ttu-id="2d7fd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d7fd-119">-ResourceGroupName</span></span>
<span data-ttu-id="2d7fd-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d7fd-120">Resource group name.</span></span>

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

### <span data-ttu-id="2d7fd-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d7fd-121">-Confirm</span></span>
<span data-ttu-id="2d7fd-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2d7fd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d7fd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d7fd-123">-WhatIf</span></span>
<span data-ttu-id="2d7fd-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2d7fd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d7fd-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2d7fd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d7fd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d7fd-126">CommonParameters</span></span>
<span data-ttu-id="2d7fd-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d7fd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d7fd-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d7fd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d7fd-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d7fd-129">INPUTS</span></span>

## <span data-ttu-id="2d7fd-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d7fd-130">OUTPUTS</span></span>

## <span data-ttu-id="2d7fd-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d7fd-131">NOTES</span></span>

## <span data-ttu-id="2d7fd-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d7fd-132">RELATED LINKS</span></span>

