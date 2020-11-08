---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AE26EA0F-9D92-4FDF-92EF-CA33BF06C0DB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68a97359e5181bbc27183c0c1dbb6f526fa2e529
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076076"
---
# <span data-ttu-id="1e06b-101">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="1e06b-101">Restart-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="1e06b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e06b-102">SYNOPSIS</span></span>
<span data-ttu-id="1e06b-103">Перезапускает задание по восстановлению сайта.</span><span class="sxs-lookup"><span data-stu-id="1e06b-103">Restarts a Site Recovery job.</span></span>

## <span data-ttu-id="1e06b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e06b-104">SYNTAX</span></span>

### <span data-ttu-id="1e06b-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1e06b-105">ByObject (Default)</span></span>
```
Restart-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1e06b-106">ById</span><span class="sxs-lookup"><span data-stu-id="1e06b-106">ById</span></span>
```
Restart-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1e06b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e06b-107">DESCRIPTION</span></span>
<span data-ttu-id="1e06b-108">Командлет **restart-AzureSiteRecoveryJob** перезапустит задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="1e06b-108">The **Restart-AzureSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="1e06b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e06b-109">EXAMPLES</span></span>

### <span data-ttu-id="1e06b-110">Пример 1: перезапуск задания</span><span class="sxs-lookup"><span data-stu-id="1e06b-110">Example 1: Restart a job</span></span>
```
PS C:\> Restart-AzureSiteRecoveryJob -Id "bbf0b839-9aaa-49e1-8354-601c9145966d"
ID               : bbf0b839-9aaa-49e1-8354-601c9145966d
ClientRequestId  : ef42c8b0-640c-4442-960b-349f83d161a5-2014-24-06 14:24:04Z-P
State            : Failed
StateDescription : Failed
StartTime        : 10/6/2014 9:41:08 AM
EndTime          : 10/6/2014 9:41:21 AM
AllowedActions   : {Cancel, Restart}
Name             : Enable protection
Tasks            : {Prerequisites check for enabling protection , Identifying replication target, Enable replication, 
                   Starting initial replication...} 
Errors           : {CreateProtectionTargetTask}
```

<span data-ttu-id="1e06b-111">Эта команда перезапускает задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="1e06b-111">This command restarts the job that has the specified ID.</span></span>

## <span data-ttu-id="1e06b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e06b-112">PARAMETERS</span></span>

### <span data-ttu-id="1e06b-113">-ID</span><span class="sxs-lookup"><span data-stu-id="1e06b-113">-Id</span></span>
<span data-ttu-id="1e06b-114">Указывает ИД задания для перезапуска.</span><span class="sxs-lookup"><span data-stu-id="1e06b-114">Specifies the ID of the job to restart.</span></span>

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

### <span data-ttu-id="1e06b-115">-Job</span><span class="sxs-lookup"><span data-stu-id="1e06b-115">-Job</span></span>
<span data-ttu-id="1e06b-116">Указывает задание, которое необходимо перезапустить.</span><span class="sxs-lookup"><span data-stu-id="1e06b-116">Specifies the job to restart.</span></span>

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

### <span data-ttu-id="1e06b-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="1e06b-117">-Profile</span></span>
<span data-ttu-id="1e06b-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1e06b-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1e06b-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1e06b-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1e06b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e06b-120">CommonParameters</span></span>
<span data-ttu-id="1e06b-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e06b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e06b-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e06b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e06b-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e06b-123">INPUTS</span></span>

## <span data-ttu-id="1e06b-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e06b-124">OUTPUTS</span></span>

## <span data-ttu-id="1e06b-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e06b-125">NOTES</span></span>

## <span data-ttu-id="1e06b-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e06b-126">RELATED LINKS</span></span>

[<span data-ttu-id="1e06b-127">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="1e06b-127">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="1e06b-128">Возобновить — AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="1e06b-128">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="1e06b-129">Остановить-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="1e06b-129">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


