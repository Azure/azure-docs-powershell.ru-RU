---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: bd8a06eb85658fe2ec06d65c0663550be78d1552
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558383"
---
# <span data-ttu-id="2ab19-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2ab19-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="2ab19-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ab19-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab19-103">Остановка и отключение репликации для элемента, защищенного с помощью репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2ab19-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ab19-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ab19-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ab19-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ab19-105">DESCRIPTION</span></span>
<span data-ttu-id="2ab19-106">Командлет **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** отключает репликацию указанного элемента, защищенного репликацией Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2ab19-106">The **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="2ab19-107">Эта операция приводит к остановке репликации для защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="2ab19-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="2ab19-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ab19-108">EXAMPLES</span></span>

### <span data-ttu-id="2ab19-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2ab19-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="2ab19-110">Запускает операцию отключения репликации для указанного элемента, защищенного репликацией, и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="2ab19-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2ab19-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ab19-111">PARAMETERS</span></span>

### <span data-ttu-id="2ab19-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ab19-112">-DefaultProfile</span></span>
<span data-ttu-id="2ab19-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ab19-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2ab19-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2ab19-114">-Force</span></span>
<span data-ttu-id="2ab19-115">Принудительное выполнение команды без дополнительных предупреждений.</span><span class="sxs-lookup"><span data-stu-id="2ab19-115">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="2ab19-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ab19-116">-InputObject</span></span>
<span data-ttu-id="2ab19-117">Входной объект для командлета: объект элемента, защищенного репликацией ASR, соответствующий элементу, защищенному репликацией, для которого требуется отключить репликацию.</span><span class="sxs-lookup"><span data-stu-id="2ab19-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

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

### <span data-ttu-id="2ab19-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="2ab19-118">-WaitForCompletion</span></span>
<span data-ttu-id="2ab19-119">Указывает, что перед возвратом командлет должен дождаться завершения операции.</span><span class="sxs-lookup"><span data-stu-id="2ab19-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="2ab19-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ab19-120">-Confirm</span></span>
<span data-ttu-id="2ab19-121">Укажите, требуется ли подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2ab19-121">Specify if confirmation is required.</span></span> <span data-ttu-id="2ab19-122">Установите для параметра Confirm значение $false, чтобы пропустить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2ab19-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="2ab19-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ab19-123">-WhatIf</span></span>
<span data-ttu-id="2ab19-124">Показывает, что произойдет, если командлет выполняется без фактического выполнения командлета.</span><span class="sxs-lookup"><span data-stu-id="2ab19-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="2ab19-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab19-125">CommonParameters</span></span>
<span data-ttu-id="2ab19-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ab19-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab19-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ab19-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab19-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ab19-128">INPUTS</span></span>

### <span data-ttu-id="2ab19-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2ab19-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="2ab19-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ab19-130">OUTPUTS</span></span>

### <span data-ttu-id="2ab19-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2ab19-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2ab19-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ab19-132">NOTES</span></span>

## <span data-ttu-id="2ab19-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ab19-133">RELATED LINKS</span></span>

[<span data-ttu-id="2ab19-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2ab19-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="2ab19-135">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2ab19-135">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="2ab19-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2ab19-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
