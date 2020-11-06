---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 44C5AF58-ADC1-4BC6-9771-3FD8F0480106
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/stop-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
ms.openlocfilehash: 800b5c6e04e0842113db7fb3494815bcd97ebfb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561136"
---
# <span data-ttu-id="644fa-101">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="644fa-101">Stop-AzureRmBackupJob</span></span>

## <span data-ttu-id="644fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="644fa-102">SYNOPSIS</span></span>
<span data-ttu-id="644fa-103">Отменяет существующее задание резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="644fa-103">Cancels an existing Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="644fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="644fa-104">SYNTAX</span></span>

### <span data-ttu-id="644fa-105">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="644fa-105">IdFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Vault <AzureRMBackupVault> -JobID <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="644fa-106">JobFiltersSet</span><span class="sxs-lookup"><span data-stu-id="644fa-106">JobFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="644fa-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="644fa-107">DESCRIPTION</span></span>
<span data-ttu-id="644fa-108">Командлет **Stop-AzureRmBackupJob** отменяет существующее задание резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="644fa-108">The **Stop-AzureRmBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="644fa-109">Используйте этот параметр для остановки задания, которое занимает слишком много времени и блокирует другие действия.</span><span class="sxs-lookup"><span data-stu-id="644fa-109">Use this parameter to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="644fa-110">Вы можете отменить только следующие типы заданий:</span><span class="sxs-lookup"><span data-stu-id="644fa-110">You can cancel only the following types of jobs:</span></span> 
- <span data-ttu-id="644fa-111">Копирование</span><span class="sxs-lookup"><span data-stu-id="644fa-111">Backup</span></span>
- <span data-ttu-id="644fa-112">Восстановление</span><span class="sxs-lookup"><span data-stu-id="644fa-112">Restore</span></span>

## <span data-ttu-id="644fa-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="644fa-113">EXAMPLES</span></span>

### <span data-ttu-id="644fa-114">Пример 1: Остановка задания резервного копирования с помощью идентификатора задания</span><span class="sxs-lookup"><span data-stu-id="644fa-114">Example 1: Stop a backup job by using a job ID</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Job = Get-AzureRmBackupJob -Vault $Vault -Operation Backup
PS C:\> Stop-AzureRmBackupJob -Vault $Vault -JobID $Job.InstanceId
```

<span data-ttu-id="644fa-115">Первая команда получает хранилище с именем Vault03 с помощью командлета **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="644fa-115">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="644fa-116">Команда сохраняет этот объект в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="644fa-116">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="644fa-117">Вторая команда получает задание резервного копирования из хранилища в $Vault с помощью командлета **Get-AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="644fa-117">The second command gets a backup job from the vault in $Vault by using the **Get-AzureRmBackupJob** cmdlet.</span></span>
<span data-ttu-id="644fa-118">Команда хранит задание в переменной $Job.</span><span class="sxs-lookup"><span data-stu-id="644fa-118">The command stores the job in the $Job variable.</span></span>
<span data-ttu-id="644fa-119">В этом примере имеется только одна операция резервного копирования в указанном хранилище.</span><span class="sxs-lookup"><span data-stu-id="644fa-119">In this example, there is only one backup operation in the specified vault.</span></span>
<span data-ttu-id="644fa-120">Последняя команда останавливает задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="644fa-120">The final command stops the job that has the specified ID.</span></span>

### <span data-ttu-id="644fa-121">Пример 2: остановка всех операций восстановления</span><span class="sxs-lookup"><span data-stu-id="644fa-121">Example 2: Stop all Restore operations</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Operation Restore | Stop-AzureRmBackupJob
```

<span data-ttu-id="644fa-122">Эта команда получает все операции восстановления из хранилища в $Vault, а затем передает их в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="644fa-122">This command gets all the restore operations in the vault in $Vault, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="644fa-123">Текущий командлет останавливает каждое задание.</span><span class="sxs-lookup"><span data-stu-id="644fa-123">The current cmdlet stops each job.</span></span>

## <span data-ttu-id="644fa-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="644fa-124">PARAMETERS</span></span>

### <span data-ttu-id="644fa-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="644fa-125">-DefaultProfile</span></span>
<span data-ttu-id="644fa-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="644fa-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="644fa-127">-Job</span><span class="sxs-lookup"><span data-stu-id="644fa-127">-Job</span></span>
<span data-ttu-id="644fa-128">Указывает задание, которое отменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="644fa-128">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="644fa-129">Чтобы получить объект **AzureRmBackupJob** , используйте командлет Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="644fa-129">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="644fa-130">-JobID</span><span class="sxs-lookup"><span data-stu-id="644fa-130">-JobID</span></span>
<span data-ttu-id="644fa-131">Указывает задание, которое отменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="644fa-131">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="644fa-132">Чтобы получить объект **AzureRmBackupJob** , используйте командлет Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="644fa-132">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="644fa-133">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="644fa-133">-Vault</span></span>
<span data-ttu-id="644fa-134">Указывает хранилище резервных копий, в котором этот командлет отменяет задание.</span><span class="sxs-lookup"><span data-stu-id="644fa-134">Specifies the Backup vault in which this cmdlet cancels a job.</span></span>
<span data-ttu-id="644fa-135">Чтобы получить объект **AzureRmBackupVault** , используйте командлет Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="644fa-135">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="644fa-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="644fa-136">CommonParameters</span></span>
<span data-ttu-id="644fa-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="644fa-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="644fa-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="644fa-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="644fa-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="644fa-139">INPUTS</span></span>

### <span data-ttu-id="644fa-140">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="644fa-140">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>
<span data-ttu-id="644fa-141">Параметры: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="644fa-141">Parameters: Job (ByValue)</span></span>

## <span data-ttu-id="644fa-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="644fa-142">OUTPUTS</span></span>

### <span data-ttu-id="644fa-143">System. void</span><span class="sxs-lookup"><span data-stu-id="644fa-143">System.Void</span></span>

## <span data-ttu-id="644fa-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="644fa-144">NOTES</span></span>

## <span data-ttu-id="644fa-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="644fa-145">RELATED LINKS</span></span>

[<span data-ttu-id="644fa-146">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="644fa-146">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="644fa-147">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="644fa-147">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="644fa-148">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="644fa-148">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


