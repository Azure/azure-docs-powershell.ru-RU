---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 358d3da36996c9b020db3a805889b7098b9c36ec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316500"
---
# <span data-ttu-id="e5062-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e5062-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="e5062-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5062-102">SYNOPSIS</span></span>

<span data-ttu-id="e5062-103">Получает элементы из контейнера в резервной копии.</span><span class="sxs-lookup"><span data-stu-id="e5062-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="e5062-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5062-104">SYNTAX</span></span>

### <span data-ttu-id="e5062-105">GetItemsForContainer (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5062-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5062-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="e5062-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5062-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="e5062-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5062-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5062-108">DESCRIPTION</span></span>

<span data-ttu-id="e5062-109">Командлет **Get-AzRecoveryServicesBackupItem** получает список защищенных элементов в контейнере и состояние защиты элементов.</span><span class="sxs-lookup"><span data-stu-id="e5062-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the list of protected items in a container and the protection status of the items.</span></span>
<span data-ttu-id="e5062-110">Контейнер, зарегистрированный в хранилище служб восстановления Azure, может содержать один или несколько элементов, которые можно защитить.</span><span class="sxs-lookup"><span data-stu-id="e5062-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="e5062-111">Для виртуальных машин Azure в контейнере виртуальных машин может быть только один элемент резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e5062-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="e5062-112">Задайте контекст хранилища с помощью параметра-VaultId.</span><span class="sxs-lookup"><span data-stu-id="e5062-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="e5062-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5062-113">EXAMPLES</span></span>

### <span data-ttu-id="e5062-114">Пример 1: получение элемента из резервной копии контейнера</span><span class="sxs-lookup"><span data-stu-id="e5062-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="e5062-115">Первая команда получает контейнер типа AzureVM и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="e5062-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="e5062-116">Вторая команда возвращает элемент резервного копирования с именем V2VM в $Container, а затем сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="e5062-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="e5062-117">Пример 2: получение элемента "общий доступ к файлам Azure" с FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e5062-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="e5062-118">Первая команда получает контейнер типа AzureStorage и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="e5062-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="e5062-119">Вторая команда возвращает элемент резервного копирования, параметр friendlyName которого соответствует значению, переданному в параметре FriendlyName, и затем сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="e5062-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="e5062-120">Использование параметра FriendlyName может привести к возврату нескольких файловых ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="e5062-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="e5062-121">В таких случаях выполните командлет, передав значение параметра-Name как свойство Name, возвращаемое в результирующем наборе $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="e5062-121">In such cases, execute the cmdlet by passing value for -Name parameter as the Name property returned in the result set of $BackupItem.</span></span>

## <span data-ttu-id="e5062-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5062-122">PARAMETERS</span></span>

### <span data-ttu-id="e5062-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="e5062-123">-BackupManagementType</span></span>

<span data-ttu-id="e5062-124">Класс защищаемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5062-124">The class of resources being protected.</span></span> <span data-ttu-id="e5062-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e5062-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e5062-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e5062-126">AzureVM</span></span>
- <span data-ttu-id="e5062-127">MAB</span><span class="sxs-lookup"><span data-stu-id="e5062-127">MAB</span></span>
- <span data-ttu-id="e5062-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="e5062-128">AzureStorage</span></span>
- <span data-ttu-id="e5062-129">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="e5062-129">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5062-130">-Container</span><span class="sxs-lookup"><span data-stu-id="e5062-130">-Container</span></span>

<span data-ttu-id="e5062-131">Указывает объект-контейнер, из которого этот командлет получает элементы резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e5062-131">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="e5062-132">Чтобы получить **AzureRmRecoveryServicesBackupContainer** , используйте командлет **Get-AzRecoveryServicesBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="e5062-132">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: GetItemsForContainer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5062-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5062-133">-DefaultProfile</span></span>

<span data-ttu-id="e5062-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5062-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5062-135">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="e5062-135">-DeleteState</span></span>
<span data-ttu-id="e5062-136">Указывает deletestate элемента допустимые значения для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="e5062-136">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e5062-137">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="e5062-137">ToBeDeleted</span></span>
- <span data-ttu-id="e5062-138">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="e5062-138">NotDeleted</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemDeleteState
Parameter Sets: (All)
Aliases:
Accepted values: ToBeDeleted, NotDeleted

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5062-139">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e5062-139">-FriendlyName</span></span>
<span data-ttu-id="e5062-140">Значение FriendlyName элемента резервной копии</span><span class="sxs-lookup"><span data-stu-id="e5062-140">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="e5062-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e5062-141">-Name</span></span>

