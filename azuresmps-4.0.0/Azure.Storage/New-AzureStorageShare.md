---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: ''
schema: 2.0.0
ms.openlocfilehash: 381bfc62ed3a80b650b61b11790a87658a75ee9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555799"
---
# <span data-ttu-id="dc67e-101">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="dc67e-101">New-AzureStorageShare</span></span>

## <span data-ttu-id="dc67e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc67e-102">SYNOPSIS</span></span>
<span data-ttu-id="dc67e-103">Создание общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="dc67e-103">Creates a file share.</span></span>

## <span data-ttu-id="dc67e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc67e-104">SYNTAX</span></span>

```
New-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="dc67e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc67e-105">DESCRIPTION</span></span>
<span data-ttu-id="dc67e-106">Командлет **New-AzureStorageShare** создает общую файловую панель.</span><span class="sxs-lookup"><span data-stu-id="dc67e-106">The **New-AzureStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="dc67e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc67e-107">EXAMPLES</span></span>

### <span data-ttu-id="dc67e-108">Пример 1: создание общего файлового файла</span><span class="sxs-lookup"><span data-stu-id="dc67e-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="dc67e-109">Эта команда создает общую файловую папке с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="dc67e-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="dc67e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc67e-110">PARAMETERS</span></span>

### <span data-ttu-id="dc67e-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dc67e-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="dc67e-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="dc67e-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="dc67e-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="dc67e-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="dc67e-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="dc67e-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="dc67e-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="dc67e-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="dc67e-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="dc67e-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="dc67e-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="dc67e-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="dc67e-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="dc67e-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="dc67e-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="dc67e-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="dc67e-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="dc67e-120">The default value is 10.</span></span>

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

### <span data-ttu-id="dc67e-121">-Context</span><span class="sxs-lookup"><span data-stu-id="dc67e-121">-Context</span></span>
<span data-ttu-id="dc67e-122">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="dc67e-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="dc67e-123">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="dc67e-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="dc67e-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc67e-124">-Name</span></span>
<span data-ttu-id="dc67e-125">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="dc67e-125">Specifies the name of a file share.</span></span>
<span data-ttu-id="dc67e-126">Этот командлет создает общую файловую панель с именем, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="dc67e-126">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="dc67e-127">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dc67e-127">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="dc67e-128">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="dc67e-128">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="dc67e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc67e-129">CommonParameters</span></span>
<span data-ttu-id="dc67e-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc67e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc67e-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc67e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc67e-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc67e-132">INPUTS</span></span>

## <span data-ttu-id="dc67e-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc67e-133">OUTPUTS</span></span>

## <span data-ttu-id="dc67e-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc67e-134">NOTES</span></span>

## <span data-ttu-id="dc67e-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc67e-135">RELATED LINKS</span></span>

[<span data-ttu-id="dc67e-136">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="dc67e-136">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="dc67e-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="dc67e-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="dc67e-138">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="dc67e-138">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
