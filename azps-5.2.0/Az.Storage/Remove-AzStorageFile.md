---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
ms.openlocfilehash: 99809e5115cb256b8e546334efce0e6e399be04f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403460"
---
# <span data-ttu-id="d3141-101">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="d3141-101">Remove-AzStorageFile</span></span>

## <span data-ttu-id="d3141-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3141-102">SYNOPSIS</span></span>
<span data-ttu-id="d3141-103">Удаляет файл.</span><span class="sxs-lookup"><span data-stu-id="d3141-103">Deletes a file.</span></span>

## <span data-ttu-id="d3141-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d3141-104">SYNTAX</span></span>

### <span data-ttu-id="d3141-105">ShareName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d3141-105">ShareName (Default)</span></span>
```
Remove-AzStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3141-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="d3141-106">Share</span></span>
```
Remove-AzStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3141-107">Каталог</span><span class="sxs-lookup"><span data-stu-id="d3141-107">Directory</span></span>
```
Remove-AzStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3141-108">Файл</span><span class="sxs-lookup"><span data-stu-id="d3141-108">File</span></span>
```
Remove-AzStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3141-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3141-109">DESCRIPTION</span></span>
<span data-ttu-id="d3141-110">С **его учетной записью** будет удален файл.</span><span class="sxs-lookup"><span data-stu-id="d3141-110">The **Remove-AzStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="d3141-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d3141-111">EXAMPLES</span></span>

### <span data-ttu-id="d3141-112">Пример 1. Удаление файла из папки</span><span class="sxs-lookup"><span data-stu-id="d3141-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="d3141-113">Эта команда удаляет файл с именем ContosoFile22 из папки ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="d3141-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="d3141-114">Пример 2. Получить файл из папки с помощью объекта файловой папки</span><span class="sxs-lookup"><span data-stu-id="d3141-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | Remove-AzStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="d3141-115">Эта команда использует командлет **Get-AzStorageShare** для получения файловой папки ContosoShare06 и передает этот объект текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="d3141-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d3141-116">Текущая команда удаляет из ContosoShare06 файл с именем ContosoFile22.</span><span class="sxs-lookup"><span data-stu-id="d3141-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="d3141-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3141-117">PARAMETERS</span></span>

### <span data-ttu-id="d3141-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d3141-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d3141-119">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d3141-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d3141-120">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="d3141-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d3141-121">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d3141-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d3141-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d3141-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d3141-123">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="d3141-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d3141-124">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="d3141-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d3141-125">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="d3141-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d3141-126">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="d3141-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d3141-127">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="d3141-127">The default value is 10.</span></span>

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

### <span data-ttu-id="d3141-128">-Контекст</span><span class="sxs-lookup"><span data-stu-id="d3141-128">-Context</span></span>
<span data-ttu-id="d3141-129">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d3141-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d3141-130">Чтобы получить контекст хранилища, воспользуйтесь [cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="d3141-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="d3141-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3141-131">-DefaultProfile</span></span>
<span data-ttu-id="d3141-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3141-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3141-133">-Каталог</span><span class="sxs-lookup"><span data-stu-id="d3141-133">-Directory</span></span>
<span data-ttu-id="d3141-134">Указывает папку как объект **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="d3141-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="d3141-135">Этот cmdlet удаляет файл из папки, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="d3141-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3141-136">-File</span><span class="sxs-lookup"><span data-stu-id="d3141-136">-File</span></span>
<span data-ttu-id="d3141-137">Определяет файл как объект **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="d3141-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="d3141-138">Этот cmdlet удаляет файл, указанный этим параметром.</span><span class="sxs-lookup"><span data-stu-id="d3141-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="d3141-139">Чтобы получить объект **CloudFile,** воспользуйтесь Get-AzStorageFile управления.</span><span class="sxs-lookup"><span data-stu-id="d3141-139">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="d3141-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3141-140">-PassThru</span></span>
<span data-ttu-id="d3141-141">Указывает на то, что этот cmdlet возвращает **boolean,** который отражает успешность операции.</span><span class="sxs-lookup"><span data-stu-id="d3141-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="d3141-142">По умолчанию этот cmdlet не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d3141-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="d3141-143">-Path</span><span class="sxs-lookup"><span data-stu-id="d3141-143">-Path</span></span>
<span data-ttu-id="d3141-144">Путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="d3141-144">Specifies the path of a file.</span></span>
<span data-ttu-id="d3141-145">Этот cmdlet удаляет файл, указанный этим параметром.</span><span class="sxs-lookup"><span data-stu-id="d3141-145">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3141-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d3141-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d3141-147">Определяет продолжительность периода времени ожидания для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="d3141-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="d3141-148">-Share</span><span class="sxs-lookup"><span data-stu-id="d3141-148">-Share</span></span>
<span data-ttu-id="d3141-149">Указывает объект **CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="d3141-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="d3141-150">Этот cmdlet removes the file in the share this parameter specifies.</span><span class="sxs-lookup"><span data-stu-id="d3141-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="d3141-151">Чтобы получить объект **CloudFileShare,** воспользуйтесь Get-AzStorageShare управления.</span><span class="sxs-lookup"><span data-stu-id="d3141-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="d3141-152">Этот объект содержит контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="d3141-152">This object contains the storage context.</span></span>
<span data-ttu-id="d3141-153">Если вы указали этот параметр, не укажите параметр *Context.*</span><span class="sxs-lookup"><span data-stu-id="d3141-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3141-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d3141-154">-ShareName</span></span>
<span data-ttu-id="d3141-155">Имя файловой папки.</span><span class="sxs-lookup"><span data-stu-id="d3141-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="d3141-156">Этот cmdlet removes the file in the share this parameter specifies.</span><span class="sxs-lookup"><span data-stu-id="d3141-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="d3141-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3141-157">-Confirm</span></span>
<span data-ttu-id="d3141-158">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d3141-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3141-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3141-159">-WhatIf</span></span>
<span data-ttu-id="d3141-160">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3141-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3141-161">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d3141-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3141-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3141-162">CommonParameters</span></span>
<span data-ttu-id="d3141-163">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3141-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3141-164">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3141-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3141-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3141-165">INPUTS</span></span>

### <span data-ttu-id="d3141-166">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="d3141-166">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="d3141-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="d3141-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="d3141-168">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="d3141-168">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="d3141-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d3141-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d3141-170">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3141-170">OUTPUTS</span></span>

### <span data-ttu-id="d3141-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="d3141-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="d3141-172">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d3141-172">NOTES</span></span>

## <span data-ttu-id="d3141-173">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3141-173">RELATED LINKS</span></span>

[<span data-ttu-id="d3141-174">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="d3141-174">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="d3141-175">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="d3141-175">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="d3141-176">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d3141-176">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
