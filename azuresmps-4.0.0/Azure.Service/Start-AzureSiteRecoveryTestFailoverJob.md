---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 9AE41884-C39F-4AEB-8030-96167F98C8DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b46cc27b2e5380f3cb533a4355a94170e941cd8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076028"
---
# <span data-ttu-id="ea8ef-101">Start-AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="ea8ef-101">Start-AzureSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="ea8ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea8ef-102">SYNOPSIS</span></span>
<span data-ttu-id="ea8ef-103">Запуск тестовой отработки отказа для объекта защиты восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-103">Starts a test failover for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="ea8ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea8ef-104">SYNTAX</span></span>

### <span data-ttu-id="ea8ef-105">ByPEId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ea8ef-105">ByPEId (Default)</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea8ef-106">ByRPId</span><span class="sxs-lookup"><span data-stu-id="ea8ef-106">ByRPId</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ea8ef-107">ByRPIdWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="ea8ef-107">ByRPIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea8ef-108">ByRPIdWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="ea8ef-108">ByRPIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea8ef-109">ByRPIdWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="ea8ef-109">ByRPIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> -Network <ASRNetwork> [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ea8ef-110">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="ea8ef-110">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ea8ef-111">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="ea8ef-111">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea8ef-112">ByPEIdWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="ea8ef-112">ByPEIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea8ef-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="ea8ef-113">ByRPObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea8ef-114">ByRPObjectWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="ea8ef-114">ByRPObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ea8ef-115">ByRPObjectWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="ea8ef-115">ByRPObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ea8ef-116">ByPEIdWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="ea8ef-116">ByPEIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ea8ef-117">ByPEIdWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="ea8ef-117">ByPEIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ea8ef-118">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="ea8ef-118">ByPEObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ea8ef-119">ByPEObjectWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="ea8ef-119">ByPEObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ea8ef-120">ByPEObjectWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="ea8ef-120">ByPEObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea8ef-121">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea8ef-121">DESCRIPTION</span></span>
<span data-ttu-id="ea8ef-122">Командлет **Start-AzureSiteRecoveryTestFailoverJob** запускает проверку отработки отказа для сущности или плана восстановления для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-122">The **Start-AzureSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="ea8ef-123">Вы можете проверить, успешно ли прошло задание с помощью командлета **Get-AzureRMSiteRecoveryJob** .</span><span class="sxs-lookup"><span data-stu-id="ea8ef-123">You can check whether the job succeeded by using the **Get-AzureRMSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="ea8ef-124">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea8ef-124">EXAMPLES</span></span>

### <span data-ttu-id="ea8ef-125">Пример 1: Начало тестовой отработки отказа</span><span class="sxs-lookup"><span data-stu-id="ea8ef-125">Example 1: Start a test failover</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer
PS C:\> Start-AzureSiteRecoveryTestFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="ea8ef-126">Первая команда использует командлет **Get-AzureSiteRecoveryProtectionContainer** для получения защищенного контейнера и сохраняет его в переменной $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-126">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="ea8ef-127">Вторая команда получает защищенные объекты, которые принадлежат защищенному контейнеру, который хранится в $ProtectionContainer с помощью командлета **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="ea8ef-127">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="ea8ef-128">Команда сохраняет результаты в переменной $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-128">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="ea8ef-129">Последняя команда запускает тестовую операцию отработки отказа для защищенных сущностей, хранящихся в $ProtectionEntity, и определяет направление отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-129">The final command starts the test failover operation for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

### <span data-ttu-id="ea8ef-130">Пример 2: начало тестового отработки отказа с помощью плана восстановления</span><span class="sxs-lookup"><span data-stu-id="ea8ef-130">Example 2: Start a test failover using a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan -Name "RecoveryPlan01"
Start-AzureSiteRecoveryTestFailoverJob -Direction PrimaryToRecovery -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="ea8ef-131">Эта команда получает план восстановления с именем RecoveryPlan01 для текущего хранилища Azure Site Recovery с помощью командлета **Get-AzureSiteRecoveryRecoveryPlan** .</span><span class="sxs-lookup"><span data-stu-id="ea8ef-131">This command gets the recovery plan named RecoveryPlan01 for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>
<span data-ttu-id="ea8ef-132">В этой команде план сохраняется в переменной $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-132">The command stores the plan in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="ea8ef-133">Вторая команда запускает тестовую операцию отработки отказа для плана восстановления, сохраненного в $RecoveryPlan, и определяет направление отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-133">The second command starts the test failover operation for the recovery plan stored in $RecoveryPlan and specifies the direction of the failover.</span></span>

## <span data-ttu-id="ea8ef-134">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea8ef-134">PARAMETERS</span></span>

