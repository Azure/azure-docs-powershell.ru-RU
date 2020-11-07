---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 2f219882199010b2765ebd4386691451d74a182d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733654"
---
# <span data-ttu-id="45b86-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="45b86-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="45b86-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45b86-102">SYNOPSIS</span></span>
<span data-ttu-id="45b86-103">Перезапускает задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="45b86-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45b86-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45b86-104">SYNTAX</span></span>

### <span data-ttu-id="45b86-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45b86-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45b86-106">ByName</span><span class="sxs-lookup"><span data-stu-id="45b86-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45b86-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45b86-107">DESCRIPTION</span></span>
<span data-ttu-id="45b86-108">Командлет **restart-AzureRmRecoveryServicesAsrJob** перезапустит задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="45b86-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="45b86-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45b86-109">EXAMPLES</span></span>

### <span data-ttu-id="45b86-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="45b86-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="45b86-111">Перезапускает указанное задание ASR и возвращает обновленный объект задания ASR для задания ASR.</span><span class="sxs-lookup"><span data-stu-id="45b86-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="45b86-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45b86-112">PARAMETERS</span></span>

### <span data-ttu-id="45b86-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45b86-113">-InputObject</span></span>
<span data-ttu-id="45b86-114">Входной объект для командлета: объект задания ASR, соответствующий перезапуску задания ASR</span><span class="sxs-lookup"><span data-stu-id="45b86-114">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>
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

### <span data-ttu-id="45b86-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="45b86-115">-Name</span></span>
<span data-ttu-id="45b86-116">Укажите задание по имени.</span><span class="sxs-lookup"><span data-stu-id="45b86-116">Specify the job by name.</span></span>

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

### <span data-ttu-id="45b86-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45b86-117">-Confirm</span></span>
<span data-ttu-id="45b86-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="45b86-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45b86-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45b86-119">-WhatIf</span></span>
<span data-ttu-id="45b86-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="45b86-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45b86-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="45b86-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45b86-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b86-122">CommonParameters</span></span>
<span data-ttu-id="45b86-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45b86-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b86-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45b86-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b86-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45b86-125">INPUTS</span></span>

### <span data-ttu-id="45b86-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="45b86-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="45b86-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45b86-127">OUTPUTS</span></span>

### <span data-ttu-id="45b86-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="45b86-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="45b86-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="45b86-129">NOTES</span></span>

## <span data-ttu-id="45b86-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45b86-130">RELATED LINKS</span></span>

[<span data-ttu-id="45b86-131">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="45b86-131">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="45b86-132">Возобновить — AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="45b86-132">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="45b86-133">Остановить-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="45b86-133">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
