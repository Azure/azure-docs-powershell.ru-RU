---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 2eaa58523ef71d90aa7ef6566d18c050fe16a51f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565062"
---
# <span data-ttu-id="6cddb-101">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6cddb-101">New-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="6cddb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6cddb-102">SYNOPSIS</span></span>
<span data-ttu-id="6cddb-103">Создание политики сохранения для доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="6cddb-103">Creates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cddb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6cddb-104">SYNTAX</span></span>

```
New-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cddb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cddb-105">DESCRIPTION</span></span>
<span data-ttu-id="6cddb-106">Командлет **New-AzureStorageShareStoredAccessPolicy** создает политику сохранения для доступа к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="6cddb-106">The **New-AzureStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="6cddb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6cddb-107">EXAMPLES</span></span>

### <span data-ttu-id="6cddb-108">Пример 1: Создание политики сохраненных прав доступа в общем доступе</span><span class="sxs-lookup"><span data-stu-id="6cddb-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="6cddb-109">Эта команда создает политику доступа с уровнем "полный доступ" в общем доступе.</span><span class="sxs-lookup"><span data-stu-id="6cddb-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="6cddb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6cddb-110">PARAMETERS</span></span>

### <span data-ttu-id="6cddb-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6cddb-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6cddb-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="6cddb-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6cddb-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="6cddb-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6cddb-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="6cddb-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6cddb-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6cddb-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6cddb-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="6cddb-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6cddb-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="6cddb-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6cddb-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="6cddb-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6cddb-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="6cddb-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6cddb-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="6cddb-120">The default value is 10.</span></span>

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

### <span data-ttu-id="6cddb-121">-Context</span><span class="sxs-lookup"><span data-stu-id="6cddb-121">-Context</span></span>
<span data-ttu-id="6cddb-122">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6cddb-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6cddb-123">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="6cddb-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="6cddb-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6cddb-124">-ExpiryTime</span></span>
<span data-ttu-id="6cddb-125">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="6cddb-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="6cddb-126">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="6cddb-126">-Permission</span></span>
<span data-ttu-id="6cddb-127">Определяет разрешения в политике сохранения доступа для доступа к общей папке хранилища или файлам.</span><span class="sxs-lookup"><span data-stu-id="6cddb-127">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>

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

### <span data-ttu-id="6cddb-128">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="6cddb-128">-Policy</span></span>
<span data-ttu-id="6cddb-129">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="6cddb-129">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="6cddb-130">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6cddb-130">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6cddb-131">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="6cddb-131">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="6cddb-132">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="6cddb-132">-ShareName</span></span>
<span data-ttu-id="6cddb-133">Указывает имя общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="6cddb-133">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="6cddb-134">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6cddb-134">-StartTime</span></span>
<span data-ttu-id="6cddb-135">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="6cddb-135">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="6cddb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cddb-136">CommonParameters</span></span>
<span data-ttu-id="6cddb-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6cddb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cddb-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cddb-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cddb-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6cddb-139">INPUTS</span></span>

### <span data-ttu-id="6cddb-140">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6cddb-140">IStorageContext</span></span>

<span data-ttu-id="6cddb-141">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="6cddb-141">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="6cddb-142">Подстрок</span><span class="sxs-lookup"><span data-stu-id="6cddb-142">String</span></span>

<span data-ttu-id="6cddb-143">Параметр ShareName принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="6cddb-143">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="6cddb-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cddb-144">OUTPUTS</span></span>

### <span data-ttu-id="6cddb-145">System. String</span><span class="sxs-lookup"><span data-stu-id="6cddb-145">System.String</span></span>

## <span data-ttu-id="6cddb-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="6cddb-146">NOTES</span></span>

## <span data-ttu-id="6cddb-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6cddb-147">RELATED LINKS</span></span>

[<span data-ttu-id="6cddb-148">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6cddb-148">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="6cddb-149">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="6cddb-149">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="6cddb-150">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6cddb-150">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="6cddb-151">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6cddb-151">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
