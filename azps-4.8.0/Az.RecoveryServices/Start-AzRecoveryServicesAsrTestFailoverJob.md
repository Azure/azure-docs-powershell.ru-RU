---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: 11d254fbf43a05e4e58f0d51f5226a6a7065dd50
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077682"
---
# <span data-ttu-id="53997-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="53997-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="53997-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="53997-102">SYNOPSIS</span></span>
<span data-ttu-id="53997-103">Запускает тестовую операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="53997-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="53997-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="53997-104">SYNTAX</span></span>

### <span data-ttu-id="53997-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="53997-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53997-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="53997-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53997-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="53997-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53997-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="53997-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53997-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="53997-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53997-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="53997-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53997-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53997-111">DESCRIPTION</span></span>
<span data-ttu-id="53997-112">Командлет **Start-AzRecoveryServicesAsrTestFailoverJob** запускает проверку отработки отказа для защищенного элемента или плана восстановления Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="53997-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="53997-113">Вы можете проверить, завершилось ли задание успешно с помощью командлета Get-AzRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="53997-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="53997-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="53997-114">EXAMPLES</span></span>

### <span data-ttu-id="53997-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="53997-115">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="53997-116">Запускает тестовую операцию отработки отказа для плана восстановления с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="53997-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="53997-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="53997-117">Example 2</span></span>

<span data-ttu-id="53997-118">Запускает тестовую операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="53997-118">Starts a test failover operation.</span></span> <span data-ttu-id="53997-119">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="53997-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverJob -AzureVMNetworkId <String> -Direction PrimaryToRecovery -RecoveryPlan $RP
```

## <span data-ttu-id="53997-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="53997-120">PARAMETERS</span></span>

### <span data-ttu-id="53997-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="53997-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="53997-122">Указывает идентификатор сети виртуальной машины Azure для виртуальной машины восстановления после отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="53997-122">Specifies the Azure vm network id for recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53997-123">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="53997-123">-CloudServiceCreationOption</span></span>
<span data-ttu-id="53997-124">Указывает, следует ли создавать новую облачную службу или использовать облачную службу восстановления, настроенную для виртуальной машины, для тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="53997-124">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, ByRPObject, ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:
Accepted values: UseRecoveryCloudService, AutoCreateCloudService

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53997-125">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="53997-125">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="53997-126">Задает основной файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="53997-126">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="53997-127">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="53997-127">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="53997-128">Задает вторичный файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="53997-128">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="53997-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53997-129">-DefaultProfile</span></span>
<span data-ttu-id="53997-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53997-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="53997-131">-Направление</span><span class="sxs-lookup"><span data-stu-id="53997-131">-Direction</span></span>
<span data-ttu-id="53997-132">Указывает направление перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="53997-132">Specifies the failover direction.</span></span>
<span data-ttu-id="53997-133">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="53997-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="53997-134">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="53997-134">PrimaryToRecovery</span></span>
- <span data-ttu-id="53997-135">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="53997-135">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="53997-136">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="53997-136">-RecoveryPlan</span></span>
<span data-ttu-id="53997-137">Указывает объект плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="53997-137">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53997-138">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="53997-138">-RecoveryPoint</span></span>
<span data-ttu-id="53997-139">Задает настраиваемую точку восстановления для проверки отработки отказа, на которую защищенный компьютер.</span><span class="sxs-lookup"><span data-stu-id="53997-139">Specifies a custom recovery point to test failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53997-140">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="53997-140">-RecoveryTag</span></span>
<span data-ttu-id="53997-141">Указывает тег восстановления для проверки отработки отказа на</span><span class="sxs-lookup"><span data-stu-id="53997-141">Specifies the recovery tag to test failover to</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53997-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="53997-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="53997-143">Задает защищенный элемент репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="53997-143">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53997-144">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="53997-144">-VMNetwork</span></span>
<span data-ttu-id="53997-145">Указывает сеть виртуальной машины для восстановления сайта для подключения тестовых виртуальных машин для отработки отказа (-ов).</span><span class="sxs-lookup"><span data-stu-id="53997-145">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53997-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53997-146">-Confirm</span></span>
<span data-ttu-id="53997-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="53997-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53997-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53997-148">-WhatIf</span></span>
<span data-ttu-id="53997-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="53997-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53997-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="53997-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53997-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53997-151">CommonParameters</span></span>
<span data-ttu-id="53997-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="53997-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53997-153">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53997-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53997-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="53997-154">INPUTS</span></span>

### <span data-ttu-id="53997-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="53997-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="53997-156">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="53997-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="53997-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="53997-157">OUTPUTS</span></span>

### <span data-ttu-id="53997-158">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="53997-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="53997-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="53997-159">NOTES</span></span>

## <span data-ttu-id="53997-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53997-160">RELATED LINKS</span></span>

[<span data-ttu-id="53997-161">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="53997-161">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
