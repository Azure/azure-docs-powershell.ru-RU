---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 43ad564f261c423882b144d3fd9fbceba1273bcf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734530"
---
# <span data-ttu-id="f4f5d-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f4f5d-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="f4f5d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f5d-103">Возвращает точки восстановления для резервного элемента.</span><span class="sxs-lookup"><span data-stu-id="f4f5d-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4f5d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4f5d-104">SYNTAX</span></span>

### <span data-ttu-id="f4f5d-105">NoFilterParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f4f5d-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4f5d-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="f4f5d-106">DateTimeFilter</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4f5d-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="f4f5d-107">RecoveryPointId</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4f5d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4f5d-108">DESCRIPTION</span></span>
<span data-ttu-id="f4f5d-109">Командлет **Get-AzureRmRecoveryServicesBackupRecoveryPoint** получает точки восстановления для резервной копии элемента резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="f4f5d-109">The **Get-AzureRmRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="f4f5d-110">После создания резервной копии элемента объект **AzureRmRecoveryServicesBackupRecoveryPoint** имеет одну или несколько точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="f4f5d-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>

<span data-ttu-id="f4f5d-111">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="f4f5d-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f4f5d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4f5d-112">EXAMPLES</span></span>

### <span data-ttu-id="f4f5d-113">Пример 1: получение точек восстановления за последнюю неделю для элемента</span><span class="sxs-lookup"><span data-stu-id="f4f5d-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="f4f5d-114">Первая команда получает дату из семи дней назад и затем сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="f4f5d-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>

<span data-ttu-id="f4f5d-115">Вторая команда получает текущую дату, а затем сохраняет ее в переменной $EndDate.</span><span class="sxs-lookup"><span data-stu-id="f4f5d-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>

<span data-ttu-id="f4f5d-116">Третья команда получает контейнеры резервного копирования для AzureVM и сохраняет их в переменной $Containers.</span><span class="sxs-lookup"><span data-stu-id="f4f5d-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>

<span data-ttu-id="f4f5d-117">Четвертая команда возвращает элемент резервного копирования с именем V2VM и сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="f4f5d-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>

<span data-ttu-id="f4f5d-118">Последняя команда получает массив точек восстановления для элемента в $BackupItem, а затем сохраняет их в переменной $RP.</span><span class="sxs-lookup"><span data-stu-id="f4f5d-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="f4f5d-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4f5d-119">PARAMETERS</span></span>

### <span data-ttu-id="f4f5d-120">-EndDate</span><span class="sxs-lookup"><span data-stu-id="f4f5d-120">-EndDate</span></span>
<span data-ttu-id="f4f5d-121">Указывает конец диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="f4f5d-121">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="f4f5d-122">-Item</span><span class="sxs-lookup"><span data-stu-id="f4f5d-122">-Item</span></span>
<span data-ttu-id="f4f5d-123">Указывает элемент, для которого этот командлет получает точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="f4f5d-123">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="f4f5d-124">Чтобы получить объект **AzureRmRecoveryServicesBackupItem** , используйте командлет Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="f4f5d-124">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="f4f5d-125">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="f4f5d-125">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="f4f5d-126">Задает расположение для скачивания входного файла для восстановления ключа KeyVault для зашифрованной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f4f5d-126">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="f4f5d-127">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="f4f5d-127">-RecoveryPointId</span></span>
<span data-ttu-id="f4f5d-128">Указывает идентификатор точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="f4f5d-128">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="f4f5d-129">-StartDate</span><span class="sxs-lookup"><span data-stu-id="f4f5d-129">-StartDate</span></span>
<span data-ttu-id="f4f5d-130">Задает начало диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="f4f5d-130">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="f4f5d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f5d-131">-DefaultProfile</span></span>
<span data-ttu-id="f4f5d-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4f5d-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4f5d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f5d-133">CommonParameters</span></span>
<span data-ttu-id="f4f5d-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4f5d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f5d-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4f5d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f5d-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4f5d-136">INPUTS</span></span>

### <span data-ttu-id="f4f5d-137">ItemBase</span><span class="sxs-lookup"><span data-stu-id="f4f5d-137">ItemBase</span></span>
<span data-ttu-id="f4f5d-138">Параметр "элемент" принимает значение типа "ItemBase" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f4f5d-138">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="f4f5d-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4f5d-139">OUTPUTS</span></span>

### <span data-ttu-id="f4f5d-140">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="f4f5d-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="f4f5d-141">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RecoveryPointBase]</span><span class="sxs-lookup"><span data-stu-id="f4f5d-141">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase]</span></span>

## <span data-ttu-id="f4f5d-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4f5d-142">NOTES</span></span>

## <span data-ttu-id="f4f5d-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4f5d-143">RELATED LINKS</span></span>

[<span data-ttu-id="f4f5d-144">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f4f5d-144">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="f4f5d-145">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="f4f5d-145">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


