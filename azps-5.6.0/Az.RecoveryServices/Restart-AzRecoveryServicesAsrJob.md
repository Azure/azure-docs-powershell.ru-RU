---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 2609ed7483499445dbdd093d0059b76b7e781ef8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953107"
---
# <span data-ttu-id="ab6ad-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ab6ad-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="ab6ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab6ad-102">SYNOPSIS</span></span>
<span data-ttu-id="ab6ad-103">Перезапуск задания восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="ab6ad-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="ab6ad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ab6ad-104">SYNTAX</span></span>

### <span data-ttu-id="ab6ad-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ab6ad-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab6ad-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ab6ad-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab6ad-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab6ad-107">DESCRIPTION</span></span>
<span data-ttu-id="ab6ad-108">Для **перезапуска azRecoveryServicesAsrJob** перезапустится задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="ab6ad-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="ab6ad-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ab6ad-109">EXAMPLES</span></span>

### <span data-ttu-id="ab6ad-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ab6ad-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="ab6ad-111">Перезапуск указанного задания ASR и возврат обновленного объекта задания ASR.</span><span class="sxs-lookup"><span data-stu-id="ab6ad-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="ab6ad-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab6ad-112">PARAMETERS</span></span>

### <span data-ttu-id="ab6ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab6ad-113">-DefaultProfile</span></span>
<span data-ttu-id="ab6ad-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab6ad-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ab6ad-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab6ad-115">-InputObject</span></span>
<span data-ttu-id="ab6ad-116">Объект ввода для cmdlet: объект задания ASR, соответствующий перезапуску задания ASR</span><span class="sxs-lookup"><span data-stu-id="ab6ad-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="ab6ad-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ab6ad-117">-Name</span></span>
<span data-ttu-id="ab6ad-118">Укажите задание по имени.</span><span class="sxs-lookup"><span data-stu-id="ab6ad-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="ab6ad-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab6ad-119">-Confirm</span></span>
<span data-ttu-id="ab6ad-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab6ad-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab6ad-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab6ad-121">-WhatIf</span></span>
<span data-ttu-id="ab6ad-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab6ad-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab6ad-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ab6ad-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab6ad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab6ad-124">CommonParameters</span></span>
<span data-ttu-id="ab6ad-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab6ad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab6ad-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab6ad-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab6ad-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab6ad-127">INPUTS</span></span>

### <span data-ttu-id="ab6ad-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="ab6ad-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ab6ad-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ab6ad-129">OUTPUTS</span></span>

### <span data-ttu-id="ab6ad-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="ab6ad-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ab6ad-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ab6ad-131">NOTES</span></span>

## <span data-ttu-id="ab6ad-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab6ad-132">RELATED LINKS</span></span>

[<span data-ttu-id="ab6ad-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ab6ad-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="ab6ad-134">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ab6ad-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="ab6ad-135">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ab6ad-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
