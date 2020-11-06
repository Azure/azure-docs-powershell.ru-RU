---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/resume-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: e6c384f56e7af9bacad40dfbc1fbf87d26dd8320
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563399"
---
# <span data-ttu-id="ed666-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ed666-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="ed666-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed666-102">SYNOPSIS</span></span>
<span data-ttu-id="ed666-103">Возобновляет приостановленное задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="ed666-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed666-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed666-104">SYNTAX</span></span>

### <span data-ttu-id="ed666-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed666-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed666-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ed666-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed666-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed666-107">DESCRIPTION</span></span>
<span data-ttu-id="ed666-108">Командлет **Resume-AzureRmRecoveryServicesAsrJob** возобновляет приостановленное задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="ed666-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="ed666-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed666-109">EXAMPLES</span></span>

### <span data-ttu-id="ed666-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ed666-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="ed666-111">Возобновить указанное задание, если оно находится в состоянии ожидания или приостановлено, и вернуть обновленный объект задания ASR, соответствующий заданию ASR.</span><span class="sxs-lookup"><span data-stu-id="ed666-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="ed666-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed666-112">PARAMETERS</span></span>

### <span data-ttu-id="ed666-113">-Примечание</span><span class="sxs-lookup"><span data-stu-id="ed666-113">-Comment</span></span>
<span data-ttu-id="ed666-114">Примечания к журналу заданий.</span><span class="sxs-lookup"><span data-stu-id="ed666-114">Comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed666-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed666-115">-Confirm</span></span>
<span data-ttu-id="ed666-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ed666-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed666-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed666-117">-DefaultProfile</span></span>
<span data-ttu-id="ed666-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed666-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="ed666-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed666-119">-InputObject</span></span>
<span data-ttu-id="ed666-120">Входной объект для командлета: объект задания ASR, соответствующий заданию, которое должно быть возобновлено.</span><span class="sxs-lookup"><span data-stu-id="ed666-120">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="ed666-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ed666-121">-Name</span></span>
<span data-ttu-id="ed666-122">Укажите задание ASR по имени.</span><span class="sxs-lookup"><span data-stu-id="ed666-122">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="ed666-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed666-123">-WhatIf</span></span>
<span data-ttu-id="ed666-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ed666-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed666-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ed666-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed666-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed666-126">CommonParameters</span></span>
<span data-ttu-id="ed666-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed666-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed666-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed666-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed666-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed666-129">INPUTS</span></span>

### <span data-ttu-id="ed666-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ed666-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ed666-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed666-131">OUTPUTS</span></span>

### <span data-ttu-id="ed666-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ed666-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ed666-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed666-133">NOTES</span></span>

## <span data-ttu-id="ed666-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed666-134">RELATED LINKS</span></span>

[<span data-ttu-id="ed666-135">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ed666-135">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="ed666-136">Restarting-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ed666-136">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="ed666-137">Остановить-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ed666-137">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
