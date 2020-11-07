---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: b71c9a5da3c89916b18bdb5446f311e3d71615bf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911830"
---
# <span data-ttu-id="2e828-101">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2e828-101">Get-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="2e828-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2e828-102">SYNOPSIS</span></span>
<span data-ttu-id="2e828-103">Получает подробные сведения о указанном задании ASR или список последних заданий ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="2e828-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="2e828-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2e828-104">SYNTAX</span></span>

### <span data-ttu-id="2e828-105">ByParam (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2e828-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e828-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2e828-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e828-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="2e828-107">ByObject</span></span>
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e828-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e828-108">DESCRIPTION</span></span>
<span data-ttu-id="2e828-109">Командлет **Get-AzRecoveryServicesAsrJob** получает задания Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2e828-109">The **Get-AzRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="2e828-110">Вы можете использовать этот командлет для просмотра заданий ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="2e828-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="2e828-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2e828-111">EXAMPLES</span></span>

### <span data-ttu-id="2e828-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2e828-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="2e828-113">Возвращает все задания в определенном объекте ASR (ссылка на объект ASR, например реплицированный элемент или план восстановления по его ИДЕНТИФИКАТОРу).</span><span class="sxs-lookup"><span data-stu-id="2e828-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="2e828-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2e828-114">PARAMETERS</span></span>

### <span data-ttu-id="2e828-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e828-115">-DefaultProfile</span></span>
<span data-ttu-id="2e828-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2e828-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2e828-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="2e828-117">-EndTime</span></span>
<span data-ttu-id="2e828-118">Указывает время окончания для заданий.</span><span class="sxs-lookup"><span data-stu-id="2e828-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="2e828-119">Этот командлет получает все задания, которые были запущены до указанного времени.</span><span class="sxs-lookup"><span data-stu-id="2e828-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="2e828-120">Чтобы получить объект **DateTime** для этого параметра, используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="2e828-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="2e828-121">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="2e828-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="2e828-122">-Job</span><span class="sxs-lookup"><span data-stu-id="2e828-122">-Job</span></span>
<span data-ttu-id="2e828-123">Указывает объект задания ASR, для которого требуется получить обновленные сведения.</span><span class="sxs-lookup"><span data-stu-id="2e828-123">Specifies the ASR job object to get updated details for.</span></span>

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

### <span data-ttu-id="2e828-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2e828-124">-Name</span></span>
<span data-ttu-id="2e828-125">Укажите задание ASR по имени.</span><span class="sxs-lookup"><span data-stu-id="2e828-125">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="2e828-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2e828-126">-StartTime</span></span>
<span data-ttu-id="2e828-127">Задает время начала для заданий.</span><span class="sxs-lookup"><span data-stu-id="2e828-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="2e828-128">Этот командлет получает все задания, которые были запущены по истечении заданного времени.</span><span class="sxs-lookup"><span data-stu-id="2e828-128">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="2e828-129">-State</span><span class="sxs-lookup"><span data-stu-id="2e828-129">-State</span></span>
<span data-ttu-id="2e828-130">Задает состояние для задания ASR.</span><span class="sxs-lookup"><span data-stu-id="2e828-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="2e828-131">Этот командлет получает все задания, которые соответствуют указанному состоянию.</span><span class="sxs-lookup"><span data-stu-id="2e828-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="2e828-132">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2e828-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2e828-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="2e828-133">NotStarted</span></span>
- <span data-ttu-id="2e828-134">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="2e828-134">InProgress</span></span>
- <span data-ttu-id="2e828-135">LSP</span><span class="sxs-lookup"><span data-stu-id="2e828-135">Succeeded</span></span>
- <span data-ttu-id="2e828-136">Другие</span><span class="sxs-lookup"><span data-stu-id="2e828-136">Other</span></span>
- <span data-ttu-id="2e828-137">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="2e828-137">Failed</span></span>
- <span data-ttu-id="2e828-138">Отменен</span><span class="sxs-lookup"><span data-stu-id="2e828-138">Cancelled</span></span>
- <span data-ttu-id="2e828-139">Остановить</span><span class="sxs-lookup"><span data-stu-id="2e828-139">Suspended</span></span>

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

### <span data-ttu-id="2e828-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="2e828-140">-TargetObjectId</span></span>
<span data-ttu-id="2e828-141">Указывает идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="2e828-141">Specifies the ID of the object.</span></span> <span data-ttu-id="2e828-142">Используется для поиска заданий в указанном объекте.</span><span class="sxs-lookup"><span data-stu-id="2e828-142">Used to search for jobs on the specified object.</span></span>

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

### <span data-ttu-id="2e828-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e828-143">CommonParameters</span></span>
<span data-ttu-id="2e828-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2e828-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e828-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e828-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e828-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2e828-146">INPUTS</span></span>

### <span data-ttu-id="2e828-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2e828-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2e828-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e828-148">OUTPUTS</span></span>

### <span data-ttu-id="2e828-149">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2e828-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2e828-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="2e828-150">NOTES</span></span>

## <span data-ttu-id="2e828-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e828-151">RELATED LINKS</span></span>

[<span data-ttu-id="2e828-152">Restarting-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2e828-152">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="2e828-153">Возобновить — AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2e828-153">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="2e828-154">Остановить-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2e828-154">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
