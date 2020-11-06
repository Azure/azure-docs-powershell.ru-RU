---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 423ec89745b21176c714c1c2e956d4320c28b034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557236"
---
# <span data-ttu-id="17e33-101">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="17e33-101">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="17e33-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="17e33-102">SYNOPSIS</span></span>
<span data-ttu-id="17e33-103">Запускает тестовую операцию очистки отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="17e33-103">Starts the test failover cleanup operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17e33-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="17e33-104">SYNTAX</span></span>

### <span data-ttu-id="17e33-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="17e33-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17e33-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="17e33-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17e33-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="17e33-107">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17e33-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17e33-108">DESCRIPTION</span></span>
<span data-ttu-id="17e33-109">Командлет **Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob** запускает тестовую операцию очистки отработки отказа для элемента, защищенного репликацией, или план восстановления, на котором выполнялась тестовая отработка отказа.</span><span class="sxs-lookup"><span data-stu-id="17e33-109">The **Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="17e33-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="17e33-110">EXAMPLES</span></span>

### <span data-ttu-id="17e33-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="17e33-111">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

<span data-ttu-id="17e33-112">Задание для отслеживания очистки тестовой отработки отказа для службы репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="17e33-112">Job to track test failover Cleanup of an Azure Site Recovery replication protected item.</span></span>

### <span data-ttu-id="17e33-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="17e33-113">Example 2</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $recoveryPlan -Comments "testing done"
```

<span data-ttu-id="17e33-114">Задание для отслеживания очистки тестового отработки отказа в службе Azure Site Recovery recoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="17e33-114">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

## <span data-ttu-id="17e33-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="17e33-115">PARAMETERS</span></span>

### <span data-ttu-id="17e33-116">-Примечание</span><span class="sxs-lookup"><span data-stu-id="17e33-116">-Comment</span></span>
<span data-ttu-id="17e33-117">Примечание пользователя для тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="17e33-117">User Comment for Test Failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e33-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17e33-118">-Confirm</span></span>
<span data-ttu-id="17e33-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="17e33-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17e33-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17e33-120">-DefaultProfile</span></span>
<span data-ttu-id="17e33-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="17e33-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17e33-122">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="17e33-122">-RecoveryPlan</span></span>
<span data-ttu-id="17e33-123">План восстановления для выполнения тестовой очистки при отработке отказа.</span><span class="sxs-lookup"><span data-stu-id="17e33-123">Recovery Plan to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="17e33-124">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="17e33-124">-ReplicationProtectedItem</span></span>
<span data-ttu-id="17e33-125">Элемент, защищенный репликацией, для которого требуется выполнить тестовую очистку отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="17e33-125">Replication Protected Item to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="17e33-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17e33-126">-ResourceId</span></span>
<span data-ttu-id="17e33-127">Идентификатор ресурса для плана защищенного элемента или восстановления для cleaningup тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="17e33-127">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e33-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17e33-128">-WhatIf</span></span>
<span data-ttu-id="17e33-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="17e33-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17e33-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="17e33-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17e33-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17e33-131">CommonParameters</span></span>
<span data-ttu-id="17e33-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="17e33-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17e33-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17e33-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17e33-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="17e33-134">INPUTS</span></span>

### <span data-ttu-id="17e33-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="17e33-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="17e33-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="17e33-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="17e33-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="17e33-137">OUTPUTS</span></span>

### <span data-ttu-id="17e33-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="17e33-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="17e33-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="17e33-139">NOTES</span></span>

## <span data-ttu-id="17e33-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17e33-140">RELATED LINKS</span></span>
