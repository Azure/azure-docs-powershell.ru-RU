---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 9b836a4c4c056699e2c74bcb4d5b373f5bfe170e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558951"
---
# <span data-ttu-id="fa33d-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="fa33d-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="fa33d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa33d-102">SYNOPSIS</span></span>
<span data-ttu-id="fa33d-103">Получает элементы из контейнера в резервной копии.</span><span class="sxs-lookup"><span data-stu-id="fa33d-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa33d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa33d-104">SYNTAX</span></span>

### <span data-ttu-id="fa33d-105">GetItemsForContainer (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fa33d-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa33d-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="fa33d-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa33d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa33d-107">DESCRIPTION</span></span>
<span data-ttu-id="fa33d-108">Командлет **Get-AzureRmRecoveryServicesBackupItem** получает элементы в контейнере или значение в резервной копии Azure и состояние защиты элементов.</span><span class="sxs-lookup"><span data-stu-id="fa33d-108">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>

<span data-ttu-id="fa33d-109">Контейнер, зарегистрированный в хранилище служб восстановления Azure, может содержать один или несколько элементов, которые можно защитить.</span><span class="sxs-lookup"><span data-stu-id="fa33d-109">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="fa33d-110">Для виртуальных машин Azure в контейнере виртуальных машин может быть только один элемент резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="fa33d-110">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>

<span data-ttu-id="fa33d-111">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="fa33d-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="fa33d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa33d-112">EXAMPLES</span></span>

### <span data-ttu-id="fa33d-113">Пример 1: получение элемента из резервной копии контейнера</span><span class="sxs-lookup"><span data-stu-id="fa33d-113">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="fa33d-114">Первая команда получает контейнер типа AzureVM и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="fa33d-114">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="fa33d-115">Вторая команда возвращает элемент резервного копирования с именем V2VM в $Container, а затем сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="fa33d-115">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="fa33d-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa33d-116">PARAMETERS</span></span>

### <span data-ttu-id="fa33d-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="fa33d-117">-BackupManagementType</span></span>
<span data-ttu-id="fa33d-118">Указывает тип управления резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="fa33d-118">Specifies the Backup management type.</span></span>
<span data-ttu-id="fa33d-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fa33d-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fa33d-120">AzureVM</span><span class="sxs-lookup"><span data-stu-id="fa33d-120">AzureVM</span></span> 
- <span data-ttu-id="fa33d-121">Марс</span><span class="sxs-lookup"><span data-stu-id="fa33d-121">MARS</span></span> 
- <span data-ttu-id="fa33d-122">SCDPM</span><span class="sxs-lookup"><span data-stu-id="fa33d-122">SCDPM</span></span> 
- <span data-ttu-id="fa33d-123">AzureBackupServer AzureSQL</span><span class="sxs-lookup"><span data-stu-id="fa33d-123">AzureBackupServer AzureSQL</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: GetItemsForVault
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa33d-124">-Container</span><span class="sxs-lookup"><span data-stu-id="fa33d-124">-Container</span></span>
<span data-ttu-id="fa33d-125">Указывает объект-контейнер, из которого этот командлет получает элементы резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="fa33d-125">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="fa33d-126">Чтобы получить **AzureRmRecoveryServicesBackupContainer** , используйте командлет Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="fa33d-126">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: ContainerBase
Parameter Sets: GetItemsForContainer
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa33d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa33d-127">-DefaultProfile</span></span>
<span data-ttu-id="fa33d-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa33d-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa33d-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fa33d-129">-Name</span></span>
<span data-ttu-id="fa33d-130">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="fa33d-130">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa33d-131">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="fa33d-131">-ProtectionState</span></span>
<span data-ttu-id="fa33d-132">Указывает состояние защиты.</span><span class="sxs-lookup"><span data-stu-id="fa33d-132">Specifies the state of protection.</span></span>
<span data-ttu-id="fa33d-133">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fa33d-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fa33d-134">IRPending.</span><span class="sxs-lookup"><span data-stu-id="fa33d-134">IRPending.</span></span>
<span data-ttu-id="fa33d-135">Начальная синхронизация не начата, но пока нет точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="fa33d-135">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="fa33d-136">Защищенного.</span><span class="sxs-lookup"><span data-stu-id="fa33d-136">Protected.</span></span>
<span data-ttu-id="fa33d-137">Защита в настоящеем.</span><span class="sxs-lookup"><span data-stu-id="fa33d-137">Protection is ongoing.</span></span> 
- <span data-ttu-id="fa33d-138">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="fa33d-138">ProtectionError.</span></span>
<span data-ttu-id="fa33d-139">Произошла ошибка защиты.</span><span class="sxs-lookup"><span data-stu-id="fa33d-139">There is a protection error.</span></span>
- <span data-ttu-id="fa33d-140">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="fa33d-140">ProtectionStopped.</span></span>
<span data-ttu-id="fa33d-141">Защита отключена.</span><span class="sxs-lookup"><span data-stu-id="fa33d-141">Protection is disabled.</span></span>

```yaml
Type: ItemProtectionState
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa33d-142">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="fa33d-142">-ProtectionStatus</span></span>
<span data-ttu-id="fa33d-143">Определяет общее состояние защиты элемента в контейнере.</span><span class="sxs-lookup"><span data-stu-id="fa33d-143">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="fa33d-144">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fa33d-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fa33d-145">Исправно</span><span class="sxs-lookup"><span data-stu-id="fa33d-145">Healthy</span></span>
- <span data-ttu-id="fa33d-146">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="fa33d-146">Unhealthy</span></span>

```yaml
Type: ItemProtectionStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa33d-147">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="fa33d-147">-WorkloadType</span></span>
<span data-ttu-id="fa33d-148">Указывает тип рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="fa33d-148">Specifies the workload type.</span></span> <span data-ttu-id="fa33d-149">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fa33d-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fa33d-150">AzureVM</span><span class="sxs-lookup"><span data-stu-id="fa33d-150">AzureVM</span></span> 
- <span data-ttu-id="fa33d-151">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="fa33d-151">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa33d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa33d-152">CommonParameters</span></span>
<span data-ttu-id="fa33d-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa33d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa33d-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa33d-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa33d-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa33d-155">INPUTS</span></span>

### <span data-ttu-id="fa33d-156">Ничего</span><span class="sxs-lookup"><span data-stu-id="fa33d-156">None</span></span>
<span data-ttu-id="fa33d-157">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="fa33d-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fa33d-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa33d-158">OUTPUTS</span></span>

### <span data-ttu-id="fa33d-159">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="fa33d-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="fa33d-160">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase]</span><span class="sxs-lookup"><span data-stu-id="fa33d-160">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase]</span></span>

## <span data-ttu-id="fa33d-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa33d-161">NOTES</span></span>

## <span data-ttu-id="fa33d-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa33d-162">RELATED LINKS</span></span>

[<span data-ttu-id="fa33d-163">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="fa33d-163">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="fa33d-164">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="fa33d-164">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="fa33d-165">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="fa33d-165">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="fa33d-166">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="fa33d-166">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


