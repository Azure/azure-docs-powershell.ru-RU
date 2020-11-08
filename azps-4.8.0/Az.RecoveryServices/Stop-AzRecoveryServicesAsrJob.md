---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: a86e58fe3c933ffaa9a382dc1e5140d3b42a34cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079365"
---
# <span data-ttu-id="10718-101">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="10718-101">Stop-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="10718-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10718-102">SYNOPSIS</span></span>
<span data-ttu-id="10718-103">Остановка задания для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="10718-103">Stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="10718-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10718-104">SYNTAX</span></span>

### <span data-ttu-id="10718-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="10718-105">ByObject (Default)</span></span>
```
Stop-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10718-106">ByName</span><span class="sxs-lookup"><span data-stu-id="10718-106">ByName</span></span>
```
Stop-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10718-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10718-107">DESCRIPTION</span></span>
<span data-ttu-id="10718-108">Командлет **Stop-AzRecoveryServicesAsrJob** останавливает указанное задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="10718-108">The **Stop-AzRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="10718-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10718-109">EXAMPLES</span></span>

### <span data-ttu-id="10718-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="10718-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="10718-111">Пытается остановить указанное задание и возвращает обновленный объект задания ASR.</span><span class="sxs-lookup"><span data-stu-id="10718-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="10718-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10718-112">PARAMETERS</span></span>

### <span data-ttu-id="10718-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10718-113">-DefaultProfile</span></span>
<span data-ttu-id="10718-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10718-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="10718-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10718-115">-InputObject</span></span>
<span data-ttu-id="10718-116">Объект input: указание объекта задания ASR, соответствующего заданию ASR, которое должно быть остановлено</span><span class="sxs-lookup"><span data-stu-id="10718-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="10718-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="10718-117">-Name</span></span>
<span data-ttu-id="10718-118">Укажите задание ASR, которое должно быть остановлено с помощью имени задания ASR.</span><span class="sxs-lookup"><span data-stu-id="10718-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="10718-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10718-119">-Confirm</span></span>
<span data-ttu-id="10718-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="10718-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10718-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10718-121">-WhatIf</span></span>
<span data-ttu-id="10718-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="10718-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10718-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="10718-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10718-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10718-124">CommonParameters</span></span>
<span data-ttu-id="10718-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10718-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10718-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10718-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10718-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10718-127">INPUTS</span></span>

### <span data-ttu-id="10718-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="10718-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="10718-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10718-129">OUTPUTS</span></span>

### <span data-ttu-id="10718-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="10718-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="10718-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="10718-131">NOTES</span></span>

## <span data-ttu-id="10718-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10718-132">RELATED LINKS</span></span>

[<span data-ttu-id="10718-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="10718-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="10718-134">Restarting-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="10718-134">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="10718-135">Возобновить — AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="10718-135">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)