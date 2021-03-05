---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: c0080985637e58232e2f7eea37344ab291d5d594
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978216"
---
# <span data-ttu-id="2668c-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="2668c-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="2668c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2668c-102">SYNOPSIS</span></span>
<span data-ttu-id="2668c-103">Эта команда содержит точки начала и окончания непрерывной цепочки журнала данного элемента резервной копии.</span><span class="sxs-lookup"><span data-stu-id="2668c-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="2668c-104">С его помощью можно определить, является ли допустимой точка времени, в которую пользователь хочет восстановитьdb.</span><span class="sxs-lookup"><span data-stu-id="2668c-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="2668c-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2668c-105">SYNTAX</span></span>

### <span data-ttu-id="2668c-106">NoFilterParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2668c-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2668c-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="2668c-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2668c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2668c-108">DESCRIPTION</span></span>
<span data-ttu-id="2668c-109">Для резервной копии элемента резервной копии Azure **стеб-azRecoveryServicesBackupRecoveryLogChain** получает точки времени восстановления в диапазоне времени.</span><span class="sxs-lookup"><span data-stu-id="2668c-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="2668c-110">После восстановления элемента у объекта **AzRecoveryServicesBackupRecoveryLogChain** будет один или несколько диапазонов времени восстановления.</span><span class="sxs-lookup"><span data-stu-id="2668c-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="2668c-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2668c-111">EXAMPLES</span></span>

### <span data-ttu-id="2668c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2668c-112">Example 1</span></span>
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="2668c-113">Первая команда получает дату от семи дней назад, а затем сохраняет ее в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="2668c-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="2668c-114">Вторая команда получает сегоднявую дату, а затем сохраняет ее в $EndDate переменной.</span><span class="sxs-lookup"><span data-stu-id="2668c-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="2668c-115">Третья команда получает контейнеры резервного копирования AzureWorkload и сохраняет их в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="2668c-115">The third command gets AzureWorkload backup containers, and stores them in the $Container variable.</span></span>
<span data-ttu-id="2668c-116">Четвертая команда получает резервную копию элемента и делит его через канальный командлет в качестве объекта резервной копии.</span><span class="sxs-lookup"><span data-stu-id="2668c-116">The fourth command gets the backup item, and then shares it across the piped cmdlet as backup item object.</span></span>
<span data-ttu-id="2668c-117">Последняя команда получает массив диапазонов времени точки восстановления для элемента в $BackupItem, а затем сохраняет их в $RP переменной.</span><span class="sxs-lookup"><span data-stu-id="2668c-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

### <span data-ttu-id="2668c-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2668c-118">Example 2</span></span>

<span data-ttu-id="2668c-119">Эта команда содержит точки начала и окончания непрерывной цепочки журнала данного элемента резервной копии.</span><span class="sxs-lookup"><span data-stu-id="2668c-119">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="2668c-120">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="2668c-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="2668c-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2668c-121">PARAMETERS</span></span>

### <span data-ttu-id="2668c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2668c-122">-DefaultProfile</span></span>
<span data-ttu-id="2668c-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2668c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2668c-124">-EndDate</span><span class="sxs-lookup"><span data-stu-id="2668c-124">-EndDate</span></span>
<span data-ttu-id="2668c-125">Время окончания диапазона времени, для которого требуется получить точку восстановления</span><span class="sxs-lookup"><span data-stu-id="2668c-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="2668c-126">-Item</span><span class="sxs-lookup"><span data-stu-id="2668c-126">-Item</span></span>
<span data-ttu-id="2668c-127">Объект защищенного элемента, для которого требуется получить точку восстановления</span><span class="sxs-lookup"><span data-stu-id="2668c-127">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="2668c-128">-StartDate</span><span class="sxs-lookup"><span data-stu-id="2668c-128">-StartDate</span></span>
<span data-ttu-id="2668c-129">Время начала диапазона времени, для которого требуется получить точку восстановления</span><span class="sxs-lookup"><span data-stu-id="2668c-129">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="2668c-130">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2668c-130">-VaultId</span></span>
<span data-ttu-id="2668c-131">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="2668c-131">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2668c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2668c-132">CommonParameters</span></span>
<span data-ttu-id="2668c-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2668c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2668c-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2668c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2668c-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2668c-135">INPUTS</span></span>

### <span data-ttu-id="2668c-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="2668c-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="2668c-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2668c-137">System.String</span></span>

## <span data-ttu-id="2668c-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2668c-138">OUTPUTS</span></span>

### <span data-ttu-id="2668c-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="2668c-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="2668c-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2668c-140">NOTES</span></span>

## <span data-ttu-id="2668c-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2668c-141">RELATED LINKS</span></span>
