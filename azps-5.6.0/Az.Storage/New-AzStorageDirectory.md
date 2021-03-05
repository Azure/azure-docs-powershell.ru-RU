---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
ms.openlocfilehash: 6f44f1545eea4e515064873cdc77f8b34819fabc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002472"
---
# <span data-ttu-id="c30b0-101">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="c30b0-101">New-AzStorageDirectory</span></span>

## <span data-ttu-id="c30b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c30b0-102">SYNOPSIS</span></span>
<span data-ttu-id="c30b0-103">Создает каталог.</span><span class="sxs-lookup"><span data-stu-id="c30b0-103">Creates a directory.</span></span>

## <span data-ttu-id="c30b0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c30b0-104">SYNTAX</span></span>

### <span data-ttu-id="c30b0-105">ShareName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c30b0-105">ShareName (Default)</span></span>
```
New-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c30b0-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="c30b0-106">Share</span></span>
```
New-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="c30b0-107">Каталог</span><span class="sxs-lookup"><span data-stu-id="c30b0-107">Directory</span></span>
```
New-AzStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="c30b0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c30b0-108">DESCRIPTION</span></span>
<span data-ttu-id="c30b0-109">**Новый-AzStorageDirectory создает** каталог.</span><span class="sxs-lookup"><span data-stu-id="c30b0-109">The **New-AzStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="c30b0-110">Этот cmdlet возвращает объект **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="c30b0-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="c30b0-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c30b0-111">EXAMPLES</span></span>

### <span data-ttu-id="c30b0-112">Пример 1. Создание папки в файловой папке</span><span class="sxs-lookup"><span data-stu-id="c30b0-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="c30b0-113">Эта команда создает папку с именем ContosoWorkingFolder в папке с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="c30b0-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="c30b0-114">Пример 2. Создание папки в папке, заданной в объекте файловой папки</span><span class="sxs-lookup"><span data-stu-id="c30b0-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | New-AzStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="c30b0-115">Эта команда использует командлет **Get-AzStorageShare** для получения файловой папки ContosoShare06 и передает ее текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="c30b0-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c30b0-116">Текущий командлет создает папку ContosoWorkingFolder в ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="c30b0-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="c30b0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c30b0-117">PARAMETERS</span></span>

### <span data-ttu-id="c30b0-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c30b0-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c30b0-119">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="c30b0-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c30b0-120">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="c30b0-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c30b0-121">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c30b0-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c30b0-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c30b0-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c30b0-123">Указывает максимальное число сетевых звонков.</span><span class="sxs-lookup"><span data-stu-id="c30b0-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c30b0-124">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="c30b0-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c30b0-125">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="c30b0-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c30b0-126">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="c30b0-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c30b0-127">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="c30b0-127">The default value is 10.</span></span>

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

### <span data-ttu-id="c30b0-128">-Контекст</span><span class="sxs-lookup"><span data-stu-id="c30b0-128">-Context</span></span>
<span data-ttu-id="c30b0-129">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c30b0-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c30b0-130">Чтобы получить контекст хранилища, воспользуйтесь [cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="c30b0-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="c30b0-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c30b0-131">-DefaultProfile</span></span>
<span data-ttu-id="c30b0-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c30b0-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c30b0-133">-Каталог</span><span class="sxs-lookup"><span data-stu-id="c30b0-133">-Directory</span></span>
<span data-ttu-id="c30b0-134">Указывает папку как объект **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="c30b0-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="c30b0-135">Этот cmdlet создает папку в расположении, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="c30b0-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="c30b0-136">Чтобы получить каталог, воспользуйтесь New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="c30b0-136">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="c30b0-137">Для получения каталога Get-AzStorageFile можно также воспользоваться этим Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="c30b0-137">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="c30b0-138">-Path</span><span class="sxs-lookup"><span data-stu-id="c30b0-138">-Path</span></span>
<span data-ttu-id="c30b0-139">Путь к папке.</span><span class="sxs-lookup"><span data-stu-id="c30b0-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="c30b0-140">Этот cmdlet создает папку для пути, указанного этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c30b0-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c30b0-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c30b0-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c30b0-142">Определяет продолжительность периода времени ожидания для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="c30b0-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c30b0-143">-Share</span><span class="sxs-lookup"><span data-stu-id="c30b0-143">-Share</span></span>
<span data-ttu-id="c30b0-144">Указывает объект **CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="c30b0-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="c30b0-145">Этот cmdlet создает папку в файловой папке, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="c30b0-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="c30b0-146">Чтобы получить объект **CloudFileShare,** воспользуйтесь Get-AzStorageShare управления.</span><span class="sxs-lookup"><span data-stu-id="c30b0-146">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="c30b0-147">Этот объект содержит контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="c30b0-147">This object contains the storage context.</span></span>
<span data-ttu-id="c30b0-148">Если вы указали этот параметр, не укажите параметр *Context.*</span><span class="sxs-lookup"><span data-stu-id="c30b0-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="c30b0-149">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c30b0-149">-ShareName</span></span>
<span data-ttu-id="c30b0-150">Имя файловой папки.</span><span class="sxs-lookup"><span data-stu-id="c30b0-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="c30b0-151">Этот cmdlet создает папку в файловой папке, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="c30b0-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="c30b0-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c30b0-152">CommonParameters</span></span>
<span data-ttu-id="c30b0-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c30b0-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c30b0-154">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c30b0-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c30b0-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c30b0-155">INPUTS</span></span>

### <span data-ttu-id="c30b0-156">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="c30b0-156">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="c30b0-157">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="c30b0-157">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="c30b0-158">System.String</span><span class="sxs-lookup"><span data-stu-id="c30b0-158">System.String</span></span>

### <span data-ttu-id="c30b0-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c30b0-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c30b0-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c30b0-160">OUTPUTS</span></span>

### <span data-ttu-id="c30b0-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="c30b0-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="c30b0-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c30b0-162">NOTES</span></span>

## <span data-ttu-id="c30b0-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c30b0-163">RELATED LINKS</span></span>

[<span data-ttu-id="c30b0-164">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="c30b0-164">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="c30b0-165">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="c30b0-165">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="c30b0-166">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c30b0-166">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="c30b0-167">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="c30b0-167">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="c30b0-168">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="c30b0-168">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)
