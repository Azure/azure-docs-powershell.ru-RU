---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 823ae6183021e368933af8d2e01a61f0b582323e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561271"
---
# <span data-ttu-id="5c5c9-101">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5c5c9-101">New-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="5c5c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c5c9-102">SYNOPSIS</span></span>
<span data-ttu-id="5c5c9-103">Создание политики сохранения для доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-103">Creates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c5c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c5c9-104">SYNTAX</span></span>

```
New-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="5c5c9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c5c9-105">DESCRIPTION</span></span>
<span data-ttu-id="5c5c9-106">Командлет **New-AzureStorageShareStoredAccessPolicy** создает политику сохранения для доступа к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-106">The **New-AzureStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="5c5c9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c5c9-107">EXAMPLES</span></span>

### <span data-ttu-id="5c5c9-108">Пример 1: Создание политики сохраненных прав доступа в общем доступе</span><span class="sxs-lookup"><span data-stu-id="5c5c9-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="5c5c9-109">Эта команда создает политику доступа с уровнем "полный доступ" в общем доступе.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="5c5c9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c5c9-110">PARAMETERS</span></span>

### <span data-ttu-id="5c5c9-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5c5c9-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5c5c9-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5c5c9-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5c5c9-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5c5c9-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5c5c9-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5c5c9-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5c5c9-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5c5c9-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5c5c9-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5c5c9-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-120">The default value is 10.</span></span>

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

### <span data-ttu-id="5c5c9-121">-Context</span><span class="sxs-lookup"><span data-stu-id="5c5c9-121">-Context</span></span>
<span data-ttu-id="5c5c9-122">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5c5c9-123">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="5c5c9-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="5c5c9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c5c9-124">-DefaultProfile</span></span>
<span data-ttu-id="5c5c9-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c5c9-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5c5c9-126">-ExpiryTime</span></span>
<span data-ttu-id="5c5c9-127">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c5c9-128">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="5c5c9-128">-Permission</span></span>
<span data-ttu-id="5c5c9-129">Определяет разрешения в политике сохранения доступа для доступа к общей папке хранилища или файлам.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="5c5c9-130">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="5c5c9-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c5c9-131">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="5c5c9-131">-Policy</span></span>
<span data-ttu-id="5c5c9-132">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-132">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c5c9-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5c5c9-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5c5c9-134">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="5c5c9-135">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="5c5c9-135">-ShareName</span></span>
<span data-ttu-id="5c5c9-136">Указывает имя общего доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-136">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="5c5c9-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5c5c9-137">-StartTime</span></span>
<span data-ttu-id="5c5c9-138">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-138">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c5c9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c5c9-139">CommonParameters</span></span>
<span data-ttu-id="5c5c9-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c5c9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c5c9-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c5c9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c5c9-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c5c9-142">INPUTS</span></span>

### <span data-ttu-id="5c5c9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="5c5c9-143">System.String</span></span>

### <span data-ttu-id="5c5c9-144">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5c5c9-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5c5c9-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c5c9-145">OUTPUTS</span></span>

### <span data-ttu-id="5c5c9-146">System. String</span><span class="sxs-lookup"><span data-stu-id="5c5c9-146">System.String</span></span>

## <span data-ttu-id="5c5c9-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c5c9-147">NOTES</span></span>

## <span data-ttu-id="5c5c9-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c5c9-148">RELATED LINKS</span></span>

[<span data-ttu-id="5c5c9-149">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5c5c9-149">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="5c5c9-150">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5c5c9-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="5c5c9-151">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5c5c9-151">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="5c5c9-152">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5c5c9-152">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
