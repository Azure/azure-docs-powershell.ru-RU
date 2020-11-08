---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrcommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 0714fc44ba8e52536e1a3eb677199da95895bc83
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066085"
---
# <span data-ttu-id="35a84-101">Start-AzRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="35a84-101">Start-AzRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="35a84-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35a84-102">SYNOPSIS</span></span>
<span data-ttu-id="35a84-103">Запускает действие фиксации отработки отказа для объекта восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="35a84-103">Starts the commit failover action for a Site Recovery object.</span></span>

## <span data-ttu-id="35a84-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35a84-104">SYNTAX</span></span>

### <span data-ttu-id="35a84-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35a84-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35a84-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="35a84-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35a84-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35a84-107">DESCRIPTION</span></span>
<span data-ttu-id="35a84-108">Командлет **Start-AzRecoveryServicesAsrCommitFailoverJob** запускает процесс фиксации отработки отказа для объекта Azure Site Recovery после операции отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="35a84-108">The **Start-AzRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="35a84-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35a84-109">EXAMPLES</span></span>

### <span data-ttu-id="35a84-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="35a84-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="35a84-111">Запускает фиксацию отработки отказа для указанного плана восстановления и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="35a84-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="35a84-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35a84-112">PARAMETERS</span></span>

### <span data-ttu-id="35a84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35a84-113">-DefaultProfile</span></span>
<span data-ttu-id="35a84-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35a84-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="35a84-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="35a84-115">-RecoveryPlan</span></span>
<span data-ttu-id="35a84-116">Указывает объект плана восстановления ASR, соответствующий плану восстановления, для которого требуется отработка отказа.</span><span class="sxs-lookup"><span data-stu-id="35a84-116">Specifies an ASR recovery plan object corresponding to recovery plan to be failovered.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35a84-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="35a84-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="35a84-118">Указывает объект элемента, защищенного репликацией ASR, соответствующий элементу, защищенному репликацией, который должен быть отказоустойчивым.</span><span class="sxs-lookup"><span data-stu-id="35a84-118">Specifies an ASR replication protected item object corresponding to replication protected item  to be failovered.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35a84-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35a84-119">-Confirm</span></span>
<span data-ttu-id="35a84-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="35a84-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35a84-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35a84-121">-WhatIf</span></span>
<span data-ttu-id="35a84-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="35a84-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35a84-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="35a84-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35a84-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a84-124">CommonParameters</span></span>
<span data-ttu-id="35a84-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35a84-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a84-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35a84-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a84-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35a84-127">INPUTS</span></span>

### <span data-ttu-id="35a84-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="35a84-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="35a84-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="35a84-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="35a84-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35a84-130">OUTPUTS</span></span>

### <span data-ttu-id="35a84-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="35a84-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="35a84-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="35a84-132">NOTES</span></span>

## <span data-ttu-id="35a84-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35a84-133">RELATED LINKS</span></span>
