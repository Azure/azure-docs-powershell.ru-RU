---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: cf8b2617e01e472de32f128d4907d68edaebb2e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235478"
---
# <span data-ttu-id="15daa-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="15daa-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="15daa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15daa-102">SYNOPSIS</span></span>
<span data-ttu-id="15daa-103">Перезапускает задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="15daa-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="15daa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15daa-104">SYNTAX</span></span>

### <span data-ttu-id="15daa-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="15daa-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15daa-106">ByName</span><span class="sxs-lookup"><span data-stu-id="15daa-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15daa-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15daa-107">DESCRIPTION</span></span>
<span data-ttu-id="15daa-108">Командлет **restart-AzRecoveryServicesAsrJob** перезапустит задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="15daa-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="15daa-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15daa-109">EXAMPLES</span></span>

### <span data-ttu-id="15daa-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="15daa-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="15daa-111">Перезапускает указанное задание ASR и возвращает обновленный объект задания ASR для задания ASR.</span><span class="sxs-lookup"><span data-stu-id="15daa-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="15daa-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15daa-112">PARAMETERS</span></span>

### <span data-ttu-id="15daa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15daa-113">-DefaultProfile</span></span>
<span data-ttu-id="15daa-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15daa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="15daa-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15daa-115">-InputObject</span></span>
<span data-ttu-id="15daa-116">Входной объект для командлета: объект задания ASR, соответствующий перезапуску задания ASR</span><span class="sxs-lookup"><span data-stu-id="15daa-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="15daa-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="15daa-117">-Name</span></span>
<span data-ttu-id="15daa-118">Укажите задание по имени.</span><span class="sxs-lookup"><span data-stu-id="15daa-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="15daa-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15daa-119">-Confirm</span></span>
<span data-ttu-id="15daa-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="15daa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15daa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15daa-121">-WhatIf</span></span>
<span data-ttu-id="15daa-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="15daa-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15daa-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="15daa-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15daa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15daa-124">CommonParameters</span></span>
<span data-ttu-id="15daa-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15daa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15daa-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15daa-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15daa-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15daa-127">INPUTS</span></span>

### <span data-ttu-id="15daa-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="15daa-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="15daa-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15daa-129">OUTPUTS</span></span>

### <span data-ttu-id="15daa-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="15daa-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="15daa-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="15daa-131">NOTES</span></span>

## <span data-ttu-id="15daa-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15daa-132">RELATED LINKS</span></span>

[<span data-ttu-id="15daa-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="15daa-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="15daa-134">Возобновить — AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="15daa-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="15daa-135">Остановить-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="15daa-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
