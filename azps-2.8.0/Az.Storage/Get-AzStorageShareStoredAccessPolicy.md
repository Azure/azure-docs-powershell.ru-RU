---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 0a29eac4c9dbf1322e29c6a9b268a6ada3e13014
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907174"
---
# <span data-ttu-id="0c6e0-101">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0c6e0-101">Get-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="0c6e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c6e0-102">SYNOPSIS</span></span>
<span data-ttu-id="0c6e0-103">Получает хранимые политики доступа для общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="0c6e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c6e0-104">SYNTAX</span></span>

```
Get-AzStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="0c6e0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c6e0-105">DESCRIPTION</span></span>
<span data-ttu-id="0c6e0-106">Командлет **Get-AzStorageShareStoredAccessPolicy** получает хранимые политики доступа для общего доступа к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-106">The **Get-AzStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="0c6e0-107">Чтобы получить определенную политику, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="0c6e0-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c6e0-108">EXAMPLES</span></span>

### <span data-ttu-id="0c6e0-109">Пример 1: получение политики доступа с сохранением в общем доступе</span><span class="sxs-lookup"><span data-stu-id="0c6e0-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="0c6e0-110">Эта команда получает сохраненную политику доступа с именем GeneralPolicy в ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="0c6e0-111">Пример 2: получение всех политик доступа для хранения в общем доступе</span><span class="sxs-lookup"><span data-stu-id="0c6e0-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="0c6e0-112">Эта команда получает все политики для сохраненного доступа в ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="0c6e0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c6e0-113">PARAMETERS</span></span>

### <span data-ttu-id="0c6e0-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0c6e0-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0c6e0-115">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0c6e0-116">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0c6e0-117">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0c6e0-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0c6e0-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0c6e0-119">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0c6e0-120">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0c6e0-121">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0c6e0-122">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0c6e0-123">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-123">The default value is 10.</span></span>

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

### <span data-ttu-id="0c6e0-124">-Context</span><span class="sxs-lookup"><span data-stu-id="0c6e0-124">-Context</span></span>
<span data-ttu-id="0c6e0-125">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="0c6e0-126">Чтобы получить контекст, используйте командлет [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="0c6e0-126">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="0c6e0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c6e0-127">-DefaultProfile</span></span>
<span data-ttu-id="0c6e0-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c6e0-129">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="0c6e0-129">-Policy</span></span>
<span data-ttu-id="0c6e0-130">Указывает имя политики сохраненного доступа, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0c6e0-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0c6e0-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0c6e0-132">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="0c6e0-133">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="0c6e0-133">-ShareName</span></span>
<span data-ttu-id="0c6e0-134">Указывает имя общего хранилища, для которого этот командлет получает политики.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="0c6e0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c6e0-135">CommonParameters</span></span>
<span data-ttu-id="0c6e0-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c6e0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c6e0-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c6e0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c6e0-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c6e0-138">INPUTS</span></span>

### <span data-ttu-id="0c6e0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0c6e0-139">System.String</span></span>

### <span data-ttu-id="0c6e0-140">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0c6e0-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0c6e0-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c6e0-141">OUTPUTS</span></span>

### <span data-ttu-id="0c6e0-142">Microsoft. Azure. Storage. File. SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="0c6e0-142">Microsoft.Azure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="0c6e0-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c6e0-143">NOTES</span></span>

## <span data-ttu-id="0c6e0-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c6e0-144">RELATED LINKS</span></span>

[<span data-ttu-id="0c6e0-145">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0c6e0-145">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="0c6e0-146">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0c6e0-146">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="0c6e0-147">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0c6e0-147">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="0c6e0-148">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0c6e0-148">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
