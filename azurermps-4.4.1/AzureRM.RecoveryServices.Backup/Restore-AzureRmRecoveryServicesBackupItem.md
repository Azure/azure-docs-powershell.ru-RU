---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: c12241457b78d9020e447b6f464d5623e90d52b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568701"
---
# <span data-ttu-id="3e0db-101">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3e0db-101">Restore-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="3e0db-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e0db-102">SYNOPSIS</span></span>
<span data-ttu-id="3e0db-103">Восстанавливает данные и конфигурацию элемента резервного копирования в точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="3e0db-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e0db-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e0db-104">SYNTAX</span></span>

```
Restore-AzureRmRecoveryServicesBackupItem [-RecoveryPoint] <RecoveryPointBase> [-StorageAccountName] <String>
 [-StorageAccountResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e0db-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e0db-105">DESCRIPTION</span></span>
<span data-ttu-id="3e0db-106">Командлет **RESTORE-AzureRmRecoveryServicesBackupItem** восстанавливает данные и конфигурацию элемента резервного копирования Azure для указанной точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="3e0db-106">The **Restore-AzureRmRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="3e0db-107">Этот командлет запускает восстановление из хранилища служб восстановления на учетную запись хранения клиента.</span><span class="sxs-lookup"><span data-stu-id="3e0db-107">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>

<span data-ttu-id="3e0db-108">Операция восстановления не восстанавливает полную виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="3e0db-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="3e0db-109">Она восстанавливает данные о дисках и сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3e0db-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="3e0db-110">После завершения операции восстановления необходимо создать виртуальную машину и запустить ее.</span><span class="sxs-lookup"><span data-stu-id="3e0db-110">After the restore operation is finished, you must create the virtual machine and start it.</span></span>

<span data-ttu-id="3e0db-111">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="3e0db-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="3e0db-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e0db-112">EXAMPLES</span></span>

### <span data-ttu-id="3e0db-113">Пример 1: Восстановление элемента в точке восстановления</span><span class="sxs-lookup"><span data-stu-id="3e0db-113">Example 1: Restore an item to a recovery point</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzureRmRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="3e0db-114">Первая команда получает контейнер резервного копирования типа AzureVM и сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="3e0db-114">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="3e0db-115">Вторая команда получает элемент резервного копирования с именем V2VM from $Container и сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="3e0db-115">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>

<span data-ttu-id="3e0db-116">Третья команда получает дату из семи дней раньше и сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="3e0db-116">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>

<span data-ttu-id="3e0db-117">Четвертая команда получает текущую дату, а затем сохраняет ее в переменной $EndDate.</span><span class="sxs-lookup"><span data-stu-id="3e0db-117">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>

<span data-ttu-id="3e0db-118">Пятая команда возвращает список точек восстановления для определенного элемента резервного копирования, отфильтрованного по $StartDate и $EndDate.</span><span class="sxs-lookup"><span data-stu-id="3e0db-118">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="3e0db-119">Указанный диапазон дат — последние 7 дней.</span><span class="sxs-lookup"><span data-stu-id="3e0db-119">The date range specified is the last 7 days.</span></span>

<span data-ttu-id="3e0db-120">Последняя команда восстанавливает диски на целевую учетную запись хранения DestAccount в группе ресурсов DestRG.</span><span class="sxs-lookup"><span data-stu-id="3e0db-120">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="3e0db-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e0db-121">PARAMETERS</span></span>

### <span data-ttu-id="3e0db-122">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3e0db-122">-RecoveryPoint</span></span>
<span data-ttu-id="3e0db-123">Указывает точку восстановления, в которую нужно восстановить виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="3e0db-123">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="3e0db-124">Чтобы получить объект **AzureRmRecoveryServicesBackupRecoveryPoint** , используйте командлет Get-AzureRmRecoveryServicesBackupRecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="3e0db-124">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e0db-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3e0db-125">-StorageAccountName</span></span>
<span data-ttu-id="3e0db-126">Указывает имя целевой учетной записи хранения в подписке.</span><span class="sxs-lookup"><span data-stu-id="3e0db-126">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="3e0db-127">В ходе процесса восстановления этот командлет сохраняет диски и сведения о конфигурации в этой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3e0db-127">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e0db-128">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e0db-128">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="3e0db-129">Указывает имя группы ресурсов, которая содержит целевую учетную запись хранилища в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="3e0db-129">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="3e0db-130">В ходе процесса восстановления этот командлет сохраняет диски и сведения о конфигурации в этой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3e0db-130">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e0db-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e0db-131">-DefaultProfile</span></span>
<span data-ttu-id="3e0db-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e0db-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e0db-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e0db-133">CommonParameters</span></span>
<span data-ttu-id="3e0db-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e0db-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e0db-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e0db-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e0db-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e0db-136">INPUTS</span></span>

### <span data-ttu-id="3e0db-137">RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="3e0db-137">RecoveryPointBase</span></span>
<span data-ttu-id="3e0db-138">Параметр "RecoveryPoint" принимает значение типа "RecoveryPointBase" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3e0db-138">Parameter 'RecoveryPoint' accepts value of type 'RecoveryPointBase' from the pipeline</span></span>

## <span data-ttu-id="3e0db-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e0db-139">OUTPUTS</span></span>

### <span data-ttu-id="3e0db-140">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="3e0db-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="3e0db-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e0db-141">NOTES</span></span>

## <span data-ttu-id="3e0db-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e0db-142">RELATED LINKS</span></span>

[<span data-ttu-id="3e0db-143">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3e0db-143">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="3e0db-144">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3e0db-144">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="3e0db-145">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3e0db-145">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


