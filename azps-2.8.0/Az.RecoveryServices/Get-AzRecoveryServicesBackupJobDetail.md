---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: c8cf8074d6b077ed67f46f747c80439b41f9abca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904925"
---
# <span data-ttu-id="4e38c-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="4e38c-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="4e38c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e38c-102">SYNOPSIS</span></span>

<span data-ttu-id="4e38c-103">Получение сведений о задании резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="4e38c-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="4e38c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e38c-104">SYNTAX</span></span>

### <span data-ttu-id="4e38c-105">JobFilterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e38c-105">JobFilterSet (Default)</span></span>

```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e38c-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="4e38c-106">IdFilterSet</span></span>

```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e38c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e38c-107">DESCRIPTION</span></span>

<span data-ttu-id="4e38c-108">Командлет **Get-AzRecoveryServicesBackupJobDetail** получает сведения о задании резервного копирования Azure для указанного задания.</span><span class="sxs-lookup"><span data-stu-id="4e38c-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="4e38c-109">Задайте контекст хранилища с помощью параметра-VaultId.</span><span class="sxs-lookup"><span data-stu-id="4e38c-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="4e38c-110">Предупреждение: псевдоним **Get-AzRecoveryServicesBackupJobDetails** будет удален в будущем, не прерывая изменения.</span><span class="sxs-lookup"><span data-stu-id="4e38c-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="4e38c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e38c-111">EXAMPLES</span></span>

### <span data-ttu-id="4e38c-112">Пример 1: получение сведений о задании резервного копирования для невыполненных заданий</span><span class="sxs-lookup"><span data-stu-id="4e38c-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="4e38c-113">Первая команда получает массив невыполненных заданий в хранилище, а затем сохраняет их в массиве $Jobs.</span><span class="sxs-lookup"><span data-stu-id="4e38c-113">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="4e38c-114">Вторая команда возвращает сведения о задании для заданий, завершившихся сбоем, в $Jobs, а затем сохраняет их в переменной $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="4e38c-114">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="4e38c-115">В последней команде отображаются сведения об ошибке для заданий, завершившихся сбоем.</span><span class="sxs-lookup"><span data-stu-id="4e38c-115">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="4e38c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e38c-116">PARAMETERS</span></span>

### <span data-ttu-id="4e38c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e38c-117">-DefaultProfile</span></span>

<span data-ttu-id="4e38c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e38c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e38c-119">-Job</span><span class="sxs-lookup"><span data-stu-id="4e38c-119">-Job</span></span>

<span data-ttu-id="4e38c-120">Указывает задание, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="4e38c-120">Specifies the job to get.</span></span>
<span data-ttu-id="4e38c-121">Чтобы получить объект **BackupJob** , используйте командлет **Get-AzRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="4e38c-121">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="4e38c-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="4e38c-122">-JobId</span></span>

<span data-ttu-id="4e38c-123">Указывает идентификатор задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="4e38c-123">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="4e38c-124">Идентификатор — это свойство JobId объекта **Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. JobBase** .</span><span class="sxs-lookup"><span data-stu-id="4e38c-124">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="4e38c-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4e38c-125">-VaultId</span></span>

<span data-ttu-id="4e38c-126">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="4e38c-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4e38c-127">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e38c-127">-CommonParameters</span></span>

<span data-ttu-id="4e38c-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e38c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e38c-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e38c-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e38c-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e38c-130">INPUTS</span></span>

### <span data-ttu-id="4e38c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4e38c-131">System.String</span></span>

## <span data-ttu-id="4e38c-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e38c-132">OUTPUTS</span></span>

### <span data-ttu-id="4e38c-133">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="4e38c-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="4e38c-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e38c-134">NOTES</span></span>

## <span data-ttu-id="4e38c-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e38c-135">RELATED LINKS</span></span>

[<span data-ttu-id="4e38c-136">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="4e38c-136">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
