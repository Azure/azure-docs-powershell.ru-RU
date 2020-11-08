---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F92D18AC-B716-42CA-9C2D-1AB5A599F73E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2fdd1063450615b729fade77c7edb51ad93bec77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076096"
---
# <span data-ttu-id="42ab9-101">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="42ab9-101">Remove-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="42ab9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42ab9-102">SYNOPSIS</span></span>
<span data-ttu-id="42ab9-103">Удаляет запись управления доступом из конфигурации службы.</span><span class="sxs-lookup"><span data-stu-id="42ab9-103">Deletes an access control record from the service configuration.</span></span>

## <span data-ttu-id="42ab9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42ab9-104">SYNTAX</span></span>

### <span data-ttu-id="42ab9-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="42ab9-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleAccessControlRecord -ACRName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="42ab9-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="42ab9-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleAccessControlRecord -ACR <AccessControlRecord> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="42ab9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42ab9-107">DESCRIPTION</span></span>
<span data-ttu-id="42ab9-108">Командлет **Remove-AzureStorSimpleAccessControlRecord** удаляет запись управления доступом из конфигурации службы.</span><span class="sxs-lookup"><span data-stu-id="42ab9-108">The **Remove-AzureStorSimpleAccessControlRecord** cmdlet deletes an access control record from the service configuration.</span></span>

## <span data-ttu-id="42ab9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42ab9-109">EXAMPLES</span></span>

### <span data-ttu-id="42ab9-110">Пример 1: удаление элемента управления Controlaccess доступа RecordAccess</span><span class="sxs-lookup"><span data-stu-id="42ab9-110">Example 1: Remove an Access Controlaccess control recordaccess control</span></span>
```
PS C:\>Remove-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -WaitForComplete -Force
VERBOSE: ClientRequestId: 574aeb7f-fbc9-46d5-bc68-1bfe4487bd8b_PS
VERBOSE: ClientRequestId: 985afe84-ef95-47cb-8c8f-df094530334b_PS
VERBOSE: About to run a job to remove your ACR! 
VERBOSE: ClientRequestId: 7eb7e1a0-2288-44da-b64c-5bf86a6b9aaf_PS


JobId        : f7934db5-8363-4152-b38e-b9a5d91f97b9
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your delete operation has completed successfully.
```

