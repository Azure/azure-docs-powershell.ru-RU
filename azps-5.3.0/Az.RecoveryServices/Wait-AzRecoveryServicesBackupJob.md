---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: d494169c989096ce562858c500289527479d42dd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505397"
---
# <span data-ttu-id="7d01c-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="7d01c-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="7d01c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d01c-102">SYNOPSIS</span></span>

<span data-ttu-id="7d01c-103">Ожидание завершения задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="7d01c-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="7d01c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7d01c-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d01c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d01c-105">DESCRIPTION</span></span>

<span data-ttu-id="7d01c-106">Выполнение задания резервного копирования Azure будет завершено с использованием **cmdlet Wait-AzRecoveryServicesBackupJob.**</span><span class="sxs-lookup"><span data-stu-id="7d01c-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="7d01c-107">Резервное копирование может занять много времени.</span><span class="sxs-lookup"><span data-stu-id="7d01c-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="7d01c-108">При запуске задания резервного копирования в составе сценария может потребоваться принудительно дождаться завершения задания, прежде чем оно продолжит работу с другими задачами.</span><span class="sxs-lookup"><span data-stu-id="7d01c-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="7d01c-109">Сценарий, который включает этот cmdlet, может быть проще, чем тот, который оповещает службу резервного копирования о состоянии задания.</span><span class="sxs-lookup"><span data-stu-id="7d01c-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="7d01c-110">Задать контекст хранилища с помощью параметра -VaultId.</span><span class="sxs-lookup"><span data-stu-id="7d01c-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="7d01c-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7d01c-111">EXAMPLES</span></span>

### <span data-ttu-id="7d01c-112">Пример 1. Ожидание завершения задания</span><span class="sxs-lookup"><span data-stu-id="7d01c-112">Example 1: Wait for a job to finish</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

<span data-ttu-id="7d01c-113">Этот сценарий оповестит первое задание, которое в настоящее время находится в процессе выполнения, пока не завершится задание или не истечет срок его ожидания (1 час).</span><span class="sxs-lookup"><span data-stu-id="7d01c-113">This script polls the first job that is currently in progress until the job has completed or timeout period of 1 hour expired.</span></span>

## <span data-ttu-id="7d01c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d01c-114">PARAMETERS</span></span>

### <span data-ttu-id="7d01c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d01c-115">-DefaultProfile</span></span>

<span data-ttu-id="7d01c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d01c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d01c-117">-Job</span><span class="sxs-lookup"><span data-stu-id="7d01c-117">-Job</span></span>

<span data-ttu-id="7d01c-118">Задание, которые нужно подождать.</span><span class="sxs-lookup"><span data-stu-id="7d01c-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="7d01c-119">Чтобы получить объект **BackupJob,** используйте **cmdlet Get-AzRecoveryServicesBackupJob.**</span><span class="sxs-lookup"><span data-stu-id="7d01c-119">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d01c-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="7d01c-120">-Timeout</span></span>

<span data-ttu-id="7d01c-121">Определяет максимальное время (в секундах), которое этот cmdlet должен выждать, пока задание завершится.</span><span class="sxs-lookup"><span data-stu-id="7d01c-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="7d01c-122">Рекомендуется указать значение времени.</span><span class="sxs-lookup"><span data-stu-id="7d01c-122">It is recommended to specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d01c-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7d01c-123">-VaultId</span></span>

<span data-ttu-id="7d01c-124">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="7d01c-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7d01c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d01c-125">CommonParameters</span></span>
<span data-ttu-id="7d01c-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d01c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d01c-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d01c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d01c-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d01c-128">INPUTS</span></span>

### <span data-ttu-id="7d01c-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="7d01c-129">System.Object</span></span>

### <span data-ttu-id="7d01c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7d01c-130">System.String</span></span>

## <span data-ttu-id="7d01c-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7d01c-131">OUTPUTS</span></span>

### <span data-ttu-id="7d01c-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="7d01c-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="7d01c-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7d01c-133">NOTES</span></span>

## <span data-ttu-id="7d01c-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d01c-134">RELATED LINKS</span></span>

[<span data-ttu-id="7d01c-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="7d01c-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
