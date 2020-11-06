---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: a1be5816427ac1aa91b9daa98701abaec044c20f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570168"
---
# <span data-ttu-id="cb9ae-101">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="cb9ae-101">New-AzureStorageShare</span></span>

## <span data-ttu-id="cb9ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="cb9ae-103">Создание общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="cb9ae-103">Creates a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb9ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb9ae-104">SYNTAX</span></span>

```
New-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="cb9ae-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb9ae-105">DESCRIPTION</span></span>
<span data-ttu-id="cb9ae-106">Командлет **New-AzureStorageShare** создает общую файловую панель.</span><span class="sxs-lookup"><span data-stu-id="cb9ae-106">The **New-AzureStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="cb9ae-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb9ae-107">EXAMPLES</span></span>

### <span data-ttu-id="cb9ae-108">Пример 1: создание общего файлового файла</span><span class="sxs-lookup"><span data-stu-id="cb9ae-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="cb9ae-109">Эта команда создает общую файловую папке с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="cb9ae-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="cb9ae-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb9ae-110">PARAMETERS</span></span>

### <span data-ttu-id="cb9ae-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cb9ae-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cb9ae-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="cb9ae-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cb9ae-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="cb9ae-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cb9ae-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="cb9ae-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb9ae-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cb9ae-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cb9ae-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="cb9ae-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cb9ae-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="cb9ae-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cb9ae-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="cb9ae-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cb9ae-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="cb9ae-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cb9ae-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="cb9ae-120">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb9ae-121">-Context</span><span class="sxs-lookup"><span data-stu-id="cb9ae-121">-Context</span></span>
<span data-ttu-id="cb9ae-122">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="cb9ae-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cb9ae-123">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="cb9ae-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="cb9ae-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cb9ae-124">-Name</span></span>
<span data-ttu-id="cb9ae-125">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="cb9ae-125">Specifies the name of a file share.</span></span>
<span data-ttu-id="cb9ae-126">Этот командлет создает общую файловую панель с именем, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="cb9ae-126">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb9ae-127">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cb9ae-127">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cb9ae-128">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="cb9ae-128">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb9ae-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9ae-129">CommonParameters</span></span>
<span data-ttu-id="cb9ae-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb9ae-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9ae-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb9ae-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9ae-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb9ae-132">INPUTS</span></span>

### <span data-ttu-id="cb9ae-133">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cb9ae-133">IStorageContext</span></span>

<span data-ttu-id="cb9ae-134">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="cb9ae-134">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="cb9ae-135">Подстрок</span><span class="sxs-lookup"><span data-stu-id="cb9ae-135">String</span></span>

<span data-ttu-id="cb9ae-136">Параметр Name принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="cb9ae-136">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="cb9ae-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb9ae-137">OUTPUTS</span></span>

## <span data-ttu-id="cb9ae-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb9ae-138">NOTES</span></span>

## <span data-ttu-id="cb9ae-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb9ae-139">RELATED LINKS</span></span>

[<span data-ttu-id="cb9ae-140">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="cb9ae-140">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="cb9ae-141">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="cb9ae-141">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="cb9ae-142">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="cb9ae-142">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
