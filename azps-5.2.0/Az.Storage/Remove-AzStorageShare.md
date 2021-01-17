---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
ms.openlocfilehash: d51980303d4cb0bcd3ba7ec9e4f976634d37c689
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403439"
---
# <span data-ttu-id="3f546-101">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="3f546-101">Remove-AzStorageShare</span></span>

## <span data-ttu-id="3f546-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f546-102">SYNOPSIS</span></span>
<span data-ttu-id="3f546-103">Удаляет файловую папку.</span><span class="sxs-lookup"><span data-stu-id="3f546-103">Deletes a file share.</span></span>

## <span data-ttu-id="3f546-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3f546-104">SYNTAX</span></span>

### <span data-ttu-id="3f546-105">ShareName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f546-105">ShareName (Default)</span></span>
```
Remove-AzStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f546-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="3f546-106">Share</span></span>
```
Remove-AzStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f546-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f546-107">DESCRIPTION</span></span>
<span data-ttu-id="3f546-108">При **этом удаляется** файловая папка.</span><span class="sxs-lookup"><span data-stu-id="3f546-108">The **Remove-AzStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="3f546-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3f546-109">EXAMPLES</span></span>

### <span data-ttu-id="3f546-110">Пример 1. Удаление файловой папки</span><span class="sxs-lookup"><span data-stu-id="3f546-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="3f546-111">Эта команда удаляет файл с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="3f546-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="3f546-112">Пример 2. Удаление файловой папки и всех ее снимков</span><span class="sxs-lookup"><span data-stu-id="3f546-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="3f546-113">Эта команда удаляет файл с именем ContosoShare06 и все его снимки.</span><span class="sxs-lookup"><span data-stu-id="3f546-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="3f546-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f546-114">PARAMETERS</span></span>

### <span data-ttu-id="3f546-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3f546-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3f546-116">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="3f546-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3f546-117">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="3f546-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3f546-118">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="3f546-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3f546-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3f546-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3f546-120">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="3f546-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3f546-121">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="3f546-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3f546-122">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="3f546-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3f546-123">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="3f546-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3f546-124">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="3f546-124">The default value is 10.</span></span>

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

### <span data-ttu-id="3f546-125">-Контекст</span><span class="sxs-lookup"><span data-stu-id="3f546-125">-Context</span></span>
<span data-ttu-id="3f546-126">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3f546-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3f546-127">Чтобы получить контекст хранилища, воспользуйтесь [cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="3f546-127">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="3f546-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f546-128">-DefaultProfile</span></span>
<span data-ttu-id="3f546-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f546-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f546-130">-Force</span><span class="sxs-lookup"><span data-stu-id="3f546-130">-Force</span></span>
<span data-ttu-id="3f546-131">Принудительно удалите обойму для всех моментальных снимков и всего содержимого.</span><span class="sxs-lookup"><span data-stu-id="3f546-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="3f546-132">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="3f546-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="3f546-133">Удаление файла "Поделиться" со всеми его снимками</span><span class="sxs-lookup"><span data-stu-id="3f546-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="3f546-134">-Name</span><span class="sxs-lookup"><span data-stu-id="3f546-134">-Name</span></span>
<span data-ttu-id="3f546-135">Имя файловой папки.</span><span class="sxs-lookup"><span data-stu-id="3f546-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="3f546-136">Этот cmdlet удаляет файловую папку, указанную этим параметром.</span><span class="sxs-lookup"><span data-stu-id="3f546-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f546-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f546-137">-PassThru</span></span>
<span data-ttu-id="3f546-138">Указывает на то, что этот cmdlet возвращает **boolean,** который отражает успешность операции.</span><span class="sxs-lookup"><span data-stu-id="3f546-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="3f546-139">По умолчанию этот cmdlet не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3f546-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="3f546-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3f546-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3f546-141">Определяет продолжительность периода времени ожидания для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="3f546-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="3f546-142">-Share</span><span class="sxs-lookup"><span data-stu-id="3f546-142">-Share</span></span>
<span data-ttu-id="3f546-143">Указывает объект **CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="3f546-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="3f546-144">Этот cmdlet удаляет объект, указанный этим параметром.</span><span class="sxs-lookup"><span data-stu-id="3f546-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="3f546-145">Чтобы получить объект **CloudFileShare,** воспользуйтесь Get-AzStorageShare управления.</span><span class="sxs-lookup"><span data-stu-id="3f546-145">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="3f546-146">Этот объект содержит контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="3f546-146">This object contains the storage context.</span></span>
<span data-ttu-id="3f546-147">Если вы указали этот параметр, не укажите параметр *Context.*</span><span class="sxs-lookup"><span data-stu-id="3f546-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="3f546-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f546-148">-Confirm</span></span>
<span data-ttu-id="3f546-149">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3f546-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f546-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f546-150">-WhatIf</span></span>
<span data-ttu-id="3f546-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f546-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f546-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3f546-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f546-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f546-153">CommonParameters</span></span>
<span data-ttu-id="3f546-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f546-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f546-155">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f546-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f546-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f546-156">INPUTS</span></span>

### <span data-ttu-id="3f546-157">System.String</span><span class="sxs-lookup"><span data-stu-id="3f546-157">System.String</span></span>

### <span data-ttu-id="3f546-158">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="3f546-158">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="3f546-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3f546-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3f546-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3f546-160">OUTPUTS</span></span>

### <span data-ttu-id="3f546-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="3f546-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="3f546-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3f546-162">NOTES</span></span>

## <span data-ttu-id="3f546-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f546-163">RELATED LINKS</span></span>

[<span data-ttu-id="3f546-164">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="3f546-164">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="3f546-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3f546-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="3f546-166">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="3f546-166">New-AzStorageShare</span></span>](./New-AzStorageShare.md)
