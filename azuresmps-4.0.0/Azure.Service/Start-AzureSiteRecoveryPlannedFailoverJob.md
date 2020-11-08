---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2575F5C4-A276-49CE-AB0C-726F359DA6F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f71138e47c851097fe36ca294784fc571b6369f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075751"
---
# <span data-ttu-id="e8851-101">Start-AzureSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="e8851-101">Start-AzureSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="e8851-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8851-102">SYNOPSIS</span></span>
<span data-ttu-id="e8851-103">Запускает плановую операцию отработки отказа для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="e8851-103">Starts a Site Recovery planned failover operation.</span></span>

## <span data-ttu-id="e8851-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8851-104">SYNTAX</span></span>

### <span data-ttu-id="e8851-105">ByRPId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e8851-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e8851-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="e8851-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e8851-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="e8851-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e8851-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="e8851-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e8851-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8851-109">DESCRIPTION</span></span>
<span data-ttu-id="e8851-110">Командлет **Start-AzureSiteRecoveryPlannedFailoverJob** запускает плановую отработку отказа для сущности или плана восстановления для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e8851-110">The **Start-AzureSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="e8851-111">С помощью командлета **Get-AzureSiteRecoveryJob** можно проверить, успешно ли прошло задание.</span><span class="sxs-lookup"><span data-stu-id="e8851-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="e8851-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8851-112">EXAMPLES</span></span>

### <span data-ttu-id="e8851-113">Пример 1: начало запланированного задания отработки отказа</span><span class="sxs-lookup"><span data-stu-id="e8851-113">Example 1: Start a planned failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryPlannedFailoverJob -Direction PrimaryToRecovery -ProtectionEntity $Protected -Optimize ForDowntime
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

<span data-ttu-id="e8851-114">Первая команда получает все защищенные контейнеры в текущем хранилище Azure Site Recovery с помощью командлета **Get-AzureSiteRecoveryProtectionContainer** , а затем сохраняет результаты в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="e8851-114">The first command gets all protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>
<span data-ttu-id="e8851-115">В этом примере есть один контейнер.</span><span class="sxs-lookup"><span data-stu-id="e8851-115">In this example, there is a single container.</span></span>

<span data-ttu-id="e8851-116">Вторая команда получает защищенные виртуальные машины, которые принадлежат контейнеру, хранящемуся в $Container с помощью командлета **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="e8851-116">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="e8851-117">Команда сохраняет результаты в переменной $Protected.</span><span class="sxs-lookup"><span data-stu-id="e8851-117">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="e8851-118">Последняя команда запускает задание отработки отказа в направлении PrimaryToRecovery для защищенных виртуальных машин, которые хранятся в $Protected.</span><span class="sxs-lookup"><span data-stu-id="e8851-118">The final command starts the failover job in the direction PrimaryToRecovery for the protected virtual machines stored in $Protected.</span></span>

## <span data-ttu-id="e8851-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8851-119">PARAMETERS</span></span>

### <span data-ttu-id="e8851-120">-Направление</span><span class="sxs-lookup"><span data-stu-id="e8851-120">-Direction</span></span>
<span data-ttu-id="e8851-121">Указывает направление отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="e8851-121">Specifies the direction of the failover.</span></span>
<span data-ttu-id="e8851-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e8851-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e8851-123">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="e8851-123">PrimaryToRecovery</span></span>
- <span data-ttu-id="e8851-124">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="e8851-124">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="e8851-125">-OPTIMIZE</span><span class="sxs-lookup"><span data-stu-id="e8851-125">-Optimize</span></span>
<span data-ttu-id="e8851-126">Указывает, для чего нужно оптимизировать.</span><span class="sxs-lookup"><span data-stu-id="e8851-126">Specifies what to optimize for.</span></span>
<span data-ttu-id="e8851-127">Этот параметр применяется для отработки отказа с сайта Azure на локальном сайте, требующего значительную синхронизацию данных.</span><span class="sxs-lookup"><span data-stu-id="e8851-127">This parameter applies for failover from an Azure site to an on-premise site which requires a significant data synchronization.</span></span>
<span data-ttu-id="e8851-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e8851-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e8851-129">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="e8851-129">ForDowntime</span></span>
- <span data-ttu-id="e8851-130">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="e8851-130">ForSynchronization</span></span>

<span data-ttu-id="e8851-131">Если указан **ForDowntime** , это указывает на то, что данные синхронизируются перед переходом на другой ресурс для минимизации простоев.</span><span class="sxs-lookup"><span data-stu-id="e8851-131">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="e8851-132">Синхронизация выполняется без выключения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e8851-132">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="e8851-133">После завершения синхронизации задание будет приостановлено.</span><span class="sxs-lookup"><span data-stu-id="e8851-133">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="e8851-134">Возобновите задачу, чтобы выполнить дополнительную операцию синхронизации, которая завершает работу виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e8851-134">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="e8851-135">Если указан **ForSynchronization** , это указывает на то, что данные синхронизируются во время отработки отказа, поэтому синхронизация данных свернута.</span><span class="sxs-lookup"><span data-stu-id="e8851-135">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="e8851-136">Поскольку этот параметр включен, виртуальная машина немедленно завершает работу.</span><span class="sxs-lookup"><span data-stu-id="e8851-136">Because this setting is enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="e8851-137">Синхронизация начинается после завершения работы, чтобы завершить операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="e8851-137">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="e8851-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="e8851-138">-Profile</span></span>
<span data-ttu-id="e8851-139">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e8851-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e8851-140">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e8851-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e8851-141">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="e8851-141">-ProtectionContainerId</span></span>
<span data-ttu-id="e8851-142">Указывает идентификатор защищенного контейнера, для которого нужно запустить задание.</span><span class="sxs-lookup"><span data-stu-id="e8851-142">Specifies the ID of the protected container for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8851-143">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e8851-143">-ProtectionEntity</span></span>
<span data-ttu-id="e8851-144">Указывает объект сущности для защиты восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="e8851-144">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8851-145">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="e8851-145">-ProtectionEntityId</span></span>
<span data-ttu-id="e8851-146">Указывает объект **ASRProtectionEntity** , для которого нужно запустить задание.</span><span class="sxs-lookup"><span data-stu-id="e8851-146">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="e8851-147">Чтобы получить объект **ASRProtectionEntity** , используйте командлет **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="e8851-147">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8851-148">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e8851-148">-RecoveryPlan</span></span>
<span data-ttu-id="e8851-149">Указывает объект плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="e8851-149">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="e8851-150">-RPId</span><span class="sxs-lookup"><span data-stu-id="e8851-150">-RPId</span></span>
<span data-ttu-id="e8851-151">Указывает идентификатор плана восстановления, для которого необходимо запустить задание.</span><span class="sxs-lookup"><span data-stu-id="e8851-151">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8851-152">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="e8851-152">-WaitForCompletion</span></span>
<span data-ttu-id="e8851-153">Указывает, что командлет ожидает завершения операции, прежде чем возвращать управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e8851-153">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="e8851-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8851-154">CommonParameters</span></span>
<span data-ttu-id="e8851-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8851-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8851-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8851-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8851-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8851-157">INPUTS</span></span>

## <span data-ttu-id="e8851-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8851-158">OUTPUTS</span></span>

## <span data-ttu-id="e8851-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8851-159">NOTES</span></span>

## <span data-ttu-id="e8851-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8851-160">RELATED LINKS</span></span>

[<span data-ttu-id="e8851-161">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e8851-161">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="e8851-162">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e8851-162">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


