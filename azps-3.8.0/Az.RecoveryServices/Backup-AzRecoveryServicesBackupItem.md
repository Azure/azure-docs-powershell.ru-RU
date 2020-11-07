---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: fb2b6c370ee7ce43c877bfac57b64a203e9238cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911921"
---
# <span data-ttu-id="ff97f-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ff97f-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="ff97f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff97f-102">SYNOPSIS</span></span>

<span data-ttu-id="ff97f-103">Запуск резервного копирования для элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="ff97f-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="ff97f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff97f-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff97f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff97f-105">DESCRIPTION</span></span>

<span data-ttu-id="ff97f-106">Командлет **BACKUP-AzRecoveryServicesBackupItem** запускает резервное копирование для защищенного элемента резервного копирования Azure, не привязанного к расписанию резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="ff97f-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="ff97f-107">Вы можете выполнить начальную архивацию немедленно, после того как вы включите защиту или начнете создание резервной копии после сбоя архивации по расписанию.</span><span class="sxs-lookup"><span data-stu-id="ff97f-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="ff97f-108">Задайте контекст хранилища с помощью параметра-VaultId.</span><span class="sxs-lookup"><span data-stu-id="ff97f-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="ff97f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff97f-109">EXAMPLES</span></span>

### <span data-ttu-id="ff97f-110">Пример 1: Начало резервного копирования для элемента резервного копирования</span><span class="sxs-lookup"><span data-stu-id="ff97f-110">Example 1: Start a backup for a Backup item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $NamedContainer = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "pstestv2vm1" -VaultId $vault.ID
PS C:\> $Item = Get-AzRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $Job = Backup-AzRecoveryServicesBackupItem -Item $Item -VaultId $vault.ID
PS C:\> $Job
Operation        Status               StartTime            EndTime                   JOBID
------------     ---------            ------               ---------                 -------
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="ff97f-111">Первая команда получает контейнер резервного копирования типа AzureVM с именем pstestv2vm1 и сохраняет его в переменной $NamedContainer.</span><span class="sxs-lookup"><span data-stu-id="ff97f-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="ff97f-112">Вторая команда возвращает элемент резервного копирования, соответствующий контейнеру в $NamedContainer, и сохраняет его в переменной $Item.</span><span class="sxs-lookup"><span data-stu-id="ff97f-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="ff97f-113">Последняя команда запускает задание резервного копирования для элемента резервного копирования в $Item.</span><span class="sxs-lookup"><span data-stu-id="ff97f-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="ff97f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff97f-114">PARAMETERS</span></span>

### <span data-ttu-id="ff97f-115">-BackupType</span><span class="sxs-lookup"><span data-stu-id="ff97f-115">-BackupType</span></span>

<span data-ttu-id="ff97f-116">Тип резервной копии, которую нужно выполнить</span><span class="sxs-lookup"><span data-stu-id="ff97f-116">Type of backup to be performed</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupType
Parameter Sets: (All)
Aliases:
Accepted values: Full, Differential, Log, CopyOnlyFull

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff97f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff97f-117">-DefaultProfile</span></span>

<span data-ttu-id="ff97f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff97f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff97f-119">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="ff97f-119">-EnableCompression</span></span>

<span data-ttu-id="ff97f-120">Если требуется включить сжатие</span><span class="sxs-lookup"><span data-stu-id="ff97f-120">If enabling compression is required</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff97f-121">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="ff97f-121">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="ff97f-122">Задает время истечения срока действия в виде объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="ff97f-122">Specifies an expiry time as a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff97f-123">-Item</span><span class="sxs-lookup"><span data-stu-id="ff97f-123">-Item</span></span>

<span data-ttu-id="ff97f-124">Указывает элемент резервного копирования, для которого этот командлет запускает операцию резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="ff97f-124">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff97f-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ff97f-125">-VaultId</span></span>

<span data-ttu-id="ff97f-126">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="ff97f-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ff97f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff97f-127">-Confirm</span></span>

<span data-ttu-id="ff97f-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ff97f-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff97f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff97f-129">-WhatIf</span></span>

<span data-ttu-id="ff97f-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ff97f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff97f-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ff97f-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff97f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff97f-132">CommonParameters</span></span>
<span data-ttu-id="ff97f-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff97f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff97f-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff97f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff97f-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff97f-135">INPUTS</span></span>

### <span data-ttu-id="ff97f-136">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="ff97f-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="ff97f-137">System. Nullable "1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ff97f-137">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ff97f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ff97f-138">System.String</span></span>

## <span data-ttu-id="ff97f-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff97f-139">OUTPUTS</span></span>

### <span data-ttu-id="ff97f-140">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="ff97f-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ff97f-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff97f-141">NOTES</span></span>

## <span data-ttu-id="ff97f-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff97f-142">RELATED LINKS</span></span>

[<span data-ttu-id="ff97f-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ff97f-143">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="ff97f-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ff97f-144">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="ff97f-145">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ff97f-145">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
