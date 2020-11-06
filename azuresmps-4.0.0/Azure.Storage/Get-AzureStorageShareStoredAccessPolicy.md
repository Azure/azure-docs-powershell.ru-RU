---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc7268d3d7d233f6a3fafeb92540e23ae3eaa6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556231"
---
# <span data-ttu-id="3ce3f-101">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3ce3f-101">Get-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="3ce3f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ce3f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce3f-103">Получает хранимые политики доступа для общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="3ce3f-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="3ce3f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ce3f-104">SYNTAX</span></span>

```
Get-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ce3f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ce3f-105">DESCRIPTION</span></span>
<span data-ttu-id="3ce3f-106">Командлет **Get-AzureStorageShareStoredAccessPolicy** получает хранимые политики доступа для общего доступа к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="3ce3f-106">The **Get-AzureStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="3ce3f-107">Чтобы получить определенную политику, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="3ce3f-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="3ce3f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ce3f-108">EXAMPLES</span></span>

### <span data-ttu-id="3ce3f-109">Пример 1: получение политики доступа с сохранением в общем доступе</span><span class="sxs-lookup"><span data-stu-id="3ce3f-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="3ce3f-110">Эта команда получает сохраненную политику доступа с именем GeneralPolicy в ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="3ce3f-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="3ce3f-111">Пример 2: получение всех политик доступа для хранения в общем доступе</span><span class="sxs-lookup"><span data-stu-id="3ce3f-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="3ce3f-112">Эта команда получает все политики для сохраненного доступа в ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="3ce3f-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="3ce3f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ce3f-113">PARAMETERS</span></span>

### <span data-ttu-id="3ce3f-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3ce3f-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3ce3f-115">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="3ce3f-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3ce3f-116">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="3ce3f-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3ce3f-117">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="3ce3f-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3ce3f-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3ce3f-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3ce3f-119">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="3ce3f-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3ce3f-120">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="3ce3f-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3ce3f-121">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="3ce3f-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3ce3f-122">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="3ce3f-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3ce3f-123">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="3ce3f-123">The default value is 10.</span></span>

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

### <span data-ttu-id="3ce3f-124">-Context</span><span class="sxs-lookup"><span data-stu-id="3ce3f-124">-Context</span></span>
<span data-ttu-id="3ce3f-125">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3ce3f-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="3ce3f-126">Чтобы получить контекст, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="3ce3f-126">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="3ce3f-127">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="3ce3f-127">-Policy</span></span>
<span data-ttu-id="3ce3f-128">Указывает имя политики сохраненного доступа, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3ce3f-128">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3ce3f-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3ce3f-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3ce3f-130">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="3ce3f-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="3ce3f-131">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="3ce3f-131">-ShareName</span></span>
<span data-ttu-id="3ce3f-132">Указывает имя общего хранилища, для которого этот командлет получает политики.</span><span class="sxs-lookup"><span data-stu-id="3ce3f-132">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="3ce3f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce3f-133">CommonParameters</span></span>
<span data-ttu-id="3ce3f-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ce3f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce3f-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce3f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce3f-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ce3f-136">INPUTS</span></span>

## <span data-ttu-id="3ce3f-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ce3f-137">OUTPUTS</span></span>

## <span data-ttu-id="3ce3f-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ce3f-138">NOTES</span></span>

## <span data-ttu-id="3ce3f-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ce3f-139">RELATED LINKS</span></span>

[<span data-ttu-id="3ce3f-140">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3ce3f-140">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="3ce3f-141">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3ce3f-141">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="3ce3f-142">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3ce3f-142">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="3ce3f-143">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3ce3f-143">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
