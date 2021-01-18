---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 6af467e5fd90a7d3028d67297b62f517f512b1b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506002"
---
# <span data-ttu-id="dafdc-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="dafdc-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="dafdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dafdc-102">SYNOPSIS</span></span>
<span data-ttu-id="dafdc-103">Возобновление приостановленного задания восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="dafdc-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="dafdc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dafdc-104">SYNTAX</span></span>

### <span data-ttu-id="dafdc-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dafdc-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dafdc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="dafdc-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dafdc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dafdc-107">DESCRIPTION</span></span>
<span data-ttu-id="dafdc-108">Для возобновления приостановленного задания восстановления сайта Azure возобновляется **cmdlet Resume-AzRecoveryServicesAsrJob.**</span><span class="sxs-lookup"><span data-stu-id="dafdc-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="dafdc-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dafdc-109">EXAMPLES</span></span>

### <span data-ttu-id="dafdc-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dafdc-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="dafdc-111">Возобновление указанного задания в том случае, если оно находится в состоянии ожидания или приостановки, и возврат обновленного объекта задания ASR, соответствующего заданиям ASR.</span><span class="sxs-lookup"><span data-stu-id="dafdc-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="dafdc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dafdc-112">PARAMETERS</span></span>

### <span data-ttu-id="dafdc-113">-Comment</span><span class="sxs-lookup"><span data-stu-id="dafdc-113">-Comment</span></span>
<span data-ttu-id="dafdc-114">При комментарии к журналу задания.</span><span class="sxs-lookup"><span data-stu-id="dafdc-114">Comments for the job log.</span></span>

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

### <span data-ttu-id="dafdc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dafdc-115">-DefaultProfile</span></span>
<span data-ttu-id="dafdc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dafdc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="dafdc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dafdc-117">-InputObject</span></span>
<span data-ttu-id="dafdc-118">Объект ввода для cmdlet: объект задания ASR, соответствующий задаче, который нужно возобновить.</span><span class="sxs-lookup"><span data-stu-id="dafdc-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="dafdc-119">-Name</span><span class="sxs-lookup"><span data-stu-id="dafdc-119">-Name</span></span>
<span data-ttu-id="dafdc-120">Укажите задание asR по имени.</span><span class="sxs-lookup"><span data-stu-id="dafdc-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="dafdc-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dafdc-121">-Confirm</span></span>
<span data-ttu-id="dafdc-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dafdc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dafdc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dafdc-123">-WhatIf</span></span>
<span data-ttu-id="dafdc-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dafdc-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dafdc-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dafdc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dafdc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dafdc-126">CommonParameters</span></span>
<span data-ttu-id="dafdc-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dafdc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dafdc-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dafdc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dafdc-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dafdc-129">INPUTS</span></span>

### <span data-ttu-id="dafdc-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="dafdc-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dafdc-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dafdc-131">OUTPUTS</span></span>

### <span data-ttu-id="dafdc-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="dafdc-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dafdc-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dafdc-133">NOTES</span></span>

## <span data-ttu-id="dafdc-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dafdc-134">RELATED LINKS</span></span>

[<span data-ttu-id="dafdc-135">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="dafdc-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="dafdc-136">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="dafdc-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="dafdc-137">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="dafdc-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
