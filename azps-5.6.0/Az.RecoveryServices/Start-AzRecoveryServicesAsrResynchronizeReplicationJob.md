---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 0675756b21c5af56ff3dc3fdff3b48d3bc9c999c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987577"
---
# <span data-ttu-id="1a65b-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="1a65b-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="1a65b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a65b-102">SYNOPSIS</span></span>
<span data-ttu-id="1a65b-103">Запускает синхронизацию репликации.</span><span class="sxs-lookup"><span data-stu-id="1a65b-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="1a65b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1a65b-104">SYNTAX</span></span>

### <span data-ttu-id="1a65b-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1a65b-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a65b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1a65b-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a65b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a65b-107">DESCRIPTION</span></span>
<span data-ttu-id="1a65b-108">Для указанного защищенного элемента начинается повторная синхронизация репликации для указанного защищенного элемента с начала работы на **start-AzRecoveryServicesAsrResynchronizeReplicationJob.**</span><span class="sxs-lookup"><span data-stu-id="1a65b-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="1a65b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1a65b-109">EXAMPLES</span></span>

### <span data-ttu-id="1a65b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1a65b-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="1a65b-111">Запускает задание для повторной синхронизации репликации для защищенного переданного элемента.</span><span class="sxs-lookup"><span data-stu-id="1a65b-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="1a65b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a65b-112">PARAMETERS</span></span>

### <span data-ttu-id="1a65b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a65b-113">-DefaultProfile</span></span>
<span data-ttu-id="1a65b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a65b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a65b-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1a65b-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1a65b-116">Элемент, защищенный репликацией ASR, для повторной синхронизации репликации.</span><span class="sxs-lookup"><span data-stu-id="1a65b-116">ASR replication protected item to resynchronize replication for.</span></span>

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

### <span data-ttu-id="1a65b-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a65b-117">-ResourceId</span></span>
<span data-ttu-id="1a65b-118">ИД ресурса элемента, защищенного репликацией, для повторной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1a65b-118">Resource Id of replication protected item to resynchronize.</span></span>

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

### <span data-ttu-id="1a65b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a65b-119">-Confirm</span></span>
<span data-ttu-id="1a65b-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a65b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a65b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a65b-121">-WhatIf</span></span>
<span data-ttu-id="1a65b-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a65b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a65b-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1a65b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a65b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a65b-124">CommonParameters</span></span>
<span data-ttu-id="1a65b-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a65b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a65b-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a65b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a65b-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a65b-127">INPUTS</span></span>

### <span data-ttu-id="1a65b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1a65b-128">System.String</span></span>

### <span data-ttu-id="1a65b-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1a65b-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1a65b-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1a65b-130">OUTPUTS</span></span>

### <span data-ttu-id="1a65b-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="1a65b-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1a65b-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1a65b-132">NOTES</span></span>

## <span data-ttu-id="1a65b-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a65b-133">RELATED LINKS</span></span>
