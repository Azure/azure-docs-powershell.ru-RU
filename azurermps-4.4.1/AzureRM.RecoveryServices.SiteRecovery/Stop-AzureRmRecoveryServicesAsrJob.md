---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: e639e6fc42e440b5088a34ee29e21d324ed7d235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733650"
---
# <span data-ttu-id="0e90c-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0e90c-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="0e90c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e90c-102">SYNOPSIS</span></span>
<span data-ttu-id="0e90c-103">Остановка задания для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="0e90c-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e90c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e90c-104">SYNTAX</span></span>

### <span data-ttu-id="0e90c-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0e90c-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e90c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0e90c-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e90c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e90c-107">DESCRIPTION</span></span>
<span data-ttu-id="0e90c-108">Командлет **Stop-AzureRmRecoveryServicesAsrJob** останавливает указанное задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="0e90c-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="0e90c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e90c-109">EXAMPLES</span></span>

### <span data-ttu-id="0e90c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0e90c-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="0e90c-111">Пытается остановить указанное задание и возвращает обновленный объект задания ASR.</span><span class="sxs-lookup"><span data-stu-id="0e90c-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="0e90c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e90c-112">PARAMETERS</span></span>

### <span data-ttu-id="0e90c-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e90c-113">-InputObject</span></span>
<span data-ttu-id="0e90c-114">Объект input: указание объекта задания ASR, соответствующего заданию ASR, которое должно быть остановлено</span><span class="sxs-lookup"><span data-stu-id="0e90c-114">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e90c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0e90c-115">-Name</span></span>
<span data-ttu-id="0e90c-116">Укажите задание ASR, которое должно быть остановлено с помощью имени задания ASR.</span><span class="sxs-lookup"><span data-stu-id="0e90c-116">Specify the ASR Job to be stopped by the ASR job name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e90c-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e90c-117">-Confirm</span></span>
<span data-ttu-id="0e90c-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0e90c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e90c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e90c-119">-WhatIf</span></span>
<span data-ttu-id="0e90c-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0e90c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e90c-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0e90c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e90c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e90c-122">CommonParameters</span></span>
<span data-ttu-id="0e90c-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e90c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e90c-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e90c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e90c-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e90c-125">INPUTS</span></span>

### <span data-ttu-id="0e90c-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0e90c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0e90c-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e90c-127">OUTPUTS</span></span>

### <span data-ttu-id="0e90c-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0e90c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0e90c-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e90c-129">NOTES</span></span>

## <span data-ttu-id="0e90c-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e90c-130">RELATED LINKS</span></span>

[<span data-ttu-id="0e90c-131">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0e90c-131">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="0e90c-132">Restarting-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0e90c-132">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="0e90c-133">Возобновить — AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0e90c-133">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
