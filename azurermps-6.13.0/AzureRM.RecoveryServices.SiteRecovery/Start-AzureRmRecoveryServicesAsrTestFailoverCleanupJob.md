---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 5d99c9cad96a3f0c4fb877ecd15f8450eb89c4fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732099"
---
# <span data-ttu-id="726b1-101">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="726b1-101">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="726b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="726b1-102">SYNOPSIS</span></span>
<span data-ttu-id="726b1-103">Запускает тестовую операцию очистки отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="726b1-103">Starts the test failover cleanup operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="726b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="726b1-104">SYNTAX</span></span>

### <span data-ttu-id="726b1-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="726b1-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="726b1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="726b1-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="726b1-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="726b1-107">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="726b1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="726b1-108">DESCRIPTION</span></span>
<span data-ttu-id="726b1-109">Командлет **Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob** запускает тестовую операцию очистки отработки отказа для элемента, защищенного репликацией, или план восстановления, на котором выполнялась тестовая отработка отказа.</span><span class="sxs-lookup"><span data-stu-id="726b1-109">The **Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="726b1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="726b1-110">EXAMPLES</span></span>

### <span data-ttu-id="726b1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="726b1-111">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

<span data-ttu-id="726b1-112">Задание для отслеживания очистки тестовой отработки отказа для службы репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="726b1-112">Job to track test failover Cleanup of an Azure Site Recovery replication protected item.</span></span>

### <span data-ttu-id="726b1-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="726b1-113">Example 2</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan $recoveryPlan -Comment "testing done"
```

<span data-ttu-id="726b1-114">Задание для отслеживания очистки тестового отработки отказа в службе Azure Site Recovery recoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="726b1-114">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

## <span data-ttu-id="726b1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="726b1-115">PARAMETERS</span></span>

### <span data-ttu-id="726b1-116">-Примечание</span><span class="sxs-lookup"><span data-stu-id="726b1-116">-Comment</span></span>
<span data-ttu-id="726b1-117">Примечание пользователя для тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="726b1-117">User Comment for Test Failover.</span></span>

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

### <span data-ttu-id="726b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="726b1-118">-DefaultProfile</span></span>
<span data-ttu-id="726b1-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="726b1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726b1-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="726b1-120">-RecoveryPlan</span></span>
<span data-ttu-id="726b1-121">План восстановления для выполнения тестовой очистки при отработке отказа.</span><span class="sxs-lookup"><span data-stu-id="726b1-121">Recovery Plan to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="726b1-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="726b1-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="726b1-123">Элемент, защищенный репликацией, для которого требуется выполнить тестовую очистку отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="726b1-123">Replication Protected Item to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="726b1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="726b1-124">-ResourceId</span></span>
<span data-ttu-id="726b1-125">Идентификатор ресурса для плана защищенного элемента или восстановления для cleaningup тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="726b1-125">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

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

### <span data-ttu-id="726b1-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="726b1-126">-Confirm</span></span>
<span data-ttu-id="726b1-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="726b1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="726b1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="726b1-128">-WhatIf</span></span>
<span data-ttu-id="726b1-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="726b1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="726b1-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="726b1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="726b1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="726b1-131">CommonParameters</span></span>
<span data-ttu-id="726b1-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="726b1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="726b1-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="726b1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="726b1-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="726b1-134">INPUTS</span></span>

### <span data-ttu-id="726b1-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="726b1-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="726b1-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="726b1-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="726b1-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="726b1-137">OUTPUTS</span></span>

### <span data-ttu-id="726b1-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="726b1-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="726b1-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="726b1-139">NOTES</span></span>

## <span data-ttu-id="726b1-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="726b1-140">RELATED LINKS</span></span>
