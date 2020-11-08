---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bf583c30d2faff1055debf366a84a0739789467
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076804"
---
# <span data-ttu-id="cd405-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="cd405-101">Start-AzsBackup</span></span>

## <span data-ttu-id="cd405-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd405-102">SYNOPSIS</span></span>
<span data-ttu-id="cd405-103">Создание резервной копии определенного местоположения.</span><span class="sxs-lookup"><span data-stu-id="cd405-103">Back up a specific location.</span></span>

## <span data-ttu-id="cd405-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd405-104">SYNTAX</span></span>

### <span data-ttu-id="cd405-105">CreateBackup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cd405-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd405-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="cd405-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd405-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd405-107">DESCRIPTION</span></span>
<span data-ttu-id="cd405-108">Создание резервной копии определенного местоположения.</span><span class="sxs-lookup"><span data-stu-id="cd405-108">Back up a specific location.</span></span>

## <span data-ttu-id="cd405-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd405-109">EXAMPLES</span></span>

### <span data-ttu-id="cd405-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cd405-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="cd405-111">Начните создавать резервные копии стеков Azure.</span><span class="sxs-lookup"><span data-stu-id="cd405-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="cd405-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd405-112">PARAMETERS</span></span>

### <span data-ttu-id="cd405-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd405-113">-AsJob</span></span>
<span data-ttu-id="cd405-114">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="cd405-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="cd405-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cd405-115">-Force</span></span>
<span data-ttu-id="cd405-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="cd405-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cd405-117">-Location</span><span class="sxs-lookup"><span data-stu-id="cd405-117">-Location</span></span>
<span data-ttu-id="cd405-118">Имя расположения резервной копии.</span><span class="sxs-lookup"><span data-stu-id="cd405-118">Name of the backup location.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd405-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd405-119">-ResourceGroupName</span></span>
<span data-ttu-id="cd405-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cd405-120">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd405-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd405-121">-ResourceId</span></span>
<span data-ttu-id="cd405-122">{Определение ИД ресурса заполнения}}</span><span class="sxs-lookup"><span data-stu-id="cd405-122">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup_FromResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd405-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd405-123">-Confirm</span></span>
<span data-ttu-id="cd405-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cd405-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd405-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd405-125">-WhatIf</span></span>
<span data-ttu-id="cd405-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cd405-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd405-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cd405-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd405-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd405-128">CommonParameters</span></span>
<span data-ttu-id="cd405-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd405-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd405-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd405-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd405-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd405-131">INPUTS</span></span>

## <span data-ttu-id="cd405-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd405-132">OUTPUTS</span></span>

### <span data-ttu-id="cd405-133">Microsoft. AzureStack. Management. Backup. admin. Models. LongRunningOperationStatus</span><span class="sxs-lookup"><span data-stu-id="cd405-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="cd405-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd405-134">NOTES</span></span>

## <span data-ttu-id="cd405-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd405-135">RELATED LINKS</span></span>

