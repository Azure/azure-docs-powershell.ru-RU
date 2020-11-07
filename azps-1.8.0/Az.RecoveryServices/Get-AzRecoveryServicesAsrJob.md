---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 85479392a34e81395d3f00e3ef3891772a2dcbec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729743"
---
# <span data-ttu-id="53782-101">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="53782-101">Get-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="53782-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="53782-102">SYNOPSIS</span></span>
<span data-ttu-id="53782-103">Получает подробные сведения о указанном задании ASR или список последних заданий ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="53782-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="53782-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="53782-104">SYNTAX</span></span>

### <span data-ttu-id="53782-105">ByParam (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="53782-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53782-106">ByName</span><span class="sxs-lookup"><span data-stu-id="53782-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53782-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="53782-107">ByObject</span></span>
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53782-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53782-108">DESCRIPTION</span></span>
<span data-ttu-id="53782-109">Командлет **Get-AzRecoveryServicesAsrJob** получает задания Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="53782-109">The **Get-AzRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="53782-110">Вы можете использовать этот командлет для просмотра заданий ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="53782-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="53782-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="53782-111">EXAMPLES</span></span>

### <span data-ttu-id="53782-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="53782-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="53782-113">Возвращает все задания в определенном объекте ASR (ссылка на объект ASR, например реплицированный элемент или план восстановления по его ИДЕНТИФИКАТОРу).</span><span class="sxs-lookup"><span data-stu-id="53782-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="53782-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="53782-114">PARAMETERS</span></span>

### <span data-ttu-id="53782-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53782-115">-DefaultProfile</span></span>
<span data-ttu-id="53782-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53782-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53782-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="53782-117">-EndTime</span></span>
<span data-ttu-id="53782-118">Указывает время окончания для заданий.</span><span class="sxs-lookup"><span data-stu-id="53782-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="53782-119">Этот командлет получает все задания, которые были запущены до указанного времени.</span><span class="sxs-lookup"><span data-stu-id="53782-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="53782-120">Чтобы получить объект **DateTime** для этого параметра, используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="53782-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="53782-121">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="53782-121">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53782-122">-Job</span><span class="sxs-lookup"><span data-stu-id="53782-122">-Job</span></span>
<span data-ttu-id="53782-123">Указывает объект задания ASR, для которого требуется получить обновленные сведения.</span><span class="sxs-lookup"><span data-stu-id="53782-123">Specifies the ASR job object to get updated details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53782-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="53782-124">-Name</span></span>
<span data-ttu-id="53782-125">Укажите задание ASR по имени.</span><span class="sxs-lookup"><span data-stu-id="53782-125">Specify the ASR job by name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53782-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="53782-126">-StartTime</span></span>
<span data-ttu-id="53782-127">Задает время начала для заданий.</span><span class="sxs-lookup"><span data-stu-id="53782-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="53782-128">Этот командлет получает все задания, которые были запущены по истечении заданного времени.</span><span class="sxs-lookup"><span data-stu-id="53782-128">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53782-129">-State</span><span class="sxs-lookup"><span data-stu-id="53782-129">-State</span></span>
<span data-ttu-id="53782-130">Задает состояние для задания ASR.</span><span class="sxs-lookup"><span data-stu-id="53782-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="53782-131">Этот командлет получает все задания, которые соответствуют указанному состоянию.</span><span class="sxs-lookup"><span data-stu-id="53782-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="53782-132">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="53782-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="53782-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="53782-133">NotStarted</span></span>
- <span data-ttu-id="53782-134">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="53782-134">InProgress</span></span>
- <span data-ttu-id="53782-135">LSP</span><span class="sxs-lookup"><span data-stu-id="53782-135">Succeeded</span></span>
- <span data-ttu-id="53782-136">Другие</span><span class="sxs-lookup"><span data-stu-id="53782-136">Other</span></span>
- <span data-ttu-id="53782-137">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="53782-137">Failed</span></span>
- <span data-ttu-id="53782-138">Отменен</span><span class="sxs-lookup"><span data-stu-id="53782-138">Cancelled</span></span>
- <span data-ttu-id="53782-139">Остановить</span><span class="sxs-lookup"><span data-stu-id="53782-139">Suspended</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53782-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="53782-140">-TargetObjectId</span></span>
<span data-ttu-id="53782-141">Указывает идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="53782-141">Specifies the ID of the object.</span></span> <span data-ttu-id="53782-142">Используется для поиска заданий в указанном объекте.</span><span class="sxs-lookup"><span data-stu-id="53782-142">Used to search for jobs on the specified object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53782-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53782-143">CommonParameters</span></span>
<span data-ttu-id="53782-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="53782-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53782-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53782-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53782-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="53782-146">INPUTS</span></span>

### <span data-ttu-id="53782-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="53782-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="53782-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="53782-148">OUTPUTS</span></span>

### <span data-ttu-id="53782-149">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="53782-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="53782-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="53782-150">NOTES</span></span>

## <span data-ttu-id="53782-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53782-151">RELATED LINKS</span></span>

[<span data-ttu-id="53782-152">Restarting-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="53782-152">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="53782-153">Возобновить — AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="53782-153">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="53782-154">Остановить-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="53782-154">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