<span data-ttu-id="42ab9-111">Эта команда удаляет запись контроля доступа с именем Acr10.</span><span class="sxs-lookup"><span data-stu-id="42ab9-111">This command deletes the access control record named Acr10.</span></span>
<span data-ttu-id="42ab9-112">Эта команда задает параметр *WaitForComplete* и, следовательно, команда ожидает завершения операции, а затем возвращает объект **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="42ab9-112">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="42ab9-113">Пример 2: Удаление записи элемента управления доступом Controlaccess с помощью элемента управления pipelineAccess Controlaccess Controlaccess</span><span class="sxs-lookup"><span data-stu-id="42ab9-113">Example 2: Remove an Access Controlaccess control record by using the pipelineAccess Controlaccess controlaccess control</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr10" | Remove-AzureStorSimpleAccessControlRecord -Force 
VERBOSE: ClientRequestId: ff8d8bd6-4c92-4ab6-8fde-e9344a253da3_PS
VERBOSE: ClientRequestId: f71c74f3-33b9-40d1-b8d5-12363e98412f_PS
VERBOSE: ClientRequestId: d5d809d0-ec22-4e45-97ee-a56edc41e503_PS
VERBOSE: About to create a job to remove your ACR! 
VERBOSE: ClientRequestId: 6ffa6bc8-37b3-49ff-bafc-721b360f09cb_PS
294a0208-a43f-4d80-b824-2319cd77c5e6
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
294a0208-a43f-4d80-b824-2319cd77c5e6 for tracking the task's status
```

<span data-ttu-id="42ab9-114">Эта команда использует **Get-AzureStorSimpleAccessControlRecord** для получения **AccessControlRecord** с именем Acr10, а затем передает этот объект текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="42ab9-114">This command uses the **Get-AzureStorSimpleAccessControlRecord** to get the **AccessControlRecord** named Acr10, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="42ab9-115">Команда запускает операцию, которая удаляет объект **AccessControlRecord** , а затем возвращает объект **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="42ab9-115">The command starts the operation that removes the **AccessControlRecord** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="42ab9-116">Чтобы просмотреть состояние задачи, используйте командлет **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="42ab9-116">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="42ab9-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42ab9-117">PARAMETERS</span></span>

### <span data-ttu-id="42ab9-118">-Запись контроля доступа</span><span class="sxs-lookup"><span data-stu-id="42ab9-118">-ACR</span></span>
<span data-ttu-id="42ab9-119">Указывает объект **AccessControlRecord** , который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="42ab9-119">Specifies an **AccessControlRecord** object to delete.</span></span>
<span data-ttu-id="42ab9-120">Чтобы получить объект **AccessControlRecord** , используйте командлет **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="42ab9-120">To obtain an **AccessControlRecord** object, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>

```yaml
Type: AccessControlRecord
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42ab9-121">-ACRName</span><span class="sxs-lookup"><span data-stu-id="42ab9-121">-ACRName</span></span>
<span data-ttu-id="42ab9-122">Указывает имя записи управления доступом, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="42ab9-122">Specifies a name of the access control record to delete.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ab9-123">-Force</span><span class="sxs-lookup"><span data-stu-id="42ab9-123">-Force</span></span>
<span data-ttu-id="42ab9-124">Указывает на то, что этот командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="42ab9-124">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="42ab9-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="42ab9-125">-Profile</span></span>
<span data-ttu-id="42ab9-126">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="42ab9-126">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="42ab9-127">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="42ab9-127">-WaitForComplete</span></span>
<span data-ttu-id="42ab9-128">Указывает на то, что этот командлет ожидает завершения операции до того, как она возвратит управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="42ab9-128">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="42ab9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ab9-129">CommonParameters</span></span>
<span data-ttu-id="42ab9-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42ab9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ab9-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42ab9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ab9-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42ab9-132">INPUTS</span></span>

### <span data-ttu-id="42ab9-133">AccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="42ab9-133">AccessControlRecord</span></span>
<span data-ttu-id="42ab9-134">Этот командлет принимает объект **AccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="42ab9-134">This cmdlet accepts an **AccessControlRecord** object.</span></span>
<span data-ttu-id="42ab9-135">Объект **AccessControlRecord** состоит из следующих полей:</span><span class="sxs-lookup"><span data-stu-id="42ab9-135">An **AccessControlRecord** object contains the following fields:</span></span> 

- <span data-ttu-id="42ab9-136">**GlobalId** ( **строка** )</span><span class="sxs-lookup"><span data-stu-id="42ab9-136">**GlobalId** ( **String** )</span></span> 
- <span data-ttu-id="42ab9-137">**InitiatorName** ( **строка** )</span><span class="sxs-lookup"><span data-stu-id="42ab9-137">**InitiatorName** ( **String** )</span></span> 
- <span data-ttu-id="42ab9-138">**InstanceId** ( **строка** )</span><span class="sxs-lookup"><span data-stu-id="42ab9-138">**InstanceId** ( **String** )</span></span> 
- <span data-ttu-id="42ab9-139">**Name** ( **строка** )</span><span class="sxs-lookup"><span data-stu-id="42ab9-139">**Name** ( **String** )</span></span> 
- <span data-ttu-id="42ab9-140">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="42ab9-140">**OperationInProgress** ( **OperationInProgress** )</span></span> 
- <span data-ttu-id="42ab9-141">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="42ab9-141">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="42ab9-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42ab9-142">OUTPUTS</span></span>

### <span data-ttu-id="42ab9-143">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="42ab9-143">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="42ab9-144">Этот командлет возвращает объект **TaskStatusInfo** , если указан параметр *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="42ab9-144">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="42ab9-145">Если этот параметр не указан, функция возвращает объект **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="42ab9-145">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="42ab9-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="42ab9-146">NOTES</span></span>

## <span data-ttu-id="42ab9-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42ab9-147">RELATED LINKS</span></span>

[<span data-ttu-id="42ab9-148">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="42ab9-148">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="42ab9-149">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="42ab9-149">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="42ab9-150">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="42ab9-150">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="42ab9-151">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="42ab9-151">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