### <span data-ttu-id="ea8ef-135">-Направление</span><span class="sxs-lookup"><span data-stu-id="ea8ef-135">-Direction</span></span>
<span data-ttu-id="ea8ef-136">Указывает направление перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-136">Specifies the failover direction.</span></span>
<span data-ttu-id="ea8ef-137">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ea8ef-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea8ef-138">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="ea8ef-138">PrimaryToRecovery</span></span>
- <span data-ttu-id="ea8ef-139">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="ea8ef-139">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8ef-140">-LogicalNetworkId</span><span class="sxs-lookup"><span data-stu-id="ea8ef-140">-LogicalNetworkId</span></span>
<span data-ttu-id="ea8ef-141">Указывает идентификатор логической сети.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-141">Specifies the ID of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithLogicalNetworkID, ByRPObjectWithLogicalNetworkID, ByPEIdWithLogicalNetworkID, ByPEObjectWithLogicalNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8ef-142">-Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="ea8ef-142">-Network</span></span>
<span data-ttu-id="ea8ef-143">Указывает сетевой объект, который будет использоваться для тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-143">Specifies the network object to use for test failover.</span></span>
<span data-ttu-id="ea8ef-144">Чтобы получить доступ к сети, используйте командлет **Get-AzureSiteRecoveryNetwork** .</span><span class="sxs-lookup"><span data-stu-id="ea8ef-144">To obtain a network, use the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByPEId, ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPObject, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID, ByPEObject, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRNetwork
Parameter Sets: ByRPIdWithVMNetwork, ByPEObjectWithVMNetwork, ByRPObjectWithVMNetwork, ByPEIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8ef-145">-NetworkType</span><span class="sxs-lookup"><span data-stu-id="ea8ef-145">-NetworkType</span></span>
<span data-ttu-id="ea8ef-146">Указывает тип сети, который будет использоваться для тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-146">Specifies the network type to use for test failover.</span></span>
<span data-ttu-id="ea8ef-147">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ea8ef-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea8ef-148">Ничего</span><span class="sxs-lookup"><span data-stu-id="ea8ef-148">None</span></span>
- <span data-ttu-id="ea8ef-149">Новые функции</span><span class="sxs-lookup"><span data-stu-id="ea8ef-149">New</span></span>
- <span data-ttu-id="ea8ef-150">Существующей</span><span class="sxs-lookup"><span data-stu-id="ea8ef-150">Existing</span></span>

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

### <span data-ttu-id="ea8ef-151">-Profile</span><span class="sxs-lookup"><span data-stu-id="ea8ef-151">-Profile</span></span>
<span data-ttu-id="ea8ef-152">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ea8ef-153">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8ef-154">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="ea8ef-154">-ProtectionContainerId</span></span>
<span data-ttu-id="ea8ef-155">Указывает идентификатор защищенного контейнера.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-155">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="ea8ef-156">Этот командлет запускает задание для защищенной виртуальной машины, которая принадлежит контейнеру, указанному этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-156">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8ef-157">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ea8ef-157">-ProtectionEntity</span></span>
<span data-ttu-id="ea8ef-158">Указывает объект сущности для защиты восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-158">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObjectWithVMNetwork, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8ef-159">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="ea8ef-159">-ProtectionEntityId</span></span>
<span data-ttu-id="ea8ef-160">Указывает идентификатор защищенной виртуальной машины, для которой необходимо запустить задание.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-160">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8ef-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ea8ef-161">-RecoveryPlan</span></span>
<span data-ttu-id="ea8ef-162">Указывает план восстановления, для которого нужно запустить задание.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-162">Specifies a recovery plan for which to start the job.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObjectWithVMNetwork, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8ef-163">-RpId</span><span class="sxs-lookup"><span data-stu-id="ea8ef-163">-RpId</span></span>
<span data-ttu-id="ea8ef-164">Указывает идентификатор плана восстановления, для которого необходимо запустить задание.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-164">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8ef-165">-VmNetworkId</span><span class="sxs-lookup"><span data-stu-id="ea8ef-165">-VmNetworkId</span></span>
<span data-ttu-id="ea8ef-166">Указывает идентификатор сети виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-166">Specifies the ID of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithVMNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithVMNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8ef-167">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="ea8ef-167">-WaitForCompletion</span></span>
<span data-ttu-id="ea8ef-168">Указывает, что командлет ожидает завершения операции, прежде чем возвращать управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-168">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="ea8ef-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea8ef-169">CommonParameters</span></span>
<span data-ttu-id="ea8ef-170">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea8ef-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea8ef-171">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea8ef-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea8ef-172">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea8ef-172">INPUTS</span></span>

## <span data-ttu-id="ea8ef-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea8ef-173">OUTPUTS</span></span>

## <span data-ttu-id="ea8ef-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea8ef-174">NOTES</span></span>

## <span data-ttu-id="ea8ef-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea8ef-175">RELATED LINKS</span></span>

[<span data-ttu-id="ea8ef-176">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ea8ef-176">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="ea8ef-177">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="ea8ef-177">Get-AzureSiteRecoveryNetwork</span></span>](./Get-AzureSiteRecoveryNetwork.md)

[<span data-ttu-id="ea8ef-178">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ea8ef-178">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="ea8ef-179">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ea8ef-179">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="ea8ef-180">Start-AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="ea8ef-180">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>](./Start-AzureSiteRecoveryUnplannedFailoverJob.md)


