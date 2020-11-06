---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c7dff6c2d9c191d852420ab2c2017a0b9d1cf8d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556156"
---
# <span data-ttu-id="6ea9d-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="6ea9d-101">Start-AzsBackup</span></span>

## <span data-ttu-id="6ea9d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ea9d-102">SYNOPSIS</span></span>
<span data-ttu-id="6ea9d-103">Создание резервной копии определенного местоположения.</span><span class="sxs-lookup"><span data-stu-id="6ea9d-103">Back up a specific location.</span></span>

## <span data-ttu-id="6ea9d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ea9d-104">SYNTAX</span></span>

### <span data-ttu-id="6ea9d-105">CreateBackup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6ea9d-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ea9d-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="6ea9d-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ea9d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ea9d-107">DESCRIPTION</span></span>
<span data-ttu-id="6ea9d-108">Создание резервной копии определенного местоположения.</span><span class="sxs-lookup"><span data-stu-id="6ea9d-108">Back up a specific location.</span></span>

## <span data-ttu-id="6ea9d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ea9d-109">EXAMPLES</span></span>

### <span data-ttu-id="6ea9d-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6ea9d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="6ea9d-111">Начните создавать резервные копии стеков Azure.</span><span class="sxs-lookup"><span data-stu-id="6ea9d-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="6ea9d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ea9d-112">PARAMETERS</span></span>

### <span data-ttu-id="6ea9d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ea9d-113">-AsJob</span></span>
<span data-ttu-id="6ea9d-114">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="6ea9d-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="6ea9d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6ea9d-115">-Force</span></span>
<span data-ttu-id="6ea9d-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="6ea9d-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6ea9d-117">-Location</span><span class="sxs-lookup"><span data-stu-id="6ea9d-117">-Location</span></span>
<span data-ttu-id="6ea9d-118">Имя расположения резервной копии.</span><span class="sxs-lookup"><span data-stu-id="6ea9d-118">Name of the backup location.</span></span>

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

### <span data-ttu-id="6ea9d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ea9d-119">-ResourceGroupName</span></span>
<span data-ttu-id="6ea9d-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ea9d-120">Name of the resource group.</span></span>

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

### <span data-ttu-id="6ea9d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ea9d-121">-ResourceId</span></span>
<span data-ttu-id="6ea9d-122">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="6ea9d-122">The resource id.</span></span>

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

### <span data-ttu-id="6ea9d-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ea9d-123">-Confirm</span></span>
<span data-ttu-id="6ea9d-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6ea9d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ea9d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ea9d-125">-WhatIf</span></span>
<span data-ttu-id="6ea9d-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6ea9d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ea9d-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6ea9d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ea9d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ea9d-128">CommonParameters</span></span>
<span data-ttu-id="6ea9d-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ea9d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ea9d-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ea9d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ea9d-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ea9d-131">INPUTS</span></span>

## <span data-ttu-id="6ea9d-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ea9d-132">OUTPUTS</span></span>

### <span data-ttu-id="6ea9d-133">Microsoft. AzureStack. Management. Backup. admin. Models. LongRunningOperationStatus</span><span class="sxs-lookup"><span data-stu-id="6ea9d-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="6ea9d-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ea9d-134">NOTES</span></span>

## <span data-ttu-id="6ea9d-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ea9d-135">RELATED LINKS</span></span>

