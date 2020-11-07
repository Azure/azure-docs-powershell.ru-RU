---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6187F603-5298-4854-94F3-0C38FCF3125F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
ms.openlocfilehash: bf4ba77a7162faaf593e11b68a82fe5a6e55df1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732490"
---
# <span data-ttu-id="f1e06-101">Get-AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="f1e06-101">Get-AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="f1e06-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1e06-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e06-103">Получает сведения о задании резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="f1e06-103">Gets the details of a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1e06-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1e06-104">SYNTAX</span></span>

### <span data-ttu-id="f1e06-105">JobsFiltersSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f1e06-105">JobsFiltersSet (Default)</span></span>
```
Get-AzureRmBackupJobDetails -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1e06-106">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="f1e06-106">IdFiltersSet</span></span>
```
Get-AzureRmBackupJobDetails -Vault <AzureRMBackupVault> -JobId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1e06-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1e06-107">DESCRIPTION</span></span>
<span data-ttu-id="f1e06-108">Командлет **Get-AzureRmBackupJobDetails** получает сведения о задании резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="f1e06-108">The **Get-AzureRmBackupJobDetails** cmdlet gets the details of an Azure Backup job.</span></span>
<span data-ttu-id="f1e06-109">Вы можете использовать этот командлет для сбора сведений о неуспешном выполнении задания.</span><span class="sxs-lookup"><span data-stu-id="f1e06-109">You can use this cmdlet to gather information about a job that fails.</span></span>

## <span data-ttu-id="f1e06-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1e06-110">EXAMPLES</span></span>

### <span data-ttu-id="f1e06-111">Пример 1: отображение сведений о невыполненном задании</span><span class="sxs-lookup"><span data-stu-id="f1e06-111">Example 1: Display the details of a failed job</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Jobs = Get-AzureRmBackupJob -Vault $Vault -Status Failed
PS C:\> $JobDetails = Get-AzureRmBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
ErrorCode ErrorMessage                            Recommendations
--------- ------------                            ---------------
   400001 Command execution failed.               {Another operation is currently in p...
```

<span data-ttu-id="f1e06-112">Первая команда получает хранилище с именем Vault03 с помощью командлета **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="f1e06-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="f1e06-113">Команда сохраняет этот объект в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="f1e06-113">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="f1e06-114">Вторая команда получает сбойные задания из хранилища в $Vault, а затем сохраняет их в переменной массива $Jobs.</span><span class="sxs-lookup"><span data-stu-id="f1e06-114">The second command gets failed jobs from the vault in $Vault, and then stores them in the $Jobs array variable.</span></span>
<span data-ttu-id="f1e06-115">Третье задание получает сведения для первого задания в переменной $Jobs и затем сохраняет эти сведения в переменной $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="f1e06-115">The third job gets details for the first job in the $Jobs variable, and then stores those details in the $JobDetails variable.</span></span>
<span data-ttu-id="f1e06-116">Последняя команда отображает свойство **ErrorDetails** для $JobDetails с помощью стандартного синтаксиса с точкой.</span><span class="sxs-lookup"><span data-stu-id="f1e06-116">The final command displays the **ErrorDetails** property of $JobDetails by using standard dot syntax.</span></span>

### <span data-ttu-id="f1e06-117">Пример 2: отображение рекомендуемого действия для невыполненного задания</span><span class="sxs-lookup"><span data-stu-id="f1e06-117">Example 2: Display the recommended action for a failed job</span></span>
```
PS C:\>$JobDetails.ErrorDetails.Recommendations
Another operation is currently in progress on this item. Please wait until the previous operation is completed, and then retry.
```

<span data-ttu-id="f1e06-118">Эта команда отображает рекомендуемое действие из переменной $JobDetails, созданной в первом примере.</span><span class="sxs-lookup"><span data-stu-id="f1e06-118">This command displays the recommended action from the $JobDetails variable that was created in the first example.</span></span>

## <span data-ttu-id="f1e06-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1e06-119">PARAMETERS</span></span>

### <span data-ttu-id="f1e06-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e06-120">-DefaultProfile</span></span>
<span data-ttu-id="f1e06-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f1e06-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1e06-122">-Job</span><span class="sxs-lookup"><span data-stu-id="f1e06-122">-Job</span></span>
<span data-ttu-id="f1e06-123">Указывает задание, для которого этот командлет получает сведения.</span><span class="sxs-lookup"><span data-stu-id="f1e06-123">Specifies a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="f1e06-124">Чтобы получить объект **AzureRmBackupJob** , используйте командлет Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="f1e06-124">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e06-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="f1e06-125">-JobId</span></span>
<span data-ttu-id="f1e06-126">Указывает идентификатор задания, сведения о котором этот командлет получает.</span><span class="sxs-lookup"><span data-stu-id="f1e06-126">Specifies the ID of a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="f1e06-127">Идентификатор — это свойство **InstanceId** объекта **AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="f1e06-127">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="f1e06-128">Чтобы получить объект **AzureRmBackupJob** , используйте Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="f1e06-128">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e06-129">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="f1e06-129">-Vault</span></span>
<span data-ttu-id="f1e06-130">Указывает хранилище резервных копий, для которого этот командлет получает сведения о задании.</span><span class="sxs-lookup"><span data-stu-id="f1e06-130">Specifies the Backup vault for which this cmdlet gets job details.</span></span>
<span data-ttu-id="f1e06-131">Чтобы получить объект **AzureRmBackupVault** , используйте командлет Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="f1e06-131">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e06-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e06-132">CommonParameters</span></span>
<span data-ttu-id="f1e06-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1e06-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e06-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1e06-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e06-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1e06-135">INPUTS</span></span>

### <span data-ttu-id="f1e06-136">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="f1e06-136">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>
<span data-ttu-id="f1e06-137">Параметры: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f1e06-137">Parameters: Job (ByValue)</span></span>

## <span data-ttu-id="f1e06-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1e06-138">OUTPUTS</span></span>

### <span data-ttu-id="f1e06-139">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="f1e06-139">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJobDetails</span></span>

## <span data-ttu-id="f1e06-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1e06-140">NOTES</span></span>

## <span data-ttu-id="f1e06-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1e06-141">RELATED LINKS</span></span>

[<span data-ttu-id="f1e06-142">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="f1e06-142">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="f1e06-143">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="f1e06-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


