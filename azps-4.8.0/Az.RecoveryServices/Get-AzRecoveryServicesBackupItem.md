---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 358d3da36996c9b020db3a805889b7098b9c36ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244702"
---
# <span data-ttu-id="e10fe-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e10fe-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="e10fe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e10fe-102">SYNOPSIS</span></span>

<span data-ttu-id="e10fe-103">Получает элементы из контейнера в резервной копии.</span><span class="sxs-lookup"><span data-stu-id="e10fe-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="e10fe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e10fe-104">SYNTAX</span></span>

### <span data-ttu-id="e10fe-105">GetItemsForContainer (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e10fe-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e10fe-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="e10fe-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e10fe-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="e10fe-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e10fe-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e10fe-108">DESCRIPTION</span></span>

<span data-ttu-id="e10fe-109">Командлет **Get-AzRecoveryServicesBackupItem** получает список защищенных элементов в контейнере и состояние защиты элементов.</span><span class="sxs-lookup"><span data-stu-id="e10fe-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the list of protected items in a container and the protection status of the items.</span></span>
<span data-ttu-id="e10fe-110">Контейнер, зарегистрированный в хранилище служб восстановления Azure, может содержать один или несколько элементов, которые можно защитить.</span><span class="sxs-lookup"><span data-stu-id="e10fe-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="e10fe-111">Для виртуальных машин Azure в контейнере виртуальных машин может быть только один элемент резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e10fe-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="e10fe-112">Задайте контекст хранилища с помощью параметра-VaultId.</span><span class="sxs-lookup"><span data-stu-id="e10fe-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="e10fe-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e10fe-113">EXAMPLES</span></span>

### <span data-ttu-id="e10fe-114">Пример 1: получение элемента из резервной копии контейнера</span><span class="sxs-lookup"><span data-stu-id="e10fe-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="e10fe-115">Первая команда получает контейнер типа AzureVM и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="e10fe-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="e10fe-116">Вторая команда возвращает элемент резервного копирования с именем V2VM в $Container, а затем сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="e10fe-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="e10fe-117">Пример 2: получение элемента "общий доступ к файлам Azure" с FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e10fe-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="e10fe-118">Первая команда получает контейнер типа AzureStorage и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="e10fe-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="e10fe-119">Вторая команда возвращает элемент резервного копирования, параметр friendlyName которого соответствует значению, переданному в параметре FriendlyName, и затем сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="e10fe-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="e10fe-120">Использование параметра FriendlyName может привести к возврату нескольких файловых ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="e10fe-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="e10fe-121">В таких случаях выполните командлет, передав значение параметра-Name как свойство Name, возвращаемое в результирующем наборе $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="e10fe-121">In such cases, execute the cmdlet by passing value for -Name parameter as the Name property returned in the result set of $BackupItem.</span></span>

## <span data-ttu-id="e10fe-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e10fe-122">PARAMETERS</span></span>

### <span data-ttu-id="e10fe-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="e10fe-123">-BackupManagementType</span></span>

<span data-ttu-id="e10fe-124">Класс защищаемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e10fe-124">The class of resources being protected.</span></span> <span data-ttu-id="e10fe-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e10fe-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e10fe-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e10fe-126">AzureVM</span></span>
- <span data-ttu-id="e10fe-127">MAB</span><span class="sxs-lookup"><span data-stu-id="e10fe-127">MAB</span></span>
- <span data-ttu-id="e10fe-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="e10fe-128">AzureStorage</span></span>
- <span data-ttu-id="e10fe-129">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="e10fe-129">AzureWorkload</span></span>

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

### <span data-ttu-id="e10fe-130">-Container</span><span class="sxs-lookup"><span data-stu-id="e10fe-130">-Container</span></span>

<span data-ttu-id="e10fe-131">Указывает объект-контейнер, из которого этот командлет получает элементы резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e10fe-131">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="e10fe-132">Чтобы получить **AzureRmRecoveryServicesBackupContainer** , используйте командлет **Get-AzRecoveryServicesBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="e10fe-132">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="e10fe-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e10fe-133">-DefaultProfile</span></span>

<span data-ttu-id="e10fe-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e10fe-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e10fe-135">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="e10fe-135">-DeleteState</span></span>
<span data-ttu-id="e10fe-136">Указывает deletestate элемента допустимые значения для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="e10fe-136">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e10fe-137">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="e10fe-137">ToBeDeleted</span></span>
- <span data-ttu-id="e10fe-138">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="e10fe-138">NotDeleted</span></span>

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

### <span data-ttu-id="e10fe-139">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e10fe-139">-FriendlyName</span></span>
<span data-ttu-id="e10fe-140">Значение FriendlyName элемента резервной копии</span><span class="sxs-lookup"><span data-stu-id="e10fe-140">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="e10fe-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e10fe-141">-Name</span></span>

