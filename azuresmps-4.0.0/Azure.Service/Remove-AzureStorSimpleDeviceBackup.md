---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 47650E39-758C-4D3C-9653-B70576CA0979
online version: ''
schema: 2.0.0
ms.openlocfilehash: a93791e3184fcabacbf90caebcb2170746922b36
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076467"
---
# <span data-ttu-id="05320-101">Remove-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="05320-101">Remove-AzureStorSimpleDeviceBackup</span></span>

## <span data-ttu-id="05320-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05320-102">SYNOPSIS</span></span>
<span data-ttu-id="05320-103">Удаляет объект резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="05320-103">Deletes a backup object.</span></span>

## <span data-ttu-id="05320-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05320-104">SYNTAX</span></span>

### <span data-ttu-id="05320-105">IdentifyById (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="05320-105">IdentifyById (Default)</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupId <String> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="05320-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="05320-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -Backup <Backup> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="05320-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05320-107">DESCRIPTION</span></span>
<span data-ttu-id="05320-108">Командлет **Remove-AzureStorSimpleDeviceBackup** удаляет один объект резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="05320-108">The **Remove-AzureStorSimpleDeviceBackup** cmdlet deletes a single backup object.</span></span>
<span data-ttu-id="05320-109">При попытке удалить резервную копию, которая уже удалена, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="05320-109">If you attempt to delete a backup that has already been deleted, this cmdlet returns an error.</span></span>

## <span data-ttu-id="05320-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05320-110">EXAMPLES</span></span>

### <span data-ttu-id="05320-111">Пример 1: Удаление резервной копии для устройства</span><span class="sxs-lookup"><span data-stu-id="05320-111">Example 1: Remove a backup for a device</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId "dcb5c991-0485-400f-8d0a-03a1341ee989" -Force
The remove job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 6c73aff2-f5a1-4b5e-
9a4e-857e128dc216 for tracking the job status
```

<span data-ttu-id="05320-112">Эта команда удаляет резервную копию с указанным ИДЕНТИФИКАТОРом для устройства с именем Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="05320-112">This command removes the backup that has the specified ID for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="05320-113">Команда запускает операцию, которая удаляет объект **резервного копирования** , а затем возвращает объект **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="05320-113">The command starts the operation that removes the **Backup** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="05320-114">Чтобы просмотреть состояние задачи, используйте командлет **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="05320-114">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="05320-115">Пример 2: удаление первой резервной копии устройства с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="05320-115">Example 2: Remove the first backup for a device by using its ID</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId $Backup[0].InstanceId -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 53a656c3-c082-4e1f-afb7-bff3db45c791
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f4411f38d07f68b88095682dbeedd9e9
```

<span data-ttu-id="05320-116">Первая команда получает резервные копии для устройства с именем Contoso63-AppVm, а затем сохраняет их в переменной $Backup.</span><span class="sxs-lookup"><span data-stu-id="05320-116">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="05320-117">Вторая команда удаляет резервную копию с устройства с именем Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="05320-117">The second command deletes a backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="05320-118">В команде используется стандартная точечная нотация для ссылки на свойство **InstanceId** первого элемента массива $Backup.</span><span class="sxs-lookup"><span data-stu-id="05320-118">The command uses standard dot notation to refer to the **InstanceId** property of the first element of the $Backup array.</span></span>
<span data-ttu-id="05320-119">Эта команда задает параметр *WaitForComplete* и, следовательно, команда ожидает завершения операции, а затем возвращает объект **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="05320-119">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="05320-120">Пример 3: удаление первой резервной копии устройства с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="05320-120">Example 3: Remove the first backup for a device by using the pipeline</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -WaitForComplete
PS C:\> $Backup[0] | Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -Force -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 48059fd8-e355-4b91-9385-630d24f31df6
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e1753f3bf68e6e44ab719436b5111e41
```

<span data-ttu-id="05320-121">Первая команда получает резервные копии для устройства с именем Contoso63-AppVm, а затем сохраняет их в переменной $Backup.</span><span class="sxs-lookup"><span data-stu-id="05320-121">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="05320-122">Вторая команда передает первый объект, хранящийся в массиве $Backup, в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="05320-122">The second command passes the first object stored in the $Backup array to the current cmdlet.</span></span>
<span data-ttu-id="05320-123">Этот командлет удаляет эту резервную копию с устройства с именем Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="05320-123">That cmdlet deletes that backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="05320-124">Эта команда задает параметр *WaitForComplete* и, следовательно, команда ожидает завершения операции, а затем возвращает объект **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="05320-124">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

## <span data-ttu-id="05320-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05320-125">PARAMETERS</span></span>

### <span data-ttu-id="05320-126">-Резервное копирование</span><span class="sxs-lookup"><span data-stu-id="05320-126">-Backup</span></span>
<span data-ttu-id="05320-127">Указывает удаляемый объект **резервного копирования** .</span><span class="sxs-lookup"><span data-stu-id="05320-127">Specifies the **Backup** object to delete.</span></span>
<span data-ttu-id="05320-128">Чтобы получить объект **резервного копирования** , используйте командлет **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="05320-128">To obtain a **Backup** object, use the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>

```yaml
Type: Backup
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05320-129">-BackupId</span><span class="sxs-lookup"><span data-stu-id="05320-129">-BackupId</span></span>
<span data-ttu-id="05320-130">Задает ИД экземпляра удаляемого архива.</span><span class="sxs-lookup"><span data-stu-id="05320-130">Specifies the instance ID of a backup to delete.</span></span>

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

### <span data-ttu-id="05320-131">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="05320-131">-DeviceName</span></span>
<span data-ttu-id="05320-132">Указывает имя устройства StorSimple, на котором нужно удалить резервную копию.</span><span class="sxs-lookup"><span data-stu-id="05320-132">Specifies the name of the StorSimple device on which to delete a backup.</span></span>

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

### <span data-ttu-id="05320-133">-Force</span><span class="sxs-lookup"><span data-stu-id="05320-133">-Force</span></span>
<span data-ttu-id="05320-134">Указывает на то, что этот командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="05320-134">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="05320-135">-Profile</span><span class="sxs-lookup"><span data-stu-id="05320-135">-Profile</span></span>
<span data-ttu-id="05320-136">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="05320-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="05320-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="05320-137">-WaitForComplete</span></span>
<span data-ttu-id="05320-138">Указывает на то, что этот командлет ожидает завершения операции до того, как она возвратит управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="05320-138">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="05320-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05320-139">CommonParameters</span></span>
<span data-ttu-id="05320-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05320-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05320-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05320-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05320-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05320-142">INPUTS</span></span>

### <span data-ttu-id="05320-143">Копирование</span><span class="sxs-lookup"><span data-stu-id="05320-143">Backup</span></span>

## <span data-ttu-id="05320-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05320-144">OUTPUTS</span></span>

### <span data-ttu-id="05320-145">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="05320-145">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="05320-146">Этот командлет возвращает объект **TaskStatusInfo** , если указан параметр *WaitForComplete* если этот параметр не указан, функция возвращает объект **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="05320-146">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="05320-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="05320-147">NOTES</span></span>

## <span data-ttu-id="05320-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05320-148">RELATED LINKS</span></span>

[<span data-ttu-id="05320-149">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="05320-149">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)


