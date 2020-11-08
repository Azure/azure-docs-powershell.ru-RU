---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 75eb9975a578e1114e994b08949eda8d3dafda0e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065360"
---
# <span data-ttu-id="5f600-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5f600-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="5f600-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5f600-102">SYNOPSIS</span></span>

<span data-ttu-id="5f600-103">Получает элементы из контейнера в резервной копии.</span><span class="sxs-lookup"><span data-stu-id="5f600-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="5f600-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5f600-104">SYNTAX</span></span>

### <span data-ttu-id="5f600-105">GetItemsForContainer (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5f600-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f600-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="5f600-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f600-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="5f600-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f600-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f600-108">DESCRIPTION</span></span>

<span data-ttu-id="5f600-109">Командлет **Get-AzRecoveryServicesBackupItem** получает элементы в контейнере или значение в резервной копии Azure и состояние защиты элементов.</span><span class="sxs-lookup"><span data-stu-id="5f600-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="5f600-110">Контейнер, зарегистрированный в хранилище служб восстановления Azure, может содержать один или несколько элементов, которые можно защитить.</span><span class="sxs-lookup"><span data-stu-id="5f600-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="5f600-111">Для виртуальных машин Azure в контейнере виртуальных машин может быть только один элемент резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="5f600-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="5f600-112">Задайте контекст хранилища с помощью параметра-VaultId.</span><span class="sxs-lookup"><span data-stu-id="5f600-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="5f600-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5f600-113">EXAMPLES</span></span>

### <span data-ttu-id="5f600-114">Пример 1: получение элемента из резервной копии контейнера</span><span class="sxs-lookup"><span data-stu-id="5f600-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="5f600-115">Первая команда получает контейнер типа AzureVM и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="5f600-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="5f600-116">Вторая команда возвращает элемент резервного копирования с именем V2VM в $Container, а затем сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="5f600-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="5f600-117">Пример 2: получение элемента "общий доступ к файлам Azure" с FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5f600-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="5f600-118">Первая команда получает контейнер типа AzureStorage и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="5f600-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="5f600-119">Вторая команда возвращает элемент резервного копирования, параметр friendlyName которого соответствует значению, переданному в параметре FriendlyName, и затем сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="5f600-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="5f600-120">Использование параметра FriendlyName может привести к возврату нескольких файловых ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5f600-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="5f600-121">В таких случаях используйте параметр-Name с значением Parameter в качестве свойства Name, возвращаемого в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="5f600-121">In such cases use -Name parameter with parameter value as the Name property returned in $BackupItem variable.</span></span>

## <span data-ttu-id="5f600-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5f600-122">PARAMETERS</span></span>

### <span data-ttu-id="5f600-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="5f600-123">-BackupManagementType</span></span>

<span data-ttu-id="5f600-124">Указывает тип управления резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="5f600-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="5f600-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5f600-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5f600-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="5f600-126">AzureVM</span></span>
- <span data-ttu-id="5f600-127">Марс</span><span class="sxs-lookup"><span data-stu-id="5f600-127">MARS</span></span>
- <span data-ttu-id="5f600-128">SCDPM</span><span class="sxs-lookup"><span data-stu-id="5f600-128">SCDPM</span></span>
- <span data-ttu-id="5f600-129">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="5f600-129">AzureBackupServer</span></span>
- <span data-ttu-id="5f600-130">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="5f600-130">AzureSQL</span></span>
- <span data-ttu-id="5f600-131">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="5f600-131">AzureStorage</span></span>
- <span data-ttu-id="5f600-132">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="5f600-132">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f600-133">-Container</span><span class="sxs-lookup"><span data-stu-id="5f600-133">-Container</span></span>

<span data-ttu-id="5f600-134">Указывает объект-контейнер, из которого этот командлет получает элементы резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="5f600-134">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="5f600-135">Чтобы получить **AzureRmRecoveryServicesBackupContainer** , используйте командлет **Get-AzRecoveryServicesBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="5f600-135">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="5f600-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f600-136">-DefaultProfile</span></span>

<span data-ttu-id="5f600-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5f600-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f600-138">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="5f600-138">-DeleteState</span></span>
<span data-ttu-id="5f600-139">Указывает deletestate элемента допустимые значения для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="5f600-139">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5f600-140">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="5f600-140">ToBeDeleted</span></span>
- <span data-ttu-id="5f600-141">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="5f600-141">NotDeleted</span></span>

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

