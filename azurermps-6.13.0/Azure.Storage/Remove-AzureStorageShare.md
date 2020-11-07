---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
ms.openlocfilehash: 43a1a18675a662e30e88dd2d96f2fc901ffab8dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733523"
---
# <span data-ttu-id="875ab-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="875ab-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="875ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="875ab-102">SYNOPSIS</span></span>
<span data-ttu-id="875ab-103">Удаление общей папке.</span><span class="sxs-lookup"><span data-stu-id="875ab-103">Deletes a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="875ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="875ab-104">SYNTAX</span></span>

### <span data-ttu-id="875ab-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="875ab-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="875ab-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="875ab-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="875ab-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="875ab-107">DESCRIPTION</span></span>
<span data-ttu-id="875ab-108">Командлет **Remove-AzureStorageShare** удаляет общую файловую панель.</span><span class="sxs-lookup"><span data-stu-id="875ab-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="875ab-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="875ab-109">EXAMPLES</span></span>

### <span data-ttu-id="875ab-110">Пример 1: Удаление общей сетевой папке</span><span class="sxs-lookup"><span data-stu-id="875ab-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="875ab-111">Эта команда удаляет общую файловую панель с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="875ab-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="875ab-112">Пример 2: Удаление общей файловой и всех ее снимков</span><span class="sxs-lookup"><span data-stu-id="875ab-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="875ab-113">Эта команда удаляет общую папке с именем ContosoShare06 и всех ее снимков.</span><span class="sxs-lookup"><span data-stu-id="875ab-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="875ab-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="875ab-114">PARAMETERS</span></span>

### <span data-ttu-id="875ab-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="875ab-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="875ab-116">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="875ab-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="875ab-117">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="875ab-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="875ab-118">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="875ab-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="875ab-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="875ab-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="875ab-120">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="875ab-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="875ab-121">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="875ab-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="875ab-122">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="875ab-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="875ab-123">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="875ab-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="875ab-124">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="875ab-124">The default value is 10.</span></span>

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

### <span data-ttu-id="875ab-125">-Context</span><span class="sxs-lookup"><span data-stu-id="875ab-125">-Context</span></span>
<span data-ttu-id="875ab-126">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="875ab-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="875ab-127">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="875ab-127">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="875ab-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="875ab-128">-DefaultProfile</span></span>
<span data-ttu-id="875ab-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="875ab-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="875ab-130">-Force</span><span class="sxs-lookup"><span data-stu-id="875ab-130">-Force</span></span>
<span data-ttu-id="875ab-131">Принудительное удаление общего доступа ко всем его снимкам и всего содержимого.</span><span class="sxs-lookup"><span data-stu-id="875ab-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="875ab-132">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="875ab-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="875ab-133">Удаление общего доступа к файлам со всеми моментальными снимками</span><span class="sxs-lookup"><span data-stu-id="875ab-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="875ab-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="875ab-134">-Name</span></span>
<span data-ttu-id="875ab-135">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="875ab-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="875ab-136">Этот командлет удаляет общую файловую панель, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="875ab-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="875ab-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="875ab-137">-PassThru</span></span>
<span data-ttu-id="875ab-138">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="875ab-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="875ab-139">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="875ab-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="875ab-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="875ab-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="875ab-141">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="875ab-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="875ab-142">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="875ab-142">-Share</span></span>
<span data-ttu-id="875ab-143">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="875ab-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="875ab-144">Этот командлет удаляет объект, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="875ab-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="875ab-145">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="875ab-145">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="875ab-146">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="875ab-146">This object contains the storage context.</span></span>
<span data-ttu-id="875ab-147">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="875ab-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="875ab-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="875ab-148">-Confirm</span></span>
<span data-ttu-id="875ab-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="875ab-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="875ab-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="875ab-150">-WhatIf</span></span>
<span data-ttu-id="875ab-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="875ab-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="875ab-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="875ab-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="875ab-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="875ab-153">CommonParameters</span></span>
<span data-ttu-id="875ab-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="875ab-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="875ab-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="875ab-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="875ab-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="875ab-156">INPUTS</span></span>

### <span data-ttu-id="875ab-157">System. String</span><span class="sxs-lookup"><span data-stu-id="875ab-157">System.String</span></span>

### <span data-ttu-id="875ab-158">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="875ab-158">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="875ab-159">Параметры: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="875ab-159">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="875ab-160">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="875ab-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="875ab-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="875ab-161">OUTPUTS</span></span>

### <span data-ttu-id="875ab-162">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="875ab-162">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="875ab-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="875ab-163">NOTES</span></span>

## <span data-ttu-id="875ab-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="875ab-164">RELATED LINKS</span></span>

[<span data-ttu-id="875ab-165">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="875ab-165">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="875ab-166">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="875ab-166">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="875ab-167">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="875ab-167">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
