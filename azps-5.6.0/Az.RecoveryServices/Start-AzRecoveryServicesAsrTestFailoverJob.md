---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: b5a06683e5254077a63d4c0b1933d51d9c1ad8e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987563"
---
# <span data-ttu-id="67766-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="67766-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="67766-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67766-102">SYNOPSIS</span></span>
<span data-ttu-id="67766-103">Запускает тестовую отбойную операцию.</span><span class="sxs-lookup"><span data-stu-id="67766-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="67766-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="67766-104">SYNTAX</span></span>

### <span data-ttu-id="67766-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="67766-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67766-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="67766-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67766-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="67766-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67766-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="67766-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67766-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="67766-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67766-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="67766-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67766-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67766-111">DESCRIPTION</span></span>
<span data-ttu-id="67766-112">Для **начала работы с azRecoveryServicesAsrTestFailoverJob** запускается отбой тестирования для защищенного элемента или плана восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="67766-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="67766-113">С помощью Get-AzRecoveryServicesAsrJob можно проверить успешное задание.</span><span class="sxs-lookup"><span data-stu-id="67766-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="67766-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="67766-114">EXAMPLES</span></span>

### <span data-ttu-id="67766-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="67766-115">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="67766-116">Запускает тестовую отбойную операцию для плана восстановления с указанными параметрами и возвращает задание ASR, используемую для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="67766-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="67766-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="67766-117">Example 2</span></span>

<span data-ttu-id="67766-118">Запускает тестовую отбойную операцию.</span><span class="sxs-lookup"><span data-stu-id="67766-118">Starts a test failover operation.</span></span> <span data-ttu-id="67766-119">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="67766-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverJob -AzureVMNetworkId <String> -Direction PrimaryToRecovery -RecoveryPlan $RP
```

## <span data-ttu-id="67766-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67766-120">PARAMETERS</span></span>

### <span data-ttu-id="67766-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="67766-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="67766-122">Определяет сетевой id Azure vm для восстановления VM после отсека.</span><span class="sxs-lookup"><span data-stu-id="67766-122">Specifies the Azure vm network id for recovery VM after failover.</span></span>

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

### <span data-ttu-id="67766-123">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="67766-123">-CloudServiceCreationOption</span></span>
<span data-ttu-id="67766-124">Указывает, следует ли создать новую облачную службу или использовать облачную службу восстановления, настроенную для VM-решения.</span><span class="sxs-lookup"><span data-stu-id="67766-124">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

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

### <span data-ttu-id="67766-125">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="67766-125">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="67766-126">Указывает основной файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="67766-126">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="67766-127">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="67766-127">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="67766-128">Определяет дополнительный файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="67766-128">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="67766-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67766-129">-DefaultProfile</span></span>
<span data-ttu-id="67766-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67766-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="67766-131">-Direction</span><span class="sxs-lookup"><span data-stu-id="67766-131">-Direction</span></span>
<span data-ttu-id="67766-132">Определяет направление отбойного пути.</span><span class="sxs-lookup"><span data-stu-id="67766-132">Specifies the failover direction.</span></span>
<span data-ttu-id="67766-133">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="67766-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67766-134">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="67766-134">PrimaryToRecovery</span></span>
- <span data-ttu-id="67766-135">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="67766-135">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="67766-136">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="67766-136">-RecoveryPlan</span></span>
<span data-ttu-id="67766-137">Указывает объект плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="67766-137">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="67766-138">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="67766-138">-RecoveryPoint</span></span>
<span data-ttu-id="67766-139">Указывает настраиваемую точку восстановления, на которая будет протестирована защищенная компьютер.</span><span class="sxs-lookup"><span data-stu-id="67766-139">Specifies a custom recovery point to test failover the protected machine to.</span></span>

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

### <span data-ttu-id="67766-140">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="67766-140">-RecoveryTag</span></span>
<span data-ttu-id="67766-141">Указывает тег восстановления для проверки отбойного сбойного скайвера, чтобы</span><span class="sxs-lookup"><span data-stu-id="67766-141">Specifies the recovery tag to test failover to</span></span>

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

### <span data-ttu-id="67766-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="67766-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="67766-143">Определяет защищенный репликацией asR элемент.</span><span class="sxs-lookup"><span data-stu-id="67766-143">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="67766-144">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="67766-144">-VMNetwork</span></span>
<span data-ttu-id="67766-145">Указывает сеть виртуальной машины восстановления сайта, к которая подключается к тестовой виртуальной машине от сбойной работы.</span><span class="sxs-lookup"><span data-stu-id="67766-145">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="67766-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67766-146">-Confirm</span></span>
<span data-ttu-id="67766-147">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67766-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67766-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67766-148">-WhatIf</span></span>
<span data-ttu-id="67766-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67766-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67766-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="67766-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67766-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67766-151">CommonParameters</span></span>
<span data-ttu-id="67766-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67766-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67766-153">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67766-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67766-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67766-154">INPUTS</span></span>

### <span data-ttu-id="67766-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="67766-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="67766-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="67766-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="67766-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67766-157">OUTPUTS</span></span>

### <span data-ttu-id="67766-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="67766-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="67766-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="67766-159">NOTES</span></span>

## <span data-ttu-id="67766-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67766-160">RELATED LINKS</span></span>

[<span data-ttu-id="67766-161">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="67766-161">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