### <span data-ttu-id="5f600-142">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5f600-142">-FriendlyName</span></span>
<span data-ttu-id="5f600-143">Значение FriendlyName элемента резервной копии</span><span class="sxs-lookup"><span data-stu-id="5f600-143">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="5f600-144">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5f600-144">-Name</span></span>

<span data-ttu-id="5f600-145">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="5f600-145">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="5f600-146">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="5f600-146">-Policy</span></span>

<span data-ttu-id="5f600-147">Объект политики защиты.</span><span class="sxs-lookup"><span data-stu-id="5f600-147">Protection policy object.</span></span>

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

### <span data-ttu-id="5f600-148">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="5f600-148">-ProtectionState</span></span>

<span data-ttu-id="5f600-149">Указывает состояние защиты.</span><span class="sxs-lookup"><span data-stu-id="5f600-149">Specifies the state of protection.</span></span>
<span data-ttu-id="5f600-150">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5f600-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5f600-151">IRPending.</span><span class="sxs-lookup"><span data-stu-id="5f600-151">IRPending.</span></span>
<span data-ttu-id="5f600-152">Начальная синхронизация не начата, но пока нет точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="5f600-152">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="5f600-153">Защищенного.</span><span class="sxs-lookup"><span data-stu-id="5f600-153">Protected.</span></span>
<span data-ttu-id="5f600-154">Защита в настоящеем.</span><span class="sxs-lookup"><span data-stu-id="5f600-154">Protection is ongoing.</span></span>
- <span data-ttu-id="5f600-155">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="5f600-155">ProtectionError.</span></span>
<span data-ttu-id="5f600-156">Произошла ошибка защиты.</span><span class="sxs-lookup"><span data-stu-id="5f600-156">There is a protection error.</span></span>
- <span data-ttu-id="5f600-157">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="5f600-157">ProtectionStopped.</span></span>
<span data-ttu-id="5f600-158">Защита отключена.</span><span class="sxs-lookup"><span data-stu-id="5f600-158">Protection is disabled.</span></span>

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

### <span data-ttu-id="5f600-159">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="5f600-159">-ProtectionStatus</span></span>

<span data-ttu-id="5f600-160">Определяет общее состояние защиты элемента в контейнере.</span><span class="sxs-lookup"><span data-stu-id="5f600-160">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="5f600-161">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5f600-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5f600-162">Исправно</span><span class="sxs-lookup"><span data-stu-id="5f600-162">Healthy</span></span>
- <span data-ttu-id="5f600-163">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="5f600-163">Unhealthy</span></span>

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

### <span data-ttu-id="5f600-164">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5f600-164">-VaultId</span></span>

<span data-ttu-id="5f600-165">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="5f600-165">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5f600-166">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="5f600-166">-WorkloadType</span></span>

<span data-ttu-id="5f600-167">Указывает тип рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5f600-167">Specifies the workload type.</span></span>
<span data-ttu-id="5f600-168">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5f600-168">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5f600-169">AzureVM</span><span class="sxs-lookup"><span data-stu-id="5f600-169">AzureVM</span></span>
- <span data-ttu-id="5f600-170">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="5f600-170">AzureSQLDatabase</span></span>
- <span data-ttu-id="5f600-171">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="5f600-171">AzureFiles</span></span>
- <span data-ttu-id="5f600-172">MSSQL</span><span class="sxs-lookup"><span data-stu-id="5f600-172">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f600-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f600-173">CommonParameters</span></span>
<span data-ttu-id="5f600-174">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5f600-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f600-175">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f600-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f600-176">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5f600-176">INPUTS</span></span>

### <span data-ttu-id="5f600-177">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="5f600-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="5f600-178">System. String</span><span class="sxs-lookup"><span data-stu-id="5f600-178">System.String</span></span>

## <span data-ttu-id="5f600-179">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f600-179">OUTPUTS</span></span>

### <span data-ttu-id="5f600-180">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="5f600-180">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="5f600-181">Пуск</span><span class="sxs-lookup"><span data-stu-id="5f600-181">NOTES</span></span>

## <span data-ttu-id="5f600-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f600-182">RELATED LINKS</span></span>

[<span data-ttu-id="5f600-183">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5f600-183">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="5f600-184">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="5f600-184">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="5f600-185">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5f600-185">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="5f600-186">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5f600-186">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
