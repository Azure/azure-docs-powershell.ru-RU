---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e9ea56c53d73b9c71d2eade4fec7025466ed82d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556267"
---
# <span data-ttu-id="993d8-101">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="993d8-101">Get-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="993d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="993d8-102">SYNOPSIS</span></span>
<span data-ttu-id="993d8-103">Получает хранимую политику или политики доступа для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="993d8-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="993d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="993d8-104">SYNTAX</span></span>

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="993d8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="993d8-105">DESCRIPTION</span></span>
<span data-ttu-id="993d8-106">Командлет **Get-AzureStorageContainerStoredAccessPolicy** включает в себя политику и политики для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="993d8-106">The **Get-AzureStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="993d8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="993d8-107">EXAMPLES</span></span>

### <span data-ttu-id="993d8-108">Пример 1: получение политики для сохраненного доступа в контейнере хранилища</span><span class="sxs-lookup"><span data-stu-id="993d8-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="993d8-109">Эта команда получает политику доступа с именем Policy22 в контейнере хранения с именем Container07.</span><span class="sxs-lookup"><span data-stu-id="993d8-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="993d8-110">Пример 2: получение всех сохраненных политик доступа в контейнере хранилища</span><span class="sxs-lookup"><span data-stu-id="993d8-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="993d8-111">Эта команда получает все политики доступа в контейнере хранилища с именем Container07.</span><span class="sxs-lookup"><span data-stu-id="993d8-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="993d8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="993d8-112">PARAMETERS</span></span>

### <span data-ttu-id="993d8-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="993d8-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="993d8-114">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="993d8-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="993d8-115">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="993d8-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="993d8-116">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="993d8-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="993d8-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="993d8-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="993d8-118">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="993d8-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="993d8-119">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="993d8-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="993d8-120">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="993d8-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="993d8-121">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="993d8-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="993d8-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="993d8-122">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="993d8-123">-Container</span><span class="sxs-lookup"><span data-stu-id="993d8-123">-Container</span></span>
<span data-ttu-id="993d8-124">Указывает имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="993d8-124">Specifies the name of your Azure storage container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="993d8-125">-Context</span><span class="sxs-lookup"><span data-stu-id="993d8-125">-Context</span></span>
<span data-ttu-id="993d8-126">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="993d8-126">Specifies the Azure storage context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="993d8-127">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="993d8-127">-Policy</span></span>
<span data-ttu-id="993d8-128">Указывает политику сохраненных доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="993d8-128">Specifies the Azure stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="993d8-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="993d8-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="993d8-130">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="993d8-130">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="993d8-131">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="993d8-131">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="993d8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="993d8-132">CommonParameters</span></span>
<span data-ttu-id="993d8-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="993d8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="993d8-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="993d8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="993d8-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="993d8-135">INPUTS</span></span>

## <span data-ttu-id="993d8-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="993d8-136">OUTPUTS</span></span>

## <span data-ttu-id="993d8-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="993d8-137">NOTES</span></span>

## <span data-ttu-id="993d8-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="993d8-138">RELATED LINKS</span></span>

[<span data-ttu-id="993d8-139">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="993d8-139">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="993d8-140">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="993d8-140">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="993d8-141">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="993d8-141">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


