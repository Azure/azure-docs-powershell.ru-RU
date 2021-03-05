---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 84b5389c4f9b404b4b74783184143af310bf1ba5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002323"
---
# <span data-ttu-id="4a570-101">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="4a570-101">New-AzStorageTable</span></span>

## <span data-ttu-id="4a570-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a570-102">SYNOPSIS</span></span>
<span data-ttu-id="4a570-103">Создает таблицу хранилища.</span><span class="sxs-lookup"><span data-stu-id="4a570-103">Creates a storage table.</span></span>

## <span data-ttu-id="4a570-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4a570-104">SYNTAX</span></span>

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a570-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a570-105">DESCRIPTION</span></span>
<span data-ttu-id="4a570-106">С **помощью cmdlet New-AzStorageTable** создается таблица хранилища, связанная с учетной записью хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="4a570-106">The **New-AzStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="4a570-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4a570-107">EXAMPLES</span></span>

### <span data-ttu-id="4a570-108">Пример 1. Создание таблицы хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="4a570-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

<span data-ttu-id="4a570-109">Эта команда создает таблицу хранилища с именем tableabc.</span><span class="sxs-lookup"><span data-stu-id="4a570-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="4a570-110">Пример 2. Создание нескольких таблиц хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="4a570-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

<span data-ttu-id="4a570-111">Эта команда создает несколько таблиц.</span><span class="sxs-lookup"><span data-stu-id="4a570-111">This command creates multiple tables.</span></span>
<span data-ttu-id="4a570-112">Для этого используется **метод разделения** класса .NET **String,** который передает имена в конвейере.</span><span class="sxs-lookup"><span data-stu-id="4a570-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="4a570-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a570-113">PARAMETERS</span></span>

### <span data-ttu-id="4a570-114">-Контекст</span><span class="sxs-lookup"><span data-stu-id="4a570-114">-Context</span></span>
<span data-ttu-id="4a570-115">Определяет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="4a570-115">Specifies the storage context.</span></span>
<span data-ttu-id="4a570-116">Для этого можно использовать New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="4a570-116">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4a570-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a570-117">-DefaultProfile</span></span>
<span data-ttu-id="4a570-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a570-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a570-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4a570-119">-Name</span></span>
<span data-ttu-id="4a570-120">Указывает имя новой таблицы.</span><span class="sxs-lookup"><span data-stu-id="4a570-120">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="4a570-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a570-121">CommonParameters</span></span>
<span data-ttu-id="4a570-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a570-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a570-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a570-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a570-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a570-124">INPUTS</span></span>

### <span data-ttu-id="4a570-125">System.String</span><span class="sxs-lookup"><span data-stu-id="4a570-125">System.String</span></span>

### <span data-ttu-id="4a570-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4a570-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4a570-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4a570-127">OUTPUTS</span></span>

### <span data-ttu-id="4a570-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="4a570-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="4a570-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4a570-129">NOTES</span></span>

## <span data-ttu-id="4a570-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a570-130">RELATED LINKS</span></span>

[<span data-ttu-id="4a570-131">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="4a570-131">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)

[<span data-ttu-id="4a570-132">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="4a570-132">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


