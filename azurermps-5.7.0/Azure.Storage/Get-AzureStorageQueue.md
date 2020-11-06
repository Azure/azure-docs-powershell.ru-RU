---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
ms.openlocfilehash: f8c419f59c05b2160ef02fbf239ecc2815bf1109
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565094"
---
# <span data-ttu-id="156ca-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="156ca-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="156ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="156ca-102">SYNOPSIS</span></span>
<span data-ttu-id="156ca-103">Выводит список очередей хранилища.</span><span class="sxs-lookup"><span data-stu-id="156ca-103">Lists storage queues.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="156ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="156ca-104">SYNTAX</span></span>

### <span data-ttu-id="156ca-105">QueueName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="156ca-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="156ca-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="156ca-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="156ca-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="156ca-107">DESCRIPTION</span></span>
<span data-ttu-id="156ca-108">Командлет **Get-AzureStorageQueue** перечисляет очереди хранения, связанные с учетной записью хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="156ca-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="156ca-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="156ca-109">EXAMPLES</span></span>

### <span data-ttu-id="156ca-110">Пример 1: список всех очередей хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="156ca-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="156ca-111">Эта команда возвращает список всех очередей хранилища для текущей учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="156ca-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="156ca-112">Пример 2: список очередей хранилища Azure с использованием подстановочных знаков</span><span class="sxs-lookup"><span data-stu-id="156ca-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="156ca-113">Эта команда использует подстановочный знак для получения списка очередей хранилища, имя которого начинается с очереди.</span><span class="sxs-lookup"><span data-stu-id="156ca-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="156ca-114">Пример 3: список очередей хранилища Azure с использованием префикса имени очереди</span><span class="sxs-lookup"><span data-stu-id="156ca-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="156ca-115">В этом примере используется параметр *prefix* для получения списка очередей хранилища, имена которых начинаются с очереди.</span><span class="sxs-lookup"><span data-stu-id="156ca-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="156ca-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="156ca-116">PARAMETERS</span></span>

### <span data-ttu-id="156ca-117">-Context</span><span class="sxs-lookup"><span data-stu-id="156ca-117">-Context</span></span>
<span data-ttu-id="156ca-118">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="156ca-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="156ca-119">Вы можете создать его с помощью командлета **New-AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="156ca-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="156ca-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="156ca-120">-Name</span></span>
<span data-ttu-id="156ca-121">Задает имя.</span><span class="sxs-lookup"><span data-stu-id="156ca-121">Specifies a name.</span></span>
<span data-ttu-id="156ca-122">Если имя не указано, командлет возвращает список всех очередей.</span><span class="sxs-lookup"><span data-stu-id="156ca-122">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="156ca-123">Если указано полное или частичное имя, командлет получает все очереди, соответствующие шаблону имени.</span><span class="sxs-lookup"><span data-stu-id="156ca-123">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="156ca-124">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="156ca-124">-Prefix</span></span>
<span data-ttu-id="156ca-125">Задает префикс, используемый в именах очередей, которые вы хотите получить.</span><span class="sxs-lookup"><span data-stu-id="156ca-125">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: String
Parameter Sets: QueuePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="156ca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="156ca-126">CommonParameters</span></span>
<span data-ttu-id="156ca-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="156ca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="156ca-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="156ca-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="156ca-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="156ca-129">INPUTS</span></span>

### <span data-ttu-id="156ca-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="156ca-130">IStorageContext</span></span>

<span data-ttu-id="156ca-131">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="156ca-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="156ca-132">Подстрок</span><span class="sxs-lookup"><span data-stu-id="156ca-132">String</span></span>

<span data-ttu-id="156ca-133">Параметр Name принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="156ca-133">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="156ca-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="156ca-134">OUTPUTS</span></span>

### <span data-ttu-id="156ca-135">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="156ca-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="156ca-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="156ca-136">NOTES</span></span>

## <span data-ttu-id="156ca-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="156ca-137">RELATED LINKS</span></span>

[<span data-ttu-id="156ca-138">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="156ca-138">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="156ca-139">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="156ca-139">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


