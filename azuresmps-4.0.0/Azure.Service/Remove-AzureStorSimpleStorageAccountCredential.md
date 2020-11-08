---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 1BD296FB-8BFC-473F-951D-D2BF265E50AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 048be9276957ee865aa3204392b1dd847b0d6acf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076449"
---
# <span data-ttu-id="68dde-101">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="68dde-101">Remove-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="68dde-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="68dde-102">SYNOPSIS</span></span>
<span data-ttu-id="68dde-103">Удаление существующих учетных данных учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="68dde-103">Deletes an existing storage account credential.</span></span>

## <span data-ttu-id="68dde-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="68dde-104">SYNTAX</span></span>

### <span data-ttu-id="68dde-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="68dde-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="68dde-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="68dde-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -SAC <StorageAccountCredentialResponse> [-WaitForComplete]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="68dde-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68dde-107">DESCRIPTION</span></span>
<span data-ttu-id="68dde-108">Командлет **Remove-AzureStorSimpleStorageAccountCredential** удаляет существующие учетные данные учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="68dde-108">The **Remove-AzureStorSimpleStorageAccountCredential** cmdlet deletes an existing storage account credential.</span></span>
<span data-ttu-id="68dde-109">Укажите учетную запись по имени или используйте командлет **Get-AzureStorSimpleStorageAccountCredential** , чтобы получить объект **StorageAccountCredential** , который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="68dde-109">Specify an account by name or use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet to obtain a **StorageAccountCredential** object to delete.</span></span>

## <span data-ttu-id="68dde-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="68dde-110">EXAMPLES</span></span>

### <span data-ttu-id="68dde-111">Пример 1: удаление учетных данных учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="68dde-111">Example 1: Remove a storage account credential</span></span>
```
PS C:\>Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" -Force
VERBOSE: ClientRequestId: 8e10d56b-ddb1-459b-b26e-a185f5a303de_PS
VERBOSE: About to create a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: 55cb6296-0156-4266-8591-d9e9bf8cc584_PS
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72 for tracking the task's status
```

<span data-ttu-id="68dde-112">Эта команда удаляет учетные данные учетной записи хранения с именем ContosoStorage07.</span><span class="sxs-lookup"><span data-stu-id="68dde-112">This command removes the account credential for the storage account named ContosoStorage07.</span></span>
<span data-ttu-id="68dde-113">Эта команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="68dde-113">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="68dde-114">Командлет удаляет учетные данные без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="68dde-114">The cmdlet removes the credential without prompting your for confirmation.</span></span>

### <span data-ttu-id="68dde-115">Пример 2: удаление учетных данных учетной записи хранения с помощью оператора конвейера</span><span class="sxs-lookup"><span data-stu-id="68dde-115">Example 2: Remove a storage account credential by using the pipeline operator</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" | Remove-AzureStorSimpleStorageAccountCredential -Force -WaitForComplete
VERBOSE: ClientRequestId: f1b46216-bf4c-4c19-8e92-1dfe3894e258_PS
VERBOSE: ClientRequestId: 0d946f8f-c771-4ade-8a83-7c08dad86c52_PS
VERBOSE: ClientRequestId: 2000bab6-8311-4192-ad12-c67e35fc2697_PS
VERBOSE: Storage Access Credential with name ContosoStorage07 found! 
VERBOSE: About to run a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: b803b165-bef8-4a8f-9509-4b515ea8bdec_PS
VERBOSE: Your delete operation completed successfully!
```

<span data-ttu-id="68dde-116">Эта команда получает учетную запись хранения с именем ContosoStorage07 с помощью командлета **Get-AzureStorSimpleStorageAccountCredential** , а затем передает этот объект в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="68dde-116">This command gets the storage account named ContosoStorage07 by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet, and then passes that object to the current cmdlet.</span></span>
<span data-ttu-id="68dde-117">Текущий командлет удаляет учетные данные для этой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="68dde-117">The current cmdlet removes the credential for that storage account.</span></span>
<span data-ttu-id="68dde-118">Эта команда задает параметр *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="68dde-118">This command specifies the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="68dde-119">Командлет не возвращает управление на консоль, пока не завершится операция удаления.</span><span class="sxs-lookup"><span data-stu-id="68dde-119">The cmdlet does not return control to the console until it completes the remove operation.</span></span>

## <span data-ttu-id="68dde-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="68dde-120">PARAMETERS</span></span>

### <span data-ttu-id="68dde-121">-Force</span><span class="sxs-lookup"><span data-stu-id="68dde-121">-Force</span></span>
<span data-ttu-id="68dde-122">Указывает на то, что этот командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="68dde-122">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="68dde-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="68dde-123">-Profile</span></span>
<span data-ttu-id="68dde-124">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="68dde-124">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="68dde-125">-SAC</span><span class="sxs-lookup"><span data-stu-id="68dde-125">-SAC</span></span>
<span data-ttu-id="68dde-126">Определяет учетные данные как объект **StorageAccountCredential** , который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="68dde-126">Specifies credential, as a **StorageAccountCredential** object, to remove.</span></span>
<span data-ttu-id="68dde-127">Чтобы получить объект **StorageAccountCredential** , используйте командлет **Get-AzureStorSimpleStorageAccountCredential** .</span><span class="sxs-lookup"><span data-stu-id="68dde-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68dde-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="68dde-128">-StorageAccountName</span></span>
<span data-ttu-id="68dde-129">Указывает имя учетной записи хранения, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="68dde-129">Specifies the name of the storage account credential to delete.</span></span>

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

### <span data-ttu-id="68dde-130">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="68dde-130">-WaitForComplete</span></span>
<span data-ttu-id="68dde-131">Указывает на то, что этот командлет ожидает завершения операции до того, как она возвратит управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="68dde-131">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="68dde-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68dde-132">CommonParameters</span></span>
<span data-ttu-id="68dde-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="68dde-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68dde-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68dde-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68dde-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="68dde-135">INPUTS</span></span>

### <span data-ttu-id="68dde-136">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="68dde-136">StorageAccountCredential</span></span>
<span data-ttu-id="68dde-137">Этот командлет принимает объект **StorageAccountCredential** с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="68dde-137">This cmdlet accepts a **StorageAccountCredential** object by using the pipeline.</span></span>

## <span data-ttu-id="68dde-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="68dde-138">OUTPUTS</span></span>

### <span data-ttu-id="68dde-139">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="68dde-139">TaskStatusInfo</span></span>
<span data-ttu-id="68dde-140">Этот командлет возвращает объект **TaskStatusInfo** , если указан параметр *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="68dde-140">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="68dde-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="68dde-141">NOTES</span></span>

## <span data-ttu-id="68dde-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68dde-142">RELATED LINKS</span></span>

[<span data-ttu-id="68dde-143">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="68dde-143">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="68dde-144">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="68dde-144">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="68dde-145">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="68dde-145">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="68dde-146">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="68dde-146">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


