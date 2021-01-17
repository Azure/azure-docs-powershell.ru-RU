---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: 11d254fbf43a05e4e58f0d51f5226a6a7065dd50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421263"
---
# <span data-ttu-id="8aab3-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="8aab3-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="8aab3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8aab3-102">SYNOPSIS</span></span>
<span data-ttu-id="8aab3-103">Запускает тестовую отбойную операцию.</span><span class="sxs-lookup"><span data-stu-id="8aab3-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="8aab3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8aab3-104">SYNTAX</span></span>

### <span data-ttu-id="8aab3-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8aab3-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8aab3-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="8aab3-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8aab3-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="8aab3-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8aab3-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="8aab3-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8aab3-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="8aab3-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8aab3-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="8aab3-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8aab3-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8aab3-111">DESCRIPTION</span></span>
<span data-ttu-id="8aab3-112">Для этого запускается отбой тестирования защищенного элемента или плана восстановления сайта Azure с использованием начните отсе одной из защищенных служб **AzRecoveryServicesAsrTestFailoverJob.**</span><span class="sxs-lookup"><span data-stu-id="8aab3-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="8aab3-113">С помощью Get-AzRecoveryServicesAsrJob можно проверить успешное задание.</span><span class="sxs-lookup"><span data-stu-id="8aab3-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="8aab3-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8aab3-114">EXAMPLES</span></span>

### <span data-ttu-id="8aab3-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8aab3-115">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="8aab3-116">Запускает тестовую отбойную операцию для плана восстановления с указанными параметрами и возвращает задание ASR, используемую для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="8aab3-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8aab3-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8aab3-117">Example 2</span></span>

<span data-ttu-id="8aab3-118">Запускает тестовую отбойную операцию.</span><span class="sxs-lookup"><span data-stu-id="8aab3-118">Starts a test failover operation.</span></span> <span data-ttu-id="8aab3-119">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="8aab3-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverJob -AzureVMNetworkId <String> -Direction PrimaryToRecovery -RecoveryPlan $RP
```

## <span data-ttu-id="8aab3-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8aab3-120">PARAMETERS</span></span>

### <span data-ttu-id="8aab3-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="8aab3-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="8aab3-122">Определяет сетевой id Azure vm для восстановления VM после отсека.</span><span class="sxs-lookup"><span data-stu-id="8aab3-122">Specifies the Azure vm network id for recovery VM after failover.</span></span>

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

### <span data-ttu-id="8aab3-123">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="8aab3-123">-CloudServiceCreationOption</span></span>
<span data-ttu-id="8aab3-124">Указывает, следует ли создать новую облачную службу или использовать облачную службу восстановления, настроенную для VM-решения.</span><span class="sxs-lookup"><span data-stu-id="8aab3-124">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

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

### <span data-ttu-id="8aab3-125">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="8aab3-125">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="8aab3-126">Указывает основной файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="8aab3-126">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="8aab3-127">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="8aab3-127">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="8aab3-128">Определяет дополнительный файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="8aab3-128">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="8aab3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aab3-129">-DefaultProfile</span></span>
<span data-ttu-id="8aab3-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8aab3-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8aab3-131">-Direction</span><span class="sxs-lookup"><span data-stu-id="8aab3-131">-Direction</span></span>
<span data-ttu-id="8aab3-132">Определяет направление отбойного пути.</span><span class="sxs-lookup"><span data-stu-id="8aab3-132">Specifies the failover direction.</span></span>
<span data-ttu-id="8aab3-133">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="8aab3-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8aab3-134">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="8aab3-134">PrimaryToRecovery</span></span>
- <span data-ttu-id="8aab3-135">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="8aab3-135">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="8aab3-136">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8aab3-136">-RecoveryPlan</span></span>
<span data-ttu-id="8aab3-137">Указывает объект плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="8aab3-137">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="8aab3-138">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8aab3-138">-RecoveryPoint</span></span>
<span data-ttu-id="8aab3-139">Указывает настраиваемую точку восстановления, на которая будет протестирована защищенная компьютер.</span><span class="sxs-lookup"><span data-stu-id="8aab3-139">Specifies a custom recovery point to test failover the protected machine to.</span></span>

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

### <span data-ttu-id="8aab3-140">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="8aab3-140">-RecoveryTag</span></span>
<span data-ttu-id="8aab3-141">Указывает тег восстановления для проверки отбойного сбойного скайвера, чтобы</span><span class="sxs-lookup"><span data-stu-id="8aab3-141">Specifies the recovery tag to test failover to</span></span>

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

### <span data-ttu-id="8aab3-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8aab3-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8aab3-143">Определяет защищенный репликацией asR элемент.</span><span class="sxs-lookup"><span data-stu-id="8aab3-143">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="8aab3-144">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="8aab3-144">-VMNetwork</span></span>
<span data-ttu-id="8aab3-145">Указывает сеть виртуальной машины восстановления сайта, к которая подключается к тестовой виртуальной машине от сбойной работы.</span><span class="sxs-lookup"><span data-stu-id="8aab3-145">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="8aab3-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8aab3-146">-Confirm</span></span>
<span data-ttu-id="8aab3-147">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8aab3-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8aab3-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8aab3-148">-WhatIf</span></span>
<span data-ttu-id="8aab3-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8aab3-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8aab3-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8aab3-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8aab3-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aab3-151">CommonParameters</span></span>
<span data-ttu-id="8aab3-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aab3-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aab3-153">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8aab3-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aab3-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8aab3-154">INPUTS</span></span>

### <span data-ttu-id="8aab3-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8aab3-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="8aab3-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8aab3-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="8aab3-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8aab3-157">OUTPUTS</span></span>

### <span data-ttu-id="8aab3-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="8aab3-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8aab3-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8aab3-159">NOTES</span></span>

## <span data-ttu-id="8aab3-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8aab3-160">RELATED LINKS</span></span>

[<span data-ttu-id="8aab3-161">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8aab3-161">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
