---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 4e8b7cda670a0e67cc635ce52f0934c806733c78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729620"
---
# <span data-ttu-id="2ccc7-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2ccc7-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="2ccc7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ccc7-102">SYNOPSIS</span></span>
<span data-ttu-id="2ccc7-103">Возобновляет приостановленное задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="2ccc7-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="2ccc7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ccc7-104">SYNTAX</span></span>

### <span data-ttu-id="2ccc7-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2ccc7-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ccc7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2ccc7-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ccc7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ccc7-107">DESCRIPTION</span></span>
<span data-ttu-id="2ccc7-108">Командлет **Resume-AzRecoveryServicesAsrJob** возобновляет приостановленное задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="2ccc7-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="2ccc7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ccc7-109">EXAMPLES</span></span>

### <span data-ttu-id="2ccc7-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2ccc7-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="2ccc7-111">Возобновить указанное задание, если оно находится в состоянии ожидания или приостановлено, и вернуть обновленный объект задания ASR, соответствующий заданию ASR.</span><span class="sxs-lookup"><span data-stu-id="2ccc7-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="2ccc7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ccc7-112">PARAMETERS</span></span>

### <span data-ttu-id="2ccc7-113">-Примечание</span><span class="sxs-lookup"><span data-stu-id="2ccc7-113">-Comment</span></span>
<span data-ttu-id="2ccc7-114">Примечания к журналу заданий.</span><span class="sxs-lookup"><span data-stu-id="2ccc7-114">Comments for the job log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ccc7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ccc7-115">-DefaultProfile</span></span>
<span data-ttu-id="2ccc7-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ccc7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2ccc7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ccc7-117">-InputObject</span></span>
<span data-ttu-id="2ccc7-118">Входной объект для командлета: объект задания ASR, соответствующий заданию, которое должно быть возобновлено.</span><span class="sxs-lookup"><span data-stu-id="2ccc7-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ccc7-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2ccc7-119">-Name</span></span>
<span data-ttu-id="2ccc7-120">Укажите задание ASR по имени.</span><span class="sxs-lookup"><span data-stu-id="2ccc7-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="2ccc7-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ccc7-121">-Confirm</span></span>
<span data-ttu-id="2ccc7-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2ccc7-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ccc7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ccc7-123">-WhatIf</span></span>
<span data-ttu-id="2ccc7-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2ccc7-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ccc7-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2ccc7-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ccc7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ccc7-126">CommonParameters</span></span>
<span data-ttu-id="2ccc7-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ccc7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ccc7-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ccc7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ccc7-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ccc7-129">INPUTS</span></span>

### <span data-ttu-id="2ccc7-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2ccc7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2ccc7-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ccc7-131">OUTPUTS</span></span>

### <span data-ttu-id="2ccc7-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2ccc7-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2ccc7-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ccc7-133">NOTES</span></span>

## <span data-ttu-id="2ccc7-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ccc7-134">RELATED LINKS</span></span>

[<span data-ttu-id="2ccc7-135">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2ccc7-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="2ccc7-136">Restarting-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2ccc7-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="2ccc7-137">Остановить-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2ccc7-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
