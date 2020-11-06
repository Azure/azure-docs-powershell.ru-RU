---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 856B76FC-88ED-4A29-9DC6-C482398D702E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/restore-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
ms.openlocfilehash: a203d125e4ff6d811a581b0713ca4a002e098ade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567450"
---
# <span data-ttu-id="ae56d-101">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="ae56d-101">Restore-AzureRmBackupItem</span></span>

## <span data-ttu-id="ae56d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae56d-102">SYNOPSIS</span></span>
<span data-ttu-id="ae56d-103">Восстанавливает данные и конфигурацию элемента резервного копирования в точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="ae56d-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae56d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae56d-104">SYNTAX</span></span>

```
Restore-AzureRmBackupItem [-StorageAccountName] <String> [-RecoveryPoint] <AzureRMBackupRecoveryPoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae56d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae56d-105">DESCRIPTION</span></span>
<span data-ttu-id="ae56d-106">Командлет **RESTORE-AzureRmBackupItem** восстанавливает данные и конфигурацию элемента резервного копирования Azure для указанной точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="ae56d-106">The **Restore-AzureRmBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="ae56d-107">Этот командлет запускает восстановление из резервного хранилища в учетную запись.</span><span class="sxs-lookup"><span data-stu-id="ae56d-107">This cmdlet starts the restore from the Backup vault to your account.</span></span>

<span data-ttu-id="ae56d-108">Операция восстановления не восстанавливает полную виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ae56d-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="ae56d-109">Она восстанавливает данные о дисках и сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ae56d-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="ae56d-110">После завершения операции восстановления необходимо создать виртуальную машину и запустить ее.</span><span class="sxs-lookup"><span data-stu-id="ae56d-110">After the restore operation finished, you must create the virtual machine and start it.</span></span>

## <span data-ttu-id="ae56d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae56d-111">EXAMPLES</span></span>

### <span data-ttu-id="ae56d-112">Пример 1: Восстановление виртуальной машины в точке восстановления</span><span class="sxs-lookup"><span data-stu-id="ae56d-112">Example 1: Restore a virtual machine to a recovery point</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> $RecoveryPoint = Get-AzureRmBackupRecoveryPoint -Item $BackupItem 
PS C:\> Restore-AzureRmBackupItem -StorageAccountName "DestinationAccount" -RecoveryPoint $RecoveryPoint 
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Restore         InProgress      26-Aug-15 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="ae56d-113">Первая команда получает хранилище с именем Vault03 с помощью командлета Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="ae56d-113">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="ae56d-114">Команда сохраняет этот объект в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="ae56d-114">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="ae56d-115">Вторая команда получает контейнер с указанным именем в хранилище $Vault с помощью командлета **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="ae56d-115">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="ae56d-116">Команда сохраняет этот объект в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="ae56d-116">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="ae56d-117">Третья команда возвращает элемент резервного копирования в контейнере $Container с помощью командлета **Get-AzureRmBackupItem** .</span><span class="sxs-lookup"><span data-stu-id="ae56d-117">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="ae56d-118">Команда сохраняет этот объект в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="ae56d-118">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="ae56d-119">Четвертая команда получает точку восстановления для элемента в $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="ae56d-119">The fourth command gets recovery point for the item in $BackupItem.</span></span>
<span data-ttu-id="ae56d-120">Команда сохраняет этот объект в переменной $RecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="ae56d-120">The command stores that object in the $RecoveryPoint variable.</span></span>

<span data-ttu-id="ae56d-121">Последняя команда восстанавливает точку восстановления в $RecoveryPoint для учетной записи с именем DestinationAccount.</span><span class="sxs-lookup"><span data-stu-id="ae56d-121">The final command restores the recovery point in $RecoveryPoint for the account named DestinationAccount.</span></span>

## <span data-ttu-id="ae56d-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae56d-122">PARAMETERS</span></span>

### <span data-ttu-id="ae56d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae56d-123">-DefaultProfile</span></span>
<span data-ttu-id="ae56d-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ae56d-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae56d-125">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ae56d-125">-RecoveryPoint</span></span>
<span data-ttu-id="ae56d-126">Указывает точку восстановления, в которую нужно восстановить виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ae56d-126">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="ae56d-127">Чтобы получить **AzureRmBackupRecoveryPoint** , используйте командлет Get-AzureRmBackupRecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="ae56d-127">To obtain an **AzureRmBackupRecoveryPoint** , use the Get-AzureRmBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: AzureRMBackupRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae56d-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ae56d-128">-StorageAccountName</span></span>
<span data-ttu-id="ae56d-129">Указывает имя целевой учетной записи хранения в подписке.</span><span class="sxs-lookup"><span data-stu-id="ae56d-129">Specifies the name of the target storage account in your subscription.</span></span>
<span data-ttu-id="ae56d-130">В ходе процесса восстановления этот командлет сохраняет диски и сведения о конфигурации в этой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ae56d-130">As a part of the restore process, this cmdlet stores the disks and the configuration information in this storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae56d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae56d-131">CommonParameters</span></span>
<span data-ttu-id="ae56d-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae56d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae56d-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae56d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae56d-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae56d-134">INPUTS</span></span>

### <span data-ttu-id="ae56d-135">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ae56d-135">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="ae56d-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae56d-136">OUTPUTS</span></span>

### <span data-ttu-id="ae56d-137">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="ae56d-137">AzureRmBackupJob</span></span>

## <span data-ttu-id="ae56d-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae56d-138">NOTES</span></span>

## <span data-ttu-id="ae56d-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae56d-139">RELATED LINKS</span></span>

[<span data-ttu-id="ae56d-140">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="ae56d-140">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="ae56d-141">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="ae56d-141">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="ae56d-142">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ae56d-142">Get-AzureRmBackupRecoveryPoint</span></span>](./Get-AzureRmBackupRecoveryPoint.md)


