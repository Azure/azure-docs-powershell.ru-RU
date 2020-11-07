---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 17836b900e56fdfd5d90211c9bceb79fce87c66e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734789"
---
# <span data-ttu-id="46141-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="46141-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="46141-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46141-102">SYNOPSIS</span></span>
<span data-ttu-id="46141-103">Остановка и отключение репликации для элемента, защищенного с помощью репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="46141-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46141-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46141-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46141-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46141-105">DESCRIPTION</span></span>
<span data-ttu-id="46141-106">Командлет **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** отключает репликацию указанного элемента, защищенного репликацией Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="46141-106">The **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="46141-107">Эта операция приводит к остановке репликации для защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="46141-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="46141-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46141-108">EXAMPLES</span></span>

### <span data-ttu-id="46141-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="46141-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="46141-110">Запускает операцию отключения репликации для указанного элемента, защищенного репликацией, и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="46141-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="46141-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46141-111">PARAMETERS</span></span>

### <span data-ttu-id="46141-112">-Force</span><span class="sxs-lookup"><span data-stu-id="46141-112">-Force</span></span>
<span data-ttu-id="46141-113">Принудительное выполнение команды без дополнительных предупреждений.</span><span class="sxs-lookup"><span data-stu-id="46141-113">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="46141-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46141-114">-InputObject</span></span>
<span data-ttu-id="46141-115">Входной объект для командлета: объект элемента, защищенного репликацией ASR, соответствующий элементу, защищенному репликацией, для которого требуется отключить репликацию.</span><span class="sxs-lookup"><span data-stu-id="46141-115">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

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

### <span data-ttu-id="46141-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="46141-116">-WaitForCompletion</span></span>
<span data-ttu-id="46141-117">Указывает, что перед возвратом командлет должен дождаться завершения операции.</span><span class="sxs-lookup"><span data-stu-id="46141-117">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="46141-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46141-118">-Confirm</span></span>
<span data-ttu-id="46141-119">Укажите, требуется ли подтверждение.</span><span class="sxs-lookup"><span data-stu-id="46141-119">Specify if confirmation is required.</span></span> <span data-ttu-id="46141-120">Установите для параметра Confirm значение $false, чтобы пропустить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="46141-120">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="46141-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46141-121">-WhatIf</span></span>
<span data-ttu-id="46141-122">Показывает, что произойдет, если командлет выполняется без фактического выполнения командлета.</span><span class="sxs-lookup"><span data-stu-id="46141-122">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="46141-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46141-123">CommonParameters</span></span>
<span data-ttu-id="46141-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46141-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46141-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46141-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46141-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46141-126">INPUTS</span></span>

### <span data-ttu-id="46141-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="46141-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="46141-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46141-128">OUTPUTS</span></span>

### <span data-ttu-id="46141-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="46141-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="46141-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="46141-130">NOTES</span></span>

## <span data-ttu-id="46141-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46141-131">RELATED LINKS</span></span>

[<span data-ttu-id="46141-132">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="46141-132">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="46141-133">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="46141-133">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="46141-134">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="46141-134">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
