---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 233a6a7c7fd7b2bfe96ed9cc0df6a88bdb9d8747
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558888"
---
# <span data-ttu-id="8b26c-101">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8b26c-101">Get-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="8b26c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b26c-102">SYNOPSIS</span></span>
<span data-ttu-id="8b26c-103">Получает подробные сведения о указанном задании ASR или список последних заданий ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="8b26c-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b26c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b26c-104">SYNTAX</span></span>

### <span data-ttu-id="8b26c-105">ByParam (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8b26c-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b26c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8b26c-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b26c-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="8b26c-107">ByObject</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b26c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b26c-108">DESCRIPTION</span></span>
<span data-ttu-id="8b26c-109">Командлет **Get-AzureRmRecoveryServicesAsrJob** получает задания Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8b26c-109">The **Get-AzureRmRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="8b26c-110">Вы можете использовать этот командлет для просмотра заданий ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="8b26c-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="8b26c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b26c-111">EXAMPLES</span></span>

### <span data-ttu-id="8b26c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b26c-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="8b26c-113">Возвращает все задания в определенном объекте ASR (ссылка на объект ASR, например реплицированный элемент или план восстановления по его ИДЕНТИФИКАТОРу).</span><span class="sxs-lookup"><span data-stu-id="8b26c-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="8b26c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b26c-114">PARAMETERS</span></span>

### <span data-ttu-id="8b26c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b26c-115">-DefaultProfile</span></span>
<span data-ttu-id="8b26c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b26c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b26c-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="8b26c-117">-EndTime</span></span>
<span data-ttu-id="8b26c-118">Указывает время окончания для заданий.</span><span class="sxs-lookup"><span data-stu-id="8b26c-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="8b26c-119">Этот командлет получает все задания, которые были запущены до указанного времени.</span><span class="sxs-lookup"><span data-stu-id="8b26c-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="8b26c-120">Чтобы получить объект **DateTime** для этого параметра, используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="8b26c-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="8b26c-121">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="8b26c-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="8b26c-122">-Job</span><span class="sxs-lookup"><span data-stu-id="8b26c-122">-Job</span></span>
<span data-ttu-id="8b26c-123">Указывает объект задания ASR, для которого требуется получить обновленные сведения.</span><span class="sxs-lookup"><span data-stu-id="8b26c-123">Specifies the ASR job object to get updated details for.</span></span>

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

### <span data-ttu-id="8b26c-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8b26c-124">-Name</span></span>
<span data-ttu-id="8b26c-125">Укажите задание ASR по имени.</span><span class="sxs-lookup"><span data-stu-id="8b26c-125">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="8b26c-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8b26c-126">-StartTime</span></span>
<span data-ttu-id="8b26c-127">Задает время начала для заданий.</span><span class="sxs-lookup"><span data-stu-id="8b26c-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="8b26c-128">Этот командлет получает все задания, которые были запущены по истечении заданного времени.</span><span class="sxs-lookup"><span data-stu-id="8b26c-128">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="8b26c-129">-State</span><span class="sxs-lookup"><span data-stu-id="8b26c-129">-State</span></span>
<span data-ttu-id="8b26c-130">Задает состояние для задания ASR.</span><span class="sxs-lookup"><span data-stu-id="8b26c-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="8b26c-131">Этот командлет получает все задания, которые соответствуют указанному состоянию.</span><span class="sxs-lookup"><span data-stu-id="8b26c-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="8b26c-132">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8b26c-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8b26c-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="8b26c-133">NotStarted</span></span>
- <span data-ttu-id="8b26c-134">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="8b26c-134">InProgress</span></span>
- <span data-ttu-id="8b26c-135">LSP</span><span class="sxs-lookup"><span data-stu-id="8b26c-135">Succeeded</span></span>
- <span data-ttu-id="8b26c-136">Другие</span><span class="sxs-lookup"><span data-stu-id="8b26c-136">Other</span></span>
- <span data-ttu-id="8b26c-137">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="8b26c-137">Failed</span></span>
- <span data-ttu-id="8b26c-138">Отменен</span><span class="sxs-lookup"><span data-stu-id="8b26c-138">Cancelled</span></span>
- <span data-ttu-id="8b26c-139">Остановить</span><span class="sxs-lookup"><span data-stu-id="8b26c-139">Suspended</span></span>

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

### <span data-ttu-id="8b26c-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="8b26c-140">-TargetObjectId</span></span>
<span data-ttu-id="8b26c-141">Указывает идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="8b26c-141">Specifies the ID of the object.</span></span> <span data-ttu-id="8b26c-142">Используется для поиска заданий в указанном объекте.</span><span class="sxs-lookup"><span data-stu-id="8b26c-142">Used to search for jobs on the specified object.</span></span>

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

### <span data-ttu-id="8b26c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b26c-143">CommonParameters</span></span>
<span data-ttu-id="8b26c-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b26c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b26c-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b26c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b26c-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b26c-146">INPUTS</span></span>

### <span data-ttu-id="8b26c-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8b26c-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8b26c-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b26c-148">OUTPUTS</span></span>

### <span data-ttu-id="8b26c-149">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="8b26c-149">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8b26c-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b26c-150">NOTES</span></span>

## <span data-ttu-id="8b26c-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b26c-151">RELATED LINKS</span></span>

[<span data-ttu-id="8b26c-152">Restarting-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8b26c-152">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="8b26c-153">Возобновить — AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8b26c-153">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="8b26c-154">Остановить-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8b26c-154">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
