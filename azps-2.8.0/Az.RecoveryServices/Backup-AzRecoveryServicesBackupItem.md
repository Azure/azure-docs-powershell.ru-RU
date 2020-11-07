---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 6c8debac9091d28091695847b36d0cbc1b219125
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905037"
---
# <span data-ttu-id="88fbc-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="88fbc-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="88fbc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88fbc-102">SYNOPSIS</span></span>

<span data-ttu-id="88fbc-103">Запуск резервного копирования для элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="88fbc-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="88fbc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88fbc-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88fbc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88fbc-105">DESCRIPTION</span></span>

<span data-ttu-id="88fbc-106">Командлет **BACKUP-AzRecoveryServicesBackupItem** запускает резервное копирование для защищенного элемента резервного копирования Azure, не привязанного к расписанию резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="88fbc-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="88fbc-107">Вы можете выполнить начальную архивацию немедленно, после того как вы включите защиту или начнете создание резервной копии после сбоя архивации по расписанию.</span><span class="sxs-lookup"><span data-stu-id="88fbc-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="88fbc-108">Задайте контекст хранилища с помощью параметра-VaultId.</span><span class="sxs-lookup"><span data-stu-id="88fbc-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="88fbc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88fbc-109">EXAMPLES</span></span>

### <span data-ttu-id="88fbc-110">Пример 1: Начало резервного копирования для элемента резервного копирования</span><span class="sxs-lookup"><span data-stu-id="88fbc-110">Example 1: Start a backup for a Backup item</span></span>

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

<span data-ttu-id="88fbc-111">Первая команда получает контейнер резервного копирования типа AzureVM с именем pstestv2vm1 и сохраняет его в переменной $NamedContainer.</span><span class="sxs-lookup"><span data-stu-id="88fbc-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="88fbc-112">Вторая команда возвращает элемент резервного копирования, соответствующий контейнеру в $NamedContainer, и сохраняет его в переменной $Item.</span><span class="sxs-lookup"><span data-stu-id="88fbc-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="88fbc-113">Последняя команда запускает задание резервного копирования для элемента резервного копирования в $Item.</span><span class="sxs-lookup"><span data-stu-id="88fbc-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="88fbc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88fbc-114">PARAMETERS</span></span>

### <span data-ttu-id="88fbc-115">-BackupType</span><span class="sxs-lookup"><span data-stu-id="88fbc-115">-BackupType</span></span>

<span data-ttu-id="88fbc-116">Тип резервной копии, которую нужно выполнить</span><span class="sxs-lookup"><span data-stu-id="88fbc-116">Type of backup to be performed</span></span>

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

### <span data-ttu-id="88fbc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88fbc-117">-DefaultProfile</span></span>

<span data-ttu-id="88fbc-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88fbc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88fbc-119">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="88fbc-119">-EnableCompression</span></span>

<span data-ttu-id="88fbc-120">Если требуется включить сжатие</span><span class="sxs-lookup"><span data-stu-id="88fbc-120">If enabling compression is required</span></span>

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

### <span data-ttu-id="88fbc-121">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="88fbc-121">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="88fbc-122">Задает время истечения срока действия в виде объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="88fbc-122">Specifies an expiry time as a **DateTime** object.</span></span>

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

### <span data-ttu-id="88fbc-123">-Item</span><span class="sxs-lookup"><span data-stu-id="88fbc-123">-Item</span></span>

<span data-ttu-id="88fbc-124">Указывает элемент резервного копирования, для которого этот командлет запускает операцию резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="88fbc-124">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="88fbc-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="88fbc-125">-VaultId</span></span>

<span data-ttu-id="88fbc-126">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="88fbc-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="88fbc-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88fbc-127">-Confirm</span></span>

<span data-ttu-id="88fbc-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="88fbc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88fbc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88fbc-129">-WhatIf</span></span>

<span data-ttu-id="88fbc-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="88fbc-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88fbc-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="88fbc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88fbc-132">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88fbc-132">-CommonParameters</span></span>

<span data-ttu-id="88fbc-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88fbc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88fbc-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88fbc-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88fbc-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88fbc-135">INPUTS</span></span>

### <span data-ttu-id="88fbc-136">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="88fbc-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="88fbc-137">System. Nullable "1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="88fbc-137">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="88fbc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="88fbc-138">System.String</span></span>

## <span data-ttu-id="88fbc-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88fbc-139">OUTPUTS</span></span>

### <span data-ttu-id="88fbc-140">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="88fbc-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="88fbc-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="88fbc-141">NOTES</span></span>

## <span data-ttu-id="88fbc-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88fbc-142">RELATED LINKS</span></span>

[<span data-ttu-id="88fbc-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="88fbc-143">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="88fbc-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="88fbc-144">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="88fbc-145">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="88fbc-145">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
