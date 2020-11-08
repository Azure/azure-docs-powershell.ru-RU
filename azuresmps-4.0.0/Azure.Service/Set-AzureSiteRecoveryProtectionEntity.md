---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 1415BBA3-3F55-46A9-B20B-DFA72342BDF4
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec7883b996e5da367884fd7d051a5299c6d62a9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076423"
---
# <span data-ttu-id="7a57e-101">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7a57e-101">Set-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="7a57e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a57e-102">SYNOPSIS</span></span>
<span data-ttu-id="7a57e-103">Задает состояние для элемента защиты восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="7a57e-103">Sets the state for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="7a57e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a57e-104">SYNTAX</span></span>

### <span data-ttu-id="7a57e-105">ByPEObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7a57e-105">ByPEObject (Default)</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a57e-106">ByIDs</span><span class="sxs-lookup"><span data-stu-id="7a57e-106">ByIDs</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainerId <String>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a57e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a57e-107">DESCRIPTION</span></span>
<span data-ttu-id="7a57e-108">Командлет **Set-AzureSiteRecoveryProtectionEntity** включает или выключает защиту для сущности "Защита Azure Site Recovery".</span><span class="sxs-lookup"><span data-stu-id="7a57e-108">The **Set-AzureSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="7a57e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a57e-109">EXAMPLES</span></span>

### <span data-ttu-id="7a57e-110">Пример 1: Включение защиты для объектов в контейнере</span><span class="sxs-lookup"><span data-stu-id="7a57e-110">Example 1: Enable protection for objects in a container</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer -Name "Cloud17"
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer -Name "VM01"
PS C:\> Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ ProtectionEntity -Protection Enable -ProtectionProfile $ProtectionContainer.AvailableProtectionProfiles[0] -OS Windows
```

<span data-ttu-id="7a57e-111">Первая команда получает контейнеры для текущего хранилища сайта Azure с помощью командлета **Get-AzureSiteRecoveryProtectionContainer** , а затем сохраняет его в переменной $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="7a57e-111">The first command gets containers for the current Azure Site vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="7a57e-112">Вторая команда получает защищенные виртуальные машины, которые принадлежат контейнеру, хранящемуся в $ProtectionContainer с помощью командлета **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="7a57e-112">The second command gets the protected virtual machines that belong to the container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="7a57e-113">Команда сохраняет результаты в переменной $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="7a57e-113">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="7a57e-114">Последняя команда обеспечивает защиту для сущностей, хранящихся в $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="7a57e-114">The final command enables protection for the entities stored in $ProtectionEntity.</span></span>

## <span data-ttu-id="7a57e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a57e-115">PARAMETERS</span></span>

### <span data-ttu-id="7a57e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7a57e-116">-Force</span></span>
<span data-ttu-id="7a57e-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="7a57e-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7a57e-118">-ID</span><span class="sxs-lookup"><span data-stu-id="7a57e-118">-Id</span></span>
<span data-ttu-id="7a57e-119">Указывает идентификатор защищенной виртуальной машины, для которой требуется включить или отключить защиту.</span><span class="sxs-lookup"><span data-stu-id="7a57e-119">Specifies the ID of a protected virtual machine for which to enable or disable protection.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a57e-120">-OS</span><span class="sxs-lookup"><span data-stu-id="7a57e-120">-OS</span></span>
<span data-ttu-id="7a57e-121">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7a57e-121">Specifies the operating system type.</span></span>
<span data-ttu-id="7a57e-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7a57e-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7a57e-123">Windows</span><span class="sxs-lookup"><span data-stu-id="7a57e-123">Windows</span></span>
- <span data-ttu-id="7a57e-124">Linux</span><span class="sxs-lookup"><span data-stu-id="7a57e-124">Linux</span></span>

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

### <span data-ttu-id="7a57e-125">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="7a57e-125">-OSDiskName</span></span>
<span data-ttu-id="7a57e-126">Указывает имя диска, который содержит операционную систему.</span><span class="sxs-lookup"><span data-stu-id="7a57e-126">Specifies the name of the disk that contains the operating system.</span></span>

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

### <span data-ttu-id="7a57e-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="7a57e-127">-Profile</span></span>
<span data-ttu-id="7a57e-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7a57e-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7a57e-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7a57e-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7a57e-130">-Защита</span><span class="sxs-lookup"><span data-stu-id="7a57e-130">-Protection</span></span>
<span data-ttu-id="7a57e-131">Указывает, следует ли включить или отключить защиту.</span><span class="sxs-lookup"><span data-stu-id="7a57e-131">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="7a57e-132">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7a57e-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7a57e-133">Включите</span><span class="sxs-lookup"><span data-stu-id="7a57e-133">Enable</span></span>
- <span data-ttu-id="7a57e-134">Ключив</span><span class="sxs-lookup"><span data-stu-id="7a57e-134">Disable</span></span>

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

### <span data-ttu-id="7a57e-135">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="7a57e-135">-ProtectionContainerId</span></span>
<span data-ttu-id="7a57e-136">Указывает идентификатор защищенного контейнера.</span><span class="sxs-lookup"><span data-stu-id="7a57e-136">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="7a57e-137">Этот командлет включает или выключает защиту виртуальной машины, которая принадлежит контейнеру, указанному в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="7a57e-137">This cmdlet enables or disables protection for a virtual machine that belongs to the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a57e-138">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7a57e-138">-ProtectionEntity</span></span>
<span data-ttu-id="7a57e-139">Указывает объект сущности для защиты.</span><span class="sxs-lookup"><span data-stu-id="7a57e-139">Specifies the protection entity object.</span></span>

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

### <span data-ttu-id="7a57e-140">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="7a57e-140">-ProtectionProfile</span></span>
<span data-ttu-id="7a57e-141">Указывает профиль защиты для включения защиты.</span><span class="sxs-lookup"><span data-stu-id="7a57e-141">Specifies a protection profile to enable protection.</span></span>
<span data-ttu-id="7a57e-142">Укажите объект **ASRProtectionProfile** , который является одним из доступных профилей защиты в связанном контейнере защиты.</span><span class="sxs-lookup"><span data-stu-id="7a57e-142">Specify an **ASRProtectionProfile** object that is one of the available protection profiles in the associated protection container.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a57e-143">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="7a57e-143">-WaitForCompletion</span></span>
<span data-ttu-id="7a57e-144">Указывает, что командлет ожидает завершения операции, прежде чем возвращать управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7a57e-144">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="7a57e-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a57e-145">-Confirm</span></span>
<span data-ttu-id="7a57e-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7a57e-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a57e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a57e-147">-WhatIf</span></span>
<span data-ttu-id="7a57e-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7a57e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a57e-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7a57e-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a57e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a57e-150">CommonParameters</span></span>
<span data-ttu-id="7a57e-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a57e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a57e-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a57e-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a57e-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a57e-153">INPUTS</span></span>

## <span data-ttu-id="7a57e-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a57e-154">OUTPUTS</span></span>

## <span data-ttu-id="7a57e-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a57e-155">NOTES</span></span>

## <span data-ttu-id="7a57e-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a57e-156">RELATED LINKS</span></span>

[<span data-ttu-id="7a57e-157">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7a57e-157">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="7a57e-158">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7a57e-158">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="7a57e-159">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7a57e-159">Update-AzureSiteRecoveryProtectionEntity</span></span>](./Update-AzureSiteRecoveryProtectionEntity.md)


