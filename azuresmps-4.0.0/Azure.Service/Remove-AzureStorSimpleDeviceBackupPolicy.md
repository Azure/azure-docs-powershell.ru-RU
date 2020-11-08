---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5AB916CB-A141-4662-8220-6C1FBB58FC69
online version: ''
schema: 2.0.0
ms.openlocfilehash: aab5e0f3ef432333eeb4aff68673c0d5c2219521
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076464"
---
# <span data-ttu-id="e44f3-101">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="e44f3-101">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="e44f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e44f3-102">SYNOPSIS</span></span>
<span data-ttu-id="e44f3-103">Удаление существующей политики резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e44f3-103">Removes an existing backup policy.</span></span>

## <span data-ttu-id="e44f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e44f3-104">SYNTAX</span></span>

### <span data-ttu-id="e44f3-105">IdentifyById (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e44f3-105">IdentifyById (Default)</span></span>
```
Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> [-Force]
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e44f3-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="e44f3-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-Force]
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e44f3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e44f3-107">DESCRIPTION</span></span>
<span data-ttu-id="e44f3-108">Командлет **Remove-AzureStorSimpleDeviceBackupPolicy** удаляет существующий объект **BackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="e44f3-108">The **Remove-AzureStorSimpleDeviceBackupPolicy** cmdlet removes an existing **BackupPolicy** object.</span></span>
<span data-ttu-id="e44f3-109">После удаления политики архивации дальнейшие резервные копии не помещаются в соответствии с этой политикой.</span><span class="sxs-lookup"><span data-stu-id="e44f3-109">After you remove a backup policy, no further backups take place based on that policy.</span></span>
<span data-ttu-id="e44f3-110">Этот командлет также удаляет все расписания, связанные с удаленной политикой.</span><span class="sxs-lookup"><span data-stu-id="e44f3-110">This cmdlet also deletes all schedules associated with the deleted policy.</span></span>

## <span data-ttu-id="e44f3-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e44f3-111">EXAMPLES</span></span>

### <span data-ttu-id="e44f3-112">Пример 1: Удаление политики архивации</span><span class="sxs-lookup"><span data-stu-id="e44f3-112">Example 1: Remove a backup policy</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "03710b4c-82c1-40ca-be5c-40289dc49642" -Force
VERBOSE: ClientRequestId: b3e4d485-eae4-4cf4-a43b-815f3abcd2dd_PS
VERBOSE: ClientRequestId: a260ee98-46aa-49e0-91ac-31d4155f4cae_PS
VERBOSE: About to create a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: 92a9c264-90df-4345-a495-92767dd266f2_PS
695be190-ac81-4cf2-b1c5-03ef6b08d005
VERBOSE: The remove task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
695be190-ac81-4cf2-b1c5-03ef6b08d005 for tracking the task's status
```

<span data-ttu-id="e44f3-113">Эта команда удаляет **BackupPolicy** с идентификатором экземпляра 03710b4c-82c1-40ca-be5c-40289dc49642, чтобы не создавать дополнительные резервные копии на основе этой политики.</span><span class="sxs-lookup"><span data-stu-id="e44f3-113">This command removes the **BackupPolicy** that has the instance ID 03710b4c-82c1-40ca-be5c-40289dc49642, so that no more backups are made based on this policy.</span></span>
<span data-ttu-id="e44f3-114">Команда также удаляет все расписания, связанные с этой политикой.</span><span class="sxs-lookup"><span data-stu-id="e44f3-114">The command also deletes all schedules associated with this policy.</span></span>
<span data-ttu-id="e44f3-115">Команда запускает операцию, которая удаляет объект **BackupPolicy** , а затем возвращает объект **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="e44f3-115">The command starts the operation that removes the **BackupPolicy** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="e44f3-116">Чтобы просмотреть состояние задачи, используйте командлет **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="e44f3-116">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="e44f3-117">Пример 2: удаление первой из политик резервного копирования для устройства</span><span class="sxs-lookup"><span data-stu-id="e44f3-117">Example 2: Remove the first of the backup policies for a device</span></span>
```
PS C:\>$Policies = Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId $Policies[0].InstanceId -Force -WaitForComplete
VERBOSE: ClientRequestId: db3b49fa-cffa-446d-ba52-daa6802e00f7_PS
VERBOSE: ClientRequestId: 70e2b56f-c2df-40d0-a1e5-d7a4d7e25962_PS
VERBOSE: About to run a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: f8eb3d4d-2c57-4fc9-9f40-79d0f2ea1b6a_PS


JobId        : 820a246e-54b6-41a9-bdd5-15d5daea9b0a
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your remove operation has completed successfully.
```

<span data-ttu-id="e44f3-118">Первая команда получает политики резервного копирования для устройства с именем Contoso63-AppVm, а затем сохраняет их в переменной $Policies.</span><span class="sxs-lookup"><span data-stu-id="e44f3-118">The first command gets the backup policies for the device named Contoso63-AppVm, and then stores them in the $Policies variable.</span></span>

