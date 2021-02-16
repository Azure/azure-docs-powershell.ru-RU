---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 71731c0a6f4f0bb917cb7490c1647add71b9a893
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220681"
---
# <span data-ttu-id="7797f-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7797f-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="7797f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7797f-102">SYNOPSIS</span></span>
<span data-ttu-id="7797f-103">Остановка и отключение репликации для элемента, защищенного репликацией для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="7797f-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="7797f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7797f-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7797f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7797f-105">DESCRIPTION</span></span>
<span data-ttu-id="7797f-106">**Cmdlet Remove-AzRecoveryServicesAsrReplicationProtectedItem** отключает репликацию указанного элемента, защищенного репликацией для восстановления сайтов Azure.</span><span class="sxs-lookup"><span data-stu-id="7797f-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="7797f-107">Эта операция приводит к остановке репликации для защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="7797f-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="7797f-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7797f-108">EXAMPLES</span></span>

### <span data-ttu-id="7797f-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7797f-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="7797f-110">Запускает операцию отключения репликации для указанного элемента, защищенного репликацией, и возвращает задание ASR, используемую для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="7797f-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7797f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7797f-111">PARAMETERS</span></span>

### <span data-ttu-id="7797f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7797f-112">-DefaultProfile</span></span>
<span data-ttu-id="7797f-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7797f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7797f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="7797f-114">-Force</span></span>
<span data-ttu-id="7797f-115">Принудительно выполнить команду, не предоставляя дополнительное предупреждение.</span><span class="sxs-lookup"><span data-stu-id="7797f-115">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7797f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7797f-116">-InputObject</span></span>
<span data-ttu-id="7797f-117">Входной объект для cmdlet: объект asR protecttion protecttion item, соответствующий элементу, защищенного репликацией, для которого репликация должна быть отключена.</span><span class="sxs-lookup"><span data-stu-id="7797f-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7797f-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="7797f-118">-WaitForCompletion</span></span>
<span data-ttu-id="7797f-119">Указывает на то, что перед возвратом cmdlet должен дождаться завершения операции.</span><span class="sxs-lookup"><span data-stu-id="7797f-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7797f-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7797f-120">-Confirm</span></span>
<span data-ttu-id="7797f-121">Укажите, требуется ли подтверждение.</span><span class="sxs-lookup"><span data-stu-id="7797f-121">Specify if confirmation is required.</span></span> <span data-ttu-id="7797f-122">Установите для параметра подтверждения значение $false, чтобы пропустить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="7797f-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="7797f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7797f-123">-WhatIf</span></span>
<span data-ttu-id="7797f-124">Показывает, что произойдет, если выполняется cmdlet без его выполнения.</span><span class="sxs-lookup"><span data-stu-id="7797f-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="7797f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7797f-125">CommonParameters</span></span>
<span data-ttu-id="7797f-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7797f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7797f-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7797f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7797f-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7797f-128">INPUTS</span></span>

### <span data-ttu-id="7797f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7797f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="7797f-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7797f-130">OUTPUTS</span></span>

### <span data-ttu-id="7797f-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="7797f-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7797f-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7797f-132">NOTES</span></span>

## <span data-ttu-id="7797f-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7797f-133">RELATED LINKS</span></span>

[<span data-ttu-id="7797f-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7797f-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7797f-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7797f-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7797f-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7797f-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
