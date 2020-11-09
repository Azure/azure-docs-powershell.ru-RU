---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
ms.openlocfilehash: 4fa89a13f9b4124232d9459d7d3eff54a6f55a5c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249352"
---
# <span data-ttu-id="4e678-101">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="4e678-101">New-AzStorageShare</span></span>

## <span data-ttu-id="4e678-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e678-102">SYNOPSIS</span></span>
<span data-ttu-id="4e678-103">Создание общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="4e678-103">Creates a file share.</span></span>

## <span data-ttu-id="4e678-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e678-104">SYNTAX</span></span>

```
New-AzStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e678-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e678-105">DESCRIPTION</span></span>
<span data-ttu-id="4e678-106">Командлет **New-AzStorageShare** создает общую файловую панель.</span><span class="sxs-lookup"><span data-stu-id="4e678-106">The **New-AzStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="4e678-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e678-107">EXAMPLES</span></span>

### <span data-ttu-id="4e678-108">Пример 1: создание общего файлового файла</span><span class="sxs-lookup"><span data-stu-id="4e678-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="4e678-109">Эта команда создает общую файловую папке с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="4e678-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="4e678-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e678-110">PARAMETERS</span></span>

### <span data-ttu-id="4e678-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4e678-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4e678-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="4e678-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4e678-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="4e678-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4e678-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="4e678-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4e678-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4e678-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4e678-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="4e678-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4e678-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="4e678-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4e678-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="4e678-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4e678-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="4e678-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4e678-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="4e678-120">The default value is 10.</span></span>

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

### <span data-ttu-id="4e678-121">-Context</span><span class="sxs-lookup"><span data-stu-id="4e678-121">-Context</span></span>
<span data-ttu-id="4e678-122">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4e678-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4e678-123">Чтобы получить контекст хранения, используйте командлет [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="4e678-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e678-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e678-124">-DefaultProfile</span></span>
<span data-ttu-id="4e678-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e678-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e678-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e678-126">-Name</span></span>
<span data-ttu-id="4e678-127">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="4e678-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="4e678-128">Этот командлет создает общую файловую панель с именем, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4e678-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e678-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4e678-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4e678-130">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="4e678-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4e678-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e678-131">CommonParameters</span></span>
<span data-ttu-id="4e678-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e678-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e678-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e678-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e678-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e678-134">INPUTS</span></span>

### <span data-ttu-id="4e678-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4e678-135">System.String</span></span>

### <span data-ttu-id="4e678-136">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4e678-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4e678-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e678-137">OUTPUTS</span></span>

### <span data-ttu-id="4e678-138">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="4e678-138">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="4e678-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e678-139">NOTES</span></span>

## <span data-ttu-id="4e678-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e678-140">RELATED LINKS</span></span>

[<span data-ttu-id="4e678-141">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="4e678-141">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="4e678-142">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4e678-142">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="4e678-143">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="4e678-143">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)