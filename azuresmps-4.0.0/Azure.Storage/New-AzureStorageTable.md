---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a58f869d5308b176a68614cbb2fa2fec401fa14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556076"
---
# <span data-ttu-id="49abc-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="49abc-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="49abc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49abc-102">SYNOPSIS</span></span>
<span data-ttu-id="49abc-103">Создание таблицы хранилища.</span><span class="sxs-lookup"><span data-stu-id="49abc-103">Creates a storage table.</span></span>

## <span data-ttu-id="49abc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49abc-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="49abc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49abc-105">DESCRIPTION</span></span>
<span data-ttu-id="49abc-106">Командлет **New-AzureStorageTable** создает таблицу хранилища, связанную с учетной записью хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="49abc-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="49abc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49abc-107">EXAMPLES</span></span>

### <span data-ttu-id="49abc-108">Пример 1: создание таблицы хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="49abc-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="49abc-109">Эта команда создает таблицу хранилища с именем tableabc.</span><span class="sxs-lookup"><span data-stu-id="49abc-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="49abc-110">Пример 2: создание нескольких таблиц хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="49abc-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="49abc-111">Эта команда создает несколько таблиц.</span><span class="sxs-lookup"><span data-stu-id="49abc-111">This command creates multiple tables.</span></span>
<span data-ttu-id="49abc-112">Он использует метод **Split** класса **String** .NET и передает имена в конвейере.</span><span class="sxs-lookup"><span data-stu-id="49abc-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="49abc-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49abc-113">PARAMETERS</span></span>

### <span data-ttu-id="49abc-114">-Context</span><span class="sxs-lookup"><span data-stu-id="49abc-114">-Context</span></span>
<span data-ttu-id="49abc-115">Указывает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="49abc-115">Specifies the storage context.</span></span>
<span data-ttu-id="49abc-116">Чтобы создать его, можно использовать командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="49abc-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="49abc-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="49abc-117">-Name</span></span>
<span data-ttu-id="49abc-118">Задает имя новой таблицы.</span><span class="sxs-lookup"><span data-stu-id="49abc-118">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="49abc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49abc-119">CommonParameters</span></span>
<span data-ttu-id="49abc-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49abc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49abc-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49abc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49abc-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49abc-122">INPUTS</span></span>

## <span data-ttu-id="49abc-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49abc-123">OUTPUTS</span></span>

## <span data-ttu-id="49abc-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="49abc-124">NOTES</span></span>

## <span data-ttu-id="49abc-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49abc-125">RELATED LINKS</span></span>

[<span data-ttu-id="49abc-126">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="49abc-126">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="49abc-127">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="49abc-127">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


