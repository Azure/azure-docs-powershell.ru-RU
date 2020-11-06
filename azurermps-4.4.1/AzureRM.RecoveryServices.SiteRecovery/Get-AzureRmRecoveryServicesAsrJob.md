---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: afef81ad904ccd5bf53f0b2a09bb10511e71fca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568698"
---
# <span data-ttu-id="2dcc0-101">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2dcc0-101">Get-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="2dcc0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2dcc0-102">SYNOPSIS</span></span>
<span data-ttu-id="2dcc0-103">Получает подробные сведения о указанном задании ASR или список последних заданий ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="2dcc0-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dcc0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2dcc0-104">SYNTAX</span></span>

### <span data-ttu-id="2dcc0-105">ByParam (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2dcc0-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [<CommonParameters>]
```

### <span data-ttu-id="2dcc0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2dcc0-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="2dcc0-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="2dcc0-107">ByObject</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [<CommonParameters>]
```

## <span data-ttu-id="2dcc0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dcc0-108">DESCRIPTION</span></span>
<span data-ttu-id="2dcc0-109">Командлет **Get-AzureRmRecoveryServicesAsrJob** получает задания Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2dcc0-109">The **Get-AzureRmRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="2dcc0-110">Вы можете использовать этот командлет для просмотра заданий ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="2dcc0-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="2dcc0-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2dcc0-111">EXAMPLES</span></span>

### <span data-ttu-id="2dcc0-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2dcc0-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="2dcc0-113">Возвращает все задания в определенном объекте ASR (ссылка на объект ASR, например реплицированный элемент или план восстановления по его ИДЕНТИФИКАТОРу).</span><span class="sxs-lookup"><span data-stu-id="2dcc0-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="2dcc0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2dcc0-114">PARAMETERS</span></span>

### <span data-ttu-id="2dcc0-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="2dcc0-115">-EndTime</span></span>
<span data-ttu-id="2dcc0-116">Указывает время окончания для заданий.</span><span class="sxs-lookup"><span data-stu-id="2dcc0-116">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="2dcc0-117">Этот командлет получает все задания, которые были запущены до указанного времени.</span><span class="sxs-lookup"><span data-stu-id="2dcc0-117">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="2dcc0-118">Чтобы получить объект **DateTime** для этого параметра, используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="2dcc0-118">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="2dcc0-119">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="2dcc0-119">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dcc0-120">-Job</span><span class="sxs-lookup"><span data-stu-id="2dcc0-120">-Job</span></span>
<span data-ttu-id="2dcc0-121">Указывает объект задания ASR, для которого требуется получить обновленные сведения.</span><span class="sxs-lookup"><span data-stu-id="2dcc0-121">Specifies the ASR job object to get updated details for.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dcc0-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2dcc0-122">-Name</span></span>
<span data-ttu-id="2dcc0-123">Укажите задание ASR по имени.</span><span class="sxs-lookup"><span data-stu-id="2dcc0-123">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="2dcc0-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2dcc0-124">-StartTime</span></span>
<span data-ttu-id="2dcc0-125">Задает время начала для заданий.</span><span class="sxs-lookup"><span data-stu-id="2dcc0-125">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="2dcc0-126">Этот командлет получает все задания, которые были запущены по истечении заданного времени.</span><span class="sxs-lookup"><span data-stu-id="2dcc0-126">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dcc0-127">-State</span><span class="sxs-lookup"><span data-stu-id="2dcc0-127">-State</span></span>
<span data-ttu-id="2dcc0-128">Задает состояние для задания ASR.</span><span class="sxs-lookup"><span data-stu-id="2dcc0-128">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="2dcc0-129">Этот командлет получает все задания, которые соответствуют указанному состоянию.</span><span class="sxs-lookup"><span data-stu-id="2dcc0-129">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="2dcc0-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2dcc0-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2dcc0-131">NotStarted</span><span class="sxs-lookup"><span data-stu-id="2dcc0-131">NotStarted</span></span>
- <span data-ttu-id="2dcc0-132">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="2dcc0-132">InProgress</span></span>
- <span data-ttu-id="2dcc0-133">LSP</span><span class="sxs-lookup"><span data-stu-id="2dcc0-133">Succeeded</span></span>
- <span data-ttu-id="2dcc0-134">Другие</span><span class="sxs-lookup"><span data-stu-id="2dcc0-134">Other</span></span>
- <span data-ttu-id="2dcc0-135">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="2dcc0-135">Failed</span></span>
- <span data-ttu-id="2dcc0-136">Отменен</span><span class="sxs-lookup"><span data-stu-id="2dcc0-136">Cancelled</span></span>
- <span data-ttu-id="2dcc0-137">Остановить</span><span class="sxs-lookup"><span data-stu-id="2dcc0-137">Suspended</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dcc0-138">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="2dcc0-138">-TargetObjectId</span></span>
<span data-ttu-id="2dcc0-139">Указывает идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="2dcc0-139">Specifies the ID of the object.</span></span> <span data-ttu-id="2dcc0-140">Используется для поиска заданий в указанном объекте.</span><span class="sxs-lookup"><span data-stu-id="2dcc0-140">Used to search for jobs on the specified object.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dcc0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dcc0-141">CommonParameters</span></span>
<span data-ttu-id="2dcc0-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2dcc0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dcc0-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dcc0-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dcc0-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2dcc0-144">INPUTS</span></span>

### <span data-ttu-id="2dcc0-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2dcc0-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2dcc0-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dcc0-146">OUTPUTS</span></span>

### <span data-ttu-id="2dcc0-147">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="2dcc0-147">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2dcc0-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="2dcc0-148">NOTES</span></span>

## <span data-ttu-id="2dcc0-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2dcc0-149">RELATED LINKS</span></span>

[<span data-ttu-id="2dcc0-150">Restarting-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2dcc0-150">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="2dcc0-151">Возобновить — AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2dcc0-151">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="2dcc0-152">Остановить-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2dcc0-152">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
