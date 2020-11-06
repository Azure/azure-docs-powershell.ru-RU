---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3ba13fb1ee18f5dcc35b81ff70ebd7c5a61d1e4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558087"
---
# <span data-ttu-id="06591-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="06591-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="06591-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="06591-102">SYNOPSIS</span></span>
<span data-ttu-id="06591-103">Список таблиц хранилища.</span><span class="sxs-lookup"><span data-stu-id="06591-103">Lists the storage tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06591-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="06591-104">SYNTAX</span></span>

### <span data-ttu-id="06591-105">TableName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="06591-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="06591-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="06591-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="06591-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06591-107">DESCRIPTION</span></span>
<span data-ttu-id="06591-108">Командлет **Get-AzureStorageTable** перечисляет таблицы хранения, связанные с учетной записью хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="06591-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="06591-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="06591-109">EXAMPLES</span></span>

### <span data-ttu-id="06591-110">Пример 1: список всех таблиц хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="06591-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="06591-111">Эта команда получает все таблицы хранилища для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="06591-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="06591-112">Пример 2: список таблиц хранилища Azure с использованием подстановочных знаков</span><span class="sxs-lookup"><span data-stu-id="06591-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="06591-113">Эта команда использует подстановочный знак для получения таблиц хранилища, имя которых начинается с Table.</span><span class="sxs-lookup"><span data-stu-id="06591-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="06591-114">Пример 3: список таблиц хранилища Azure с использованием префикса имени таблицы</span><span class="sxs-lookup"><span data-stu-id="06591-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="06591-115">Эта команда использует параметр *prefix* для получения таблиц хранилища, имя которых начинается с Table.</span><span class="sxs-lookup"><span data-stu-id="06591-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="06591-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="06591-116">PARAMETERS</span></span>

### <span data-ttu-id="06591-117">-Context</span><span class="sxs-lookup"><span data-stu-id="06591-117">-Context</span></span>
<span data-ttu-id="06591-118">Указывает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="06591-118">Specifies the storage context.</span></span>
<span data-ttu-id="06591-119">Чтобы создать его, можно использовать командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="06591-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="06591-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="06591-120">-Name</span></span>
<span data-ttu-id="06591-121">Указывает имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="06591-121">Specifies the table name.</span></span>
<span data-ttu-id="06591-122">Если имя таблицы пусто, командлет выводит список всех таблиц.</span><span class="sxs-lookup"><span data-stu-id="06591-122">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="06591-123">В противном случае выводится список всех таблиц, соответствующих указанному имени или шаблону обычного имени.</span><span class="sxs-lookup"><span data-stu-id="06591-123">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="06591-124">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="06591-124">-Prefix</span></span>
<span data-ttu-id="06591-125">Задает префикс, используемый в имени таблицы или таблиц, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="06591-125">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="06591-126">Вы можете использовать этот параметр, чтобы найти все таблицы, которые начинаются с одной строки, например Table.</span><span class="sxs-lookup"><span data-stu-id="06591-126">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: String
Parameter Sets: TablePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06591-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06591-127">CommonParameters</span></span>
<span data-ttu-id="06591-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="06591-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06591-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06591-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06591-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="06591-130">INPUTS</span></span>

### <span data-ttu-id="06591-131">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="06591-131">IStorageContext</span></span>

<span data-ttu-id="06591-132">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="06591-132">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="06591-133">Подстрок</span><span class="sxs-lookup"><span data-stu-id="06591-133">String</span></span>

<span data-ttu-id="06591-134">Параметр Name принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="06591-134">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="06591-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="06591-135">OUTPUTS</span></span>

### <span data-ttu-id="06591-136">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="06591-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="06591-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="06591-137">NOTES</span></span>

## <span data-ttu-id="06591-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06591-138">RELATED LINKS</span></span>

[<span data-ttu-id="06591-139">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="06591-139">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="06591-140">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="06591-140">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


