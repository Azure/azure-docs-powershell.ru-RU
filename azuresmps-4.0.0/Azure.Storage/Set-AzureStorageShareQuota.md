---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 778c5020dc47bc8db7bda664b2e352045d851dfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556359"
---
# <span data-ttu-id="9f152-101">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="9f152-101">Set-AzureStorageShareQuota</span></span>

## <span data-ttu-id="9f152-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f152-102">SYNOPSIS</span></span>
<span data-ttu-id="9f152-103">Задает емкость хранилища для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="9f152-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="9f152-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f152-104">SYNTAX</span></span>

### <span data-ttu-id="9f152-105">Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="9f152-105">ShareName</span></span>
```
Set-AzureStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f152-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="9f152-106">Share</span></span>
```
Set-AzureStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="9f152-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f152-107">DESCRIPTION</span></span>
<span data-ttu-id="9f152-108">Командлет **Set-AzureStorageShareQuota** Задает емкость хранилища для указанной общей записи.</span><span class="sxs-lookup"><span data-stu-id="9f152-108">The **Set-AzureStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="9f152-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f152-109">EXAMPLES</span></span>

### <span data-ttu-id="9f152-110">Пример 1: Настройка емкости хранилища для общего доступа</span><span class="sxs-lookup"><span data-stu-id="9f152-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzureStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="9f152-111">Эта команда задает емкость хранилища для общего ресурса с именем ContosoShare01 на 1024 ГБ.</span><span class="sxs-lookup"><span data-stu-id="9f152-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="9f152-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f152-112">PARAMETERS</span></span>

### <span data-ttu-id="9f152-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9f152-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9f152-114">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="9f152-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9f152-115">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="9f152-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9f152-116">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="9f152-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9f152-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9f152-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9f152-118">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="9f152-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9f152-119">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="9f152-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9f152-120">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="9f152-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9f152-121">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="9f152-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9f152-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="9f152-122">The default value is 10.</span></span>

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

### <span data-ttu-id="9f152-123">-Context</span><span class="sxs-lookup"><span data-stu-id="9f152-123">-Context</span></span>
<span data-ttu-id="9f152-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="9f152-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9f152-125">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="9f152-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f152-126">-Quota</span><span class="sxs-lookup"><span data-stu-id="9f152-126">-Quota</span></span>
<span data-ttu-id="9f152-127">Указывает значение квоты в гигабайтах (ГБ).</span><span class="sxs-lookup"><span data-stu-id="9f152-127">Specifies the quota value in gigabytes (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f152-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9f152-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9f152-129">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="9f152-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="9f152-130">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="9f152-130">-Share</span></span>
<span data-ttu-id="9f152-131">Указывает объект **CloudFileShare** для представления общего доступа, для которого этот командлет устанавливает квоту.</span><span class="sxs-lookup"><span data-stu-id="9f152-131">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="9f152-132">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="9f152-132">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f152-133">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="9f152-133">-ShareName</span></span>
<span data-ttu-id="9f152-134">Указывает имя общей файловой панели, для которой задается квота.</span><span class="sxs-lookup"><span data-stu-id="9f152-134">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f152-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f152-135">CommonParameters</span></span>
<span data-ttu-id="9f152-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f152-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f152-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f152-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f152-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f152-138">INPUTS</span></span>

## <span data-ttu-id="9f152-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f152-139">OUTPUTS</span></span>

## <span data-ttu-id="9f152-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f152-140">NOTES</span></span>

## <span data-ttu-id="9f152-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f152-141">RELATED LINKS</span></span>

[<span data-ttu-id="9f152-142">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9f152-142">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="9f152-143">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9f152-143">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="9f152-144">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="9f152-144">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
