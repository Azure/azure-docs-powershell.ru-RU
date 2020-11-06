---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 590512c822bd55b992c8cc58eab4091863792e21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567093"
---
# <span data-ttu-id="4e71a-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="4e71a-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="4e71a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e71a-102">SYNOPSIS</span></span>
<span data-ttu-id="4e71a-103">Запускает действие фиксации отработки отказа для объекта восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="4e71a-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e71a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e71a-104">SYNTAX</span></span>

### <span data-ttu-id="4e71a-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e71a-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e71a-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="4e71a-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e71a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e71a-107">DESCRIPTION</span></span>
<span data-ttu-id="4e71a-108">Командлет **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** запускает процесс фиксации отработки отказа для объекта Azure Site Recovery после операции отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="4e71a-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="4e71a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e71a-109">EXAMPLES</span></span>

### <span data-ttu-id="4e71a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e71a-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="4e71a-111">Запускает фиксацию отработки отказа для указанного плана восстановления и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="4e71a-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="4e71a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e71a-112">PARAMETERS</span></span>

### <span data-ttu-id="4e71a-113">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4e71a-113">-RecoveryPlan</span></span>
<span data-ttu-id="4e71a-114">Указывает объект плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="4e71a-114">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e71a-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4e71a-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="4e71a-116">Указывает объект защищенного элемента репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="4e71a-116">Specifies an ASR replication protected item object.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e71a-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e71a-117">-Confirm</span></span>
<span data-ttu-id="4e71a-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e71a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e71a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e71a-119">-WhatIf</span></span>
<span data-ttu-id="4e71a-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e71a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e71a-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e71a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e71a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e71a-122">CommonParameters</span></span>
<span data-ttu-id="4e71a-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e71a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e71a-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e71a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e71a-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e71a-125">INPUTS</span></span>

### <span data-ttu-id="4e71a-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4e71a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="4e71a-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4e71a-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="4e71a-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e71a-128">OUTPUTS</span></span>

### <span data-ttu-id="4e71a-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4e71a-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4e71a-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e71a-130">NOTES</span></span>

## <span data-ttu-id="4e71a-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e71a-131">RELATED LINKS</span></span>