<span data-ttu-id="e10fe-142">Указывает имя элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e10fe-142">Specifies the name of backup item.</span></span> <span data-ttu-id="e10fe-143">В качестве общего файлового файла укажите уникальный идентификатор защищенного общего доступа к файлам.</span><span class="sxs-lookup"><span data-stu-id="e10fe-143">For file share, specify the unique ID of protected file share.</span></span>

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

### <span data-ttu-id="e10fe-144">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="e10fe-144">-Policy</span></span>

<span data-ttu-id="e10fe-145">Объект политики защиты.</span><span class="sxs-lookup"><span data-stu-id="e10fe-145">Protection policy object.</span></span>

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

### <span data-ttu-id="e10fe-146">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="e10fe-146">-ProtectionState</span></span>

<span data-ttu-id="e10fe-147">Указывает состояние защиты.</span><span class="sxs-lookup"><span data-stu-id="e10fe-147">Specifies the state of protection.</span></span>
<span data-ttu-id="e10fe-148">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e10fe-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e10fe-149">IRPending.</span><span class="sxs-lookup"><span data-stu-id="e10fe-149">IRPending.</span></span>
<span data-ttu-id="e10fe-150">Начальная синхронизация не начата, но пока нет точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="e10fe-150">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="e10fe-151">Защищенного.</span><span class="sxs-lookup"><span data-stu-id="e10fe-151">Protected.</span></span>
<span data-ttu-id="e10fe-152">Защита в настоящеем.</span><span class="sxs-lookup"><span data-stu-id="e10fe-152">Protection is ongoing.</span></span>
- <span data-ttu-id="e10fe-153">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="e10fe-153">ProtectionError.</span></span>
<span data-ttu-id="e10fe-154">Произошла ошибка защиты.</span><span class="sxs-lookup"><span data-stu-id="e10fe-154">There is a protection error.</span></span>
- <span data-ttu-id="e10fe-155">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="e10fe-155">ProtectionStopped.</span></span>
<span data-ttu-id="e10fe-156">Защита отключена.</span><span class="sxs-lookup"><span data-stu-id="e10fe-156">Protection is disabled.</span></span>

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

### <span data-ttu-id="e10fe-157">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="e10fe-157">-ProtectionStatus</span></span>

<span data-ttu-id="e10fe-158">Определяет общее состояние защиты элемента в контейнере.</span><span class="sxs-lookup"><span data-stu-id="e10fe-158">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="e10fe-159">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e10fe-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e10fe-160">Исправно</span><span class="sxs-lookup"><span data-stu-id="e10fe-160">Healthy</span></span>
- <span data-ttu-id="e10fe-161">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="e10fe-161">Unhealthy</span></span>

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

### <span data-ttu-id="e10fe-162">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e10fe-162">-VaultId</span></span>

<span data-ttu-id="e10fe-163">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e10fe-163">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e10fe-164">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="e10fe-164">-WorkloadType</span></span>

<span data-ttu-id="e10fe-165">Тип рабочей нагрузки ресурса.</span><span class="sxs-lookup"><span data-stu-id="e10fe-165">Workload type of the resource.</span></span> <span data-ttu-id="e10fe-166">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e10fe-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e10fe-167">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e10fe-167">AzureVM</span></span>
- <span data-ttu-id="e10fe-168">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="e10fe-168">AzureFiles</span></span>
- <span data-ttu-id="e10fe-169">MSSQL</span><span class="sxs-lookup"><span data-stu-id="e10fe-169">MSSQL</span></span>

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

### <span data-ttu-id="e10fe-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e10fe-170">CommonParameters</span></span>
<span data-ttu-id="e10fe-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e10fe-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e10fe-172">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e10fe-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e10fe-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e10fe-173">INPUTS</span></span>

### <span data-ttu-id="e10fe-174">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="e10fe-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="e10fe-175">System. String</span><span class="sxs-lookup"><span data-stu-id="e10fe-175">System.String</span></span>

## <span data-ttu-id="e10fe-176">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e10fe-176">OUTPUTS</span></span>

### <span data-ttu-id="e10fe-177">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="e10fe-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="e10fe-178">Пуск</span><span class="sxs-lookup"><span data-stu-id="e10fe-178">NOTES</span></span>

## <span data-ttu-id="e10fe-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e10fe-179">RELATED LINKS</span></span>

[<span data-ttu-id="e10fe-180">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e10fe-180">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="e10fe-181">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="e10fe-181">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="e10fe-182">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e10fe-182">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="e10fe-183">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e10fe-183">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
