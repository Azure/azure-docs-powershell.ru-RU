---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 44A22B6C-5FD4-43B0-9726-71E28AE53E9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: de1b7a24c1af362297319d0297ce356b00ef9d49
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075778"
---
# <span data-ttu-id="5815d-101">Start-AzureSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="5815d-101">Start-AzureSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="5815d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5815d-102">SYNOPSIS</span></span>
<span data-ttu-id="5815d-103">Запускает действие фиксации отработки отказа для объекта восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="5815d-103">Starts the commit failover action for a Site Recovery object.</span></span>

## <span data-ttu-id="5815d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5815d-104">SYNTAX</span></span>

### <span data-ttu-id="5815d-105">ByRPId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5815d-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RPId <String> [-Direction <String>] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5815d-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="5815d-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 [-Direction <String>] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5815d-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="5815d-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5815d-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="5815d-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5815d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5815d-109">DESCRIPTION</span></span>
<span data-ttu-id="5815d-110">Командлет **Start-AzureSiteRecoveryCommitFailoverJob** запускает процесс фиксации отработки отказа для объекта Azure Site Recovery после операции отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="5815d-110">The **Start-AzureSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="5815d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5815d-111">EXAMPLES</span></span>

### <span data-ttu-id="5815d-112">Пример 1: начало задания фиксации отработки отказа</span><span class="sxs-lookup"><span data-stu-id="5815d-112">Example 1: Start a commit failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity $Protected
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

<span data-ttu-id="5815d-113">Первая команда получает все защищенные контейнеры для текущего хранилища Azure Site Recovery с помощью командлета **Get-AzureSiteRecoveryProtectionContainer** , а затем сохраняет результаты в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="5815d-113">The first command gets all protected containers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>

<span data-ttu-id="5815d-114">Вторая команда получает защищенные виртуальные машины, которые принадлежат контейнеру, хранящемуся в $Container с помощью командлета **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="5815d-114">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="5815d-115">Команда сохраняет результаты в переменной $Protected.</span><span class="sxs-lookup"><span data-stu-id="5815d-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="5815d-116">Последняя команда запускает задание отработки отказа для защищенных объектов, хранящихся в $Protected.</span><span class="sxs-lookup"><span data-stu-id="5815d-116">The final command starts the failover job for the protected objects stored in $Protected.</span></span>

## <span data-ttu-id="5815d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5815d-117">PARAMETERS</span></span>

### <span data-ttu-id="5815d-118">-Направление</span><span class="sxs-lookup"><span data-stu-id="5815d-118">-Direction</span></span>
<span data-ttu-id="5815d-119">Указывает направление отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="5815d-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="5815d-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5815d-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5815d-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="5815d-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="5815d-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="5815d-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="5815d-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="5815d-123">-Profile</span></span>
<span data-ttu-id="5815d-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5815d-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5815d-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5815d-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5815d-126">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="5815d-126">-ProtectionContainerId</span></span>
<span data-ttu-id="5815d-127">Указывает идентификатор защищенного контейнера.</span><span class="sxs-lookup"><span data-stu-id="5815d-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="5815d-128">Этот командлет запускает задание для защищенной виртуальной машины, которая принадлежит контейнеру, указанному этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5815d-128">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="5815d-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5815d-129">-ProtectionEntity</span></span>
<span data-ttu-id="5815d-130">Указывает объект **ASRProtectionEntity** , для которого нужно запустить задание.</span><span class="sxs-lookup"><span data-stu-id="5815d-130">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="5815d-131">Чтобы получить объект **ASRProtectionEntity** , используйте командлет **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="5815d-131">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

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

### <span data-ttu-id="5815d-132">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="5815d-132">-ProtectionEntityId</span></span>
<span data-ttu-id="5815d-133">Указывает идентификатор защищенной виртуальной машины, для которой необходимо запустить задание.</span><span class="sxs-lookup"><span data-stu-id="5815d-133">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

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

### <span data-ttu-id="5815d-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5815d-134">-RecoveryPlan</span></span>
<span data-ttu-id="5815d-135">Указывает объект плана восстановления, для которого нужно запустить задание.</span><span class="sxs-lookup"><span data-stu-id="5815d-135">Specifies a recovery plan object for which to start the job.</span></span>
<span data-ttu-id="5815d-136">Чтобы получить объект **ASRRecoveryPlan** , используйте командлет **Get-AzureSiteRecoveryRecoveryPlan** .</span><span class="sxs-lookup"><span data-stu-id="5815d-136">To obtain an **ASRRecoveryPlan** object, use the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>

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

### <span data-ttu-id="5815d-137">-RPId</span><span class="sxs-lookup"><span data-stu-id="5815d-137">-RPId</span></span>
<span data-ttu-id="5815d-138">Указывает идентификатор плана восстановления, для которого необходимо запустить задание.</span><span class="sxs-lookup"><span data-stu-id="5815d-138">Specifies the ID of a recovery plan for which to start the job.</span></span>

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

### <span data-ttu-id="5815d-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="5815d-139">-WaitForCompletion</span></span>
<span data-ttu-id="5815d-140">Указывает, что командлет ожидает завершения операции, прежде чем возвращать управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5815d-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="5815d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5815d-141">CommonParameters</span></span>
<span data-ttu-id="5815d-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5815d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5815d-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5815d-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5815d-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5815d-144">INPUTS</span></span>

## <span data-ttu-id="5815d-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5815d-145">OUTPUTS</span></span>

## <span data-ttu-id="5815d-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="5815d-146">NOTES</span></span>

## <span data-ttu-id="5815d-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5815d-147">RELATED LINKS</span></span>

[<span data-ttu-id="5815d-148">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5815d-148">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="5815d-149">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="5815d-149">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="5815d-150">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5815d-150">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


