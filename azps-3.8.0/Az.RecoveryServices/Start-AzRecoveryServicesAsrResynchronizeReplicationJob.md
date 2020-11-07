---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 0429976c64ed6e7989208c28fea1ee0a008436c8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912709"
---
# <span data-ttu-id="fc699-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="fc699-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="fc699-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc699-102">SYNOPSIS</span></span>
<span data-ttu-id="fc699-103">Запуск повторной синхронизации репликации.</span><span class="sxs-lookup"><span data-stu-id="fc699-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="fc699-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc699-104">SYNTAX</span></span>

### <span data-ttu-id="fc699-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fc699-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc699-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fc699-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc699-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc699-107">DESCRIPTION</span></span>
<span data-ttu-id="fc699-108">Командлет **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** запускает повторную синхронизацию репликации для указанного защищенного элемента, если он находится в состоянии "требуется повторная синхронизация".</span><span class="sxs-lookup"><span data-stu-id="fc699-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="fc699-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc699-109">EXAMPLES</span></span>

### <span data-ttu-id="fc699-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fc699-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="fc699-111">Запускает задание для повторной синхронизации репликации при успешном элементе, защищенном репликацией.</span><span class="sxs-lookup"><span data-stu-id="fc699-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="fc699-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc699-112">PARAMETERS</span></span>

### <span data-ttu-id="fc699-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc699-113">-DefaultProfile</span></span>
<span data-ttu-id="fc699-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc699-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc699-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fc699-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="fc699-116">Защищенный элемент репликации ASR для повторной синхронизации репликации.</span><span class="sxs-lookup"><span data-stu-id="fc699-116">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc699-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc699-117">-ResourceId</span></span>
<span data-ttu-id="fc699-118">Идентификатор ресурса защищенного элемента репликации для повторной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fc699-118">Resource Id of replication protected item to resynchronize.</span></span>

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

### <span data-ttu-id="fc699-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc699-119">-Confirm</span></span>
<span data-ttu-id="fc699-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fc699-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc699-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc699-121">-WhatIf</span></span>
<span data-ttu-id="fc699-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fc699-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc699-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fc699-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc699-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc699-124">CommonParameters</span></span>
<span data-ttu-id="fc699-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc699-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc699-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc699-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc699-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc699-127">INPUTS</span></span>

### <span data-ttu-id="fc699-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fc699-128">System.String</span></span>

### <span data-ttu-id="fc699-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fc699-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="fc699-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc699-130">OUTPUTS</span></span>

### <span data-ttu-id="fc699-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fc699-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fc699-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc699-132">NOTES</span></span>

## <span data-ttu-id="fc699-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc699-133">RELATED LINKS</span></span>
