---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 10131025768b93fd1bbd692b07a22a03d8a88726
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729565"
---
# <span data-ttu-id="0a32e-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="0a32e-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="0a32e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a32e-102">SYNOPSIS</span></span>
<span data-ttu-id="0a32e-103">Ожидание завершения задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="0a32e-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="0a32e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a32e-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a32e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a32e-105">DESCRIPTION</span></span>
<span data-ttu-id="0a32e-106">Командлет **Wait-AzRecoveryServicesBackupJob** ожидает завершения задания резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="0a32e-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="0a32e-107">Задания резервного копирования могут занять много времени.</span><span class="sxs-lookup"><span data-stu-id="0a32e-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="0a32e-108">Если вы запускаете задание резервного копирования в составе сценария, может потребоваться принудительное ожидание завершения задания, прежде чем продолжить выполнение других задач.</span><span class="sxs-lookup"><span data-stu-id="0a32e-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="0a32e-109">Сценарий, включающий этот командлет, может быть более простым, чем тот, который опрашивает службу резервного копирования для задания состояния.</span><span class="sxs-lookup"><span data-stu-id="0a32e-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="0a32e-110">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="0a32e-110">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="0a32e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a32e-111">EXAMPLES</span></span>

### <span data-ttu-id="0a32e-112">Пример 1: ожидание завершения задания</span><span class="sxs-lookup"><span data-stu-id="0a32e-112">Example 1: Wait for a job to finish</span></span>
```
PS C:\>
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress
    $Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $Job = Get-AzBackAzureRmRecoveryServicesBackupJob -Job $Job
    }
   Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="0a32e-113">Этот сценарий опрашивает первое задание, которое выполняется в данный момент, пока задание не будет завершено.</span><span class="sxs-lookup"><span data-stu-id="0a32e-113">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="0a32e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a32e-114">PARAMETERS</span></span>

### <span data-ttu-id="0a32e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a32e-115">-DefaultProfile</span></span>
<span data-ttu-id="0a32e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a32e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a32e-117">-Job</span><span class="sxs-lookup"><span data-stu-id="0a32e-117">-Job</span></span>
<span data-ttu-id="0a32e-118">Указывает задание, которое нужно дождаться.</span><span class="sxs-lookup"><span data-stu-id="0a32e-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="0a32e-119">Чтобы получить объект **BackupJob** , используйте командлет Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="0a32e-119">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="0a32e-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="0a32e-120">-Timeout</span></span>
<span data-ttu-id="0a32e-121">Задает максимальное время в секундах, в течение которого этот командлет ожидает завершения задания.</span><span class="sxs-lookup"><span data-stu-id="0a32e-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="0a32e-122">Рекомендуется указать значение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="0a32e-122">It is recommended to specify a time-out value.</span></span>

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

### <span data-ttu-id="0a32e-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0a32e-123">-VaultId</span></span>
<span data-ttu-id="0a32e-124">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="0a32e-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0a32e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a32e-125">CommonParameters</span></span>
<span data-ttu-id="0a32e-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a32e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a32e-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a32e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a32e-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a32e-128">INPUTS</span></span>

### <span data-ttu-id="0a32e-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="0a32e-129">System.Object</span></span>

### <span data-ttu-id="0a32e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0a32e-130">System.String</span></span>

## <span data-ttu-id="0a32e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a32e-131">OUTPUTS</span></span>

### <span data-ttu-id="0a32e-132">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="0a32e-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="0a32e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a32e-133">NOTES</span></span>

## <span data-ttu-id="0a32e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a32e-134">RELATED LINKS</span></span>

[<span data-ttu-id="0a32e-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="0a32e-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)


