---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: ba31be7094da4c4c17fa8c674728b8c32bfa2b8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557232"
---
# <span data-ttu-id="1c485-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="1c485-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="1c485-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1c485-102">SYNOPSIS</span></span>
<span data-ttu-id="1c485-103">Запускает внеплановую операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="1c485-103">Starts a unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c485-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1c485-104">SYNTAX</span></span>

### <span data-ttu-id="1c485-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1c485-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c485-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="1c485-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c485-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="1c485-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c485-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c485-108">DESCRIPTION</span></span>
<span data-ttu-id="1c485-109">Командлет **Start-AzureRmRecoveryServicesAsrTestFailoverJob** запускает проверку отработки отказа для защищенного элемента или плана восстановления Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1c485-109">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="1c485-110">Вы можете проверить, завершилось ли задание успешно с помощью командлета Get-AzureRmRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="1c485-110">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="1c485-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1c485-111">EXAMPLES</span></span>

### <span data-ttu-id="1c485-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1c485-112">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="1c485-113">Запускает тестовую операцию отработки отказа для плана восстановления с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="1c485-113">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1c485-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1c485-114">PARAMETERS</span></span>

### <span data-ttu-id="1c485-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c485-115">-Confirm</span></span>
<span data-ttu-id="1c485-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1c485-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c485-117">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1c485-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="1c485-118">Задает путь к файлу основного сертификата для шифрования данных для отработки отказа защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="1c485-118">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="1c485-119">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1c485-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="1c485-120">Указывает путь к вторичному сертификату шифрования данных для отработки отказа защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="1c485-120">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="1c485-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c485-121">-DefaultProfile</span></span>
<span data-ttu-id="1c485-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c485-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="1c485-123">-Направление</span><span class="sxs-lookup"><span data-stu-id="1c485-123">-Direction</span></span>
<span data-ttu-id="1c485-124">Указывает направление перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="1c485-124">Specifies the failover direction.</span></span>
<span data-ttu-id="1c485-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1c485-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1c485-126">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="1c485-126">PrimaryToRecovery</span></span>
- <span data-ttu-id="1c485-127">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="1c485-127">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="1c485-128">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="1c485-128">-PerformSourceSideAction</span></span>
<span data-ttu-id="1c485-129">Выполнение операции на стороне источника перед началом внеплановой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="1c485-129">Perform operation in source side before starting unplanned failover.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c485-130">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1c485-130">-RecoveryPlan</span></span>
<span data-ttu-id="1c485-131">Указывает объект плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="1c485-131">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c485-132">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1c485-132">-RecoveryPoint</span></span>
<span data-ttu-id="1c485-133">Задает настраиваемую точку восстановления для отработки отказа защищенного компьютера.</span><span class="sxs-lookup"><span data-stu-id="1c485-133">Specifies a custom recovery point to failover the protected machine to.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c485-134">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="1c485-134">-RecoveryTag</span></span>
<span data-ttu-id="1c485-135">Указывает тег восстановления для перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="1c485-135">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObject
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c485-136">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1c485-136">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1c485-137">Указывает защищенный элемент репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1c485-137">Specifies an azure site recovery replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c485-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c485-138">-WhatIf</span></span>
<span data-ttu-id="1c485-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1c485-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c485-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1c485-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c485-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c485-141">CommonParameters</span></span>
<span data-ttu-id="1c485-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1c485-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c485-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c485-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c485-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1c485-144">INPUTS</span></span>

### <span data-ttu-id="1c485-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1c485-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="1c485-146">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1c485-146">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1c485-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c485-147">OUTPUTS</span></span>

### <span data-ttu-id="1c485-148">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1c485-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1c485-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="1c485-149">NOTES</span></span>

## <span data-ttu-id="1c485-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c485-150">RELATED LINKS</span></span>

[<span data-ttu-id="1c485-151">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="1c485-151">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
