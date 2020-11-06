---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrcommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 4543b127af4c0c6ca882daf93c95fb1dce614b73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558360"
---
# <span data-ttu-id="c8b86-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="c8b86-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="c8b86-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8b86-102">SYNOPSIS</span></span>
<span data-ttu-id="c8b86-103">Запускает действие фиксации отработки отказа для объекта восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="c8b86-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8b86-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8b86-104">SYNTAX</span></span>

### <span data-ttu-id="c8b86-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c8b86-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8b86-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="c8b86-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8b86-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8b86-107">DESCRIPTION</span></span>
<span data-ttu-id="c8b86-108">Командлет **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** запускает процесс фиксации отработки отказа для объекта Azure Site Recovery после операции отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="c8b86-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="c8b86-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8b86-109">EXAMPLES</span></span>

### <span data-ttu-id="c8b86-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c8b86-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="c8b86-111">Запускает фиксацию отработки отказа для указанного плана восстановления и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="c8b86-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c8b86-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8b86-112">PARAMETERS</span></span>

### <span data-ttu-id="c8b86-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8b86-113">-DefaultProfile</span></span>
<span data-ttu-id="c8b86-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8b86-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c8b86-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c8b86-115">-RecoveryPlan</span></span>
<span data-ttu-id="c8b86-116">Указывает объект плана восстановления ASR, соответствующий плану восстановления, для которого требуется отработка отказа.</span><span class="sxs-lookup"><span data-stu-id="c8b86-116">Specifies an ASR recovery plan object corresponding to recovery plan to be failovered.</span></span>

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

### <span data-ttu-id="c8b86-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c8b86-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="c8b86-118">Указывает объект элемента, защищенного репликацией ASR, соответствующий элементу, защищенному репликацией, который должен быть отказоустойчивым.</span><span class="sxs-lookup"><span data-stu-id="c8b86-118">Specifies an ASR replication protected item object corresponding to replication protected item  to be failovered.</span></span>

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

### <span data-ttu-id="c8b86-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8b86-119">-Confirm</span></span>
<span data-ttu-id="c8b86-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c8b86-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8b86-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8b86-121">-WhatIf</span></span>
<span data-ttu-id="c8b86-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c8b86-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8b86-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c8b86-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8b86-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8b86-124">CommonParameters</span></span>
<span data-ttu-id="c8b86-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8b86-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8b86-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8b86-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8b86-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8b86-127">INPUTS</span></span>

### <span data-ttu-id="c8b86-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c8b86-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="c8b86-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c8b86-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="c8b86-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8b86-130">OUTPUTS</span></span>

### <span data-ttu-id="c8b86-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c8b86-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c8b86-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8b86-132">NOTES</span></span>

## <span data-ttu-id="c8b86-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8b86-133">RELATED LINKS</span></span>
