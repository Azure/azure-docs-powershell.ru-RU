---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: ''
schema: 2.0.0
ms.openlocfilehash: a95d5afafbed6ab6e3ba81cbfd509fd7b531217e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731808"
---
# <span data-ttu-id="68920-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="68920-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="68920-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="68920-102">SYNOPSIS</span></span>
<span data-ttu-id="68920-103">Создание политики сохраненного доступа для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="68920-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="68920-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="68920-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="68920-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68920-105">DESCRIPTION</span></span>
<span data-ttu-id="68920-106">Командлет **New-AzureStorageContainerStoredAccessPolicy** создает политику сохраненного доступа для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="68920-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="68920-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="68920-107">EXAMPLES</span></span>

### <span data-ttu-id="68920-108">Пример 1: Создание политики для сохраненного доступа в контейнере хранилища</span><span class="sxs-lookup"><span data-stu-id="68920-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="68920-109">Эта команда создает политику доступа с именем Policy01 в контейнере хранения с именем MyContainer.</span><span class="sxs-lookup"><span data-stu-id="68920-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="68920-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="68920-110">PARAMETERS</span></span>

### <span data-ttu-id="68920-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="68920-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="68920-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="68920-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="68920-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="68920-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="68920-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="68920-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="68920-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="68920-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="68920-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="68920-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="68920-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="68920-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="68920-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="68920-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="68920-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="68920-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="68920-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="68920-120">The default value is 10.</span></span>

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

### <span data-ttu-id="68920-121">-Container</span><span class="sxs-lookup"><span data-stu-id="68920-121">-Container</span></span>
<span data-ttu-id="68920-122">Указывает имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="68920-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="68920-123">-Context</span><span class="sxs-lookup"><span data-stu-id="68920-123">-Context</span></span>
<span data-ttu-id="68920-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="68920-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="68920-125">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="68920-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="68920-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="68920-126">-ExpiryTime</span></span>
<span data-ttu-id="68920-127">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="68920-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68920-128">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="68920-128">-Permission</span></span>
<span data-ttu-id="68920-129">Указывает уровень общедоступного доступа к этому контейнеру.</span><span class="sxs-lookup"><span data-stu-id="68920-129">Specifies the level of public access to this container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68920-130">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="68920-130">-Policy</span></span>
<span data-ttu-id="68920-131">Указывает политику сохраненного доступа, которая включает разрешения для этого маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="68920-131">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68920-132">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="68920-132">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="68920-133">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="68920-133">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="68920-134">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="68920-134">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="68920-135">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="68920-135">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="68920-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="68920-136">-StartTime</span></span>
<span data-ttu-id="68920-137">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="68920-137">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68920-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68920-138">CommonParameters</span></span>
<span data-ttu-id="68920-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="68920-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68920-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68920-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68920-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="68920-141">INPUTS</span></span>

## <span data-ttu-id="68920-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="68920-142">OUTPUTS</span></span>

## <span data-ttu-id="68920-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="68920-143">NOTES</span></span>

## <span data-ttu-id="68920-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68920-144">RELATED LINKS</span></span>

[<span data-ttu-id="68920-145">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="68920-145">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="68920-146">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="68920-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="68920-147">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="68920-147">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="68920-148">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="68920-148">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