<span data-ttu-id="e44f3-119">Вторая команда удаляет первую политику резервного копирования из Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="e44f3-119">The second command removes the first backup policy from Contoso63-AppVm.</span></span>
<span data-ttu-id="e44f3-120">В команде используется стандартный синтаксис с точкой, чтобы определить свойство **InstanceId** первого элемента в $Policies.</span><span class="sxs-lookup"><span data-stu-id="e44f3-120">The command uses standard dot syntax to identify the **InstanceId** property of the first item in $Policies.</span></span>
<span data-ttu-id="e44f3-121">Эта команда задает параметр *WaitForComplete* , поэтому команда завершает задачу и возвращает объект **TaskStatusInfo** для задачи.</span><span class="sxs-lookup"><span data-stu-id="e44f3-121">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the task.</span></span>

### <span data-ttu-id="e44f3-122">Пример 3: Удаление политики резервного копирования с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="e44f3-122">Example 3: Remove a backup policy by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQAVolume01_Default" | Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -Force -WaitForComplete
VERBOSE: ClientRequestId: 60080fb1-2f88-4c17-bfd7-21aa73440a9c_PS
VERBOSE: ClientRequestId: 04c91121-50d7-4796-9af6-fc6a7d6b6a0e_PS
VERBOSE: ClientRequestId: 47ceb37c-672f-42e8-bd19-1190925c46cd_PS
VERBOSE: ClientRequestId: cbc39757-f2cc-4cc5-93ea-4ec0fbfb0ca8_PS
VERBOSE: ClientRequestId: 3614d47a-51fc-4500-a5f1-5401301ca4e3_PS
VERBOSE: About to create a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: dbd7166e-1888-4b11-9af9-8d49712a8c8b_PS
702ad240-5730-4015-b051-56055bd2c2d3
VERBOSE: The remove task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
702ad240-5730-4015-b051-56055bd2c2d3 for tracking the task's status
VERBOSE: BackupPolicy with id bfe0bf8a-2d09-4690-93da-38a4f24e9f4f found!
```

<span data-ttu-id="e44f3-123">Эта команда получает объект **BackupPolicyDetails** с помощью **Get-AzureStorSimpleDeviceBackupPolicy** и передает его в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="e44f3-123">This command gets a **BackupPolicyDetails** object by using **Get-AzureStorSimpleDeviceBackupPolicy** , and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e44f3-124">Текущий командлет удаляет политику резервного копирования с именем TSQAVolume01_Default.</span><span class="sxs-lookup"><span data-stu-id="e44f3-124">The current cmdlet removes the backup policy named TSQAVolume01_Default.</span></span>

## <span data-ttu-id="e44f3-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e44f3-125">PARAMETERS</span></span>

### <span data-ttu-id="e44f3-126">-BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="e44f3-126">-BackupPolicy</span></span>
<span data-ttu-id="e44f3-127">Указывает объект **BackupPolicyDetails** , который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e44f3-127">Specifies the **BackupPolicyDetails** object to delete.</span></span>
<span data-ttu-id="e44f3-128">Чтобы получить объект **BackupPolicyDetails** , используйте командлет **Get-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="e44f3-128">To obtain a **BackupPolicyDetails** object, use the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e44f3-129">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="e44f3-129">-BackupPolicyId</span></span>
<span data-ttu-id="e44f3-130">Задает ИД экземпляра объекта **BackupPolicy** , который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e44f3-130">Specifies the instance ID of the **BackupPolicy** object to delete.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44f3-131">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="e44f3-131">-DeviceName</span></span>
<span data-ttu-id="e44f3-132">Указывает имя устройства StorSimple, на котором нужно удалить политику резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e44f3-132">Specifies the name of the StorSimple device on which to delete the backup policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44f3-133">-Force</span><span class="sxs-lookup"><span data-stu-id="e44f3-133">-Force</span></span>
<span data-ttu-id="e44f3-134">Указывает на то, что этот командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e44f3-134">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44f3-135">-Profile</span><span class="sxs-lookup"><span data-stu-id="e44f3-135">-Profile</span></span>
<span data-ttu-id="e44f3-136">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="e44f3-136">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44f3-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="e44f3-137">-WaitForComplete</span></span>
<span data-ttu-id="e44f3-138">Указывает на то, что этот командлет ожидает завершения операции до того, как она возвратит управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e44f3-138">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44f3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e44f3-139">CommonParameters</span></span>
<span data-ttu-id="e44f3-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e44f3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e44f3-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e44f3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e44f3-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e44f3-142">INPUTS</span></span>

### <span data-ttu-id="e44f3-143">BackupPolicyDetails</span><span class="sxs-lookup"><span data-stu-id="e44f3-143">BackupPolicyDetails</span></span>
<span data-ttu-id="e44f3-144">Этот командлет принимает объект **BackupPolicyDetails** , который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e44f3-144">This cmdlet accepts a **BackupPolicyDetails** object to delete.</span></span>

## <span data-ttu-id="e44f3-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e44f3-145">OUTPUTS</span></span>

### <span data-ttu-id="e44f3-146">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="e44f3-146">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="e44f3-147">Этот командлет возвращает объект **TaskStatusInfo** , если указан параметр *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="e44f3-147">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="e44f3-148">Если этот параметр не указан, функция возвращает объект **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="e44f3-148">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="e44f3-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="e44f3-149">NOTES</span></span>

## <span data-ttu-id="e44f3-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e44f3-150">RELATED LINKS</span></span>

[<span data-ttu-id="e44f3-151">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="e44f3-151">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="e44f3-152">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="e44f3-152">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="e44f3-153">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="e44f3-153">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="e44f3-154">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="e44f3-154">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


