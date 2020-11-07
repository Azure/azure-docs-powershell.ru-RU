---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: c861bbe3b422360f58f36cbe859343f7dcc7ed37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729713"
---
# <span data-ttu-id="96cd6-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="96cd6-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="96cd6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="96cd6-103">Получает элементы из контейнера в резервной копии.</span><span class="sxs-lookup"><span data-stu-id="96cd6-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="96cd6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96cd6-104">SYNTAX</span></span>

### <span data-ttu-id="96cd6-105">GetItemsForContainer (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96cd6-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="96cd6-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="96cd6-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="96cd6-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="96cd6-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96cd6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96cd6-108">DESCRIPTION</span></span>
<span data-ttu-id="96cd6-109">Командлет **Get-AzRecoveryServicesBackupItem** получает элементы в контейнере или значение в резервной копии Azure и состояние защиты элементов.</span><span class="sxs-lookup"><span data-stu-id="96cd6-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="96cd6-110">Контейнер, зарегистрированный в хранилище служб восстановления Azure, может содержать один или несколько элементов, которые можно защитить.</span><span class="sxs-lookup"><span data-stu-id="96cd6-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="96cd6-111">Для виртуальных машин Azure в контейнере виртуальных машин может быть только один элемент резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="96cd6-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="96cd6-112">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="96cd6-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="96cd6-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96cd6-113">EXAMPLES</span></span>

### <span data-ttu-id="96cd6-114">Пример 1: получение элемента из резервной копии контейнера</span><span class="sxs-lookup"><span data-stu-id="96cd6-114">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="96cd6-115">Первая команда получает контейнер типа AzureVM и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="96cd6-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="96cd6-116">Вторая команда возвращает элемент резервного копирования с именем V2VM в $Container, а затем сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="96cd6-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="96cd6-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96cd6-117">PARAMETERS</span></span>

### <span data-ttu-id="96cd6-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="96cd6-118">-BackupManagementType</span></span>
<span data-ttu-id="96cd6-119">Указывает тип управления резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="96cd6-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="96cd6-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="96cd6-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96cd6-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="96cd6-121">AzureVM</span></span> 
- <span data-ttu-id="96cd6-122">Марс</span><span class="sxs-lookup"><span data-stu-id="96cd6-122">MARS</span></span> 
- <span data-ttu-id="96cd6-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="96cd6-123">SCDPM</span></span> 
- <span data-ttu-id="96cd6-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="96cd6-124">AzureBackupServer</span></span> 
- <span data-ttu-id="96cd6-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="96cd6-125">AzureSQL</span></span>
- <span data-ttu-id="96cd6-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="96cd6-126">AzureStorage</span></span>

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

### <span data-ttu-id="96cd6-127">-Container</span><span class="sxs-lookup"><span data-stu-id="96cd6-127">-Container</span></span>
<span data-ttu-id="96cd6-128">Указывает объект-контейнер, из которого этот командлет получает элементы резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="96cd6-128">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="96cd6-129">Чтобы получить **AzureRmRecoveryServicesBackupContainer** , используйте командлет Get-AzRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="96cd6-129">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="96cd6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96cd6-130">-DefaultProfile</span></span>
<span data-ttu-id="96cd6-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96cd6-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96cd6-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="96cd6-132">-Name</span></span>
<span data-ttu-id="96cd6-133">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="96cd6-133">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="96cd6-134">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="96cd6-134">-Policy</span></span>
<span data-ttu-id="96cd6-135">Объект политики защиты.</span><span class="sxs-lookup"><span data-stu-id="96cd6-135">Protection policy object.</span></span>

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

### <span data-ttu-id="96cd6-136">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="96cd6-136">-ProtectionState</span></span>
<span data-ttu-id="96cd6-137">Указывает состояние защиты.</span><span class="sxs-lookup"><span data-stu-id="96cd6-137">Specifies the state of protection.</span></span>
<span data-ttu-id="96cd6-138">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="96cd6-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96cd6-139">IRPending.</span><span class="sxs-lookup"><span data-stu-id="96cd6-139">IRPending.</span></span>
<span data-ttu-id="96cd6-140">Начальная синхронизация не начата, но пока нет точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="96cd6-140">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="96cd6-141">Защищенного.</span><span class="sxs-lookup"><span data-stu-id="96cd6-141">Protected.</span></span>
<span data-ttu-id="96cd6-142">Защита в настоящеем.</span><span class="sxs-lookup"><span data-stu-id="96cd6-142">Protection is ongoing.</span></span> 
- <span data-ttu-id="96cd6-143">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="96cd6-143">ProtectionError.</span></span>
<span data-ttu-id="96cd6-144">Произошла ошибка защиты.</span><span class="sxs-lookup"><span data-stu-id="96cd6-144">There is a protection error.</span></span>
- <span data-ttu-id="96cd6-145">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="96cd6-145">ProtectionStopped.</span></span>
<span data-ttu-id="96cd6-146">Защита отключена.</span><span class="sxs-lookup"><span data-stu-id="96cd6-146">Protection is disabled.</span></span>

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

### <span data-ttu-id="96cd6-147">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="96cd6-147">-ProtectionStatus</span></span>
<span data-ttu-id="96cd6-148">Определяет общее состояние защиты элемента в контейнере.</span><span class="sxs-lookup"><span data-stu-id="96cd6-148">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="96cd6-149">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="96cd6-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96cd6-150">Исправно</span><span class="sxs-lookup"><span data-stu-id="96cd6-150">Healthy</span></span>
- <span data-ttu-id="96cd6-151">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="96cd6-151">Unhealthy</span></span>

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

### <span data-ttu-id="96cd6-152">-VaultId</span><span class="sxs-lookup"><span data-stu-id="96cd6-152">-VaultId</span></span>
<span data-ttu-id="96cd6-153">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="96cd6-153">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="96cd6-154">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="96cd6-154">-WorkloadType</span></span>
<span data-ttu-id="96cd6-155">Указывает тип рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="96cd6-155">Specifies the workload type.</span></span> <span data-ttu-id="96cd6-156">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="96cd6-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96cd6-157">AzureVM</span><span class="sxs-lookup"><span data-stu-id="96cd6-157">AzureVM</span></span> 
- <span data-ttu-id="96cd6-158">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="96cd6-158">AzureSQLDatabase</span></span>
- <span data-ttu-id="96cd6-159">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="96cd6-159">AzureFiles</span></span>

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

### <span data-ttu-id="96cd6-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96cd6-160">CommonParameters</span></span>
<span data-ttu-id="96cd6-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96cd6-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96cd6-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96cd6-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96cd6-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96cd6-163">INPUTS</span></span>

### <span data-ttu-id="96cd6-164">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="96cd6-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="96cd6-165">System. String</span><span class="sxs-lookup"><span data-stu-id="96cd6-165">System.String</span></span>

## <span data-ttu-id="96cd6-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96cd6-166">OUTPUTS</span></span>

### <span data-ttu-id="96cd6-167">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="96cd6-167">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="96cd6-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="96cd6-168">NOTES</span></span>

## <span data-ttu-id="96cd6-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96cd6-169">RELATED LINKS</span></span>

[<span data-ttu-id="96cd6-170">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="96cd6-170">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="96cd6-171">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="96cd6-171">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="96cd6-172">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="96cd6-172">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="96cd6-173">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="96cd6-173">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)


