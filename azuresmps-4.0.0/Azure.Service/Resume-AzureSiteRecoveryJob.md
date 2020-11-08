---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: E214AFEB-90A6-4553-94D4-FBEA6ADE572E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee340c2302670628bb8a3893567d7f8a2da754f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076440"
---
# <span data-ttu-id="b3054-101">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="b3054-101">Resume-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="b3054-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3054-102">SYNOPSIS</span></span>
<span data-ttu-id="b3054-103">Возобновляет приостановленное задание восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="b3054-103">Resumes a suspended Site Recovery job.</span></span>

## <span data-ttu-id="b3054-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3054-104">SYNTAX</span></span>

### <span data-ttu-id="b3054-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b3054-105">ByObject (Default)</span></span>
```
Resume-AzureSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b3054-106">ById</span><span class="sxs-lookup"><span data-stu-id="b3054-106">ById</span></span>
```
Resume-AzureSiteRecoveryJob -Id <String> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b3054-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3054-107">DESCRIPTION</span></span>
<span data-ttu-id="b3054-108">Командлет **Resume-AzureSiteRecoveryJob** возобновляет приостановленное задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="b3054-108">The **Resume-AzureSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="b3054-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3054-109">EXAMPLES</span></span>

### <span data-ttu-id="b3054-110">Пример 1: возобновление всех заданий</span><span class="sxs-lookup"><span data-stu-id="b3054-110">Example 1: Resume all jobs</span></span>
```
PS C:\> $Jobs = Get-AzureSiteRecoveryJob  
PS C:\> Resume-AzureSiteRecoveryJob -Job $Jobs
ID               : d16397fb-cdf1-4972-b677-c333f3c557b4
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : Suspended
StateDescription : WaitingForManualAction
StartTime        : 10/6/2014 10:19:28 AM
EndTime          : 10/6/2014 10:19:31 AM
AllowedActions   : {Cancel, RestartTestFailoverCleanup}
Name             : Test failover
Tasks            : {Recovery plan preflight checks, Create test environment, All groups failover: Pre steps (1), 
                   Recovery plan failover...} 
Errors           : {}
```

<span data-ttu-id="b3054-111">Первая команда получает все задания Azure Site Recovery для текущего хранилища сайта с помощью командлета **Get-AzureSiteRecoveryJob** , а затем сохраняет результаты в переменной $jobs.</span><span class="sxs-lookup"><span data-stu-id="b3054-111">The first command gets all the Azure Site Recovery jobs for the current Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="b3054-112">Вторая команда возобновление задания, заданного $Jobs.</span><span class="sxs-lookup"><span data-stu-id="b3054-112">The second command resumes the job specified by $Jobs.</span></span>

## <span data-ttu-id="b3054-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3054-113">PARAMETERS</span></span>

### <span data-ttu-id="b3054-114">-Примечания</span><span class="sxs-lookup"><span data-stu-id="b3054-114">-Comments</span></span>
<span data-ttu-id="b3054-115">Указывает комментарии для журнала заданий.</span><span class="sxs-lookup"><span data-stu-id="b3054-115">Specifies the comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3054-116">-ID</span><span class="sxs-lookup"><span data-stu-id="b3054-116">-Id</span></span>
<span data-ttu-id="b3054-117">Указывает идентификатор задания, которое нужно возобновить.</span><span class="sxs-lookup"><span data-stu-id="b3054-117">Specifies the ID of a job to resume.</span></span>

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

### <span data-ttu-id="b3054-118">-Job</span><span class="sxs-lookup"><span data-stu-id="b3054-118">-Job</span></span>
<span data-ttu-id="b3054-119">Указывает задание, которое нужно возобновить.</span><span class="sxs-lookup"><span data-stu-id="b3054-119">Specifies the job to resume.</span></span>

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

### <span data-ttu-id="b3054-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="b3054-120">-Profile</span></span>
<span data-ttu-id="b3054-121">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b3054-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b3054-122">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b3054-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b3054-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3054-123">CommonParameters</span></span>
<span data-ttu-id="b3054-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3054-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3054-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3054-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3054-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3054-126">INPUTS</span></span>

## <span data-ttu-id="b3054-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3054-127">OUTPUTS</span></span>

## <span data-ttu-id="b3054-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3054-128">NOTES</span></span>

## <span data-ttu-id="b3054-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3054-129">RELATED LINKS</span></span>

[<span data-ttu-id="b3054-130">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="b3054-130">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="b3054-131">Restarting-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="b3054-131">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="b3054-132">Остановить-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="b3054-132">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


