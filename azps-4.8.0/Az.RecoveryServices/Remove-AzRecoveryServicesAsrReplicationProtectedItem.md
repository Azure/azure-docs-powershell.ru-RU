---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 71731c0a6f4f0bb917cb7490c1647add71b9a893
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236654"
---
# <span data-ttu-id="13d8f-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="13d8f-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="13d8f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="13d8f-103">Остановка и отключение репликации для элемента, защищенного с помощью репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="13d8f-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="13d8f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13d8f-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13d8f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13d8f-105">DESCRIPTION</span></span>
<span data-ttu-id="13d8f-106">Командлет **Remove-AzRecoveryServicesAsrReplicationProtectedItem** отключает репликацию указанного элемента, защищенного репликацией Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="13d8f-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="13d8f-107">Эта операция приводит к остановке репликации для защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="13d8f-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="13d8f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13d8f-108">EXAMPLES</span></span>

### <span data-ttu-id="13d8f-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="13d8f-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="13d8f-110">Запускает операцию отключения репликации для указанного элемента, защищенного репликацией, и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="13d8f-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="13d8f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13d8f-111">PARAMETERS</span></span>

### <span data-ttu-id="13d8f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13d8f-112">-DefaultProfile</span></span>
<span data-ttu-id="13d8f-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13d8f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="13d8f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="13d8f-114">-Force</span></span>
<span data-ttu-id="13d8f-115">Принудительное выполнение команды без дополнительных предупреждений.</span><span class="sxs-lookup"><span data-stu-id="13d8f-115">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="13d8f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13d8f-116">-InputObject</span></span>
<span data-ttu-id="13d8f-117">Входной объект для командлета: объект элемента, защищенного репликацией ASR, соответствующий элементу, защищенному репликацией, для которого требуется отключить репликацию.</span><span class="sxs-lookup"><span data-stu-id="13d8f-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

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

### <span data-ttu-id="13d8f-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="13d8f-118">-WaitForCompletion</span></span>
<span data-ttu-id="13d8f-119">Указывает, что перед возвратом командлет должен дождаться завершения операции.</span><span class="sxs-lookup"><span data-stu-id="13d8f-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="13d8f-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13d8f-120">-Confirm</span></span>
<span data-ttu-id="13d8f-121">Укажите, требуется ли подтверждение.</span><span class="sxs-lookup"><span data-stu-id="13d8f-121">Specify if confirmation is required.</span></span> <span data-ttu-id="13d8f-122">Установите для параметра Confirm значение $false, чтобы пропустить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="13d8f-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="13d8f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13d8f-123">-WhatIf</span></span>
<span data-ttu-id="13d8f-124">Показывает, что произойдет, если командлет выполняется без фактического выполнения командлета.</span><span class="sxs-lookup"><span data-stu-id="13d8f-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="13d8f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d8f-125">CommonParameters</span></span>
<span data-ttu-id="13d8f-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13d8f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d8f-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13d8f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d8f-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13d8f-128">INPUTS</span></span>

### <span data-ttu-id="13d8f-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="13d8f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="13d8f-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13d8f-130">OUTPUTS</span></span>

### <span data-ttu-id="13d8f-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="13d8f-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="13d8f-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="13d8f-132">NOTES</span></span>

## <span data-ttu-id="13d8f-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13d8f-133">RELATED LINKS</span></span>

[<span data-ttu-id="13d8f-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="13d8f-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="13d8f-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="13d8f-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="13d8f-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="13d8f-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)