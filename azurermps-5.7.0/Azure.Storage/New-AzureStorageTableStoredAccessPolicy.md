---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 163c6ba0841b19edc76421259b1cd9cc8411e35e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565060"
---
# <span data-ttu-id="c0f00-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c0f00-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="c0f00-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0f00-102">SYNOPSIS</span></span>
<span data-ttu-id="c0f00-103">Создание политики сохранения для доступа к таблице хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c0f00-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0f00-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0f00-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="c0f00-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0f00-105">DESCRIPTION</span></span>
<span data-ttu-id="c0f00-106">Командлет **New-AzureStorageTableStoredAccessPolicy** создает политику сохраненного доступа для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c0f00-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="c0f00-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0f00-107">EXAMPLES</span></span>

### <span data-ttu-id="c0f00-108">Пример 1: Создание политики сохраненных прав доступа в таблице</span><span class="sxs-lookup"><span data-stu-id="c0f00-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="c0f00-109">Эта команда создает политику доступа с именем Policy02 в таблице хранения с именем MyTable.</span><span class="sxs-lookup"><span data-stu-id="c0f00-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="c0f00-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0f00-110">PARAMETERS</span></span>

### <span data-ttu-id="c0f00-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c0f00-111">-Context</span></span>
<span data-ttu-id="c0f00-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c0f00-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c0f00-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c0f00-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c0f00-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c0f00-114">-ExpiryTime</span></span>
<span data-ttu-id="c0f00-115">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="c0f00-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="c0f00-116">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="c0f00-116">-Permission</span></span>
<span data-ttu-id="c0f00-117">Определяет разрешения в политике сохранения доступа для доступа к таблице хранения.</span><span class="sxs-lookup"><span data-stu-id="c0f00-117">Specifies permissions in the stored access policy to access the storage table.</span></span>

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

### <span data-ttu-id="c0f00-118">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="c0f00-118">-Policy</span></span>
<span data-ttu-id="c0f00-119">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="c0f00-119">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="c0f00-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c0f00-120">-StartTime</span></span>
<span data-ttu-id="c0f00-121">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="c0f00-121">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="c0f00-122">-Таблица</span><span class="sxs-lookup"><span data-stu-id="c0f00-122">-Table</span></span>
<span data-ttu-id="c0f00-123">Указывает имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c0f00-123">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="c0f00-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0f00-124">CommonParameters</span></span>
<span data-ttu-id="c0f00-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0f00-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0f00-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0f00-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0f00-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0f00-127">INPUTS</span></span>

### <span data-ttu-id="c0f00-128">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c0f00-128">IStorageContext</span></span>

<span data-ttu-id="c0f00-129">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c0f00-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="c0f00-130">Подстрок</span><span class="sxs-lookup"><span data-stu-id="c0f00-130">String</span></span>

<span data-ttu-id="c0f00-131">Параметр "Таблица" принимает значение типа String из конвейера</span><span class="sxs-lookup"><span data-stu-id="c0f00-131">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c0f00-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0f00-132">OUTPUTS</span></span>

### <span data-ttu-id="c0f00-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c0f00-133">System.String</span></span>

## <span data-ttu-id="c0f00-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0f00-134">NOTES</span></span>

## <span data-ttu-id="c0f00-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0f00-135">RELATED LINKS</span></span>

[<span data-ttu-id="c0f00-136">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c0f00-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="c0f00-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c0f00-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="c0f00-138">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c0f00-138">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="c0f00-139">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c0f00-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


