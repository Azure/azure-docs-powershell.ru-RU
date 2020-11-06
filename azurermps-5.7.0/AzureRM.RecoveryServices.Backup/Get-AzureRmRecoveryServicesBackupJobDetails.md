---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 133a779a1227c74830fdae69b52db321a63a12e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558947"
---
# <span data-ttu-id="82788-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="82788-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="82788-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82788-102">SYNOPSIS</span></span>
<span data-ttu-id="82788-103">Получение сведений о задании резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="82788-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82788-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82788-104">SYNTAX</span></span>

### <span data-ttu-id="82788-105">JobFilterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="82788-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82788-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="82788-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82788-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82788-107">DESCRIPTION</span></span>
<span data-ttu-id="82788-108">Командлет **Get-AzureRmRecoveryServicesBackupJobDetails** получает сведения о задании резервного копирования Azure для указанного задания.</span><span class="sxs-lookup"><span data-stu-id="82788-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>

<span data-ttu-id="82788-109">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="82788-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="82788-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82788-110">EXAMPLES</span></span>

### <span data-ttu-id="82788-111">Пример 1: получение сведений о задании резервного копирования для невыполненных заданий</span><span class="sxs-lookup"><span data-stu-id="82788-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="82788-112">Первая команда получает массив невыполненных заданий в хранилище, а затем сохраняет их в массиве $Jobs.</span><span class="sxs-lookup"><span data-stu-id="82788-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>

<span data-ttu-id="82788-113">Вторая команда возвращает сведения о задании для заданий, завершившихся сбоем, в $Jobs, а затем сохраняет их в переменной $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="82788-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>

<span data-ttu-id="82788-114">В последней команде отображаются сведения об ошибке для заданий, завершившихся сбоем.</span><span class="sxs-lookup"><span data-stu-id="82788-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="82788-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82788-115">PARAMETERS</span></span>

### <span data-ttu-id="82788-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82788-116">-DefaultProfile</span></span>
<span data-ttu-id="82788-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82788-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82788-118">-Job</span><span class="sxs-lookup"><span data-stu-id="82788-118">-Job</span></span>
<span data-ttu-id="82788-119">Указывает задание, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="82788-119">Specifies the job to get.</span></span>
<span data-ttu-id="82788-120">Чтобы получить объект **BackupJob** , используйте командлет Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="82788-120">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: JobBase
Parameter Sets: JobFilterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82788-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="82788-121">-JobId</span></span>
<span data-ttu-id="82788-122">Указывает идентификатор задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="82788-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="82788-123">Идентификатор — это свойство InstanceId объекта **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="82788-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

```yaml
Type: String
Parameter Sets: IdFilterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82788-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82788-124">CommonParameters</span></span>
<span data-ttu-id="82788-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82788-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82788-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82788-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82788-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82788-127">INPUTS</span></span>

### <span data-ttu-id="82788-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="82788-128">None</span></span>
<span data-ttu-id="82788-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="82788-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="82788-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82788-130">OUTPUTS</span></span>

### <span data-ttu-id="82788-131">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="82788-131">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="82788-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="82788-132">NOTES</span></span>

## <span data-ttu-id="82788-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82788-133">RELATED LINKS</span></span>

[<span data-ttu-id="82788-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="82788-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


