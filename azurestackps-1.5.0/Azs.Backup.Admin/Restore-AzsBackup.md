---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 385947ead1039103933cb7e752dc5dee768b388a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555963"
---
# <span data-ttu-id="ef411-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="ef411-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="ef411-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef411-102">SYNOPSIS</span></span>
<span data-ttu-id="ef411-103">Восстановите резервную копию.</span><span class="sxs-lookup"><span data-stu-id="ef411-103">Restore a backup.</span></span>

## <span data-ttu-id="ef411-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef411-104">SYNTAX</span></span>

### <span data-ttu-id="ef411-105">Backups_Restore (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ef411-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef411-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef411-106">ResourceId</span></span>
```
Restore-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef411-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef411-107">DESCRIPTION</span></span>
<span data-ttu-id="ef411-108">Восстановите резервную копию.</span><span class="sxs-lookup"><span data-stu-id="ef411-108">Restore a backup.</span></span>

## <span data-ttu-id="ef411-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef411-109">EXAMPLES</span></span>

### <span data-ttu-id="ef411-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ef411-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsBackup -Backup 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e
```

<span data-ttu-id="ef411-111">Восстановление из резервной копии стека Azure.</span><span class="sxs-lookup"><span data-stu-id="ef411-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="ef411-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef411-112">PARAMETERS</span></span>

### <span data-ttu-id="ef411-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef411-113">-AsJob</span></span>
<span data-ttu-id="ef411-114">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="ef411-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="ef411-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ef411-115">-Force</span></span>
<span data-ttu-id="ef411-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ef411-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ef411-117">-Location</span><span class="sxs-lookup"><span data-stu-id="ef411-117">-Location</span></span>
<span data-ttu-id="ef411-118">Имя расположения для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="ef411-118">Name of location to backup.</span></span>

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

### <span data-ttu-id="ef411-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ef411-119">-Name</span></span>
<span data-ttu-id="ef411-120">Имя резервной копии.</span><span class="sxs-lookup"><span data-stu-id="ef411-120">Name of the backup.</span></span>

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

### <span data-ttu-id="ef411-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef411-121">-ResourceGroupName</span></span>
<span data-ttu-id="ef411-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef411-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="ef411-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef411-123">-ResourceId</span></span>
<span data-ttu-id="ef411-124">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="ef411-124">The resource id.</span></span>

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

### <span data-ttu-id="ef411-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef411-125">-Confirm</span></span>
<span data-ttu-id="ef411-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ef411-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef411-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef411-127">-WhatIf</span></span>
<span data-ttu-id="ef411-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ef411-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef411-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ef411-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef411-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef411-130">CommonParameters</span></span>
<span data-ttu-id="ef411-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef411-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef411-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef411-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef411-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef411-133">INPUTS</span></span>

## <span data-ttu-id="ef411-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef411-134">OUTPUTS</span></span>

## <span data-ttu-id="ef411-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef411-135">NOTES</span></span>

## <span data-ttu-id="ef411-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef411-136">RELATED LINKS</span></span>

