---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: ''
schema: 2.0.0
ms.openlocfilehash: f92144b5cf5ffba1c470acf15c1c0145ebcc753f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555552"
---
# <span data-ttu-id="c43dd-101">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c43dd-101">Stop-AzureStorageFileCopy</span></span>

## <span data-ttu-id="c43dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c43dd-102">SYNOPSIS</span></span>
<span data-ttu-id="c43dd-103">Останавливает операцию копирования в указанном конечном файле.</span><span class="sxs-lookup"><span data-stu-id="c43dd-103">Stops a copy operation to the specified destination file.</span></span>

## <span data-ttu-id="c43dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c43dd-104">SYNTAX</span></span>

### <span data-ttu-id="c43dd-105">Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="c43dd-105">ShareName</span></span>
```
Stop-AzureStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c43dd-106">Файл</span><span class="sxs-lookup"><span data-stu-id="c43dd-106">File</span></span>
```
Stop-AzureStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c43dd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c43dd-107">DESCRIPTION</span></span>
<span data-ttu-id="c43dd-108">Командлет **Stop-AzureStorageFileCopy** прекращает копирование файла в конечный файл.</span><span class="sxs-lookup"><span data-stu-id="c43dd-108">The **Stop-AzureStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="c43dd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c43dd-109">EXAMPLES</span></span>

### <span data-ttu-id="c43dd-110">Пример 1: остановка операции копирования</span><span class="sxs-lookup"><span data-stu-id="c43dd-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzureStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="c43dd-111">Эта команда останавливает копирование файла с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="c43dd-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="c43dd-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c43dd-112">PARAMETERS</span></span>

### <span data-ttu-id="c43dd-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c43dd-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c43dd-114">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="c43dd-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c43dd-115">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="c43dd-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c43dd-116">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c43dd-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c43dd-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c43dd-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c43dd-118">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="c43dd-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c43dd-119">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="c43dd-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c43dd-120">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="c43dd-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c43dd-121">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="c43dd-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c43dd-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="c43dd-122">The default value is 10.</span></span>

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

### <span data-ttu-id="c43dd-123">-Context</span><span class="sxs-lookup"><span data-stu-id="c43dd-123">-Context</span></span>
<span data-ttu-id="c43dd-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c43dd-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c43dd-125">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="c43dd-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="c43dd-126">-CopyId</span><span class="sxs-lookup"><span data-stu-id="c43dd-126">-CopyId</span></span>
<span data-ttu-id="c43dd-127">Указывает идентификатор операции копирования.</span><span class="sxs-lookup"><span data-stu-id="c43dd-127">Specifies the ID of the copy operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c43dd-128">-Файл</span><span class="sxs-lookup"><span data-stu-id="c43dd-128">-File</span></span>
<span data-ttu-id="c43dd-129">Указывает объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="c43dd-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="c43dd-130">Вы можете создать файл в облаке или получить его с помощью командлета Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="c43dd-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="c43dd-131">-FilePath</span><span class="sxs-lookup"><span data-stu-id="c43dd-131">-FilePath</span></span>
<span data-ttu-id="c43dd-132">Задает путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="c43dd-132">Specifies the path of a file.</span></span>

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

### <span data-ttu-id="c43dd-133">-Force</span><span class="sxs-lookup"><span data-stu-id="c43dd-133">-Force</span></span>
<span data-ttu-id="c43dd-134">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c43dd-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c43dd-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c43dd-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c43dd-136">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="c43dd-136">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c43dd-137">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="c43dd-137">-ShareName</span></span>
<span data-ttu-id="c43dd-138">Указывает имя общего доступа.</span><span class="sxs-lookup"><span data-stu-id="c43dd-138">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="c43dd-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c43dd-139">-Confirm</span></span>
<span data-ttu-id="c43dd-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c43dd-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c43dd-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c43dd-141">-WhatIf</span></span>
<span data-ttu-id="c43dd-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c43dd-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c43dd-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c43dd-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c43dd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c43dd-144">CommonParameters</span></span>
<span data-ttu-id="c43dd-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c43dd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c43dd-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c43dd-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c43dd-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c43dd-147">INPUTS</span></span>

## <span data-ttu-id="c43dd-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c43dd-148">OUTPUTS</span></span>

## <span data-ttu-id="c43dd-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="c43dd-149">NOTES</span></span>

## <span data-ttu-id="c43dd-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c43dd-150">RELATED LINKS</span></span>

[<span data-ttu-id="c43dd-151">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="c43dd-151">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="c43dd-152">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="c43dd-152">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="c43dd-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c43dd-153">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="c43dd-154">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c43dd-154">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)
