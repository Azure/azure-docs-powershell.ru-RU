---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d501faaebcc5e381dc2a7270c8b55b148e2812b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066748"
---
# <span data-ttu-id="d5078-101">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="d5078-101">Get-AzStorageTable</span></span>

## <span data-ttu-id="d5078-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5078-102">SYNOPSIS</span></span>
<span data-ttu-id="d5078-103">Список таблиц хранилища.</span><span class="sxs-lookup"><span data-stu-id="d5078-103">Lists the storage tables.</span></span>

## <span data-ttu-id="d5078-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5078-104">SYNTAX</span></span>

### <span data-ttu-id="d5078-105">TableName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d5078-105">TableName (Default)</span></span>
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5078-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="d5078-106">TablePrefix</span></span>
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5078-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5078-107">DESCRIPTION</span></span>
<span data-ttu-id="d5078-108">Командлет **Get-AzStorageTable** перечисляет таблицы хранения, связанные с учетной записью хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="d5078-108">The **Get-AzStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="d5078-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5078-109">EXAMPLES</span></span>

### <span data-ttu-id="d5078-110">Пример 1: список всех таблиц хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="d5078-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzStorageTable
```

<span data-ttu-id="d5078-111">Эта команда получает все таблицы хранилища для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d5078-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="d5078-112">Пример 2: список таблиц хранилища Azure с использованием подстановочных знаков</span><span class="sxs-lookup"><span data-stu-id="d5078-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzStorageTable -Name table*
```

<span data-ttu-id="d5078-113">Эта команда использует подстановочный знак для получения таблиц хранилища, имя которых начинается с Table.</span><span class="sxs-lookup"><span data-stu-id="d5078-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="d5078-114">Пример 3: список таблиц хранилища Azure с использованием префикса имени таблицы</span><span class="sxs-lookup"><span data-stu-id="d5078-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

<span data-ttu-id="d5078-115">Эта команда использует параметр *prefix* для получения таблиц хранилища, имя которых начинается с Table.</span><span class="sxs-lookup"><span data-stu-id="d5078-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="d5078-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5078-116">PARAMETERS</span></span>

### <span data-ttu-id="d5078-117">-Context</span><span class="sxs-lookup"><span data-stu-id="d5078-117">-Context</span></span>
<span data-ttu-id="d5078-118">Указывает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="d5078-118">Specifies the storage context.</span></span>
<span data-ttu-id="d5078-119">Чтобы создать его, можно использовать командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d5078-119">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d5078-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5078-120">-DefaultProfile</span></span>
<span data-ttu-id="d5078-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5078-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5078-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d5078-122">-Name</span></span>
<span data-ttu-id="d5078-123">Указывает имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="d5078-123">Specifies the table name.</span></span>
<span data-ttu-id="d5078-124">Если имя таблицы пусто, командлет выводит список всех таблиц.</span><span class="sxs-lookup"><span data-stu-id="d5078-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="d5078-125">В противном случае выводится список всех таблиц, соответствующих указанному имени или шаблону обычного имени.</span><span class="sxs-lookup"><span data-stu-id="d5078-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5078-126">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="d5078-126">-Prefix</span></span>
<span data-ttu-id="d5078-127">Задает префикс, используемый в имени таблицы или таблиц, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="d5078-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="d5078-128">Вы можете использовать этот параметр, чтобы найти все таблицы, которые начинаются с одной строки, например Table.</span><span class="sxs-lookup"><span data-stu-id="d5078-128">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: System.String
Parameter Sets: TablePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5078-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5078-129">CommonParameters</span></span>
<span data-ttu-id="d5078-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5078-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5078-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5078-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5078-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5078-132">INPUTS</span></span>

### <span data-ttu-id="d5078-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d5078-133">System.String</span></span>

### <span data-ttu-id="d5078-134">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d5078-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d5078-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5078-135">OUTPUTS</span></span>

### <span data-ttu-id="d5078-136">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d5078-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="d5078-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5078-137">NOTES</span></span>

## <span data-ttu-id="d5078-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5078-138">RELATED LINKS</span></span>

[<span data-ttu-id="d5078-139">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="d5078-139">New-AzStorageTable</span></span>](./New-AzStorageTable.md)

[<span data-ttu-id="d5078-140">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="d5078-140">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


