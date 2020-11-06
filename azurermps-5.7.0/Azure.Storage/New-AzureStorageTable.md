---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
ms.openlocfilehash: 53bb5f3a34cddf9e74bfb9d9c9f1bd1d109d8f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565061"
---
# <span data-ttu-id="1ec1f-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="1ec1f-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="1ec1f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ec1f-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec1f-103">Создание таблицы хранилища.</span><span class="sxs-lookup"><span data-stu-id="1ec1f-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ec1f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ec1f-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="1ec1f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ec1f-105">DESCRIPTION</span></span>
<span data-ttu-id="1ec1f-106">Командлет **New-AzureStorageTable** создает таблицу хранилища, связанную с учетной записью хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec1f-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="1ec1f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ec1f-107">EXAMPLES</span></span>

### <span data-ttu-id="1ec1f-108">Пример 1: создание таблицы хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="1ec1f-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="1ec1f-109">Эта команда создает таблицу хранилища с именем tableabc.</span><span class="sxs-lookup"><span data-stu-id="1ec1f-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="1ec1f-110">Пример 2: создание нескольких таблиц хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="1ec1f-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="1ec1f-111">Эта команда создает несколько таблиц.</span><span class="sxs-lookup"><span data-stu-id="1ec1f-111">This command creates multiple tables.</span></span>
<span data-ttu-id="1ec1f-112">Он использует метод **Split** класса **String** .NET и передает имена в конвейере.</span><span class="sxs-lookup"><span data-stu-id="1ec1f-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="1ec1f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ec1f-113">PARAMETERS</span></span>

### <span data-ttu-id="1ec1f-114">-Context</span><span class="sxs-lookup"><span data-stu-id="1ec1f-114">-Context</span></span>
<span data-ttu-id="1ec1f-115">Указывает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="1ec1f-115">Specifies the storage context.</span></span>
<span data-ttu-id="1ec1f-116">Чтобы создать его, можно использовать командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1ec1f-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1ec1f-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1ec1f-117">-Name</span></span>
<span data-ttu-id="1ec1f-118">Задает имя новой таблицы.</span><span class="sxs-lookup"><span data-stu-id="1ec1f-118">Specifies a name for the new table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec1f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec1f-119">CommonParameters</span></span>
<span data-ttu-id="1ec1f-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ec1f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec1f-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ec1f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec1f-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ec1f-122">INPUTS</span></span>

### <span data-ttu-id="1ec1f-123">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1ec1f-123">IStorageContext</span></span>

<span data-ttu-id="1ec1f-124">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="1ec1f-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="1ec1f-125">Подстрок</span><span class="sxs-lookup"><span data-stu-id="1ec1f-125">String</span></span>

<span data-ttu-id="1ec1f-126">Параметр Name принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="1ec1f-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="1ec1f-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ec1f-127">OUTPUTS</span></span>

### <span data-ttu-id="1ec1f-128">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="1ec1f-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="1ec1f-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ec1f-129">NOTES</span></span>

## <span data-ttu-id="1ec1f-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ec1f-130">RELATED LINKS</span></span>

[<span data-ttu-id="1ec1f-131">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="1ec1f-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="1ec1f-132">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="1ec1f-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


