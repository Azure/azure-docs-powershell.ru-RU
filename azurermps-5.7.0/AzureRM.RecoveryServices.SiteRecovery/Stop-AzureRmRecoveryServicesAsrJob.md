---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/stop-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: c573cd8162961660dac57be3d3f5fe18cd055a89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557231"
---
# <span data-ttu-id="f0fda-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f0fda-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="f0fda-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0fda-102">SYNOPSIS</span></span>
<span data-ttu-id="f0fda-103">Остановка задания для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="f0fda-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0fda-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0fda-104">SYNTAX</span></span>

### <span data-ttu-id="f0fda-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0fda-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0fda-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f0fda-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0fda-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0fda-107">DESCRIPTION</span></span>
<span data-ttu-id="f0fda-108">Командлет **Stop-AzureRmRecoveryServicesAsrJob** останавливает указанное задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="f0fda-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="f0fda-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0fda-109">EXAMPLES</span></span>

### <span data-ttu-id="f0fda-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f0fda-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="f0fda-111">Пытается остановить указанное задание и возвращает обновленный объект задания ASR.</span><span class="sxs-lookup"><span data-stu-id="f0fda-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="f0fda-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0fda-112">PARAMETERS</span></span>

### <span data-ttu-id="f0fda-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0fda-113">-Confirm</span></span>
<span data-ttu-id="f0fda-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f0fda-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0fda-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0fda-115">-DefaultProfile</span></span>
<span data-ttu-id="f0fda-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0fda-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="f0fda-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0fda-117">-InputObject</span></span>
<span data-ttu-id="f0fda-118">Объект input: указание объекта задания ASR, соответствующего заданию ASR, которое должно быть остановлено</span><span class="sxs-lookup"><span data-stu-id="f0fda-118">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="f0fda-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f0fda-119">-Name</span></span>
<span data-ttu-id="f0fda-120">Укажите задание ASR, которое должно быть остановлено с помощью имени задания ASR.</span><span class="sxs-lookup"><span data-stu-id="f0fda-120">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="f0fda-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0fda-121">-WhatIf</span></span>
<span data-ttu-id="f0fda-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f0fda-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0fda-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f0fda-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0fda-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0fda-124">CommonParameters</span></span>
<span data-ttu-id="f0fda-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0fda-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0fda-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0fda-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0fda-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0fda-127">INPUTS</span></span>

### <span data-ttu-id="f0fda-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f0fda-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f0fda-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0fda-129">OUTPUTS</span></span>

### <span data-ttu-id="f0fda-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f0fda-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f0fda-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0fda-131">NOTES</span></span>

## <span data-ttu-id="f0fda-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0fda-132">RELATED LINKS</span></span>

[<span data-ttu-id="f0fda-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f0fda-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="f0fda-134">Restarting-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f0fda-134">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="f0fda-135">Возобновить — AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f0fda-135">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
