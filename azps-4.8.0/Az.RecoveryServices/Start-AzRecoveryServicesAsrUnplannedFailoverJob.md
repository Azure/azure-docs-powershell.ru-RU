---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 61bb846067127b8e7d0a4deca0dd9a726d9dd1f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077678"
---
# <span data-ttu-id="ad219-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="ad219-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="ad219-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad219-102">SYNOPSIS</span></span>
<span data-ttu-id="ad219-103">Запускает внеплановую операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="ad219-103">Starts an unplanned failover operation.</span></span>

## <span data-ttu-id="ad219-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad219-104">SYNTAX</span></span>

### <span data-ttu-id="ad219-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad219-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad219-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="ad219-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad219-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="ad219-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad219-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad219-108">DESCRIPTION</span></span>
<span data-ttu-id="ad219-109">Командлет **Start-AzRecoveryServicesAsrUnplannedFailoverJob** запускает внеплановая отработка отказа защищенного элемента или плана восстановления для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ad219-109">The **Start-AzRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="ad219-110">Вы можете проверить, завершилось ли задание успешно с помощью командлета Get-AzRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="ad219-110">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="ad219-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad219-111">EXAMPLES</span></span>

### <span data-ttu-id="ad219-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ad219-112">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $RecoveryNetwork
```

<span data-ttu-id="ad219-113">Запускает незапланированную операцию отработки отказа для плана восстановления с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="ad219-113">Starts the unplanned failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="ad219-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ad219-114">Example 2</span></span>

<span data-ttu-id="ad219-115">Запускает внеплановую операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="ad219-115">Starts an unplanned failover operation.</span></span> <span data-ttu-id="ad219-116">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="ad219-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrUnplannedFailoverJob -Direction PrimaryToRecovery -RecoveryPoint $rp[0] -ReplicationProtectedItem $ReplicationProtectedItem
```

## <span data-ttu-id="ad219-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad219-117">PARAMETERS</span></span>

### <span data-ttu-id="ad219-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ad219-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="ad219-119">Задает путь к файлу основного сертификата для шифрования данных для отработки отказа защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="ad219-119">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad219-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ad219-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="ad219-121">Указывает путь к вторичному сертификату шифрования данных для отработки отказа защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="ad219-121">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad219-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad219-122">-DefaultProfile</span></span>
<span data-ttu-id="ad219-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad219-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ad219-124">-Направление</span><span class="sxs-lookup"><span data-stu-id="ad219-124">-Direction</span></span>
<span data-ttu-id="ad219-125">Указывает направление перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="ad219-125">Specifies the failover direction.</span></span>
<span data-ttu-id="ad219-126">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ad219-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ad219-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="ad219-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="ad219-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="ad219-128">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad219-129">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="ad219-129">-PerformSourceSideAction</span></span>
<span data-ttu-id="ad219-130">Выполнение операции на стороне источника перед началом внеплановой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="ad219-130">Perform operation in source side before starting unplanned failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad219-131">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ad219-131">-RecoveryPlan</span></span>
<span data-ttu-id="ad219-132">Указывает объект плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="ad219-132">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad219-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ad219-133">-RecoveryPoint</span></span>
<span data-ttu-id="ad219-134">Задает настраиваемую точку восстановления для отработки отказа защищенного компьютера.</span><span class="sxs-lookup"><span data-stu-id="ad219-134">Specifies a custom recovery point to failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad219-135">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="ad219-135">-RecoveryTag</span></span>
<span data-ttu-id="ad219-136">Указывает тег восстановления для перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="ad219-136">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad219-137">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ad219-137">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ad219-138">Указывает защищенный элемент репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ad219-138">Specifies an azure site recovery replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad219-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad219-139">-Confirm</span></span>
<span data-ttu-id="ad219-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ad219-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad219-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad219-141">-WhatIf</span></span>
<span data-ttu-id="ad219-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ad219-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad219-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ad219-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad219-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad219-144">CommonParameters</span></span>
<span data-ttu-id="ad219-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad219-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad219-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad219-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad219-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad219-147">INPUTS</span></span>

### <span data-ttu-id="ad219-148">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ad219-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="ad219-149">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ad219-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="ad219-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad219-150">OUTPUTS</span></span>

### <span data-ttu-id="ad219-151">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ad219-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ad219-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad219-152">NOTES</span></span>

## <span data-ttu-id="ad219-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad219-153">RELATED LINKS</span></span>

[<span data-ttu-id="ad219-154">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ad219-154">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
