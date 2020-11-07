---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 03da361f8dd68d345782568dc243d4438cad1d77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734534"
---
# <span data-ttu-id="3b3e6-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3b3e6-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="3b3e6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b3e6-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3e6-103">Получает элементы из контейнера в резервной копии.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b3e6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b3e6-104">SYNTAX</span></span>

### <span data-ttu-id="3b3e6-105">GetItemsForContainer (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3b3e6-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b3e6-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="3b3e6-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b3e6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b3e6-107">DESCRIPTION</span></span>
<span data-ttu-id="3b3e6-108">Командлет **Get-AzureRmRecoveryServicesBackupItem** получает элементы в контейнере или значение в резервной копии Azure и состояние защиты элементов.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-108">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>

<span data-ttu-id="3b3e6-109">Контейнер, зарегистрированный в хранилище служб восстановления Azure, может содержать один или несколько элементов, которые можно защитить.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-109">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="3b3e6-110">Для виртуальных машин Azure в контейнере виртуальных машин может быть только один элемент резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-110">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>

<span data-ttu-id="3b3e6-111">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="3b3e6-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b3e6-112">EXAMPLES</span></span>

### <span data-ttu-id="3b3e6-113">Пример 1: получение элемента из резервной копии контейнера</span><span class="sxs-lookup"><span data-stu-id="3b3e6-113">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="3b3e6-114">Первая команда получает контейнер типа AzureVM и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-114">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="3b3e6-115">Вторая команда возвращает элемент резервного копирования с именем V2VM в $Container, а затем сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-115">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="3b3e6-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b3e6-116">PARAMETERS</span></span>

### <span data-ttu-id="3b3e6-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="3b3e6-117">-BackupManagementType</span></span>
<span data-ttu-id="3b3e6-118">Указывает тип управления резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-118">Specifies the Backup management type.</span></span>
<span data-ttu-id="3b3e6-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3b3e6-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3b3e6-120">AzureVM</span><span class="sxs-lookup"><span data-stu-id="3b3e6-120">AzureVM</span></span> 
- <span data-ttu-id="3b3e6-121">Марс</span><span class="sxs-lookup"><span data-stu-id="3b3e6-121">MARS</span></span> 
- <span data-ttu-id="3b3e6-122">SCDPM</span><span class="sxs-lookup"><span data-stu-id="3b3e6-122">SCDPM</span></span> 
- <span data-ttu-id="3b3e6-123">AzureBackupServer AzureSQL</span><span class="sxs-lookup"><span data-stu-id="3b3e6-123">AzureBackupServer AzureSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3e6-124">-Container</span><span class="sxs-lookup"><span data-stu-id="3b3e6-124">-Container</span></span>
<span data-ttu-id="3b3e6-125">Указывает объект-контейнер, из которого этот командлет получает элементы резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-125">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="3b3e6-126">Чтобы получить **AzureRmRecoveryServicesBackupContainer** , используйте командлет Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-126">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="3b3e6-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3b3e6-127">-Name</span></span>
<span data-ttu-id="3b3e6-128">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-128">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="3b3e6-129">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="3b3e6-129">-ProtectionState</span></span>
<span data-ttu-id="3b3e6-130">Указывает состояние защиты.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-130">Specifies the state of protection.</span></span>
<span data-ttu-id="3b3e6-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3b3e6-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3b3e6-132">IRPending.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-132">IRPending.</span></span>
<span data-ttu-id="3b3e6-133">Начальная синхронизация не начата, но пока нет точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-133">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="3b3e6-134">Защищенного.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-134">Protected.</span></span>
<span data-ttu-id="3b3e6-135">Защита в настоящеем.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-135">Protection is ongoing.</span></span> 
- <span data-ttu-id="3b3e6-136">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-136">ProtectionError.</span></span>
<span data-ttu-id="3b3e6-137">Произошла ошибка защиты.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-137">There is a protection error.</span></span>
- <span data-ttu-id="3b3e6-138">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-138">ProtectionStopped.</span></span>
<span data-ttu-id="3b3e6-139">Защита отключена.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-139">Protection is disabled.</span></span>

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

### <span data-ttu-id="3b3e6-140">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="3b3e6-140">-ProtectionStatus</span></span>
<span data-ttu-id="3b3e6-141">Определяет общее состояние защиты элемента в контейнере.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-141">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="3b3e6-142">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3b3e6-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3b3e6-143">Исправно</span><span class="sxs-lookup"><span data-stu-id="3b3e6-143">Healthy</span></span>
- <span data-ttu-id="3b3e6-144">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="3b3e6-144">Unhealthy</span></span>

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

### <span data-ttu-id="3b3e6-145">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="3b3e6-145">-WorkloadType</span></span>
<span data-ttu-id="3b3e6-146">Указывает тип рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-146">Specifies the workload type.</span></span> <span data-ttu-id="3b3e6-147">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3b3e6-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3b3e6-148">AzureVM</span><span class="sxs-lookup"><span data-stu-id="3b3e6-148">AzureVM</span></span> 
- <span data-ttu-id="3b3e6-149">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="3b3e6-149">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3e6-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b3e6-150">-DefaultProfile</span></span>
<span data-ttu-id="3b3e6-151">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b3e6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3e6-152">CommonParameters</span></span>
<span data-ttu-id="3b3e6-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3e6-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b3e6-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3e6-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b3e6-155">INPUTS</span></span>

## <span data-ttu-id="3b3e6-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b3e6-156">OUTPUTS</span></span>

### <span data-ttu-id="3b3e6-157">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="3b3e6-157">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="3b3e6-158">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase]</span><span class="sxs-lookup"><span data-stu-id="3b3e6-158">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase]</span></span>

## <span data-ttu-id="3b3e6-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b3e6-159">NOTES</span></span>

## <span data-ttu-id="3b3e6-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b3e6-160">RELATED LINKS</span></span>

[<span data-ttu-id="3b3e6-161">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3b3e6-161">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="3b3e6-162">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="3b3e6-162">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="3b3e6-163">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3b3e6-163">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="3b3e6-164">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3b3e6-164">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


