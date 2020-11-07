---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 48a17c0b2bd8c1d62de1b3ebd5eccc5171d65837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905786"
---
# <span data-ttu-id="e319c-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="e319c-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="e319c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e319c-102">SYNOPSIS</span></span>
<span data-ttu-id="e319c-103">Запуск повторной синхронизации репликации.</span><span class="sxs-lookup"><span data-stu-id="e319c-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="e319c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e319c-104">SYNTAX</span></span>

### <span data-ttu-id="e319c-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e319c-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e319c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e319c-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e319c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e319c-107">DESCRIPTION</span></span>
<span data-ttu-id="e319c-108">Командлет **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** запускает повторную синхронизацию репликации для указанного защищенного элемента, если он находится в состоянии "требуется повторная синхронизация".</span><span class="sxs-lookup"><span data-stu-id="e319c-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="e319c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e319c-109">EXAMPLES</span></span>

### <span data-ttu-id="e319c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e319c-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="e319c-111">Запускает задание для повторной синхронизации репликации при успешном элементе, защищенном репликацией.</span><span class="sxs-lookup"><span data-stu-id="e319c-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="e319c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e319c-112">PARAMETERS</span></span>

### <span data-ttu-id="e319c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e319c-113">-DefaultProfile</span></span>
<span data-ttu-id="e319c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e319c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e319c-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e319c-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e319c-116">Защищенный элемент репликации ASR для повторной синхронизации репликации.</span><span class="sxs-lookup"><span data-stu-id="e319c-116">ASR replication protected item to resynchronize replication for.</span></span>

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

### <span data-ttu-id="e319c-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e319c-117">-ResourceId</span></span>
<span data-ttu-id="e319c-118">Идентификатор ресурса защищенного элемента репликации для повторной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e319c-118">Resource Id of replication protected item to resynchronize.</span></span>

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

### <span data-ttu-id="e319c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e319c-119">-Confirm</span></span>
<span data-ttu-id="e319c-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e319c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e319c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e319c-121">-WhatIf</span></span>
<span data-ttu-id="e319c-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e319c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e319c-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e319c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e319c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e319c-124">CommonParameters</span></span>
<span data-ttu-id="e319c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e319c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e319c-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e319c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e319c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e319c-127">INPUTS</span></span>

### <span data-ttu-id="e319c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e319c-128">System.String</span></span>

### <span data-ttu-id="e319c-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e319c-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e319c-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e319c-130">OUTPUTS</span></span>

### <span data-ttu-id="e319c-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e319c-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e319c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="e319c-132">NOTES</span></span>

## <span data-ttu-id="e319c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e319c-133">RELATED LINKS</span></span>
