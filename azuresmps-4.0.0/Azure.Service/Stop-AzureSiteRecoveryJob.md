---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8FF1362B-C7AB-4769-A88B-D1B6E214A006
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8275b8dfec4263c5ab7a8022dcb65edccb1171
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076407"
---
# <span data-ttu-id="f3cf7-101">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="f3cf7-101">Stop-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="f3cf7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="f3cf7-103">Остановка задания по восстановлению сайта.</span><span class="sxs-lookup"><span data-stu-id="f3cf7-103">Stops a Site Recovery job.</span></span>

## <span data-ttu-id="f3cf7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3cf7-104">SYNTAX</span></span>

### <span data-ttu-id="f3cf7-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f3cf7-105">ByObject (Default)</span></span>
```
Stop-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f3cf7-106">ById</span><span class="sxs-lookup"><span data-stu-id="f3cf7-106">ById</span></span>
```
Stop-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f3cf7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3cf7-107">DESCRIPTION</span></span>
<span data-ttu-id="f3cf7-108">Командлет **Stop-AzureSiteRecoveryJob** останавливает задание Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f3cf7-108">The **Stop-AzureSiteRecoveryJob** cmdlet stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="f3cf7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3cf7-109">EXAMPLES</span></span>

### <span data-ttu-id="f3cf7-110">Пример 1: остановка всех заданий</span><span class="sxs-lookup"><span data-stu-id="f3cf7-110">Example 1: Stop all jobs</span></span>
```
PS C:\>$Jobs = Get-AzureSiteRecoveryJob 
PS C:\> Stop-AzureSiteRecoveryJob -Job $Jobs
```

<span data-ttu-id="f3cf7-111">Первая команда получает задания Azure Site Recovery для текущего хранилища Azure Site Recovery с помощью командлета **Get-AzureSiteRecoveryJob** , а затем сохраняет результаты в переменной $jobs.</span><span class="sxs-lookup"><span data-stu-id="f3cf7-111">The first command gets the Azure Site Recovery jobs for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="f3cf7-112">Вторая команда останавливает задания, заданные $Jobs.</span><span class="sxs-lookup"><span data-stu-id="f3cf7-112">The second command stops the jobs specified by $Jobs.</span></span>

## <span data-ttu-id="f3cf7-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3cf7-113">PARAMETERS</span></span>

### <span data-ttu-id="f3cf7-114">-ID</span><span class="sxs-lookup"><span data-stu-id="f3cf7-114">-Id</span></span>
<span data-ttu-id="f3cf7-115">Указывает ИД задания, которое нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="f3cf7-115">Specifies the ID of the job to stop.</span></span>

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

### <span data-ttu-id="f3cf7-116">-Job</span><span class="sxs-lookup"><span data-stu-id="f3cf7-116">-Job</span></span>
<span data-ttu-id="f3cf7-117">Указывает задание, которое нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="f3cf7-117">Specifies the job to stop.</span></span>

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

### <span data-ttu-id="f3cf7-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="f3cf7-118">-Profile</span></span>
<span data-ttu-id="f3cf7-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f3cf7-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f3cf7-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f3cf7-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f3cf7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3cf7-121">CommonParameters</span></span>
<span data-ttu-id="f3cf7-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3cf7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3cf7-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3cf7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3cf7-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3cf7-124">INPUTS</span></span>

## <span data-ttu-id="f3cf7-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3cf7-125">OUTPUTS</span></span>

## <span data-ttu-id="f3cf7-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3cf7-126">NOTES</span></span>

## <span data-ttu-id="f3cf7-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3cf7-127">RELATED LINKS</span></span>

[<span data-ttu-id="f3cf7-128">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="f3cf7-128">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="f3cf7-129">Restarting-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="f3cf7-129">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="f3cf7-130">Возобновить — AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="f3cf7-130">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)


