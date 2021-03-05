---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: fca503fbca9a20d9b6f9e8cb07c5e703e6ecc280
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995291"
---
# <span data-ttu-id="bf098-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="bf098-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="bf098-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf098-102">SYNOPSIS</span></span>
<span data-ttu-id="bf098-103">Начало незапланированной отбойной операции.</span><span class="sxs-lookup"><span data-stu-id="bf098-103">Starts an unplanned failover operation.</span></span>

## <span data-ttu-id="bf098-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bf098-104">SYNTAX</span></span>

### <span data-ttu-id="bf098-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bf098-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf098-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="bf098-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf098-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="bf098-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf098-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf098-108">DESCRIPTION</span></span>
<span data-ttu-id="bf098-109">Для **начала работы с azRecoveryServicesAsrUnplannedFailoverJob** начинается незапланированный сбой защищенного элемента или плана восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="bf098-109">The **Start-AzRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="bf098-110">С помощью Get-AzRecoveryServicesAsrJob можно проверить успешное задание.</span><span class="sxs-lookup"><span data-stu-id="bf098-110">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="bf098-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bf098-111">EXAMPLES</span></span>

### <span data-ttu-id="bf098-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bf098-112">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $RecoveryNetwork
```

<span data-ttu-id="bf098-113">Запускает незапланированную отбойную операцию для плана восстановления с указанными параметрами и возвращает задание ASR, используемую для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="bf098-113">Starts the unplanned failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="bf098-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bf098-114">Example 2</span></span>

<span data-ttu-id="bf098-115">Начало незапланированной отбойной операции.</span><span class="sxs-lookup"><span data-stu-id="bf098-115">Starts an unplanned failover operation.</span></span> <span data-ttu-id="bf098-116">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="bf098-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrUnplannedFailoverJob -Direction PrimaryToRecovery -RecoveryPoint $rp[0] -ReplicationProtectedItem $ReplicationProtectedItem
```

## <span data-ttu-id="bf098-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf098-117">PARAMETERS</span></span>

### <span data-ttu-id="bf098-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="bf098-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="bf098-119">Путь к основному файлу сертификата шифрования данных для отбойного действия защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="bf098-119">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="bf098-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="bf098-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="bf098-121">Путь к дополнительному файлу сертификата шифрования данных для отбойного действия защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="bf098-121">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="bf098-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf098-122">-DefaultProfile</span></span>
<span data-ttu-id="bf098-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bf098-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="bf098-124">-Direction</span><span class="sxs-lookup"><span data-stu-id="bf098-124">-Direction</span></span>
<span data-ttu-id="bf098-125">Определяет направление отбойного пути.</span><span class="sxs-lookup"><span data-stu-id="bf098-125">Specifies the failover direction.</span></span>
<span data-ttu-id="bf098-126">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="bf098-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bf098-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="bf098-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="bf098-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="bf098-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="bf098-129">-PerformSourceSideaction</span><span class="sxs-lookup"><span data-stu-id="bf098-129">-PerformSourceSideAction</span></span>
<span data-ttu-id="bf098-130">Перед запуском незапланированной отбойной работы выполните операцию на стороне источника.</span><span class="sxs-lookup"><span data-stu-id="bf098-130">Perform operation in source side before starting unplanned failover.</span></span>

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

### <span data-ttu-id="bf098-131">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bf098-131">-RecoveryPlan</span></span>
<span data-ttu-id="bf098-132">Указывает объект плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="bf098-132">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="bf098-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="bf098-133">-RecoveryPoint</span></span>
<span data-ttu-id="bf098-134">Указывает настраиваемую точку восстановления для отбойного восстановления защищенного компьютера.</span><span class="sxs-lookup"><span data-stu-id="bf098-134">Specifies a custom recovery point to failover the protected machine to.</span></span>

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

### <span data-ttu-id="bf098-135">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="bf098-135">-RecoveryTag</span></span>
<span data-ttu-id="bf098-136">Указывает тег восстановления, который нужно отоправить.</span><span class="sxs-lookup"><span data-stu-id="bf098-136">Specifies the recovery tag to failover to.</span></span>

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

### <span data-ttu-id="bf098-137">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bf098-137">-ReplicationProtectedItem</span></span>
<span data-ttu-id="bf098-138">Указывает элемент, защищенный репликацией для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="bf098-138">Specifies an azure site recovery replication protected item.</span></span>

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

### <span data-ttu-id="bf098-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf098-139">-Confirm</span></span>
<span data-ttu-id="bf098-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bf098-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf098-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf098-141">-WhatIf</span></span>
<span data-ttu-id="bf098-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf098-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf098-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bf098-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf098-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf098-144">CommonParameters</span></span>
<span data-ttu-id="bf098-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf098-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf098-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf098-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf098-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf098-147">INPUTS</span></span>

### <span data-ttu-id="bf098-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bf098-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="bf098-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bf098-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="bf098-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bf098-150">OUTPUTS</span></span>

### <span data-ttu-id="bf098-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="bf098-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bf098-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bf098-152">NOTES</span></span>

## <span data-ttu-id="bf098-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf098-153">RELATED LINKS</span></span>

[<span data-ttu-id="bf098-154">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="bf098-154">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
