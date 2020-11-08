---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: ED6CDEA3-0A5D-47E6-B9D7-47D1862212DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: b907627200ec2463d997ebb4faa834e2821b1c7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076210"
---
# <span data-ttu-id="87636-101">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="87636-101">New-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="87636-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87636-102">SYNOPSIS</span></span>
<span data-ttu-id="87636-103">Создание записи управления доступом.</span><span class="sxs-lookup"><span data-stu-id="87636-103">Creates an access control record.</span></span>

## <span data-ttu-id="87636-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87636-104">SYNTAX</span></span>

```
New-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="87636-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87636-105">DESCRIPTION</span></span>
<span data-ttu-id="87636-106">Командлет **New-AzureStorSimpleAccessControlRecord** создает запись управления доступом.</span><span class="sxs-lookup"><span data-stu-id="87636-106">The **New-AzureStorSimpleAccessControlRecord** cmdlet creates an access control record.</span></span>
<span data-ttu-id="87636-107">Для настройки томов можно использовать объект **AccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="87636-107">You can use an **AccessControlRecord** object to configure volumes.</span></span>

## <span data-ttu-id="87636-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87636-108">EXAMPLES</span></span>

### <span data-ttu-id="87636-109">Пример 1: создание записи управления доступом Controlaccess и ожидание элемента управления resultaccess</span><span class="sxs-lookup"><span data-stu-id="87636-109">Example 1: Create an Access Controlaccess control record and wait for the resultaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "Iqn10" -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 08719243-3a76-43a5-a88b-e5f2b63ed3d9
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e12362c2c06615108ba8436cf85fcd40
```

<span data-ttu-id="87636-110">Эта команда создает запись контроля доступа с именем Acr10 для инициатора iSCSI с именем Iqn10.</span><span class="sxs-lookup"><span data-stu-id="87636-110">This command creates an access control record named Acr10 for the iSCSI initiator named Iqn10.</span></span>
<span data-ttu-id="87636-111">Эта команда задает параметр *WaitForComplete* и, следовательно, команда ожидает завершения операции, а затем возвращает объект **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="87636-111">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="87636-112">Пример 2: создание элемента управления Controlaccess доступа RecordAccess</span><span class="sxs-lookup"><span data-stu-id="87636-112">Example 2: Create an Access Controlaccess control recordaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr11" -IQNInitiatorName "Iqn11"
VERBOSE: The create job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
2bd56fbb-4b95-4f2c-b99f-6321231a018d for tracking the job status
```

<span data-ttu-id="87636-113">Эта команда создает запись контроля доступа с именем Acr11 для инициатора iSCSI с именем Iqn11.</span><span class="sxs-lookup"><span data-stu-id="87636-113">This command creates an access control record named Acr11 for the iSCSI initiator named Iqn11.</span></span>
<span data-ttu-id="87636-114">В этой команде не указан параметр *WaitForComplete* и, следовательно, команда запускает задачу, а затем возвращает объект **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="87636-114">This command does not specify the *WaitForComplete* parameter, and, therefore, the command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="87636-115">Чтобы просмотреть состояние задачи, используйте командлет **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="87636-115">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="87636-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87636-116">PARAMETERS</span></span>

### <span data-ttu-id="87636-117">-ACRName</span><span class="sxs-lookup"><span data-stu-id="87636-117">-ACRName</span></span>
<span data-ttu-id="87636-118">Задает имя записи управления доступом.</span><span class="sxs-lookup"><span data-stu-id="87636-118">Specifies a name for the access control record.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87636-119">-IQNInitiatorName</span><span class="sxs-lookup"><span data-stu-id="87636-119">-IQNInitiatorName</span></span>
<span data-ttu-id="87636-120">Задает полное имя iSCSI (IQN) инициатора iSCSI, которому этот командлет предоставляет доступ к тому.</span><span class="sxs-lookup"><span data-stu-id="87636-120">Specifies the iSCSI qualified name (IQN) of the iSCSI initiator to which this cmdlet provides access for the volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IQN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87636-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="87636-121">-Profile</span></span>
<span data-ttu-id="87636-122">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="87636-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="87636-123">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="87636-123">-WaitForComplete</span></span>
<span data-ttu-id="87636-124">Указывает на то, что этот командлет ожидает завершения операции до того, как она возвратит управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="87636-124">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="87636-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87636-125">CommonParameters</span></span>
<span data-ttu-id="87636-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87636-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87636-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87636-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87636-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87636-128">INPUTS</span></span>

### <span data-ttu-id="87636-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="87636-129">None</span></span>

## <span data-ttu-id="87636-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87636-130">OUTPUTS</span></span>

### <span data-ttu-id="87636-131">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="87636-131">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="87636-132">Этот командлет возвращает объект **TaskStatusInfo** , если указан параметр *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="87636-132">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="87636-133">Если этот параметр не указан, функция возвращает объект **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="87636-133">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="87636-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="87636-134">NOTES</span></span>

## <span data-ttu-id="87636-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87636-135">RELATED LINKS</span></span>

[<span data-ttu-id="87636-136">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="87636-136">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="87636-137">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="87636-137">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="87636-138">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="87636-138">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="87636-139">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="87636-139">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