<span data-ttu-id="e5062-142">Указывает имя элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e5062-142">Specifies the name of backup item.</span></span> <span data-ttu-id="e5062-143">В качестве общего файлового файла укажите уникальный идентификатор защищенного общего доступа к файлам.</span><span class="sxs-lookup"><span data-stu-id="e5062-143">For file share, specify the unique ID of protected file share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5062-144">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="e5062-144">-Policy</span></span>

<span data-ttu-id="e5062-145">Объект политики защиты.</span><span class="sxs-lookup"><span data-stu-id="e5062-145">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: GetItemsForPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5062-146">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="e5062-146">-ProtectionState</span></span>

<span data-ttu-id="e5062-147">Указывает состояние защиты.</span><span class="sxs-lookup"><span data-stu-id="e5062-147">Specifies the state of protection.</span></span>
<span data-ttu-id="e5062-148">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e5062-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e5062-149">IRPending.</span><span class="sxs-lookup"><span data-stu-id="e5062-149">IRPending.</span></span>
<span data-ttu-id="e5062-150">Начальная синхронизация не начата, но пока нет точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="e5062-150">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="e5062-151">Защищенного.</span><span class="sxs-lookup"><span data-stu-id="e5062-151">Protected.</span></span>
<span data-ttu-id="e5062-152">Защита в настоящеем.</span><span class="sxs-lookup"><span data-stu-id="e5062-152">Protection is ongoing.</span></span>
- <span data-ttu-id="e5062-153">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="e5062-153">ProtectionError.</span></span>
<span data-ttu-id="e5062-154">Произошла ошибка защиты.</span><span class="sxs-lookup"><span data-stu-id="e5062-154">There is a protection error.</span></span>
- <span data-ttu-id="e5062-155">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="e5062-155">ProtectionStopped.</span></span>
<span data-ttu-id="e5062-156">Защита отключена.</span><span class="sxs-lookup"><span data-stu-id="e5062-156">Protection is disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionState
Parameter Sets: (All)
Aliases:
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5062-157">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="e5062-157">-ProtectionStatus</span></span>

<span data-ttu-id="e5062-158">Определяет общее состояние защиты элемента в контейнере.</span><span class="sxs-lookup"><span data-stu-id="e5062-158">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="e5062-159">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e5062-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e5062-160">Исправно</span><span class="sxs-lookup"><span data-stu-id="e5062-160">Healthy</span></span>
- <span data-ttu-id="e5062-161">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="e5062-161">Unhealthy</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionStatus
Parameter Sets: (All)
Aliases:
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5062-162">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e5062-162">-VaultId</span></span>

<span data-ttu-id="e5062-163">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e5062-163">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5062-164">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="e5062-164">-WorkloadType</span></span>

<span data-ttu-id="e5062-165">Тип рабочей нагрузки ресурса.</span><span class="sxs-lookup"><span data-stu-id="e5062-165">Workload type of the resource.</span></span> <span data-ttu-id="e5062-166">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e5062-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e5062-167">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e5062-167">AzureVM</span></span>
- <span data-ttu-id="e5062-168">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="e5062-168">AzureFiles</span></span>
- <span data-ttu-id="e5062-169">MSSQL</span><span class="sxs-lookup"><span data-stu-id="e5062-169">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5062-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5062-170">CommonParameters</span></span>
<span data-ttu-id="e5062-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5062-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5062-172">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5062-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5062-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5062-173">INPUTS</span></span>

### <span data-ttu-id="e5062-174">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="e5062-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="e5062-175">System. String</span><span class="sxs-lookup"><span data-stu-id="e5062-175">System.String</span></span>

## <span data-ttu-id="e5062-176">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5062-176">OUTPUTS</span></span>

### <span data-ttu-id="e5062-177">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="e5062-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="e5062-178">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5062-178">NOTES</span></span>

## <span data-ttu-id="e5062-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5062-179">RELATED LINKS</span></span>

[<span data-ttu-id="e5062-180">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e5062-180">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="e5062-181">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="e5062-181">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="e5062-182">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e5062-182">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="e5062-183">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e5062-183">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
