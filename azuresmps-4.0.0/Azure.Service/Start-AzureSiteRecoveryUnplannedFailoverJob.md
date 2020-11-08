---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AC73119B-BB76-425B-AA44-44502028ECC4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a74a02f219b5bb64957ab919168cb79ccf681869
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075806"
---
# <span data-ttu-id="74139-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="74139-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="74139-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74139-102">SYNOPSIS</span></span>
<span data-ttu-id="74139-103">Запускает внеплановая отработка отказа для объекта защиты восстановления сайта или плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="74139-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

## <span data-ttu-id="74139-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74139-104">SYNTAX</span></span>

### <span data-ttu-id="74139-105">ByRPId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="74139-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RPId <String> -Direction <String> [-PrimaryAction <Boolean>]
 [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="74139-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="74139-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="74139-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="74139-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PrimaryAction <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="74139-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="74139-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="74139-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74139-109">DESCRIPTION</span></span>
<span data-ttu-id="74139-110">Командлет **Start-AzureSiteRecoveryUnplannedFailoverJob** запускает внеплановую отработку отказа для сущности или плана восстановления для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="74139-110">The **Start-AzureSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="74139-111">С помощью командлета **Get-AzureSiteRecoveryJob** можно проверить, успешно ли прошло задание.</span><span class="sxs-lookup"><span data-stu-id="74139-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="74139-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74139-112">EXAMPLES</span></span>

### <span data-ttu-id="74139-113">Пример 1: Начало незапланированного задания отработки отказа</span><span class="sxs-lookup"><span data-stu-id="74139-113">Example 1: Start an unplanned failover job</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer 
PS C:\> Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
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

<span data-ttu-id="74139-114">Первая команда получает защищенный контейнер с помощью командлета **Get-AzureSiteRecoveryProtectionContainer** , а затем сохраняет его в переменной $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="74139-114">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="74139-115">Вторая команда получает защищенные объекты, которые принадлежат защищенному контейнеру, который хранится в $ProtectionContainer с помощью командлета **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="74139-115">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="74139-116">Команда сохраняет результаты в переменной $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="74139-116">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="74139-117">Последняя команда запускает отработку отказа для защищенных сущностей, хранящихся в $ProtectionEntity, и определяет направление отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="74139-117">The final command starts the failover for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

## <span data-ttu-id="74139-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74139-118">PARAMETERS</span></span>

### <span data-ttu-id="74139-119">-Направление</span><span class="sxs-lookup"><span data-stu-id="74139-119">-Direction</span></span>
<span data-ttu-id="74139-120">Указывает направление отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="74139-120">Specifies the direction of the failover.</span></span>
<span data-ttu-id="74139-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="74139-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="74139-122">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="74139-122">PrimaryToRecovery</span></span>
- <span data-ttu-id="74139-123">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="74139-123">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="74139-124">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="74139-124">-PerformSourceSideActions</span></span>
<span data-ttu-id="74139-125">Указывает на то, что действие может выполнять действия на стороне источника.</span><span class="sxs-lookup"><span data-stu-id="74139-125">Indicates that the action can perform source side actions.</span></span>

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

### <span data-ttu-id="74139-126">-PerformSourceSiteOperations</span><span class="sxs-lookup"><span data-stu-id="74139-126">-PerformSourceSiteOperations</span></span>
<span data-ttu-id="74139-127">Указывает на то, что операции с исходным сайтом можно выполнить.</span><span class="sxs-lookup"><span data-stu-id="74139-127">Indicates that source site operations can be performed.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByPEId, ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74139-128">-PrimaryAction</span><span class="sxs-lookup"><span data-stu-id="74139-128">-PrimaryAction</span></span>
<span data-ttu-id="74139-129">Указывает, что требуются действия первичного сайта.</span><span class="sxs-lookup"><span data-stu-id="74139-129">Indicates that  primary site actions are required.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByRPId, ByRPObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74139-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="74139-130">-Profile</span></span>
<span data-ttu-id="74139-131">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="74139-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="74139-132">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="74139-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="74139-133">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="74139-133">-ProtectionContainerId</span></span>
<span data-ttu-id="74139-134">Указывает идентификатор защищенного контейнера.</span><span class="sxs-lookup"><span data-stu-id="74139-134">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="74139-135">Этот командлет запускает задание для защищенной виртуальной машины, которая принадлежит контейнеру, указанному этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="74139-135">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="74139-136">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="74139-136">-ProtectionEntity</span></span>
<span data-ttu-id="74139-137">Указывает объект сущности для защиты восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="74139-137">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="74139-138">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="74139-138">-ProtectionEntityId</span></span>
<span data-ttu-id="74139-139">Указывает идентификатор защищенной виртуальной машины, для которой необходимо запустить задание.</span><span class="sxs-lookup"><span data-stu-id="74139-139">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

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

### <span data-ttu-id="74139-140">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="74139-140">-RecoveryPlan</span></span>
<span data-ttu-id="74139-141">Указывает объект плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="74139-141">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="74139-142">-RPId</span><span class="sxs-lookup"><span data-stu-id="74139-142">-RPId</span></span>
<span data-ttu-id="74139-143">Указывает идентификатор плана восстановления, для которого необходимо запустить задание.</span><span class="sxs-lookup"><span data-stu-id="74139-143">Specifies the ID of a recovery plan for which to start the job.</span></span>

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

### <span data-ttu-id="74139-144">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="74139-144">-WaitForCompletion</span></span>
<span data-ttu-id="74139-145">Указывает, что командлет ожидает завершения операции, прежде чем возвращать управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="74139-145">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="74139-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74139-146">CommonParameters</span></span>
<span data-ttu-id="74139-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74139-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74139-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74139-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74139-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74139-149">INPUTS</span></span>

## <span data-ttu-id="74139-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74139-150">OUTPUTS</span></span>

## <span data-ttu-id="74139-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="74139-151">NOTES</span></span>

## <span data-ttu-id="74139-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74139-152">RELATED LINKS</span></span>

[<span data-ttu-id="74139-153">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="74139-153">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="74139-154">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="74139-154">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="74139-155">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="74139-155">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="74139-156">Start-AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="74139-156">Start-AzureSiteRecoveryTestFailoverJob</span></span>](./Start-AzureSiteRecoveryTestFailoverJob.md)


