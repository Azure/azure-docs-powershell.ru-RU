---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75e94fe8270287410902b215ec4e33ac9cd51624
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556256"
---
# <span data-ttu-id="91e4e-101">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="91e4e-101">Get-AzureStorageFileCopyState</span></span>

## <span data-ttu-id="91e4e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="91e4e-103">Получает состояние операции копирования.</span><span class="sxs-lookup"><span data-stu-id="91e4e-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="91e4e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91e4e-104">SYNTAX</span></span>

### <span data-ttu-id="91e4e-105">Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="91e4e-105">ShareName</span></span>
```
Get-AzureStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="91e4e-106">Файл</span><span class="sxs-lookup"><span data-stu-id="91e4e-106">File</span></span>
```
Get-AzureStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="91e4e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91e4e-107">DESCRIPTION</span></span>
<span data-ttu-id="91e4e-108">Командлет **Get-AzureStorageFileCopyState** получает состояние операции копирования файлов в хранилище Azure.</span><span class="sxs-lookup"><span data-stu-id="91e4e-108">The **Get-AzureStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="91e4e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91e4e-109">EXAMPLES</span></span>

### <span data-ttu-id="91e4e-110">Пример 1: получение состояния копии по имени файла</span><span class="sxs-lookup"><span data-stu-id="91e4e-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzureStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="91e4e-111">Эта команда возвращает состояние операции копирования для файла с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="91e4e-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="91e4e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91e4e-112">PARAMETERS</span></span>

### <span data-ttu-id="91e4e-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="91e4e-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="91e4e-114">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="91e4e-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="91e4e-115">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="91e4e-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="91e4e-116">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="91e4e-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="91e4e-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="91e4e-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="91e4e-118">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="91e4e-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="91e4e-119">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="91e4e-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="91e4e-120">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="91e4e-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="91e4e-121">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="91e4e-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="91e4e-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="91e4e-122">The default value is 10.</span></span>

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

### <span data-ttu-id="91e4e-123">-Context</span><span class="sxs-lookup"><span data-stu-id="91e4e-123">-Context</span></span>
<span data-ttu-id="91e4e-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="91e4e-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="91e4e-125">Чтобы получить контекст, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="91e4e-125">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91e4e-126">-Файл</span><span class="sxs-lookup"><span data-stu-id="91e4e-126">-File</span></span>
<span data-ttu-id="91e4e-127">Указывает объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="91e4e-127">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="91e4e-128">Вы можете создать файл в облаке или получить его с помощью командлета Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="91e4e-128">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91e4e-129">-FilePath</span><span class="sxs-lookup"><span data-stu-id="91e4e-129">-FilePath</span></span>
<span data-ttu-id="91e4e-130">Задает путь к файлу относительно общего доступа к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="91e4e-130">Specifies the path of the file relative to an Azure Storage share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91e4e-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="91e4e-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="91e4e-132">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="91e4e-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="91e4e-133">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="91e4e-133">-ShareName</span></span>
<span data-ttu-id="91e4e-134">Указывает имя общего доступа.</span><span class="sxs-lookup"><span data-stu-id="91e4e-134">Specifies the name of a share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91e4e-135">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="91e4e-135">-WaitForComplete</span></span>
<span data-ttu-id="91e4e-136">Указывает на то, что этот командлет ожидает завершения копирования.</span><span class="sxs-lookup"><span data-stu-id="91e4e-136">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="91e4e-137">Если этот параметр не указан, этот командлет возвращает результат немедленно.</span><span class="sxs-lookup"><span data-stu-id="91e4e-137">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="91e4e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e4e-138">CommonParameters</span></span>
<span data-ttu-id="91e4e-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91e4e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e4e-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91e4e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e4e-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91e4e-141">INPUTS</span></span>

## <span data-ttu-id="91e4e-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91e4e-142">OUTPUTS</span></span>

## <span data-ttu-id="91e4e-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="91e4e-143">NOTES</span></span>

## <span data-ttu-id="91e4e-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91e4e-144">RELATED LINKS</span></span>

[<span data-ttu-id="91e4e-145">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="91e4e-145">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="91e4e-146">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="91e4e-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="91e4e-147">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="91e4e-147">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)

[<span data-ttu-id="91e4e-148">Остановить-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="91e4e-148">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
