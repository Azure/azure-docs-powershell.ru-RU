---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
ms.openlocfilehash: ac36914167bd5bda2e79576d9879d6f8c92ba7fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243168"
---
# <span data-ttu-id="7352e-101">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7352e-101">Stop-AzStorageFileCopy</span></span>

## <span data-ttu-id="7352e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7352e-102">SYNOPSIS</span></span>
<span data-ttu-id="7352e-103">Остановка операции копирования в указанный файл назначения.</span><span class="sxs-lookup"><span data-stu-id="7352e-103">Stops a copy operation to the specified destination file.</span></span>

## <span data-ttu-id="7352e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7352e-104">SYNTAX</span></span>

### <span data-ttu-id="7352e-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="7352e-105">ShareName</span></span>
```
Stop-AzStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7352e-106">Файл</span><span class="sxs-lookup"><span data-stu-id="7352e-106">File</span></span>
```
Stop-AzStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7352e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7352e-107">DESCRIPTION</span></span>
<span data-ttu-id="7352e-108">При **этом файл перестает** копироваться в файл назначения.</span><span class="sxs-lookup"><span data-stu-id="7352e-108">The **Stop-AzStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="7352e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7352e-109">EXAMPLES</span></span>

### <span data-ttu-id="7352e-110">Пример 1. Остановка операции копирования</span><span class="sxs-lookup"><span data-stu-id="7352e-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="7352e-111">Эта команда прекращает копирование файла с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="7352e-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="7352e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7352e-112">PARAMETERS</span></span>

### <span data-ttu-id="7352e-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7352e-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7352e-114">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="7352e-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7352e-115">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="7352e-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7352e-116">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="7352e-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7352e-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7352e-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7352e-118">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="7352e-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7352e-119">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="7352e-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7352e-120">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="7352e-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7352e-121">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="7352e-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7352e-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="7352e-122">The default value is 10.</span></span>

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

### <span data-ttu-id="7352e-123">-Контекст</span><span class="sxs-lookup"><span data-stu-id="7352e-123">-Context</span></span>
<span data-ttu-id="7352e-124">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7352e-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7352e-125">Чтобы получить контекст хранилища, воспользуйтесь [cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="7352e-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="7352e-126">-CopyId</span><span class="sxs-lookup"><span data-stu-id="7352e-126">-CopyId</span></span>
<span data-ttu-id="7352e-127">Определяет ИД операции копирования.</span><span class="sxs-lookup"><span data-stu-id="7352e-127">Specifies the ID of the copy operation.</span></span>

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

### <span data-ttu-id="7352e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7352e-128">-DefaultProfile</span></span>
<span data-ttu-id="7352e-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7352e-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7352e-130">-File</span><span class="sxs-lookup"><span data-stu-id="7352e-130">-File</span></span>
<span data-ttu-id="7352e-131">Указывает объект **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="7352e-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="7352e-132">Вы можете создать облачный файл или получить его с помощью Get-AzStorageFile-файла.</span><span class="sxs-lookup"><span data-stu-id="7352e-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7352e-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="7352e-133">-FilePath</span></span>
<span data-ttu-id="7352e-134">Путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="7352e-134">Specifies the path of a file.</span></span>

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

### <span data-ttu-id="7352e-135">-Force</span><span class="sxs-lookup"><span data-stu-id="7352e-135">-Force</span></span>
<span data-ttu-id="7352e-136">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7352e-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7352e-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7352e-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7352e-138">Определяет продолжительность периода времени ожидания для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="7352e-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="7352e-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="7352e-139">-ShareName</span></span>
<span data-ttu-id="7352e-140">Указывает имя поделиться.</span><span class="sxs-lookup"><span data-stu-id="7352e-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="7352e-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7352e-141">-Confirm</span></span>
<span data-ttu-id="7352e-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7352e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7352e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7352e-143">-WhatIf</span></span>
<span data-ttu-id="7352e-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7352e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7352e-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7352e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7352e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7352e-146">CommonParameters</span></span>
<span data-ttu-id="7352e-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7352e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7352e-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7352e-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7352e-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7352e-149">INPUTS</span></span>

### <span data-ttu-id="7352e-150">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="7352e-150">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="7352e-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7352e-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7352e-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7352e-152">OUTPUTS</span></span>

### <span data-ttu-id="7352e-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="7352e-153">System.Void</span></span>

## <span data-ttu-id="7352e-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7352e-154">NOTES</span></span>

## <span data-ttu-id="7352e-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7352e-155">RELATED LINKS</span></span>

[<span data-ttu-id="7352e-156">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="7352e-156">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="7352e-157">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="7352e-157">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="7352e-158">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7352e-158">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="7352e-159">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7352e-159">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)
