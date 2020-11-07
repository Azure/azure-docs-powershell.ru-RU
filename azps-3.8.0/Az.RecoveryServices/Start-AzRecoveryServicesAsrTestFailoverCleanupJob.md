---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 24fbbd3d0d9d2e165a2edfbf289b434c886b0b0c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912706"
---
# <span data-ttu-id="42529-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="42529-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="42529-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42529-102">SYNOPSIS</span></span>
<span data-ttu-id="42529-103">Запускает тестовую операцию очистки отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="42529-103">Starts the test failover cleanup operation.</span></span>

## <span data-ttu-id="42529-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42529-104">SYNTAX</span></span>

### <span data-ttu-id="42529-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="42529-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42529-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="42529-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42529-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="42529-107">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42529-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42529-108">DESCRIPTION</span></span>
<span data-ttu-id="42529-109">Командлет **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** запускает тестовую операцию очистки отработки отказа для элемента, защищенного репликацией, или план восстановления, на котором выполнялась тестовая отработка отказа.</span><span class="sxs-lookup"><span data-stu-id="42529-109">The **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="42529-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42529-110">EXAMPLES</span></span>

### <span data-ttu-id="42529-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="42529-111">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

<span data-ttu-id="42529-112">Задание для отслеживания очистки тестовой отработки отказа для службы репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="42529-112">Job to track test failover Cleanup of an Azure Site Recovery replication protected item.</span></span>

### <span data-ttu-id="42529-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="42529-113">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan $recoveryPlan -Comment "testing done"
```

<span data-ttu-id="42529-114">Задание для отслеживания очистки тестового отработки отказа в службе Azure Site Recovery recoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="42529-114">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

## <span data-ttu-id="42529-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42529-115">PARAMETERS</span></span>

### <span data-ttu-id="42529-116">-Примечание</span><span class="sxs-lookup"><span data-stu-id="42529-116">-Comment</span></span>
<span data-ttu-id="42529-117">Примечание пользователя для тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="42529-117">User Comment for Test Failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42529-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42529-118">-DefaultProfile</span></span>
<span data-ttu-id="42529-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42529-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42529-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="42529-120">-RecoveryPlan</span></span>
<span data-ttu-id="42529-121">План восстановления для выполнения тестовой очистки при отработке отказа.</span><span class="sxs-lookup"><span data-stu-id="42529-121">Recovery Plan to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="42529-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="42529-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="42529-123">Элемент, защищенный репликацией, для которого требуется выполнить тестовую очистку отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="42529-123">Replication Protected Item to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="42529-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42529-124">-ResourceId</span></span>
<span data-ttu-id="42529-125">Идентификатор ресурса для плана защищенного элемента или восстановления для cleaningup тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="42529-125">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42529-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42529-126">-Confirm</span></span>
<span data-ttu-id="42529-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="42529-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42529-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42529-128">-WhatIf</span></span>
<span data-ttu-id="42529-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="42529-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42529-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="42529-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42529-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42529-131">CommonParameters</span></span>
<span data-ttu-id="42529-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42529-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42529-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42529-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42529-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42529-134">INPUTS</span></span>

### <span data-ttu-id="42529-135">System. String</span><span class="sxs-lookup"><span data-stu-id="42529-135">System.String</span></span>

### <span data-ttu-id="42529-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="42529-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="42529-137">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="42529-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="42529-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42529-138">OUTPUTS</span></span>

### <span data-ttu-id="42529-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="42529-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="42529-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="42529-140">NOTES</span></span>

## <span data-ttu-id="42529-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42529-141">RELATED LINKS</span></span>
