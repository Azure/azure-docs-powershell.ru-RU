---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetable
schema: 2.0.0
ms.openlocfilehash: 4fe02c9824945593de4b4160e9db10b1573a335a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913946"
---
# <span data-ttu-id="b5823-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="b5823-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="b5823-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5823-102">SYNOPSIS</span></span>
<span data-ttu-id="b5823-103">Создание таблицы хранилища.</span><span class="sxs-lookup"><span data-stu-id="b5823-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5823-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5823-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5823-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5823-105">DESCRIPTION</span></span>
<span data-ttu-id="b5823-106">Командлет **New-AzureStorageTable** создает таблицу хранилища, связанную с учетной записью хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="b5823-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="b5823-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5823-107">EXAMPLES</span></span>

### <span data-ttu-id="b5823-108">Пример 1: создание таблицы хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="b5823-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="b5823-109">Эта команда создает таблицу хранилища с именем tableabc.</span><span class="sxs-lookup"><span data-stu-id="b5823-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="b5823-110">Пример 2: создание нескольких таблиц хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="b5823-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="b5823-111">Эта команда создает несколько таблиц.</span><span class="sxs-lookup"><span data-stu-id="b5823-111">This command creates multiple tables.</span></span>
<span data-ttu-id="b5823-112">Он использует метод **Split** класса **String** .NET и передает имена в конвейере.</span><span class="sxs-lookup"><span data-stu-id="b5823-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="b5823-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5823-113">PARAMETERS</span></span>

### <span data-ttu-id="b5823-114">-Context</span><span class="sxs-lookup"><span data-stu-id="b5823-114">-Context</span></span>
<span data-ttu-id="b5823-115">Указывает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="b5823-115">Specifies the storage context.</span></span>
<span data-ttu-id="b5823-116">Чтобы создать его, можно использовать командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b5823-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b5823-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5823-117">-DefaultProfile</span></span>
<span data-ttu-id="b5823-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5823-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5823-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b5823-119">-Name</span></span>
<span data-ttu-id="b5823-120">Задает имя новой таблицы.</span><span class="sxs-lookup"><span data-stu-id="b5823-120">Specifies a name for the new table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5823-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5823-121">CommonParameters</span></span>
<span data-ttu-id="b5823-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5823-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5823-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5823-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5823-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5823-124">INPUTS</span></span>

### <span data-ttu-id="b5823-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b5823-125">System.String</span></span>

### <span data-ttu-id="b5823-126">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b5823-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b5823-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5823-127">OUTPUTS</span></span>

### <span data-ttu-id="b5823-128">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="b5823-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="b5823-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5823-129">NOTES</span></span>

## <span data-ttu-id="b5823-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5823-130">RELATED LINKS</span></span>

[<span data-ttu-id="b5823-131">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="b5823-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="b5823-132">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="b5823-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


