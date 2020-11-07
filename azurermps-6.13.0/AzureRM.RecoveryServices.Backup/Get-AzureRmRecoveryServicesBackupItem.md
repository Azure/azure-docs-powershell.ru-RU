---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: a1037f742fab47ae84edae6e1558e313e563c25a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733816"
---
# <span data-ttu-id="56907-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="56907-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="56907-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56907-102">SYNOPSIS</span></span>
<span data-ttu-id="56907-103">Получает элементы из контейнера в резервной копии.</span><span class="sxs-lookup"><span data-stu-id="56907-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56907-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56907-104">SYNTAX</span></span>

### <span data-ttu-id="56907-105">GetItemsForContainer (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="56907-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56907-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="56907-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56907-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="56907-107">GetItemsForPolicy</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56907-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56907-108">DESCRIPTION</span></span>
<span data-ttu-id="56907-109">Командлет **Get-AzureRmRecoveryServicesBackupItem** получает элементы в контейнере или значение в резервной копии Azure и состояние защиты элементов.</span><span class="sxs-lookup"><span data-stu-id="56907-109">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="56907-110">Контейнер, зарегистрированный в хранилище служб восстановления Azure, может содержать один или несколько элементов, которые можно защитить.</span><span class="sxs-lookup"><span data-stu-id="56907-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="56907-111">Для виртуальных машин Azure в контейнере виртуальных машин может быть только один элемент резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="56907-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="56907-112">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="56907-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="56907-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56907-113">EXAMPLES</span></span>

### <span data-ttu-id="56907-114">Пример 1: получение элемента из резервной копии контейнера</span><span class="sxs-lookup"><span data-stu-id="56907-114">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="56907-115">Первая команда получает контейнер типа AzureVM и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="56907-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="56907-116">Вторая команда возвращает элемент резервного копирования с именем V2VM в $Container, а затем сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="56907-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="56907-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56907-117">PARAMETERS</span></span>

### <span data-ttu-id="56907-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="56907-118">-BackupManagementType</span></span>
<span data-ttu-id="56907-119">Указывает тип управления резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="56907-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="56907-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="56907-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56907-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="56907-121">AzureVM</span></span> 
- <span data-ttu-id="56907-122">Марс</span><span class="sxs-lookup"><span data-stu-id="56907-122">MARS</span></span> 
- <span data-ttu-id="56907-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="56907-123">SCDPM</span></span> 
- <span data-ttu-id="56907-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="56907-124">AzureBackupServer</span></span> 
- <span data-ttu-id="56907-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="56907-125">AzureSQL</span></span>
- <span data-ttu-id="56907-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="56907-126">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56907-127">-Container</span><span class="sxs-lookup"><span data-stu-id="56907-127">-Container</span></span>
<span data-ttu-id="56907-128">Указывает объект-контейнер, из которого этот командлет получает элементы резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="56907-128">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="56907-129">Чтобы получить **AzureRmRecoveryServicesBackupContainer** , используйте командлет Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="56907-129">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="56907-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56907-130">-DefaultProfile</span></span>
<span data-ttu-id="56907-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56907-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56907-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="56907-132">-Name</span></span>
<span data-ttu-id="56907-133">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="56907-133">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="56907-134">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="56907-134">-Policy</span></span>
<span data-ttu-id="56907-135">Объект политики защиты.</span><span class="sxs-lookup"><span data-stu-id="56907-135">Protection policy object.</span></span>

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

### <span data-ttu-id="56907-136">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="56907-136">-ProtectionState</span></span>
<span data-ttu-id="56907-137">Указывает состояние защиты.</span><span class="sxs-lookup"><span data-stu-id="56907-137">Specifies the state of protection.</span></span>
<span data-ttu-id="56907-138">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="56907-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56907-139">IRPending.</span><span class="sxs-lookup"><span data-stu-id="56907-139">IRPending.</span></span>
<span data-ttu-id="56907-140">Начальная синхронизация не начата, но пока нет точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="56907-140">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="56907-141">Защищенного.</span><span class="sxs-lookup"><span data-stu-id="56907-141">Protected.</span></span>
<span data-ttu-id="56907-142">Защита в настоящеем.</span><span class="sxs-lookup"><span data-stu-id="56907-142">Protection is ongoing.</span></span> 
- <span data-ttu-id="56907-143">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="56907-143">ProtectionError.</span></span>
<span data-ttu-id="56907-144">Произошла ошибка защиты.</span><span class="sxs-lookup"><span data-stu-id="56907-144">There is a protection error.</span></span>
- <span data-ttu-id="56907-145">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="56907-145">ProtectionStopped.</span></span>
<span data-ttu-id="56907-146">Защита отключена.</span><span class="sxs-lookup"><span data-stu-id="56907-146">Protection is disabled.</span></span>

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

### <span data-ttu-id="56907-147">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="56907-147">-ProtectionStatus</span></span>
<span data-ttu-id="56907-148">Определяет общее состояние защиты элемента в контейнере.</span><span class="sxs-lookup"><span data-stu-id="56907-148">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="56907-149">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="56907-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56907-150">Исправно</span><span class="sxs-lookup"><span data-stu-id="56907-150">Healthy</span></span>
- <span data-ttu-id="56907-151">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="56907-151">Unhealthy</span></span>

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

### <span data-ttu-id="56907-152">-VaultId</span><span class="sxs-lookup"><span data-stu-id="56907-152">-VaultId</span></span>
<span data-ttu-id="56907-153">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="56907-153">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="56907-154">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="56907-154">-WorkloadType</span></span>
<span data-ttu-id="56907-155">Указывает тип рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="56907-155">Specifies the workload type.</span></span> <span data-ttu-id="56907-156">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="56907-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56907-157">AzureVM</span><span class="sxs-lookup"><span data-stu-id="56907-157">AzureVM</span></span> 
- <span data-ttu-id="56907-158">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="56907-158">AzureSQLDatabase</span></span>
- <span data-ttu-id="56907-159">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="56907-159">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56907-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56907-160">CommonParameters</span></span>
<span data-ttu-id="56907-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56907-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56907-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56907-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56907-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56907-163">INPUTS</span></span>

### <span data-ttu-id="56907-164">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="56907-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="56907-165">System. String</span><span class="sxs-lookup"><span data-stu-id="56907-165">System.String</span></span>
<span data-ttu-id="56907-166">Параметры: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="56907-166">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="56907-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56907-167">OUTPUTS</span></span>

### <span data-ttu-id="56907-168">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="56907-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="56907-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="56907-169">NOTES</span></span>

## <span data-ttu-id="56907-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56907-170">RELATED LINKS</span></span>

[<span data-ttu-id="56907-171">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="56907-171">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="56907-172">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="56907-172">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="56907-173">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="56907-173">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="56907-174">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="56907-174">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


