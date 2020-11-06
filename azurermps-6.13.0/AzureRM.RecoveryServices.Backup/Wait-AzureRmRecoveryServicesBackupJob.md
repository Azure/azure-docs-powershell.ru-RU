---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/wait-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 377250dcc8cbeb3727e7d2bf3f0dd0a8581d6401
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566430"
---
# <span data-ttu-id="36b6e-101">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="36b6e-101">Wait-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="36b6e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36b6e-102">SYNOPSIS</span></span>
<span data-ttu-id="36b6e-103">Ожидание завершения задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="36b6e-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36b6e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36b6e-104">SYNTAX</span></span>

```
Wait-AzureRmRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36b6e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36b6e-105">DESCRIPTION</span></span>
<span data-ttu-id="36b6e-106">Командлет **Wait-AzureRmRecoveryServicesBackupJob** ожидает завершения задания резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="36b6e-106">The **Wait-AzureRmRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="36b6e-107">Задания резервного копирования могут занять много времени.</span><span class="sxs-lookup"><span data-stu-id="36b6e-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="36b6e-108">Если вы запускаете задание резервного копирования в составе сценария, может потребоваться принудительное ожидание завершения задания, прежде чем продолжить выполнение других задач.</span><span class="sxs-lookup"><span data-stu-id="36b6e-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="36b6e-109">Сценарий, включающий этот командлет, может быть более простым, чем тот, который опрашивает службу резервного копирования для задания состояния.</span><span class="sxs-lookup"><span data-stu-id="36b6e-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="36b6e-110">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="36b6e-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="36b6e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36b6e-111">EXAMPLES</span></span>

### <span data-ttu-id="36b6e-112">Пример 1: ожидание завершения задания</span><span class="sxs-lookup"><span data-stu-id="36b6e-112">Example 1: Wait for a job to finish</span></span>
```
PS C:\>
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
    $Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $Job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob -Job $Job
    }
   Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="36b6e-113">Этот сценарий опрашивает первое задание, которое выполняется в данный момент, пока задание не будет завершено.</span><span class="sxs-lookup"><span data-stu-id="36b6e-113">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="36b6e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36b6e-114">PARAMETERS</span></span>

### <span data-ttu-id="36b6e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b6e-115">-DefaultProfile</span></span>
<span data-ttu-id="36b6e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36b6e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36b6e-117">-Job</span><span class="sxs-lookup"><span data-stu-id="36b6e-117">-Job</span></span>
<span data-ttu-id="36b6e-118">Указывает задание, которое нужно дождаться.</span><span class="sxs-lookup"><span data-stu-id="36b6e-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="36b6e-119">Чтобы получить объект **BackupJob** , используйте командлет Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="36b6e-119">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="36b6e-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="36b6e-120">-Timeout</span></span>
<span data-ttu-id="36b6e-121">Задает максимальное время в секундах, в течение которого этот командлет ожидает завершения задания.</span><span class="sxs-lookup"><span data-stu-id="36b6e-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="36b6e-122">Рекомендуется указать значение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="36b6e-122">It is recommended to specify a time-out value.</span></span>

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

### <span data-ttu-id="36b6e-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="36b6e-123">-VaultId</span></span>
<span data-ttu-id="36b6e-124">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="36b6e-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="36b6e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b6e-125">CommonParameters</span></span>
<span data-ttu-id="36b6e-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36b6e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b6e-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36b6e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b6e-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36b6e-128">INPUTS</span></span>

### <span data-ttu-id="36b6e-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="36b6e-129">System.Object</span></span>
<span data-ttu-id="36b6e-130">Параметры: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="36b6e-130">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="36b6e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="36b6e-131">System.String</span></span>
<span data-ttu-id="36b6e-132">Параметры: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="36b6e-132">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="36b6e-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36b6e-133">OUTPUTS</span></span>

### <span data-ttu-id="36b6e-134">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="36b6e-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="36b6e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="36b6e-135">NOTES</span></span>

## <span data-ttu-id="36b6e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36b6e-136">RELATED LINKS</span></span>

[<span data-ttu-id="36b6e-137">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="36b6e-137">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


