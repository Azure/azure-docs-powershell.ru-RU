---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 7ebbb3cf53c422a3a4d5c73f156cd3890eaa41e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246365"
---
# <span data-ttu-id="539ce-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="539ce-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="539ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="539ce-102">SYNOPSIS</span></span>

<span data-ttu-id="539ce-103">Получение сведений о задании резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="539ce-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="539ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="539ce-104">SYNTAX</span></span>

### <span data-ttu-id="539ce-105">JobFilterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="539ce-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="539ce-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="539ce-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="539ce-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="539ce-107">DESCRIPTION</span></span>

<span data-ttu-id="539ce-108">Командлет **Get-AzRecoveryServicesBackupJobDetail** получает сведения о задании резервного копирования Azure для указанного задания.</span><span class="sxs-lookup"><span data-stu-id="539ce-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="539ce-109">Задайте контекст хранилища с помощью параметра-VaultId.</span><span class="sxs-lookup"><span data-stu-id="539ce-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="539ce-110">Предупреждение: псевдоним **Get-AzRecoveryServicesBackupJobDetails** будет удален в будущем, не прерывая изменения.</span><span class="sxs-lookup"><span data-stu-id="539ce-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="539ce-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="539ce-111">EXAMPLES</span></span>

### <span data-ttu-id="539ce-112">Пример 1: получение сведений о задании резервного копирования для невыполненных заданий</span><span class="sxs-lookup"><span data-stu-id="539ce-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="539ce-113">Первая команда извлекает подходящее хранилище.</span><span class="sxs-lookup"><span data-stu-id="539ce-113">The first command fetches the relevant vault.</span></span> <span data-ttu-id="539ce-114">Вторая команда получает массив невыполненных заданий в хранилище, а затем сохраняет их в массиве $Jobs.</span><span class="sxs-lookup"><span data-stu-id="539ce-114">The second command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="539ce-115">Третья команда получает сведения о задании для 1-го невыполненного задания в $Jobs, а затем сохраняет их в переменной $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="539ce-115">The third command gets the job details for the 1st failed job in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="539ce-116">В последней команде отображаются сведения об ошибке для заданий, завершившихся сбоем.</span><span class="sxs-lookup"><span data-stu-id="539ce-116">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="539ce-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="539ce-117">PARAMETERS</span></span>

### <span data-ttu-id="539ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="539ce-118">-DefaultProfile</span></span>

<span data-ttu-id="539ce-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="539ce-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="539ce-120">-Job</span><span class="sxs-lookup"><span data-stu-id="539ce-120">-Job</span></span>

<span data-ttu-id="539ce-121">Указывает задание, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="539ce-121">Specifies the job to get.</span></span>
<span data-ttu-id="539ce-122">Чтобы получить объект **BackupJob** , используйте командлет **Get-AzRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="539ce-122">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="539ce-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="539ce-123">-JobId</span></span>

<span data-ttu-id="539ce-124">Указывает идентификатор задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="539ce-124">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="539ce-125">Идентификатор — это свойство JobId объекта **Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. JobBase** .</span><span class="sxs-lookup"><span data-stu-id="539ce-125">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="539ce-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="539ce-126">-VaultId</span></span>

<span data-ttu-id="539ce-127">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="539ce-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="539ce-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="539ce-128">CommonParameters</span></span>
<span data-ttu-id="539ce-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="539ce-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="539ce-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="539ce-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="539ce-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="539ce-131">INPUTS</span></span>

### <span data-ttu-id="539ce-132">System. String</span><span class="sxs-lookup"><span data-stu-id="539ce-132">System.String</span></span>

## <span data-ttu-id="539ce-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="539ce-133">OUTPUTS</span></span>

### <span data-ttu-id="539ce-134">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="539ce-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="539ce-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="539ce-135">NOTES</span></span>

## <span data-ttu-id="539ce-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="539ce-136">RELATED LINKS</span></span>

[<span data-ttu-id="539ce-137">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="539ce-137">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
