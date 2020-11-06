---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 1df32bfcf049346b3f434b252a413eef020d0b77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563419"
---
# <span data-ttu-id="fc3d1-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fc3d1-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="fc3d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc3d1-102">SYNOPSIS</span></span>
<span data-ttu-id="fc3d1-103">Остановка и отключение репликации для элемента, защищенного с помощью репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="fc3d1-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc3d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc3d1-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc3d1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc3d1-105">DESCRIPTION</span></span>
<span data-ttu-id="fc3d1-106">Командлет **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** отключает репликацию указанного элемента, защищенного репликацией Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="fc3d1-106">The **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="fc3d1-107">Эта операция приводит к остановке репликации для защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="fc3d1-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="fc3d1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc3d1-108">EXAMPLES</span></span>

### <span data-ttu-id="fc3d1-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fc3d1-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="fc3d1-110">Запускает операцию отключения репликации для указанного элемента, защищенного репликацией, и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="fc3d1-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="fc3d1-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc3d1-111">PARAMETERS</span></span>

### <span data-ttu-id="fc3d1-112">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc3d1-112">-Confirm</span></span>
<span data-ttu-id="fc3d1-113">Укажите, требуется ли подтверждение.</span><span class="sxs-lookup"><span data-stu-id="fc3d1-113">Specify if confirmation is required.</span></span> <span data-ttu-id="fc3d1-114">Установите для параметра Confirm значение $false, чтобы пропустить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="fc3d1-114">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="fc3d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc3d1-115">-DefaultProfile</span></span>
<span data-ttu-id="fc3d1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc3d1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="fc3d1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fc3d1-117">-Force</span></span>
<span data-ttu-id="fc3d1-118">Принудительное выполнение команды без дополнительных предупреждений.</span><span class="sxs-lookup"><span data-stu-id="fc3d1-118">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc3d1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc3d1-119">-InputObject</span></span>
<span data-ttu-id="fc3d1-120">Входной объект для командлета: объект элемента, защищенного репликацией ASR, соответствующий элементу, защищенному репликацией, для которого требуется отключить репликацию.</span><span class="sxs-lookup"><span data-stu-id="fc3d1-120">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc3d1-121">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="fc3d1-121">-WaitForCompletion</span></span>
<span data-ttu-id="fc3d1-122">Указывает, что перед возвратом командлет должен дождаться завершения операции.</span><span class="sxs-lookup"><span data-stu-id="fc3d1-122">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc3d1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc3d1-123">-WhatIf</span></span>
<span data-ttu-id="fc3d1-124">Показывает, что произойдет, если командлет выполняется без фактического выполнения командлета.</span><span class="sxs-lookup"><span data-stu-id="fc3d1-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="fc3d1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc3d1-125">CommonParameters</span></span>
<span data-ttu-id="fc3d1-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc3d1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc3d1-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc3d1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc3d1-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc3d1-128">INPUTS</span></span>

### <span data-ttu-id="fc3d1-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fc3d1-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="fc3d1-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc3d1-130">OUTPUTS</span></span>

### <span data-ttu-id="fc3d1-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fc3d1-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fc3d1-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc3d1-132">NOTES</span></span>

## <span data-ttu-id="fc3d1-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc3d1-133">RELATED LINKS</span></span>

[<span data-ttu-id="fc3d1-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fc3d1-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="fc3d1-135">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fc3d1-135">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="fc3d1-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fc3d1-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
