---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 676ba76cb4412e03c684be4d166e8707c5652b26
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393852"
---
# <span data-ttu-id="f4685-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f4685-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="f4685-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4685-102">SYNOPSIS</span></span>

<span data-ttu-id="f4685-103">Получает точки восстановления для элемента, который был восстановлен.</span><span class="sxs-lookup"><span data-stu-id="f4685-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="f4685-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f4685-104">SYNTAX</span></span>

### <span data-ttu-id="f4685-105">NoFilterParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f4685-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4685-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="f4685-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4685-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="f4685-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4685-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4685-108">DESCRIPTION</span></span>

<span data-ttu-id="f4685-109">С **его использованием** можно получить точки восстановления для резервного копирования в Azure.</span><span class="sxs-lookup"><span data-stu-id="f4685-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="f4685-110">После восстановления элемента у объекта **AzureRmRecoveryServicesBackupRecoveryPoint** будет одна или несколько точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="f4685-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="f4685-111">Задать контекст хранилища с помощью параметра -VaultId.</span><span class="sxs-lookup"><span data-stu-id="f4685-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="f4685-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f4685-112">EXAMPLES</span></span>

### <span data-ttu-id="f4685-113">Пример 1. Получить баллы за последнюю неделю для элемента</span><span class="sxs-lookup"><span data-stu-id="f4685-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="f4685-114">Первая команда получает объект vault на основе vaultName.</span><span class="sxs-lookup"><span data-stu-id="f4685-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="f4685-115">Вторая команда получает дату от семи дней назад и сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="f4685-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="f4685-116">Третья команда получает сегоднявую дату, а затем сохраняет ее в переменной $EndDate.</span><span class="sxs-lookup"><span data-stu-id="f4685-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="f4685-117">Четвертая команда получает контейнеры резервной копии AzureVM и сохраняет их в $Container переменной.</span><span class="sxs-lookup"><span data-stu-id="f4685-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="f4685-118">Пятая команда получает элемент резервной копии на основе workloadType, vaultId, а затем $BackupItem переменной.</span><span class="sxs-lookup"><span data-stu-id="f4685-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="f4685-119">Последняя команда получает массив точек восстановления для элемента в $BackupItem и сохраняет их в переменной $RP восстановления.</span><span class="sxs-lookup"><span data-stu-id="f4685-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="f4685-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4685-120">PARAMETERS</span></span>

### <span data-ttu-id="f4685-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4685-121">-DefaultProfile</span></span>

<span data-ttu-id="f4685-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4685-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4685-123">-EndDate</span><span class="sxs-lookup"><span data-stu-id="f4685-123">-EndDate</span></span>

<span data-ttu-id="f4685-124">Конец диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="f4685-124">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="f4685-125">-Item</span><span class="sxs-lookup"><span data-stu-id="f4685-125">-Item</span></span>

<span data-ttu-id="f4685-126">Элемент, для которого этот cmdlet получает точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="f4685-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="f4685-127">Чтобы получить объект **AzureRmRecoveryServicesBackupItem,** используйте cmdlet **Get-AzRecoveryServicesBackupItem.**</span><span class="sxs-lookup"><span data-stu-id="f4685-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

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

### <span data-ttu-id="f4685-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="f4685-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="f4685-129">Расположение для скачивания входного файла для восстановления ключа KeyVault для зашифрованной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f4685-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="f4685-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="f4685-130">-RecoveryPointId</span></span>

<span data-ttu-id="f4685-131">Определяет ИД точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="f4685-131">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="f4685-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="f4685-132">-StartDate</span></span>

<span data-ttu-id="f4685-133">Начало диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="f4685-133">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="f4685-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f4685-134">-VaultId</span></span>

<span data-ttu-id="f4685-135">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="f4685-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f4685-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4685-136">CommonParameters</span></span>
<span data-ttu-id="f4685-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4685-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4685-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4685-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4685-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4685-139">INPUTS</span></span>

### <span data-ttu-id="f4685-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="f4685-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="f4685-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f4685-141">System.String</span></span>

## <span data-ttu-id="f4685-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f4685-142">OUTPUTS</span></span>

### <span data-ttu-id="f4685-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="f4685-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="f4685-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f4685-144">NOTES</span></span>

## <span data-ttu-id="f4685-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4685-145">RELATED LINKS</span></span>

[<span data-ttu-id="f4685-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f4685-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="f4685-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="f4685-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
