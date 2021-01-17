---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 7ebbb3cf53c422a3a4d5c73f156cd3890eaa41e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399852"
---
# <span data-ttu-id="9a764-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="9a764-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="9a764-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a764-102">SYNOPSIS</span></span>

<span data-ttu-id="9a764-103">Сведения о резервном копировании.</span><span class="sxs-lookup"><span data-stu-id="9a764-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="9a764-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9a764-104">SYNTAX</span></span>

### <span data-ttu-id="9a764-105">JobFilterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a764-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a764-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="9a764-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a764-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a764-107">DESCRIPTION</span></span>

<span data-ttu-id="9a764-108">Чтобы получить сведения о задании, можно получить сведения о резервном копировании Azure для определенного задания с использованием cmdlet **Get-AzRecoveryServicesBackupJobDetail.**</span><span class="sxs-lookup"><span data-stu-id="9a764-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="9a764-109">Задать контекст хранилища с помощью параметра -VaultId.</span><span class="sxs-lookup"><span data-stu-id="9a764-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="9a764-110">Предупреждение. **Псевдоним Get-AzRecoveryServicesBackupJobDetails** будет удален в последующих выпусках изменений.</span><span class="sxs-lookup"><span data-stu-id="9a764-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="9a764-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9a764-111">EXAMPLES</span></span>

### <span data-ttu-id="9a764-112">Пример 1. Получить сведения о задании резервного копирования для сбойных заданий</span><span class="sxs-lookup"><span data-stu-id="9a764-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="9a764-113">Первая команда извлекает соответствующий сейф.</span><span class="sxs-lookup"><span data-stu-id="9a764-113">The first command fetches the relevant vault.</span></span> <span data-ttu-id="9a764-114">Вторая команда получает массив сбойных заданий в сейфе и сохраняет их в $Jobs массиве.</span><span class="sxs-lookup"><span data-stu-id="9a764-114">The second command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="9a764-115">Третья команда получает сведения о первой сбойной работе в $Jobs и сохраняет их в переменной $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="9a764-115">The third command gets the job details for the 1st failed job in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="9a764-116">В последней команде отображаются сведения об ошибках для сбойных заданий.</span><span class="sxs-lookup"><span data-stu-id="9a764-116">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="9a764-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a764-117">PARAMETERS</span></span>

### <span data-ttu-id="9a764-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a764-118">-DefaultProfile</span></span>

<span data-ttu-id="9a764-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a764-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a764-120">-Job</span><span class="sxs-lookup"><span data-stu-id="9a764-120">-Job</span></span>

<span data-ttu-id="9a764-121">Задание, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="9a764-121">Specifies the job to get.</span></span>
<span data-ttu-id="9a764-122">Чтобы получить объект **BackupJob,** используйте **cmdlet Get-AzRecoveryServicesBackupJob.**</span><span class="sxs-lookup"><span data-stu-id="9a764-122">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a764-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="9a764-123">-JobId</span></span>

<span data-ttu-id="9a764-124">Определяет код задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="9a764-124">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="9a764-125">Код — это свойство JobId объекта **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase.**</span><span class="sxs-lookup"><span data-stu-id="9a764-125">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a764-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9a764-126">-VaultId</span></span>

<span data-ttu-id="9a764-127">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="9a764-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9a764-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a764-128">CommonParameters</span></span>
<span data-ttu-id="9a764-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a764-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a764-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a764-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a764-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a764-131">INPUTS</span></span>

### <span data-ttu-id="9a764-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9a764-132">System.String</span></span>

## <span data-ttu-id="9a764-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9a764-133">OUTPUTS</span></span>

### <span data-ttu-id="9a764-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="9a764-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="9a764-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9a764-135">NOTES</span></span>

## <span data-ttu-id="9a764-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a764-136">RELATED LINKS</span></span>

[<span data-ttu-id="9a764-137">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9a764-137">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
