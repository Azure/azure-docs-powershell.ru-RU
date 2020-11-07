---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 9a5d0f0607692217cf4016a1261f23b725d07e68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729692"
---
# <span data-ttu-id="708d5-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="708d5-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="708d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="708d5-102">SYNOPSIS</span></span>
<span data-ttu-id="708d5-103">Возвращает точки восстановления для резервного элемента.</span><span class="sxs-lookup"><span data-stu-id="708d5-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="708d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="708d5-104">SYNTAX</span></span>

### <span data-ttu-id="708d5-105">NoFilterParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="708d5-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="708d5-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="708d5-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="708d5-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="708d5-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="708d5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="708d5-108">DESCRIPTION</span></span>
<span data-ttu-id="708d5-109">Командлет **Get-AzRecoveryServicesBackupRecoveryPoint** получает точки восстановления для резервной копии элемента резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="708d5-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="708d5-110">После создания резервной копии элемента объект **AzureRmRecoveryServicesBackupRecoveryPoint** имеет одну или несколько точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="708d5-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="708d5-111">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="708d5-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="708d5-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="708d5-112">EXAMPLES</span></span>

### <span data-ttu-id="708d5-113">Пример 1: получение точек восстановления за последнюю неделю для элемента</span><span class="sxs-lookup"><span data-stu-id="708d5-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="708d5-114">Первая команда получает дату из семи дней назад и затем сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="708d5-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="708d5-115">Вторая команда получает текущую дату, а затем сохраняет ее в переменной $EndDate.</span><span class="sxs-lookup"><span data-stu-id="708d5-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="708d5-116">Третья команда получает контейнеры резервного копирования для AzureVM и сохраняет их в переменной $Containers.</span><span class="sxs-lookup"><span data-stu-id="708d5-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="708d5-117">Четвертая команда возвращает элемент резервного копирования с именем V2VM и сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="708d5-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="708d5-118">Последняя команда получает массив точек восстановления для элемента в $BackupItem, а затем сохраняет их в переменной $RP.</span><span class="sxs-lookup"><span data-stu-id="708d5-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="708d5-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="708d5-119">PARAMETERS</span></span>

### <span data-ttu-id="708d5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="708d5-120">-DefaultProfile</span></span>
<span data-ttu-id="708d5-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="708d5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="708d5-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="708d5-122">-EndDate</span></span>
<span data-ttu-id="708d5-123">Указывает конец диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="708d5-123">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="708d5-124">-Item</span><span class="sxs-lookup"><span data-stu-id="708d5-124">-Item</span></span>
<span data-ttu-id="708d5-125">Указывает элемент, для которого этот командлет получает точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="708d5-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="708d5-126">Чтобы получить объект **AzureRmRecoveryServicesBackupItem** , используйте командлет Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="708d5-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="708d5-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="708d5-127">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="708d5-128">Задает расположение для скачивания входного файла для восстановления ключа KeyVault для зашифрованной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="708d5-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="708d5-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="708d5-129">-RecoveryPointId</span></span>
<span data-ttu-id="708d5-130">Указывает идентификатор точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="708d5-130">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="708d5-131">-StartDate</span><span class="sxs-lookup"><span data-stu-id="708d5-131">-StartDate</span></span>
<span data-ttu-id="708d5-132">Задает начало диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="708d5-132">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="708d5-133">-VaultId</span><span class="sxs-lookup"><span data-stu-id="708d5-133">-VaultId</span></span>
<span data-ttu-id="708d5-134">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="708d5-134">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="708d5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="708d5-135">CommonParameters</span></span>
<span data-ttu-id="708d5-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="708d5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="708d5-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="708d5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="708d5-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="708d5-138">INPUTS</span></span>

### <span data-ttu-id="708d5-139">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="708d5-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="708d5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="708d5-140">System.String</span></span>

## <span data-ttu-id="708d5-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="708d5-141">OUTPUTS</span></span>

### <span data-ttu-id="708d5-142">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="708d5-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="708d5-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="708d5-143">NOTES</span></span>

## <span data-ttu-id="708d5-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="708d5-144">RELATED LINKS</span></span>

[<span data-ttu-id="708d5-145">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="708d5-145">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="708d5-146">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="708d5-146">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


