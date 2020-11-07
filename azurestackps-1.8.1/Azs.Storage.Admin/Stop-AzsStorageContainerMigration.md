---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8c9a27b1722c1c7f08d9daeab0205dd20d9ba8b9
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908686"
---
# <span data-ttu-id="cc617-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="cc617-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="cc617-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cc617-102">SYNOPSIS</span></span>
<span data-ttu-id="cc617-103">Отмена задания миграции контейнера.</span><span class="sxs-lookup"><span data-stu-id="cc617-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="cc617-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cc617-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc617-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc617-105">DESCRIPTION</span></span>
<span data-ttu-id="cc617-106">Отмена задания миграции контейнера.</span><span class="sxs-lookup"><span data-stu-id="cc617-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="cc617-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cc617-107">EXAMPLES</span></span>

### <span data-ttu-id="cc617-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="cc617-108">EXAMPLE 1</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="cc617-109">Отмена миграции контейнеров.</span><span class="sxs-lookup"><span data-stu-id="cc617-109">Cancel container migration.</span></span>

## <span data-ttu-id="cc617-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cc617-110">PARAMETERS</span></span>

### <span data-ttu-id="cc617-111">-JobId</span><span class="sxs-lookup"><span data-stu-id="cc617-111">-JobId</span></span>
<span data-ttu-id="cc617-112">Код операции.</span><span class="sxs-lookup"><span data-stu-id="cc617-112">Operation Id.</span></span>

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

### <span data-ttu-id="cc617-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc617-113">-ResourceGroupName</span></span>
<span data-ttu-id="cc617-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc617-114">Resource group name.</span></span>

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

### <span data-ttu-id="cc617-115">-FarmName</span><span class="sxs-lookup"><span data-stu-id="cc617-115">-FarmName</span></span>
<span data-ttu-id="cc617-116">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="cc617-116">Farm Id.</span></span>

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

### <span data-ttu-id="cc617-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc617-117">-AsJob</span></span>
<span data-ttu-id="cc617-118">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="cc617-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="cc617-119">-Force</span><span class="sxs-lookup"><span data-stu-id="cc617-119">-Force</span></span>
<span data-ttu-id="cc617-120">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="cc617-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cc617-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc617-121">-WhatIf</span></span>
<span data-ttu-id="cc617-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cc617-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc617-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cc617-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc617-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc617-124">-Confirm</span></span>
<span data-ttu-id="cc617-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cc617-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc617-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc617-126">CommonParameters</span></span>
<span data-ttu-id="cc617-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cc617-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc617-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc617-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc617-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cc617-129">INPUTS</span></span>

## <span data-ttu-id="cc617-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc617-130">OUTPUTS</span></span>

## <span data-ttu-id="cc617-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="cc617-131">NOTES</span></span>

## <span data-ttu-id="cc617-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc617-132">RELATED LINKS</span></span>
