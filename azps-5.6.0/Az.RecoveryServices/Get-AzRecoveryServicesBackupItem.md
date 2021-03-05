---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 084f18e1091059680e0c59b234b295120049cef6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984248"
---
# <span data-ttu-id="63663-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="63663-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="63663-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63663-102">SYNOPSIS</span></span>

<span data-ttu-id="63663-103">Элементы из контейнера в архиве.</span><span class="sxs-lookup"><span data-stu-id="63663-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="63663-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="63663-104">SYNTAX</span></span>

### <span data-ttu-id="63663-105">GetItemsForContainer (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="63663-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>]  [-UseSecondaryRegion] [<CommonParameters>]
```

### <span data-ttu-id="63663-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="63663-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>]  [-UseSecondaryRegion] [<CommonParameters>]
```

### <span data-ttu-id="63663-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="63663-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>]  [-UseSecondaryRegion] [<CommonParameters>]
```

## <span data-ttu-id="63663-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63663-108">DESCRIPTION</span></span>

<span data-ttu-id="63663-109">Для получения списка защищенных элементов в контейнере и состояния их защиты возвращается cmdlet **Get-AzRecoveryServicesBackupItem.**</span><span class="sxs-lookup"><span data-stu-id="63663-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the list of protected items in a container and the protection status of the items.</span></span>
<span data-ttu-id="63663-110">Контейнер, зарегистрированный в хранилище служб восстановления Azure, может иметь один или несколько элементов, которые можно защитить.</span><span class="sxs-lookup"><span data-stu-id="63663-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="63663-111">На виртуальных машинах Azure в контейнере виртуальной машины может быть только один элемент резервной копии.</span><span class="sxs-lookup"><span data-stu-id="63663-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="63663-112">Задать контекст хранилища с помощью параметра -VaultId.</span><span class="sxs-lookup"><span data-stu-id="63663-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="63663-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="63663-113">EXAMPLES</span></span>

### <span data-ttu-id="63663-114">Пример 1. Получить элемент из контейнера резервной копии</span><span class="sxs-lookup"><span data-stu-id="63663-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="63663-115">Первая команда получает контейнер типа AzureVM, а затем сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="63663-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="63663-116">Вторая команда получает элемент резервной копии с именем V2VM в $Container, а затем $BackupItem переменной.</span><span class="sxs-lookup"><span data-stu-id="63663-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="63663-117">Пример 2. Получить элемент azure File Share Item от FriendlyName</span><span class="sxs-lookup"><span data-stu-id="63663-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -FriendlyName "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="63663-118">Первая команда получает контейнер типа AzureStorage, а затем сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="63663-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="63663-119">Вторая команда получает элемент резервной копии, значение friendlyName которого совпадает со значением, переданным в параметре FriendlyName, и сохраняет его в $BackupItem переменной.</span><span class="sxs-lookup"><span data-stu-id="63663-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="63663-120">Использование параметра FriendlyName может вернуть несколько файловой папки Azure.</span><span class="sxs-lookup"><span data-stu-id="63663-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="63663-121">В таких случаях выполните cmdlet, передавая значение параметра -Name в качестве свойства Name, возвращаемого в наборе результатов $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="63663-121">In such cases, execute the cmdlet by passing value for -Name parameter as the Name property returned in the result set of $BackupItem.</span></span>

## <span data-ttu-id="63663-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63663-122">PARAMETERS</span></span>

### <span data-ttu-id="63663-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="63663-123">-BackupManagementType</span></span>

<span data-ttu-id="63663-124">Класс защищенных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63663-124">The class of resources being protected.</span></span> <span data-ttu-id="63663-125">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="63663-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="63663-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="63663-126">AzureVM</span></span>
- <span data-ttu-id="63663-127">MAB</span><span class="sxs-lookup"><span data-stu-id="63663-127">MAB</span></span>
- <span data-ttu-id="63663-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="63663-128">AzureStorage</span></span>
- <span data-ttu-id="63663-129">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="63663-129">AzureWorkload</span></span>

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

### <span data-ttu-id="63663-130">-Container</span><span class="sxs-lookup"><span data-stu-id="63663-130">-Container</span></span>

<span data-ttu-id="63663-131">Определяет объект контейнера, из которого этот cmdlet получает резервные копии элементов.</span><span class="sxs-lookup"><span data-stu-id="63663-131">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="63663-132">Чтобы получить **azureRmRecoveryServicesBackupContainer,** используйте cmdlet **Get-AzRecoveryServicesBackupContainer.**</span><span class="sxs-lookup"><span data-stu-id="63663-132">To obtain an **AzureRmRecoveryServicesBackupContainer**, use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="63663-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63663-133">-DefaultProfile</span></span>

<span data-ttu-id="63663-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63663-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63663-135">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="63663-135">-DeleteState</span></span>
<span data-ttu-id="63663-136">Определяет значение deletestate элемента. Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="63663-136">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="63663-137">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="63663-137">ToBeDeleted</span></span>
- <span data-ttu-id="63663-138">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="63663-138">NotDeleted</span></span>

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

### <span data-ttu-id="63663-139">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="63663-139">-FriendlyName</span></span>
<span data-ttu-id="63663-140">FriendlyName для элемента, который был засвечен</span><span class="sxs-lookup"><span data-stu-id="63663-140">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="63663-141">-Name</span><span class="sxs-lookup"><span data-stu-id="63663-141">-Name</span></span>

<span data-ttu-id="63663-142">Указывает имя элемента резервной копии.</span><span class="sxs-lookup"><span data-stu-id="63663-142">Specifies the name of backup item.</span></span> <span data-ttu-id="63663-143">Для файловой папки укажите уникальный ИД защищенной папки.</span><span class="sxs-lookup"><span data-stu-id="63663-143">For file share, specify the unique ID of protected file share.</span></span>

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

### <span data-ttu-id="63663-144">-Политика</span><span class="sxs-lookup"><span data-stu-id="63663-144">-Policy</span></span>

<span data-ttu-id="63663-145">Объект политики защиты.</span><span class="sxs-lookup"><span data-stu-id="63663-145">Protection policy object.</span></span>

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

### <span data-ttu-id="63663-146">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="63663-146">-ProtectionState</span></span>

<span data-ttu-id="63663-147">Определяет состояние защиты.</span><span class="sxs-lookup"><span data-stu-id="63663-147">Specifies the state of protection.</span></span>
<span data-ttu-id="63663-148">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="63663-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="63663-149">IRPending.</span><span class="sxs-lookup"><span data-stu-id="63663-149">IRPending.</span></span>
<span data-ttu-id="63663-150">Начальная синхронизация не начата, и точка восстановления пока не установлена.</span><span class="sxs-lookup"><span data-stu-id="63663-150">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="63663-151">Защищено.</span><span class="sxs-lookup"><span data-stu-id="63663-151">Protected.</span></span>
<span data-ttu-id="63663-152">Защита в настоящее время продолжается.</span><span class="sxs-lookup"><span data-stu-id="63663-152">Protection is ongoing.</span></span>
- <span data-ttu-id="63663-153">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="63663-153">ProtectionError.</span></span>
<span data-ttu-id="63663-154">Ошибка защиты.</span><span class="sxs-lookup"><span data-stu-id="63663-154">There is a protection error.</span></span>
- <span data-ttu-id="63663-155">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="63663-155">ProtectionStopped.</span></span>
<span data-ttu-id="63663-156">Защита отключена.</span><span class="sxs-lookup"><span data-stu-id="63663-156">Protection is disabled.</span></span>

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

### <span data-ttu-id="63663-157">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="63663-157">-ProtectionStatus</span></span>

<span data-ttu-id="63663-158">Определяет общее состояние защиты элемента в контейнере.</span><span class="sxs-lookup"><span data-stu-id="63663-158">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="63663-159">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="63663-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="63663-160">Здоровое питание</span><span class="sxs-lookup"><span data-stu-id="63663-160">Healthy</span></span>
- <span data-ttu-id="63663-161">Неработоспособная</span><span class="sxs-lookup"><span data-stu-id="63663-161">Unhealthy</span></span>

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

### <span data-ttu-id="63663-162">-VaultId</span><span class="sxs-lookup"><span data-stu-id="63663-162">-VaultId</span></span>

<span data-ttu-id="63663-163">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="63663-163">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="63663-164">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="63663-164">-WorkloadType</span></span>

<span data-ttu-id="63663-165">Тип рабочей нагрузки ресурса.</span><span class="sxs-lookup"><span data-stu-id="63663-165">Workload type of the resource.</span></span> <span data-ttu-id="63663-166">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="63663-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="63663-167">AzureVM</span><span class="sxs-lookup"><span data-stu-id="63663-167">AzureVM</span></span>
- <span data-ttu-id="63663-168">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="63663-168">AzureFiles</span></span>
- <span data-ttu-id="63663-169">MSSQL</span><span class="sxs-lookup"><span data-stu-id="63663-169">MSSQL</span></span>

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

### <span data-ttu-id="63663-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63663-170">CommonParameters</span></span>
<span data-ttu-id="63663-171">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63663-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63663-172">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63663-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63663-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63663-173">INPUTS</span></span>

### <span data-ttu-id="63663-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="63663-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="63663-175">System.String</span><span class="sxs-lookup"><span data-stu-id="63663-175">System.String</span></span>

## <span data-ttu-id="63663-176">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="63663-176">OUTPUTS</span></span>

### <span data-ttu-id="63663-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="63663-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="63663-178">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="63663-178">NOTES</span></span>

## <span data-ttu-id="63663-179">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63663-179">RELATED LINKS</span></span>

[<span data-ttu-id="63663-180">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="63663-180">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="63663-181">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="63663-181">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="63663-182">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="63663-182">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="63663-183">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="63663-183">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
