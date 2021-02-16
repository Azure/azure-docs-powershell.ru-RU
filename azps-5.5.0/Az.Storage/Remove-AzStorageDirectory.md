---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
ms.openlocfilehash: 3ac8cb302c65fd42fdd699588b71bc1b081cc9d2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229780"
---
# <span data-ttu-id="fa3d7-101">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="fa3d7-101">Remove-AzStorageDirectory</span></span>

## <span data-ttu-id="fa3d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa3d7-102">SYNOPSIS</span></span>
<span data-ttu-id="fa3d7-103">Удаляет каталог.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-103">Deletes a directory.</span></span>

## <span data-ttu-id="fa3d7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fa3d7-104">SYNTAX</span></span>

### <span data-ttu-id="fa3d7-105">ShareName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fa3d7-105">ShareName (Default)</span></span>
```
Remove-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa3d7-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="fa3d7-106">Share</span></span>
```
Remove-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa3d7-107">Каталог</span><span class="sxs-lookup"><span data-stu-id="fa3d7-107">Directory</span></span>
```
Remove-AzStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa3d7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa3d7-108">DESCRIPTION</span></span>
<span data-ttu-id="fa3d7-109">При **этом каталог** удаляется с его учетной записью.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-109">The **Remove-AzStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="fa3d7-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fa3d7-110">EXAMPLES</span></span>

### <span data-ttu-id="fa3d7-111">Пример 1. Удаление папки</span><span class="sxs-lookup"><span data-stu-id="fa3d7-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="fa3d7-112">Эта команда удаляет папку ContosoWorkingFolder из папки ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="fa3d7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa3d7-113">PARAMETERS</span></span>

### <span data-ttu-id="fa3d7-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fa3d7-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fa3d7-115">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fa3d7-116">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fa3d7-117">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fa3d7-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fa3d7-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fa3d7-119">Указывает максимальное число сетевых звонков.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fa3d7-120">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fa3d7-121">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fa3d7-122">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fa3d7-123">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-123">The default value is 10.</span></span>

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

### <span data-ttu-id="fa3d7-124">-Контекст</span><span class="sxs-lookup"><span data-stu-id="fa3d7-124">-Context</span></span>
<span data-ttu-id="fa3d7-125">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fa3d7-126">Чтобы получить контекст хранилища, воспользуйтесь [cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="fa3d7-126">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="fa3d7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa3d7-127">-DefaultProfile</span></span>
<span data-ttu-id="fa3d7-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa3d7-129">-Каталог</span><span class="sxs-lookup"><span data-stu-id="fa3d7-129">-Directory</span></span>
<span data-ttu-id="fa3d7-130">Указывает папку как объект **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="fa3d7-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="fa3d7-131">Этот cmdlet удаляет папку, указанную этим параметром.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="fa3d7-132">Чтобы получить каталог, воспользуйтесь New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-132">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="fa3d7-133">Для получения каталога также можно использовать **cmdlet Get-AzStorageFile.**</span><span class="sxs-lookup"><span data-stu-id="fa3d7-133">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="fa3d7-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa3d7-134">-PassThru</span></span>
<span data-ttu-id="fa3d7-135">Означает, что если этот cmdlet успешно, он возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="fa3d7-136">Если вы указали этот параметр и не сможете сделать это из-за недопустимого значения параметра _Path,_ будет возвращена ошибка.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="fa3d7-137">Если этот параметр не задан, этот cmdlet не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="fa3d7-138">-Path</span><span class="sxs-lookup"><span data-stu-id="fa3d7-138">-Path</span></span>
<span data-ttu-id="fa3d7-139">Путь к папке.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="fa3d7-140">Если эта папка пуста, этот cmdlet удалит ее.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="fa3d7-141">Если папка не пустая, этот cmdlet не вносит никаких изменений и возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa3d7-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fa3d7-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fa3d7-143">Определяет продолжительность периода времени ожидания для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="fa3d7-144">-Share</span><span class="sxs-lookup"><span data-stu-id="fa3d7-144">-Share</span></span>
<span data-ttu-id="fa3d7-145">Указывает объект **CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="fa3d7-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="fa3d7-146">Этот cmdlet удаляет папку под файловой папкой, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="fa3d7-147">Чтобы получить объект **CloudFileShare,** воспользуйтесь Get-AzStorageShare управления.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-147">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="fa3d7-148">Этот объект содержит контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-148">This object contains the storage context.</span></span>
<span data-ttu-id="fa3d7-149">Если вы указали этот параметр, не укажите параметр *Context.*</span><span class="sxs-lookup"><span data-stu-id="fa3d7-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="fa3d7-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="fa3d7-150">-ShareName</span></span>
<span data-ttu-id="fa3d7-151">Имя файловой папки.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="fa3d7-152">Этот cmdlet удаляет папку под файловой папкой, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="fa3d7-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa3d7-153">-Confirm</span></span>
<span data-ttu-id="fa3d7-154">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa3d7-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa3d7-155">-WhatIf</span></span>
<span data-ttu-id="fa3d7-156">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa3d7-157">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa3d7-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa3d7-158">CommonParameters</span></span>
<span data-ttu-id="fa3d7-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa3d7-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa3d7-160">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa3d7-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa3d7-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa3d7-161">INPUTS</span></span>

### <span data-ttu-id="fa3d7-162">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="fa3d7-162">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="fa3d7-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="fa3d7-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="fa3d7-164">System.String</span><span class="sxs-lookup"><span data-stu-id="fa3d7-164">System.String</span></span>

### <span data-ttu-id="fa3d7-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fa3d7-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fa3d7-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fa3d7-166">OUTPUTS</span></span>

### <span data-ttu-id="fa3d7-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="fa3d7-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="fa3d7-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fa3d7-168">NOTES</span></span>

## <span data-ttu-id="fa3d7-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa3d7-169">RELATED LINKS</span></span>

[<span data-ttu-id="fa3d7-170">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="fa3d7-170">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="fa3d7-171">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="fa3d7-171">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="fa3d7-172">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="fa3d7-172">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)
