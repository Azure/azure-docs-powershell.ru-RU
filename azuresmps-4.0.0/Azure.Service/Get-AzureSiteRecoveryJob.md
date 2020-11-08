---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2957C0DE-3A2F-4337-A778-2B95654972E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d0b272732cf6c1e1b2025c8e7f48b58e4807cdb3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075595"
---
# <span data-ttu-id="5fb1f-101">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5fb1f-101">Get-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="5fb1f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5fb1f-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb1f-103">Возвращает сведения о операции для хранилища сайта.</span><span class="sxs-lookup"><span data-stu-id="5fb1f-103">Gets the operation information for a Site Recovery vault.</span></span>

## <span data-ttu-id="5fb1f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5fb1f-104">SYNTAX</span></span>

### <span data-ttu-id="5fb1f-105">ByParam (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5fb1f-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5fb1f-106">ById</span><span class="sxs-lookup"><span data-stu-id="5fb1f-106">ById</span></span>
```
Get-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5fb1f-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="5fb1f-107">ByObject</span></span>
```
Get-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5fb1f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fb1f-108">DESCRIPTION</span></span>
<span data-ttu-id="5fb1f-109">Командлет **Get-AzureSiteRecoveryJob** получает задания Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5fb1f-109">The **Get-AzureSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="5fb1f-110">Вы можете использовать этот командлет, чтобы просмотреть сведения об операции для текущего хранилища сайта для восстановления.</span><span class="sxs-lookup"><span data-stu-id="5fb1f-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="5fb1f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5fb1f-111">EXAMPLES</span></span>

### <span data-ttu-id="5fb1f-112">Пример 1: получение задания с указанием идентификатора</span><span class="sxs-lookup"><span data-stu-id="5fb1f-112">Example 1: Get a job by specifying an ID</span></span>
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

<span data-ttu-id="5fb1f-113">Эта команда получает задание Azure Site Recovery с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="5fb1f-113">This command gets the  Azure Site Recovery job that has the specified ID.</span></span>

### <span data-ttu-id="5fb1f-114">Пример 2: получение задания на основе времени</span><span class="sxs-lookup"><span data-stu-id="5fb1f-114">Example 2: Gets a job based on time</span></span>
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

<span data-ttu-id="5fb1f-115">Эта команда возвращает задания для восстановления сайта, которые находятся в интервале между указанными временем начала и временем окончания.</span><span class="sxs-lookup"><span data-stu-id="5fb1f-115">This command gets Site Recovery jobs that fall between the specified start time and end time.</span></span>

## <span data-ttu-id="5fb1f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5fb1f-116">PARAMETERS</span></span>

### <span data-ttu-id="5fb1f-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5fb1f-117">-EndTime</span></span>
<span data-ttu-id="5fb1f-118">Указывает время окончания для заданий.</span><span class="sxs-lookup"><span data-stu-id="5fb1f-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="5fb1f-119">Этот командлет получает все задания, которые были запущены до указанного времени.</span><span class="sxs-lookup"><span data-stu-id="5fb1f-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="5fb1f-120">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="5fb1f-120">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="5fb1f-121">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="5fb1f-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="5fb1f-122">-ID</span><span class="sxs-lookup"><span data-stu-id="5fb1f-122">-Id</span></span>
<span data-ttu-id="5fb1f-123">Указывает идентификатор задания, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="5fb1f-123">Specifies the ID of a job to get.</span></span>

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

### <span data-ttu-id="5fb1f-124">-Job</span><span class="sxs-lookup"><span data-stu-id="5fb1f-124">-Job</span></span>
<span data-ttu-id="5fb1f-125">Указывает задание для получения.</span><span class="sxs-lookup"><span data-stu-id="5fb1f-125">Specifies a job to get.</span></span>

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

### <span data-ttu-id="5fb1f-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="5fb1f-126">-Profile</span></span>
<span data-ttu-id="5fb1f-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5fb1f-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5fb1f-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5fb1f-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5fb1f-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5fb1f-129">-StartTime</span></span>
<span data-ttu-id="5fb1f-130">Задает время начала для заданий.</span><span class="sxs-lookup"><span data-stu-id="5fb1f-130">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="5fb1f-131">Этот командлет получает все задания, которые были запущены по истечении заданного времени.</span><span class="sxs-lookup"><span data-stu-id="5fb1f-131">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="5fb1f-132">-State</span><span class="sxs-lookup"><span data-stu-id="5fb1f-132">-State</span></span>
<span data-ttu-id="5fb1f-133">Задает состояние ввода для задания по восстановлению сайта.</span><span class="sxs-lookup"><span data-stu-id="5fb1f-133">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="5fb1f-134">Этот командлет получает все задания, которые соответствуют указанному состоянию.</span><span class="sxs-lookup"><span data-stu-id="5fb1f-134">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="5fb1f-135">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5fb1f-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5fb1f-136">NotStarted</span><span class="sxs-lookup"><span data-stu-id="5fb1f-136">NotStarted</span></span>
- <span data-ttu-id="5fb1f-137">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="5fb1f-137">InProgress</span></span>
- <span data-ttu-id="5fb1f-138">LSP</span><span class="sxs-lookup"><span data-stu-id="5fb1f-138">Succeeded</span></span>
- <span data-ttu-id="5fb1f-139">Другие</span><span class="sxs-lookup"><span data-stu-id="5fb1f-139">Other</span></span>
- <span data-ttu-id="5fb1f-140">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="5fb1f-140">Failed</span></span>
- <span data-ttu-id="5fb1f-141">Отменен</span><span class="sxs-lookup"><span data-stu-id="5fb1f-141">Cancelled</span></span>
- <span data-ttu-id="5fb1f-142">Остановить</span><span class="sxs-lookup"><span data-stu-id="5fb1f-142">Suspended</span></span>

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

### <span data-ttu-id="5fb1f-143">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="5fb1f-143">-TargetObjectId</span></span>
<span data-ttu-id="5fb1f-144">Указывает идентификатор объекта, для которого задано задание.</span><span class="sxs-lookup"><span data-stu-id="5fb1f-144">Specifies the ID of the object targeted by the job.</span></span>

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

### <span data-ttu-id="5fb1f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb1f-145">CommonParameters</span></span>
<span data-ttu-id="5fb1f-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5fb1f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb1f-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fb1f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb1f-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5fb1f-148">INPUTS</span></span>

## <span data-ttu-id="5fb1f-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fb1f-149">OUTPUTS</span></span>

## <span data-ttu-id="5fb1f-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="5fb1f-150">NOTES</span></span>

## <span data-ttu-id="5fb1f-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5fb1f-151">RELATED LINKS</span></span>

[<span data-ttu-id="5fb1f-152">Командлеты служб Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="5fb1f-152">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)

[<span data-ttu-id="5fb1f-153">Restarting-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5fb1f-153">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="5fb1f-154">Возобновить — AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5fb1f-154">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="5fb1f-155">Остановить-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5fb1f-155">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


