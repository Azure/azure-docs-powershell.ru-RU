---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/backup-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 9838db99fa1126f3948bb16f9ee16180cb652904
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562739"
---
# <span data-ttu-id="36419-101">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="36419-101">Backup-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="36419-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36419-102">SYNOPSIS</span></span>
<span data-ttu-id="36419-103">Запуск резервного копирования для элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="36419-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36419-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36419-104">SYNTAX</span></span>

```
Backup-AzureRmRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36419-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36419-105">DESCRIPTION</span></span>
<span data-ttu-id="36419-106">Командлет **BACKUP-AzureRmRecoveryServicesBackupItem** запускает резервное копирование для защищенного элемента резервного копирования Azure, не привязанного к расписанию резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="36419-106">The **Backup-AzureRmRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="36419-107">Вы можете выполнить начальную архивацию немедленно, после того как вы включите защиту или начнете создание резервной копии после сбоя архивации по расписанию.</span><span class="sxs-lookup"><span data-stu-id="36419-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="36419-108">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="36419-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="36419-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36419-109">EXAMPLES</span></span>

### <span data-ttu-id="36419-110">Пример 1: Начало резервного копирования для элемента резервного копирования</span><span class="sxs-lookup"><span data-stu-id="36419-110">Example 1: Start a backup for a Backup item</span></span>
```
PS C:\> $NamedContainer = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzureRmRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzureRmRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="36419-111">Первая команда получает контейнер резервного копирования типа AzureVM с именем pstestv2vm1 и сохраняет его в переменной $NamedContainer.</span><span class="sxs-lookup"><span data-stu-id="36419-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="36419-112">Вторая команда возвращает элемент резервного копирования, соответствующий контейнеру в $NamedContainer, и сохраняет его в переменной $Item.</span><span class="sxs-lookup"><span data-stu-id="36419-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="36419-113">Последняя команда запускает задание резервного копирования для элемента резервного копирования в $Item.</span><span class="sxs-lookup"><span data-stu-id="36419-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="36419-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36419-114">PARAMETERS</span></span>

### <span data-ttu-id="36419-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36419-115">-DefaultProfile</span></span>
<span data-ttu-id="36419-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36419-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36419-117">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="36419-117">-ExpiryDateTimeUTC</span></span>
<span data-ttu-id="36419-118">Задает время истечения срока действия в виде объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="36419-118">Specifies an expiry time as a **DateTime** object.</span></span>

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

### <span data-ttu-id="36419-119">-Item</span><span class="sxs-lookup"><span data-stu-id="36419-119">-Item</span></span>
<span data-ttu-id="36419-120">Указывает элемент резервного копирования, для которого этот командлет запускает операцию резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="36419-120">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="36419-121">-VaultId</span><span class="sxs-lookup"><span data-stu-id="36419-121">-VaultId</span></span>
<span data-ttu-id="36419-122">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="36419-122">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="36419-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36419-123">-Confirm</span></span>
<span data-ttu-id="36419-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="36419-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36419-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36419-125">-WhatIf</span></span>
<span data-ttu-id="36419-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="36419-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36419-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="36419-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36419-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36419-128">CommonParameters</span></span>
<span data-ttu-id="36419-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36419-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36419-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36419-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36419-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36419-131">INPUTS</span></span>

### <span data-ttu-id="36419-132">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="36419-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="36419-133">Параметры: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="36419-133">Parameters: Item (ByValue)</span></span>

### <span data-ttu-id="36419-134">System. Nullable "1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="36419-134">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="36419-135">System. String</span><span class="sxs-lookup"><span data-stu-id="36419-135">System.String</span></span>
<span data-ttu-id="36419-136">Параметры: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="36419-136">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="36419-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36419-137">OUTPUTS</span></span>

### <span data-ttu-id="36419-138">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="36419-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="36419-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="36419-139">NOTES</span></span>

## <span data-ttu-id="36419-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36419-140">RELATED LINKS</span></span>

[<span data-ttu-id="36419-141">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="36419-141">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="36419-142">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="36419-142">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="36419-143">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="36419-143">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


