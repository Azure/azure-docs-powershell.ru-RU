---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 870EE77E-57D9-4B52-9F80-CB24D642E6E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f94d95b40fb89f0c1df89ad0c8a9b78eb283184
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076400"
---
# <span data-ttu-id="1aed7-101">Update-AzureSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="1aed7-101">Update-AzureSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="1aed7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1aed7-102">SYNOPSIS</span></span>
<span data-ttu-id="1aed7-103">Обновляет исходный и целевой сервер для защиты объекта восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="1aed7-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

## <span data-ttu-id="1aed7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1aed7-104">SYNTAX</span></span>

### <span data-ttu-id="1aed7-105">ByRPObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1aed7-105">ByRPObject (Default)</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1aed7-106">ByRPId</span><span class="sxs-lookup"><span data-stu-id="1aed7-106">ByRPId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1aed7-107">ByPEId</span><span class="sxs-lookup"><span data-stu-id="1aed7-107">ByPEId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1aed7-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="1aed7-108">ByPEObject</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1aed7-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1aed7-109">DESCRIPTION</span></span>
<span data-ttu-id="1aed7-110">Командлет **Update-AzureSiteRecoveryProtectionDirection** обновляет исходный и целевой сервер для защиты объекта Azure Site Recovery после завершения операции фиксации отказа.</span><span class="sxs-lookup"><span data-stu-id="1aed7-110">The **Update-AzureSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after a commit failover operation finishes.</span></span>

## <span data-ttu-id="1aed7-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1aed7-111">EXAMPLES</span></span>

### <span data-ttu-id="1aed7-112">Пример 1: изменение направления защищенного объекта в контейнере</span><span class="sxs-lookup"><span data-stu-id="1aed7-112">Example 1: Modify the direction for a protected object in a container</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container  
PS C:\> Update-AzureSiteRecoveryProtectionDirection -Direction RecoveryToPrimary -ProtectionEntity $Protected 
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

<span data-ttu-id="1aed7-113">Первая команда получает защищенные контейнеры в текущем хранилище Azure Site Recovery с помощью командлета **Get-AzureSiteRecoveryProtectionContainer** , а затем сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="1aed7-113">The first command gets the protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="1aed7-114">Вторая команда получает виртуальные машины, которые принадлежат контейнеру, хранящемуся в $Container, с помощью командлета **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="1aed7-114">The second command gets the virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="1aed7-115">Команда сохраняет результаты в переменной $Protected.</span><span class="sxs-lookup"><span data-stu-id="1aed7-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="1aed7-116">Последняя команда задает направление RecoverToPrimary для объектов, хранящихся в $Protected.</span><span class="sxs-lookup"><span data-stu-id="1aed7-116">The final command sets the direction to RecoverToPrimary for the objects stored in $Protected.</span></span>

## <span data-ttu-id="1aed7-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1aed7-117">PARAMETERS</span></span>

### <span data-ttu-id="1aed7-118">-Направление</span><span class="sxs-lookup"><span data-stu-id="1aed7-118">-Direction</span></span>
<span data-ttu-id="1aed7-119">Указывает направление фиксации.</span><span class="sxs-lookup"><span data-stu-id="1aed7-119">Specifies the direction of the commit.</span></span>
<span data-ttu-id="1aed7-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1aed7-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1aed7-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="1aed7-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="1aed7-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="1aed7-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="1aed7-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="1aed7-123">-Profile</span></span>
<span data-ttu-id="1aed7-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1aed7-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1aed7-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1aed7-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1aed7-126">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="1aed7-126">-ProtectionContainerId</span></span>
<span data-ttu-id="1aed7-127">Указывает идентификатор защищенного контейнера.</span><span class="sxs-lookup"><span data-stu-id="1aed7-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="1aed7-128">Этот командлет изменяет направление для защищенной виртуальной машины, которая принадлежит контейнеру, указанному в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="1aed7-128">This cmdlet modifies the direction for a protected virtual machine that belongs to the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="1aed7-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="1aed7-129">-ProtectionEntity</span></span>
<span data-ttu-id="1aed7-130">Указывает объект сущности для защиты.</span><span class="sxs-lookup"><span data-stu-id="1aed7-130">Specifies the protection entity object.</span></span>

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

### <span data-ttu-id="1aed7-131">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="1aed7-131">-ProtectionEntityId</span></span>
<span data-ttu-id="1aed7-132">Указывает идентификатор защищенной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1aed7-132">Specifies the ID of a protected virtual machine.</span></span>
<span data-ttu-id="1aed7-133">Этот командлет изменяет направление для защищенной виртуальной машины, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="1aed7-133">This cmdlet modifies the direction for the protected virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="1aed7-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1aed7-134">-RecoveryPlan</span></span>
<span data-ttu-id="1aed7-135">Указывает объект плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="1aed7-135">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="1aed7-136">-RPId</span><span class="sxs-lookup"><span data-stu-id="1aed7-136">-RPId</span></span>
<span data-ttu-id="1aed7-137">Указывает идентификатор плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="1aed7-137">Specifies the ID of a recovery plan.</span></span>
<span data-ttu-id="1aed7-138">Этот командлет изменяет направление для плана восстановления, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="1aed7-138">This cmdlet modifies the direction for the recovery plan that this parameter specifies.</span></span>

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

### <span data-ttu-id="1aed7-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="1aed7-139">-WaitForCompletion</span></span>
<span data-ttu-id="1aed7-140">Указывает, что командлет ожидает завершения операции, прежде чем возвращать управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1aed7-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="1aed7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aed7-141">CommonParameters</span></span>
<span data-ttu-id="1aed7-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1aed7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aed7-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aed7-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aed7-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1aed7-144">INPUTS</span></span>

## <span data-ttu-id="1aed7-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1aed7-145">OUTPUTS</span></span>

## <span data-ttu-id="1aed7-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="1aed7-146">NOTES</span></span>

## <span data-ttu-id="1aed7-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1aed7-147">RELATED LINKS</span></span>

[<span data-ttu-id="1aed7-148">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1aed7-148">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="1aed7-149">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="1aed7-149">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


