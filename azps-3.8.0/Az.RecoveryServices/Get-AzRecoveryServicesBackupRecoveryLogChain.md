---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: 8a0fbc09f9c46bea6ac09d75911ac83b68f0e296
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074733"
---
# <span data-ttu-id="27df3-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="27df3-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="27df3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27df3-102">SYNOPSIS</span></span>
<span data-ttu-id="27df3-103">Эта команда перечисляет начальную и конечную точки неразрывной цепочки журналов заданного элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="27df3-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="27df3-104">Используйте его, чтобы определить, является ли установленное на момент времени, когда пользователь хочет восстановить базу данных, является допустимым.</span><span class="sxs-lookup"><span data-stu-id="27df3-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="27df3-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27df3-105">SYNTAX</span></span>

### <span data-ttu-id="27df3-106">NoFilterParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27df3-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27df3-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="27df3-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27df3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27df3-108">DESCRIPTION</span></span>
<span data-ttu-id="27df3-109">Командлет **Get-AzRecoveryServicesBackupRecoveryLogChain** возвращает временные точки восстановления для резервной копии элемента резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="27df3-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="27df3-110">После создания резервной копии элемента объект **AzRecoveryServicesBackupRecoveryLogChain** содержит один или несколько диапазонов времени восстановления.</span><span class="sxs-lookup"><span data-stu-id="27df3-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="27df3-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27df3-111">EXAMPLES</span></span>

### <span data-ttu-id="27df3-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="27df3-112">Example 1</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="27df3-113">Первая команда получает дату из семи дней назад и затем сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="27df3-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="27df3-114">Вторая команда получает текущую дату, а затем сохраняет ее в переменной $EndDate.</span><span class="sxs-lookup"><span data-stu-id="27df3-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="27df3-115">Третья команда получает контейнеры резервного копирования AzureWorkload и сохраняет их в переменной $Containers.</span><span class="sxs-lookup"><span data-stu-id="27df3-115">The third command gets AzureWorkload backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="27df3-116">Четвертая команда возвращает элемент резервного копирования, а затем сохраняет его в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="27df3-116">The fourth command gets the backup item, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="27df3-117">Последняя команда получает массив диапазонов времени точки восстановления для элемента в $BackupItem, а затем сохраняет их в переменной $RP.</span><span class="sxs-lookup"><span data-stu-id="27df3-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="27df3-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27df3-118">PARAMETERS</span></span>

### <span data-ttu-id="27df3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27df3-119">-DefaultProfile</span></span>
<span data-ttu-id="27df3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27df3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27df3-121">-EndDate</span><span class="sxs-lookup"><span data-stu-id="27df3-121">-EndDate</span></span>
<span data-ttu-id="27df3-122">Время окончания временного интервала, для которого требуется извлечь точку восстановления</span><span class="sxs-lookup"><span data-stu-id="27df3-122">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="27df3-123">-Item</span><span class="sxs-lookup"><span data-stu-id="27df3-123">-Item</span></span>
<span data-ttu-id="27df3-124">Защищенный объект элемента, для которого требуется получить точку восстановления</span><span class="sxs-lookup"><span data-stu-id="27df3-124">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="27df3-125">-StartDate</span><span class="sxs-lookup"><span data-stu-id="27df3-125">-StartDate</span></span>
<span data-ttu-id="27df3-126">Время начала временного интервала, для которого требуется извлечь точку восстановления</span><span class="sxs-lookup"><span data-stu-id="27df3-126">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="27df3-127">-VaultId</span><span class="sxs-lookup"><span data-stu-id="27df3-127">-VaultId</span></span>
<span data-ttu-id="27df3-128">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="27df3-128">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="27df3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27df3-129">CommonParameters</span></span>
<span data-ttu-id="27df3-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27df3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27df3-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27df3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27df3-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27df3-132">INPUTS</span></span>

### <span data-ttu-id="27df3-133">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="27df3-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="27df3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="27df3-134">System.String</span></span>

## <span data-ttu-id="27df3-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27df3-135">OUTPUTS</span></span>

### <span data-ttu-id="27df3-136">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="27df3-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="27df3-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="27df3-137">NOTES</span></span>

## <span data-ttu-id="27df3-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27df3-138">RELATED LINKS</span></span>
