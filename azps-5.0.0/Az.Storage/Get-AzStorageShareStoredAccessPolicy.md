---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 2e444fba12f0ffebfd3d6679293cac31fc574e93
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246627"
---
# <span data-ttu-id="c527c-101">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c527c-101">Get-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="c527c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c527c-102">SYNOPSIS</span></span>
<span data-ttu-id="c527c-103">Получает хранимые политики доступа для общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="c527c-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="c527c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c527c-104">SYNTAX</span></span>

```
Get-AzStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c527c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c527c-105">DESCRIPTION</span></span>
<span data-ttu-id="c527c-106">Командлет **Get-AzStorageShareStoredAccessPolicy** получает хранимые политики доступа для общего доступа к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="c527c-106">The **Get-AzStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="c527c-107">Чтобы получить определенную политику, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="c527c-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="c527c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c527c-108">EXAMPLES</span></span>

### <span data-ttu-id="c527c-109">Пример 1: получение политики доступа с сохранением в общем доступе</span><span class="sxs-lookup"><span data-stu-id="c527c-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="c527c-110">Эта команда получает сохраненную политику доступа с именем GeneralPolicy в ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="c527c-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="c527c-111">Пример 2: получение всех политик доступа для хранения в общем доступе</span><span class="sxs-lookup"><span data-stu-id="c527c-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="c527c-112">Эта команда получает все политики для сохраненного доступа в ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="c527c-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="c527c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c527c-113">PARAMETERS</span></span>

### <span data-ttu-id="c527c-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c527c-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c527c-115">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="c527c-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c527c-116">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="c527c-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c527c-117">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c527c-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c527c-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c527c-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c527c-119">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="c527c-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c527c-120">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="c527c-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c527c-121">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="c527c-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c527c-122">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="c527c-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c527c-123">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="c527c-123">The default value is 10.</span></span>

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

### <span data-ttu-id="c527c-124">-Context</span><span class="sxs-lookup"><span data-stu-id="c527c-124">-Context</span></span>
<span data-ttu-id="c527c-125">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c527c-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="c527c-126">Чтобы получить контекст, используйте командлет [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="c527c-126">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="c527c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c527c-127">-DefaultProfile</span></span>
<span data-ttu-id="c527c-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c527c-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c527c-129">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="c527c-129">-Policy</span></span>
<span data-ttu-id="c527c-130">Указывает имя политики сохраненного доступа, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c527c-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c527c-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c527c-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c527c-132">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="c527c-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c527c-133">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="c527c-133">-ShareName</span></span>
<span data-ttu-id="c527c-134">Указывает имя общего хранилища, для которого этот командлет получает политики.</span><span class="sxs-lookup"><span data-stu-id="c527c-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="c527c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c527c-135">CommonParameters</span></span>
<span data-ttu-id="c527c-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c527c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c527c-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c527c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c527c-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c527c-138">INPUTS</span></span>

### <span data-ttu-id="c527c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c527c-139">System.String</span></span>

### <span data-ttu-id="c527c-140">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c527c-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c527c-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c527c-141">OUTPUTS</span></span>

### <span data-ttu-id="c527c-142">Microsoft. Azure. Storage. File. SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="c527c-142">Microsoft.Azure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="c527c-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="c527c-143">NOTES</span></span>

## <span data-ttu-id="c527c-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c527c-144">RELATED LINKS</span></span>

[<span data-ttu-id="c527c-145">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c527c-145">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="c527c-146">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c527c-146">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="c527c-147">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c527c-147">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="c527c-148">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c527c-148">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
