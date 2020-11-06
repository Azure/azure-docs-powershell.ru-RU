---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: d547de0af8d4f7b4f98a572d95dcc023d975fc2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567540"
---
# <span data-ttu-id="e08ab-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="e08ab-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="e08ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e08ab-102">SYNOPSIS</span></span>
<span data-ttu-id="e08ab-103">Запускает тестовую операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="e08ab-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e08ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e08ab-104">SYNTAX</span></span>

### <span data-ttu-id="e08ab-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e08ab-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e08ab-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="e08ab-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e08ab-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="e08ab-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e08ab-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="e08ab-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e08ab-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="e08ab-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e08ab-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="e08ab-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e08ab-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e08ab-111">DESCRIPTION</span></span>
<span data-ttu-id="e08ab-112">Командлет **Start-AzureRmRecoveryServicesAsrTestFailoverJob** запускает проверку отработки отказа для защищенного элемента или плана восстановления Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e08ab-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="e08ab-113">Вы можете проверить, завершилось ли задание успешно с помощью командлета Get-AzureRmRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="e08ab-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="e08ab-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e08ab-114">EXAMPLES</span></span>

### <span data-ttu-id="e08ab-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e08ab-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="e08ab-116">Запускает тестовую операцию отработки отказа для плана восстановления с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="e08ab-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e08ab-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e08ab-117">PARAMETERS</span></span>

### <span data-ttu-id="e08ab-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="e08ab-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="e08ab-119">Указывает идентификатор виртуальной сети Azure для подключения теста со сбоем для проверки поверх виртуальных машин (-ов).</span><span class="sxs-lookup"><span data-stu-id="e08ab-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e08ab-120">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="e08ab-120">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="e08ab-121">Задает основной файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="e08ab-121">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="e08ab-122">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="e08ab-122">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="e08ab-123">Задает вторичный файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="e08ab-123">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="e08ab-124">-Направление</span><span class="sxs-lookup"><span data-stu-id="e08ab-124">-Direction</span></span>
<span data-ttu-id="e08ab-125">Указывает направление перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="e08ab-125">Specifies the failover direction.</span></span>
<span data-ttu-id="e08ab-126">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e08ab-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e08ab-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="e08ab-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="e08ab-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="e08ab-128">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e08ab-129">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e08ab-129">-RecoveryPlan</span></span>
<span data-ttu-id="e08ab-130">Указывает объект плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="e08ab-130">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e08ab-131">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e08ab-131">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e08ab-132">Задает защищенный элемент репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="e08ab-132">Specifies an ASR replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e08ab-133">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="e08ab-133">-VMNetwork</span></span>
<span data-ttu-id="e08ab-134">Указывает сеть виртуальной машины для восстановления сайта для подключения тестовых виртуальных машин для отработки отказа (-ов).</span><span class="sxs-lookup"><span data-stu-id="e08ab-134">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e08ab-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e08ab-135">-Confirm</span></span>
<span data-ttu-id="e08ab-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e08ab-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e08ab-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e08ab-137">-WhatIf</span></span>
<span data-ttu-id="e08ab-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e08ab-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e08ab-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e08ab-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e08ab-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e08ab-140">CommonParameters</span></span>
<span data-ttu-id="e08ab-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e08ab-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e08ab-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e08ab-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e08ab-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e08ab-143">INPUTS</span></span>

### <span data-ttu-id="e08ab-144">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e08ab-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="e08ab-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e08ab-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e08ab-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e08ab-146">OUTPUTS</span></span>

### <span data-ttu-id="e08ab-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e08ab-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e08ab-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="e08ab-148">NOTES</span></span>

## <span data-ttu-id="e08ab-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e08ab-149">RELATED LINKS</span></span>

[<span data-ttu-id="e08ab-150">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e08ab-150">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
