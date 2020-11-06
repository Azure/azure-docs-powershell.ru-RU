---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/restart-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 0ac09a527aff78648d3af14413baa33da137d59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563407"
---
# <span data-ttu-id="fdaf6-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="fdaf6-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="fdaf6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fdaf6-102">SYNOPSIS</span></span>
<span data-ttu-id="fdaf6-103">Перезапускает задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdaf6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fdaf6-104">SYNTAX</span></span>

### <span data-ttu-id="fdaf6-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fdaf6-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdaf6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fdaf6-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdaf6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fdaf6-107">DESCRIPTION</span></span>
<span data-ttu-id="fdaf6-108">Командлет **restart-AzureRmRecoveryServicesAsrJob** перезапустит задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="fdaf6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fdaf6-109">EXAMPLES</span></span>

### <span data-ttu-id="fdaf6-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fdaf6-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="fdaf6-111">Перезапускает указанное задание ASR и возвращает обновленный объект задания ASR для задания ASR.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="fdaf6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fdaf6-112">PARAMETERS</span></span>

### <span data-ttu-id="fdaf6-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fdaf6-113">-Confirm</span></span>
<span data-ttu-id="fdaf6-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdaf6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdaf6-115">-DefaultProfile</span></span>
<span data-ttu-id="fdaf6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="fdaf6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdaf6-117">-InputObject</span></span>
<span data-ttu-id="fdaf6-118">Входной объект для командлета: объект задания ASR, соответствующий перезапуску задания ASR</span><span class="sxs-lookup"><span data-stu-id="fdaf6-118">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>
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

### <span data-ttu-id="fdaf6-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fdaf6-119">-Name</span></span>
<span data-ttu-id="fdaf6-120">Укажите задание по имени.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-120">Specify the job by name.</span></span>

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

### <span data-ttu-id="fdaf6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdaf6-121">-WhatIf</span></span>
<span data-ttu-id="fdaf6-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdaf6-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdaf6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdaf6-124">CommonParameters</span></span>
<span data-ttu-id="fdaf6-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fdaf6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdaf6-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdaf6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdaf6-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fdaf6-127">INPUTS</span></span>

### <span data-ttu-id="fdaf6-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fdaf6-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fdaf6-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fdaf6-129">OUTPUTS</span></span>

### <span data-ttu-id="fdaf6-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fdaf6-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fdaf6-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="fdaf6-131">NOTES</span></span>

## <span data-ttu-id="fdaf6-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fdaf6-132">RELATED LINKS</span></span>

[<span data-ttu-id="fdaf6-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="fdaf6-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="fdaf6-134">Возобновить — AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="fdaf6-134">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="fdaf6-135">Остановить-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="fdaf6-135">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
