---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 2703ca4684d3bf59f5b3fd47415897a2c80f6c3d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074730"
---
# <span data-ttu-id="f0b0e-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f0b0e-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="f0b0e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0b0e-102">SYNOPSIS</span></span>

<span data-ttu-id="f0b0e-103">Возвращает точки восстановления для резервного элемента.</span><span class="sxs-lookup"><span data-stu-id="f0b0e-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="f0b0e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0b0e-104">SYNTAX</span></span>

### <span data-ttu-id="f0b0e-105">NoFilterParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0b0e-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0b0e-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="f0b0e-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0b0e-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="f0b0e-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0b0e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0b0e-108">DESCRIPTION</span></span>

<span data-ttu-id="f0b0e-109">Командлет **Get-AzRecoveryServicesBackupRecoveryPoint** получает точки восстановления для резервной копии элемента резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="f0b0e-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="f0b0e-110">После создания резервной копии элемента объект **AzureRmRecoveryServicesBackupRecoveryPoint** имеет одну или несколько точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="f0b0e-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="f0b0e-111">Задайте контекст хранилища с помощью параметра-VaultId.</span><span class="sxs-lookup"><span data-stu-id="f0b0e-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="f0b0e-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0b0e-112">EXAMPLES</span></span>

### <span data-ttu-id="f0b0e-113">Пример 1: получение точек восстановления за последнюю неделю для элемента</span><span class="sxs-lookup"><span data-stu-id="f0b0e-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="f0b0e-114">Первая команда получает дату из семи дней назад и затем сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="f0b0e-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="f0b0e-115">Вторая команда получает текущую дату, а затем сохраняет ее в переменной $EndDate.</span><span class="sxs-lookup"><span data-stu-id="f0b0e-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="f0b0e-116">Третья команда получает контейнеры резервного копирования для AzureVM и сохраняет их в переменной $Containers.</span><span class="sxs-lookup"><span data-stu-id="f0b0e-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="f0b0e-117">Четвертая команда возвращает элемент резервного копирования с именем V2VM и сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="f0b0e-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="f0b0e-118">Последняя команда получает массив точек восстановления для элемента в $BackupItem, а затем сохраняет их в переменной $RP.</span><span class="sxs-lookup"><span data-stu-id="f0b0e-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="f0b0e-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0b0e-119">PARAMETERS</span></span>

### <span data-ttu-id="f0b0e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0b0e-120">-DefaultProfile</span></span>

<span data-ttu-id="f0b0e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0b0e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0b0e-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="f0b0e-122">-EndDate</span></span>

<span data-ttu-id="f0b0e-123">Указывает конец диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="f0b0e-123">Specifies the end of the date range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b0e-124">-Item</span><span class="sxs-lookup"><span data-stu-id="f0b0e-124">-Item</span></span>

<span data-ttu-id="f0b0e-125">Указывает элемент, для которого этот командлет получает точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="f0b0e-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="f0b0e-126">Чтобы получить объект **AzureRmRecoveryServicesBackupItem** , используйте командлет **Get-AzRecoveryServicesBackupItem** .</span><span class="sxs-lookup"><span data-stu-id="f0b0e-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b0e-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="f0b0e-127">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="f0b0e-128">Задает расположение для скачивания входного файла для восстановления ключа KeyVault для зашифрованной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0b0e-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b0e-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="f0b0e-129">-RecoveryPointId</span></span>

<span data-ttu-id="f0b0e-130">Указывает идентификатор точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="f0b0e-130">Specifies the recovery point ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b0e-131">-StartDate</span><span class="sxs-lookup"><span data-stu-id="f0b0e-131">-StartDate</span></span>

<span data-ttu-id="f0b0e-132">Задает начало диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="f0b0e-132">Specifies the start of the date range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b0e-133">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f0b0e-133">-VaultId</span></span>

<span data-ttu-id="f0b0e-134">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="f0b0e-134">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f0b0e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0b0e-135">CommonParameters</span></span>
<span data-ttu-id="f0b0e-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0b0e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0b0e-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0b0e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0b0e-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0b0e-138">INPUTS</span></span>

### <span data-ttu-id="f0b0e-139">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="f0b0e-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="f0b0e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f0b0e-140">System.String</span></span>

## <span data-ttu-id="f0b0e-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0b0e-141">OUTPUTS</span></span>

### <span data-ttu-id="f0b0e-142">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="f0b0e-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="f0b0e-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0b0e-143">NOTES</span></span>

## <span data-ttu-id="f0b0e-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0b0e-144">RELATED LINKS</span></span>

[<span data-ttu-id="f0b0e-145">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f0b0e-145">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="f0b0e-146">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="f0b0e-146">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
