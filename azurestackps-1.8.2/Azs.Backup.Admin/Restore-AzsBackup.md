---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 573a47b3684020817130e1d41c764abef717de0a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076805"
---
# <span data-ttu-id="2771a-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="2771a-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="2771a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2771a-102">SYNOPSIS</span></span>
<span data-ttu-id="2771a-103">Восстановите резервную копию.</span><span class="sxs-lookup"><span data-stu-id="2771a-103">Restore a backup.</span></span>

## <span data-ttu-id="2771a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2771a-104">SYNTAX</span></span>

### <span data-ttu-id="2771a-105">Backups_Restore (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2771a-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2771a-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2771a-106">ResourceId</span></span>
```
Restore-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2771a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2771a-107">DESCRIPTION</span></span>
<span data-ttu-id="2771a-108">Восстановите резервную копию.</span><span class="sxs-lookup"><span data-stu-id="2771a-108">Restore a backup.</span></span>

## <span data-ttu-id="2771a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2771a-109">EXAMPLES</span></span>

### <span data-ttu-id="2771a-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2771a-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsBackup -Backup 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e
```

<span data-ttu-id="2771a-111">Восстановление из резервной копии стека Azure.</span><span class="sxs-lookup"><span data-stu-id="2771a-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="2771a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2771a-112">PARAMETERS</span></span>

### <span data-ttu-id="2771a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2771a-113">-AsJob</span></span>
<span data-ttu-id="2771a-114">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="2771a-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="2771a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2771a-115">-Force</span></span>
<span data-ttu-id="2771a-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2771a-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2771a-117">-Location</span><span class="sxs-lookup"><span data-stu-id="2771a-117">-Location</span></span>
<span data-ttu-id="2771a-118">Имя расположения для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="2771a-118">Name of location to backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2771a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2771a-119">-Name</span></span>
<span data-ttu-id="2771a-120">Имя резервной копии.</span><span class="sxs-lookup"><span data-stu-id="2771a-120">Name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2771a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2771a-121">-ResourceGroupName</span></span>
<span data-ttu-id="2771a-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2771a-122">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2771a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2771a-123">-ResourceId</span></span>
<span data-ttu-id="2771a-124">{Определение ИД ресурса заполнения}}</span><span class="sxs-lookup"><span data-stu-id="2771a-124">{{Fill ResourceId Description}}</span></span>

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

### <span data-ttu-id="2771a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2771a-125">-Confirm</span></span>
<span data-ttu-id="2771a-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2771a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2771a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2771a-127">-WhatIf</span></span>
<span data-ttu-id="2771a-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2771a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2771a-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2771a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2771a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2771a-130">CommonParameters</span></span>
<span data-ttu-id="2771a-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2771a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2771a-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2771a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2771a-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2771a-133">INPUTS</span></span>

## <span data-ttu-id="2771a-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2771a-134">OUTPUTS</span></span>

## <span data-ttu-id="2771a-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="2771a-135">NOTES</span></span>

## <span data-ttu-id="2771a-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2771a-136">RELATED LINKS</span></span>

