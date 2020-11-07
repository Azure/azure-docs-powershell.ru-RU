---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
ms.openlocfilehash: d2ce188c9e8c53a0920bea1f0e85a94d9f0d8e3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906997"
---
# <span data-ttu-id="59f3a-101">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="59f3a-101">Stop-AzStorageFileCopy</span></span>

## <span data-ttu-id="59f3a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="59f3a-103">Останавливает операцию копирования в указанном конечном файле.</span><span class="sxs-lookup"><span data-stu-id="59f3a-103">Stops a copy operation to the specified destination file.</span></span>

## <span data-ttu-id="59f3a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59f3a-104">SYNTAX</span></span>

### <span data-ttu-id="59f3a-105">Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="59f3a-105">ShareName</span></span>
```
Stop-AzStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59f3a-106">Файл</span><span class="sxs-lookup"><span data-stu-id="59f3a-106">File</span></span>
```
Stop-AzStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59f3a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59f3a-107">DESCRIPTION</span></span>
<span data-ttu-id="59f3a-108">Командлет **Stop-AzStorageFileCopy** прекращает копирование файла в конечный файл.</span><span class="sxs-lookup"><span data-stu-id="59f3a-108">The **Stop-AzStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="59f3a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59f3a-109">EXAMPLES</span></span>

### <span data-ttu-id="59f3a-110">Пример 1: остановка операции копирования</span><span class="sxs-lookup"><span data-stu-id="59f3a-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="59f3a-111">Эта команда останавливает копирование файла с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="59f3a-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="59f3a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59f3a-112">PARAMETERS</span></span>

### <span data-ttu-id="59f3a-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="59f3a-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="59f3a-114">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="59f3a-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="59f3a-115">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="59f3a-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="59f3a-116">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="59f3a-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f3a-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="59f3a-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="59f3a-118">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="59f3a-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="59f3a-119">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="59f3a-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="59f3a-120">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="59f3a-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="59f3a-121">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="59f3a-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="59f3a-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="59f3a-122">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f3a-123">-Context</span><span class="sxs-lookup"><span data-stu-id="59f3a-123">-Context</span></span>
<span data-ttu-id="59f3a-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="59f3a-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="59f3a-125">Чтобы получить контекст хранения, используйте командлет [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="59f3a-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59f3a-126">-CopyId</span><span class="sxs-lookup"><span data-stu-id="59f3a-126">-CopyId</span></span>
<span data-ttu-id="59f3a-127">Указывает идентификатор операции копирования.</span><span class="sxs-lookup"><span data-stu-id="59f3a-127">Specifies the ID of the copy operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f3a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f3a-128">-DefaultProfile</span></span>
<span data-ttu-id="59f3a-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59f3a-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f3a-130">-Файл</span><span class="sxs-lookup"><span data-stu-id="59f3a-130">-File</span></span>
<span data-ttu-id="59f3a-131">Указывает объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="59f3a-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="59f3a-132">Вы можете создать файл в облаке или получить его с помощью командлета Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="59f3a-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59f3a-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="59f3a-133">-FilePath</span></span>
<span data-ttu-id="59f3a-134">Задает путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="59f3a-134">Specifies the path of a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f3a-135">-Force</span><span class="sxs-lookup"><span data-stu-id="59f3a-135">-Force</span></span>
<span data-ttu-id="59f3a-136">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="59f3a-136">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f3a-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="59f3a-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="59f3a-138">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="59f3a-138">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f3a-139">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="59f3a-139">-ShareName</span></span>
<span data-ttu-id="59f3a-140">Указывает имя общего доступа.</span><span class="sxs-lookup"><span data-stu-id="59f3a-140">Specifies the name of a share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f3a-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59f3a-141">-Confirm</span></span>
<span data-ttu-id="59f3a-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="59f3a-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f3a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59f3a-143">-WhatIf</span></span>
<span data-ttu-id="59f3a-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="59f3a-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59f3a-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="59f3a-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f3a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f3a-146">CommonParameters</span></span>
<span data-ttu-id="59f3a-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59f3a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f3a-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59f3a-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f3a-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59f3a-149">INPUTS</span></span>

### <span data-ttu-id="59f3a-150">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="59f3a-150">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="59f3a-151">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="59f3a-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="59f3a-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59f3a-152">OUTPUTS</span></span>

### <span data-ttu-id="59f3a-153">System. void</span><span class="sxs-lookup"><span data-stu-id="59f3a-153">System.Void</span></span>

## <span data-ttu-id="59f3a-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="59f3a-154">NOTES</span></span>

## <span data-ttu-id="59f3a-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59f3a-155">RELATED LINKS</span></span>

[<span data-ttu-id="59f3a-156">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="59f3a-156">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="59f3a-157">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="59f3a-157">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="59f3a-158">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="59f3a-158">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="59f3a-159">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="59f3a-159">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)
