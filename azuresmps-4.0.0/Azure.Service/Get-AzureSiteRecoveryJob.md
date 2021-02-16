---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2957C0DE-3A2F-4337-A778-2B95654972E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a7c99e2ce307d700e43094ffa9be47e5449acc0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411659"
---
# <span data-ttu-id="9ee47-101">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9ee47-101">Get-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="9ee47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ee47-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee47-103">Получает сведения об операции для хранилища восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="9ee47-103">Gets the operation information for a Site Recovery vault.</span></span>

## <span data-ttu-id="9ee47-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9ee47-104">SYNTAX</span></span>

### <span data-ttu-id="9ee47-105">ByParam (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ee47-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9ee47-106">ById</span><span class="sxs-lookup"><span data-stu-id="9ee47-106">ById</span></span>
```
Get-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9ee47-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="9ee47-107">ByObject</span></span>
```
Get-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9ee47-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ee47-108">DESCRIPTION</span></span>
<span data-ttu-id="9ee47-109">Для получения заданий восстановления сайта Azure к работе **возвращается cmdlet Get-AzureSiteRecoveryJob.**</span><span class="sxs-lookup"><span data-stu-id="9ee47-109">The **Get-AzureSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="9ee47-110">С помощью этого cmdlet можно просмотреть сведения об операциях для текущего хранилища восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="9ee47-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="9ee47-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9ee47-111">EXAMPLES</span></span>

### <span data-ttu-id="9ee47-112">Пример 1. Задание задания с указанием ИД</span><span class="sxs-lookup"><span data-stu-id="9ee47-112">Example 1: Get a job by specifying an ID</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -Id "033785cc-9f72-4f07-8e78-e4d1e942a7ae" 
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="9ee47-113">Эта команда получает задание восстановления сайта Azure с указанным ИД.</span><span class="sxs-lookup"><span data-stu-id="9ee47-113">This command gets the  Azure Site Recovery job that has the specified ID.</span></span>

### <span data-ttu-id="9ee47-114">Пример 2. Получает задание по времени</span><span class="sxs-lookup"><span data-stu-id="9ee47-114">Example 2: Gets a job based on time</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -StartTime "20-02-2015 01:00:00" -EndTime "21-02-2015 01:00:00"
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="9ee47-115">Эта команда получает задания восстановления сайта, которые выпадают между указанным временем начала и временем окончания.</span><span class="sxs-lookup"><span data-stu-id="9ee47-115">This command gets Site Recovery jobs that fall between the specified start time and end time.</span></span>

## <span data-ttu-id="9ee47-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ee47-116">PARAMETERS</span></span>

### <span data-ttu-id="9ee47-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="9ee47-117">-EndTime</span></span>
<span data-ttu-id="9ee47-118">Время окончания заданий.</span><span class="sxs-lookup"><span data-stu-id="9ee47-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="9ee47-119">Этот cmdlet получает все задания, которые были начданы раньше указанного времени.</span><span class="sxs-lookup"><span data-stu-id="9ee47-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="9ee47-120">Чтобы получить объект **даты и времени,** используйте cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="9ee47-120">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="9ee47-121">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9ee47-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="9ee47-122">-Id</span><span class="sxs-lookup"><span data-stu-id="9ee47-122">-Id</span></span>
<span data-ttu-id="9ee47-123">Определяет ИД задания, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="9ee47-123">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee47-124">-Job</span><span class="sxs-lookup"><span data-stu-id="9ee47-124">-Job</span></span>
<span data-ttu-id="9ee47-125">Задание, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="9ee47-125">Specifies a job to get.</span></span>

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

### <span data-ttu-id="9ee47-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="9ee47-126">-Profile</span></span>
<span data-ttu-id="9ee47-127">Определяет профиль Azure, для которого читается этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ee47-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9ee47-128">Если не указать профиль, этот cmdlet будет читать данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9ee47-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee47-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9ee47-129">-StartTime</span></span>
<span data-ttu-id="9ee47-130">Время начала заданий.</span><span class="sxs-lookup"><span data-stu-id="9ee47-130">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="9ee47-131">Этот cmdlet возвращает все задания, которые начинались после заданного времени.</span><span class="sxs-lookup"><span data-stu-id="9ee47-131">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="9ee47-132">-State</span><span class="sxs-lookup"><span data-stu-id="9ee47-132">-State</span></span>
<span data-ttu-id="9ee47-133">Определяет состояние входных данных для задания восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="9ee47-133">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="9ee47-134">Этот командлет возвращает все задания, которые соответствуют указанному штату.</span><span class="sxs-lookup"><span data-stu-id="9ee47-134">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="9ee47-135">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="9ee47-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9ee47-136">NotStarted</span><span class="sxs-lookup"><span data-stu-id="9ee47-136">NotStarted</span></span>
- <span data-ttu-id="9ee47-137">InProgress</span><span class="sxs-lookup"><span data-stu-id="9ee47-137">InProgress</span></span>
- <span data-ttu-id="9ee47-138">Успешно</span><span class="sxs-lookup"><span data-stu-id="9ee47-138">Succeeded</span></span>
- <span data-ttu-id="9ee47-139">Другое</span><span class="sxs-lookup"><span data-stu-id="9ee47-139">Other</span></span>
- <span data-ttu-id="9ee47-140">Сбой</span><span class="sxs-lookup"><span data-stu-id="9ee47-140">Failed</span></span>
- <span data-ttu-id="9ee47-141">Отменено</span><span class="sxs-lookup"><span data-stu-id="9ee47-141">Cancelled</span></span>
- <span data-ttu-id="9ee47-142">Приостановлено</span><span class="sxs-lookup"><span data-stu-id="9ee47-142">Suspended</span></span>

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

### <span data-ttu-id="9ee47-143">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="9ee47-143">-TargetObjectId</span></span>
<span data-ttu-id="9ee47-144">Определяет ИД объекта, целевого для задания.</span><span class="sxs-lookup"><span data-stu-id="9ee47-144">Specifies the ID of the object targeted by the job.</span></span>

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

### <span data-ttu-id="9ee47-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee47-145">CommonParameters</span></span>
<span data-ttu-id="9ee47-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ee47-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee47-147">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ee47-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee47-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ee47-148">INPUTS</span></span>

## <span data-ttu-id="9ee47-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9ee47-149">OUTPUTS</span></span>

## <span data-ttu-id="9ee47-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9ee47-150">NOTES</span></span>

## <span data-ttu-id="9ee47-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ee47-151">RELATED LINKS</span></span>



[<span data-ttu-id="9ee47-152">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9ee47-152">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="9ee47-153">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9ee47-153">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="9ee47-154">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9ee47-154">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


