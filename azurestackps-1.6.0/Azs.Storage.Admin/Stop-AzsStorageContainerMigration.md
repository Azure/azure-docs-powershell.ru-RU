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
ms.locfileid: "93555176"
---
# <span data-ttu-id="24397-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="24397-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="24397-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="24397-102">SYNOPSIS</span></span>
<span data-ttu-id="24397-103">Отмена задания миграции контейнера.</span><span class="sxs-lookup"><span data-stu-id="24397-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="24397-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="24397-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24397-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24397-105">DESCRIPTION</span></span>
<span data-ttu-id="24397-106">Отмена задания миграции контейнера.</span><span class="sxs-lookup"><span data-stu-id="24397-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="24397-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="24397-107">EXAMPLES</span></span>

### <span data-ttu-id="24397-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="24397-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="24397-109">Отмена миграции контейнеров.</span><span class="sxs-lookup"><span data-stu-id="24397-109">Cancel container migration.</span></span>

## <span data-ttu-id="24397-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="24397-110">PARAMETERS</span></span>

### <span data-ttu-id="24397-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24397-111">-AsJob</span></span>
<span data-ttu-id="24397-112">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="24397-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="24397-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="24397-113">-FarmName</span></span>
<span data-ttu-id="24397-114">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="24397-114">Farm Id.</span></span>

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

### <span data-ttu-id="24397-115">-Force</span><span class="sxs-lookup"><span data-stu-id="24397-115">-Force</span></span>
<span data-ttu-id="24397-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="24397-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="24397-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="24397-117">-JobId</span></span>
<span data-ttu-id="24397-118">Код операции.</span><span class="sxs-lookup"><span data-stu-id="24397-118">Operation Id.</span></span>

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

### <span data-ttu-id="24397-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24397-119">-ResourceGroupName</span></span>
<span data-ttu-id="24397-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="24397-120">Resource group name.</span></span>

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

### <span data-ttu-id="24397-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24397-121">-Confirm</span></span>
<span data-ttu-id="24397-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="24397-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24397-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24397-123">-WhatIf</span></span>
<span data-ttu-id="24397-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="24397-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24397-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="24397-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24397-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24397-126">CommonParameters</span></span>
<span data-ttu-id="24397-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="24397-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24397-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24397-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24397-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="24397-129">INPUTS</span></span>

## <span data-ttu-id="24397-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="24397-130">OUTPUTS</span></span>

## <span data-ttu-id="24397-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="24397-131">NOTES</span></span>

## <span data-ttu-id="24397-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24397-132">RELATED LINKS</span></span>

