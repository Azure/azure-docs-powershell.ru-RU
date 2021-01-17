---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d501faaebcc5e381dc2a7270c8b55b148e2812b4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422743"
---
# <span data-ttu-id="3fc54-101">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="3fc54-101">Get-AzStorageTable</span></span>

## <span data-ttu-id="3fc54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fc54-102">SYNOPSIS</span></span>
<span data-ttu-id="3fc54-103">Список таблиц хранилища.</span><span class="sxs-lookup"><span data-stu-id="3fc54-103">Lists the storage tables.</span></span>

## <span data-ttu-id="3fc54-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3fc54-104">SYNTAX</span></span>

### <span data-ttu-id="3fc54-105">TableName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3fc54-105">TableName (Default)</span></span>
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3fc54-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="3fc54-106">TablePrefix</span></span>
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3fc54-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fc54-107">DESCRIPTION</span></span>
<span data-ttu-id="3fc54-108">С **помощью cmdlet Get-AzStorageTable вы** можете перечислить таблицы хранилища, связанные с учетной записью хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="3fc54-108">The **Get-AzStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="3fc54-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3fc54-109">EXAMPLES</span></span>

### <span data-ttu-id="3fc54-110">Пример 1. Список всех таблиц хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="3fc54-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzStorageTable
```

<span data-ttu-id="3fc54-111">Эта команда получает все таблицы хранилища для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3fc54-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="3fc54-112">Пример 2. Список таблиц хранилища Azure с использованием поддеревного знака</span><span class="sxs-lookup"><span data-stu-id="3fc54-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzStorageTable -Name table*
```

<span data-ttu-id="3fc54-113">Для получения таблиц хранения, имена которых начинаются с таблицы, используются поддиавные знаки.</span><span class="sxs-lookup"><span data-stu-id="3fc54-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="3fc54-114">Пример 3. Список таблиц хранилища Azure с использованием префикса имени таблицы</span><span class="sxs-lookup"><span data-stu-id="3fc54-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

<span data-ttu-id="3fc54-115">Для получения таблиц *хранения,* имена которых начинаются с таблицы, используется параметр "Префикс".</span><span class="sxs-lookup"><span data-stu-id="3fc54-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="3fc54-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fc54-116">PARAMETERS</span></span>

### <span data-ttu-id="3fc54-117">-Контекст</span><span class="sxs-lookup"><span data-stu-id="3fc54-117">-Context</span></span>
<span data-ttu-id="3fc54-118">Определяет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="3fc54-118">Specifies the storage context.</span></span>
<span data-ttu-id="3fc54-119">Для этого можно использовать New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="3fc54-119">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3fc54-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fc54-120">-DefaultProfile</span></span>
<span data-ttu-id="3fc54-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3fc54-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fc54-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3fc54-122">-Name</span></span>
<span data-ttu-id="3fc54-123">Указывает имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="3fc54-123">Specifies the table name.</span></span>
<span data-ttu-id="3fc54-124">Если имя таблицы пустое, в этом списке будут перечислены все таблицы.</span><span class="sxs-lookup"><span data-stu-id="3fc54-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="3fc54-125">В противном случае будут перечислены все таблицы, которые соответствуют указанному имени или шаблону обычного имени.</span><span class="sxs-lookup"><span data-stu-id="3fc54-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="3fc54-126">-Префикс</span><span class="sxs-lookup"><span data-stu-id="3fc54-126">-Prefix</span></span>
<span data-ttu-id="3fc54-127">Указывает префикс, используемый в имени нужной таблицы или таблиц.</span><span class="sxs-lookup"><span data-stu-id="3fc54-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="3fc54-128">С помощью этой строки можно найти все таблицы, которые начинаются с одной и той же строки, например таблицы.</span><span class="sxs-lookup"><span data-stu-id="3fc54-128">You can use this to find all tables that start with the same string, such as table.</span></span>

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

### <span data-ttu-id="3fc54-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fc54-129">CommonParameters</span></span>
<span data-ttu-id="3fc54-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fc54-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fc54-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fc54-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fc54-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3fc54-132">INPUTS</span></span>

### <span data-ttu-id="3fc54-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3fc54-133">System.String</span></span>

### <span data-ttu-id="3fc54-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3fc54-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3fc54-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3fc54-135">OUTPUTS</span></span>

### <span data-ttu-id="3fc54-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="3fc54-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="3fc54-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3fc54-137">NOTES</span></span>

## <span data-ttu-id="3fc54-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3fc54-138">RELATED LINKS</span></span>

[<span data-ttu-id="3fc54-139">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="3fc54-139">New-AzStorageTable</span></span>](./New-AzStorageTable.md)

[<span data-ttu-id="3fc54-140">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="3fc54-140">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


