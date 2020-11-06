---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: f76cd56055e800dc5d7d5ac15e66be23621ffbe2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555556"
---
# <span data-ttu-id="f3c2a-101">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f3c2a-101">New-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="f3c2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3c2a-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c2a-103">Создание политики сохранения для доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="f3c2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3c2a-104">SYNTAX</span></span>

```
New-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3c2a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3c2a-105">DESCRIPTION</span></span>
<span data-ttu-id="f3c2a-106">Командлет **New-AzureStorageShareStoredAccessPolicy** создает политику сохранения для доступа к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-106">The **New-AzureStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="f3c2a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3c2a-107">EXAMPLES</span></span>

### <span data-ttu-id="f3c2a-108">Пример 1: Создание политики сохраненных прав доступа в общем доступе</span><span class="sxs-lookup"><span data-stu-id="f3c2a-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="f3c2a-109">Эта команда создает политику доступа с уровнем "полный доступ" в общем доступе.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="f3c2a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3c2a-110">PARAMETERS</span></span>

### <span data-ttu-id="f3c2a-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f3c2a-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f3c2a-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f3c2a-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f3c2a-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f3c2a-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f3c2a-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f3c2a-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f3c2a-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f3c2a-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f3c2a-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f3c2a-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-120">The default value is 10.</span></span>

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

### <span data-ttu-id="f3c2a-121">-Context</span><span class="sxs-lookup"><span data-stu-id="f3c2a-121">-Context</span></span>
<span data-ttu-id="f3c2a-122">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f3c2a-123">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="f3c2a-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="f3c2a-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f3c2a-124">-ExpiryTime</span></span>
<span data-ttu-id="f3c2a-125">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="f3c2a-126">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="f3c2a-126">-Permission</span></span>
<span data-ttu-id="f3c2a-127">Определяет разрешения в политике сохранения доступа для доступа к общей папке хранилища или файлам.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-127">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>

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

### <span data-ttu-id="f3c2a-128">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="f3c2a-128">-Policy</span></span>
<span data-ttu-id="f3c2a-129">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-129">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="f3c2a-130">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f3c2a-130">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f3c2a-131">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-131">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f3c2a-132">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="f3c2a-132">-ShareName</span></span>
<span data-ttu-id="f3c2a-133">Указывает имя общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-133">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="f3c2a-134">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f3c2a-134">-StartTime</span></span>
<span data-ttu-id="f3c2a-135">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-135">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="f3c2a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c2a-136">CommonParameters</span></span>
<span data-ttu-id="f3c2a-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c2a-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3c2a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c2a-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3c2a-139">INPUTS</span></span>

## <span data-ttu-id="f3c2a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3c2a-140">OUTPUTS</span></span>

## <span data-ttu-id="f3c2a-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3c2a-141">NOTES</span></span>

## <span data-ttu-id="f3c2a-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3c2a-142">RELATED LINKS</span></span>

[<span data-ttu-id="f3c2a-143">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f3c2a-143">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="f3c2a-144">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f3c2a-144">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="f3c2a-145">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f3c2a-145">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="f3c2a-146">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f3c2a-146">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
