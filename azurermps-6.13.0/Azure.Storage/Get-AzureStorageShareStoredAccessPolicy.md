---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 247de1e6c93f8f581f6e34beb778b079d6c9987e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732332"
---
# <span data-ttu-id="39ae6-101">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="39ae6-101">Get-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="39ae6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="39ae6-102">SYNOPSIS</span></span>
<span data-ttu-id="39ae6-103">Получает хранимые политики доступа для общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="39ae6-103">Gets stored access policies for a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39ae6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="39ae6-104">SYNTAX</span></span>

```
Get-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="39ae6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39ae6-105">DESCRIPTION</span></span>
<span data-ttu-id="39ae6-106">Командлет **Get-AzureStorageShareStoredAccessPolicy** получает хранимые политики доступа для общего доступа к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="39ae6-106">The **Get-AzureStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="39ae6-107">Чтобы получить определенную политику, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="39ae6-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="39ae6-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="39ae6-108">EXAMPLES</span></span>

### <span data-ttu-id="39ae6-109">Пример 1: получение политики доступа с сохранением в общем доступе</span><span class="sxs-lookup"><span data-stu-id="39ae6-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="39ae6-110">Эта команда получает сохраненную политику доступа с именем GeneralPolicy в ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="39ae6-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="39ae6-111">Пример 2: получение всех политик доступа для хранения в общем доступе</span><span class="sxs-lookup"><span data-stu-id="39ae6-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="39ae6-112">Эта команда получает все политики для сохраненного доступа в ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="39ae6-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="39ae6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="39ae6-113">PARAMETERS</span></span>

### <span data-ttu-id="39ae6-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="39ae6-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="39ae6-115">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="39ae6-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="39ae6-116">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="39ae6-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="39ae6-117">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="39ae6-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="39ae6-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="39ae6-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="39ae6-119">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="39ae6-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="39ae6-120">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="39ae6-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="39ae6-121">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="39ae6-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="39ae6-122">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="39ae6-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="39ae6-123">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="39ae6-123">The default value is 10.</span></span>

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

### <span data-ttu-id="39ae6-124">-Context</span><span class="sxs-lookup"><span data-stu-id="39ae6-124">-Context</span></span>
<span data-ttu-id="39ae6-125">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="39ae6-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="39ae6-126">Чтобы получить контекст, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="39ae6-126">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="39ae6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39ae6-127">-DefaultProfile</span></span>
<span data-ttu-id="39ae6-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39ae6-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39ae6-129">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="39ae6-129">-Policy</span></span>
<span data-ttu-id="39ae6-130">Указывает имя политики сохраненного доступа, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="39ae6-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39ae6-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="39ae6-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="39ae6-132">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="39ae6-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="39ae6-133">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="39ae6-133">-ShareName</span></span>
<span data-ttu-id="39ae6-134">Указывает имя общего хранилища, для которого этот командлет получает политики.</span><span class="sxs-lookup"><span data-stu-id="39ae6-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39ae6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39ae6-135">CommonParameters</span></span>
<span data-ttu-id="39ae6-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="39ae6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39ae6-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39ae6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39ae6-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="39ae6-138">INPUTS</span></span>

### <span data-ttu-id="39ae6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="39ae6-139">System.String</span></span>

### <span data-ttu-id="39ae6-140">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="39ae6-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="39ae6-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="39ae6-141">OUTPUTS</span></span>

### <span data-ttu-id="39ae6-142">Microsoft. WindowsAzure. Storage. File. SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="39ae6-142">Microsoft.WindowsAzure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="39ae6-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="39ae6-143">NOTES</span></span>

## <span data-ttu-id="39ae6-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39ae6-144">RELATED LINKS</span></span>

[<span data-ttu-id="39ae6-145">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="39ae6-145">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="39ae6-146">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="39ae6-146">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="39ae6-147">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="39ae6-147">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="39ae6-148">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="39ae6-148">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
