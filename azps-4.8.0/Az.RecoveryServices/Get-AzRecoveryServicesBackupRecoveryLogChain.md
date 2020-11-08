---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: ba82e1ddf8385f74b271feb9119280d48fc1b859
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244700"
---
# <span data-ttu-id="2b5fc-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="2b5fc-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="2b5fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b5fc-102">SYNOPSIS</span></span>
<span data-ttu-id="2b5fc-103">Эта команда перечисляет начальную и конечную точки неразрывной цепочки журналов заданного элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="2b5fc-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="2b5fc-104">Используйте его, чтобы определить, является ли установленное на момент времени, когда пользователь хочет восстановить базу данных, является допустимым.</span><span class="sxs-lookup"><span data-stu-id="2b5fc-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="2b5fc-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b5fc-105">SYNTAX</span></span>

### <span data-ttu-id="2b5fc-106">NoFilterParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2b5fc-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b5fc-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="2b5fc-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b5fc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b5fc-108">DESCRIPTION</span></span>
<span data-ttu-id="2b5fc-109">Командлет **Get-AzRecoveryServicesBackupRecoveryLogChain** возвращает временные точки восстановления для резервной копии элемента резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="2b5fc-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="2b5fc-110">После создания резервной копии элемента объект **AzRecoveryServicesBackupRecoveryLogChain** содержит один или несколько диапазонов времени восстановления.</span><span class="sxs-lookup"><span data-stu-id="2b5fc-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="2b5fc-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b5fc-111">EXAMPLES</span></span>

### <span data-ttu-id="2b5fc-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2b5fc-112">Example 1</span></span>
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="2b5fc-113">Первая команда получает дату из семи дней назад и затем сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="2b5fc-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="2b5fc-114">Вторая команда получает текущую дату, а затем сохраняет ее в переменной $EndDate.</span><span class="sxs-lookup"><span data-stu-id="2b5fc-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="2b5fc-115">Третья команда получает контейнеры резервного копирования AzureWorkload и сохраняет их в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="2b5fc-115">The third command gets AzureWorkload backup containers, and stores them in the $Container variable.</span></span>
<span data-ttu-id="2b5fc-116">Четвертая команда возвращает элемент резервного копирования, а затем предоставляет его в рамках командлета "передается" в качестве объекта элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="2b5fc-116">The fourth command gets the backup item, and then shares it across the piped cmdlet as backup item object.</span></span>
<span data-ttu-id="2b5fc-117">Последняя команда получает массив диапазонов времени точки восстановления для элемента в $BackupItem, а затем сохраняет их в переменной $RP.</span><span class="sxs-lookup"><span data-stu-id="2b5fc-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

### <span data-ttu-id="2b5fc-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2b5fc-118">Example 2</span></span>

<span data-ttu-id="2b5fc-119">Эта команда перечисляет начальную и конечную точки неразрывной цепочки журналов заданного элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="2b5fc-119">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="2b5fc-120">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="2b5fc-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="2b5fc-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b5fc-121">PARAMETERS</span></span>

### <span data-ttu-id="2b5fc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b5fc-122">-DefaultProfile</span></span>
<span data-ttu-id="2b5fc-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b5fc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b5fc-124">-EndDate</span><span class="sxs-lookup"><span data-stu-id="2b5fc-124">-EndDate</span></span>
<span data-ttu-id="2b5fc-125">Время окончания временного интервала, для которого требуется извлечь точку восстановления</span><span class="sxs-lookup"><span data-stu-id="2b5fc-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="2b5fc-126">-Item</span><span class="sxs-lookup"><span data-stu-id="2b5fc-126">-Item</span></span>
<span data-ttu-id="2b5fc-127">Защищенный объект элемента, для которого требуется получить точку восстановления</span><span class="sxs-lookup"><span data-stu-id="2b5fc-127">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="2b5fc-128">-StartDate</span><span class="sxs-lookup"><span data-stu-id="2b5fc-128">-StartDate</span></span>
<span data-ttu-id="2b5fc-129">Время начала временного интервала, для которого требуется извлечь точку восстановления</span><span class="sxs-lookup"><span data-stu-id="2b5fc-129">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="2b5fc-130">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2b5fc-130">-VaultId</span></span>
<span data-ttu-id="2b5fc-131">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="2b5fc-131">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2b5fc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b5fc-132">CommonParameters</span></span>
<span data-ttu-id="2b5fc-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b5fc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b5fc-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b5fc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b5fc-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b5fc-135">INPUTS</span></span>

### <span data-ttu-id="2b5fc-136">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="2b5fc-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="2b5fc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2b5fc-137">System.String</span></span>

## <span data-ttu-id="2b5fc-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b5fc-138">OUTPUTS</span></span>

### <span data-ttu-id="2b5fc-139">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="2b5fc-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="2b5fc-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b5fc-140">NOTES</span></span>

## <span data-ttu-id="2b5fc-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b5fc-141">RELATED LINKS</span></span>
