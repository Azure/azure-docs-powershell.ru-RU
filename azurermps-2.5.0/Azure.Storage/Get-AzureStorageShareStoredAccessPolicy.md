---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragesharestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 5e4a6c5ad69ae8f31564335a410a67ec58181f3d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913508"
---
# <span data-ttu-id="548c1-101">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="548c1-101">Get-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="548c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="548c1-102">SYNOPSIS</span></span>
<span data-ttu-id="548c1-103">Получает хранимые политики доступа для общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="548c1-103">Gets stored access policies for a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="548c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="548c1-104">SYNTAX</span></span>

```
Get-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="548c1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="548c1-105">DESCRIPTION</span></span>
<span data-ttu-id="548c1-106">Командлет **Get-AzureStorageShareStoredAccessPolicy** получает хранимые политики доступа для общего доступа к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="548c1-106">The **Get-AzureStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="548c1-107">Чтобы получить определенную политику, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="548c1-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="548c1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="548c1-108">EXAMPLES</span></span>

### <span data-ttu-id="548c1-109">Пример 1: получение политики доступа с сохранением в общем доступе</span><span class="sxs-lookup"><span data-stu-id="548c1-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="548c1-110">Эта команда получает сохраненную политику доступа с именем GeneralPolicy в ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="548c1-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="548c1-111">Пример 2: получение всех политик доступа для хранения в общем доступе</span><span class="sxs-lookup"><span data-stu-id="548c1-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="548c1-112">Эта команда получает все политики для сохраненного доступа в ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="548c1-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="548c1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="548c1-113">PARAMETERS</span></span>

### <span data-ttu-id="548c1-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="548c1-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="548c1-115">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="548c1-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="548c1-116">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="548c1-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="548c1-117">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="548c1-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="548c1-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="548c1-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="548c1-119">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="548c1-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="548c1-120">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="548c1-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="548c1-121">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="548c1-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="548c1-122">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="548c1-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="548c1-123">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="548c1-123">The default value is 10.</span></span>

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

### <span data-ttu-id="548c1-124">-Context</span><span class="sxs-lookup"><span data-stu-id="548c1-124">-Context</span></span>
<span data-ttu-id="548c1-125">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="548c1-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="548c1-126">Чтобы получить контекст, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="548c1-126">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="548c1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="548c1-127">-DefaultProfile</span></span>
<span data-ttu-id="548c1-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="548c1-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="548c1-129">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="548c1-129">-Policy</span></span>
<span data-ttu-id="548c1-130">Указывает имя политики сохраненного доступа, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="548c1-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="548c1-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="548c1-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="548c1-132">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="548c1-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="548c1-133">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="548c1-133">-ShareName</span></span>
<span data-ttu-id="548c1-134">Указывает имя общего хранилища, для которого этот командлет получает политики.</span><span class="sxs-lookup"><span data-stu-id="548c1-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="548c1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548c1-135">CommonParameters</span></span>
<span data-ttu-id="548c1-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="548c1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="548c1-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="548c1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548c1-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="548c1-138">INPUTS</span></span>

### <span data-ttu-id="548c1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="548c1-139">System.String</span></span>

### <span data-ttu-id="548c1-140">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="548c1-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="548c1-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="548c1-141">OUTPUTS</span></span>

### <span data-ttu-id="548c1-142">Microsoft. WindowsAzure. Storage. File. SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="548c1-142">Microsoft.WindowsAzure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="548c1-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="548c1-143">NOTES</span></span>

## <span data-ttu-id="548c1-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="548c1-144">RELATED LINKS</span></span>

[<span data-ttu-id="548c1-145">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="548c1-145">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="548c1-146">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="548c1-146">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="548c1-147">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="548c1-147">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="548c1-148">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="548c1-148">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
