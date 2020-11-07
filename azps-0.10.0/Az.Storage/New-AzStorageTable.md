---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 29b2bb0c6a9c6e8e34c08a7ce04ca1c3ed071c84
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910713"
---
# <span data-ttu-id="244f6-101">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="244f6-101">New-AzStorageTable</span></span>

## <span data-ttu-id="244f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="244f6-102">SYNOPSIS</span></span>
<span data-ttu-id="244f6-103">Создание таблицы хранилища.</span><span class="sxs-lookup"><span data-stu-id="244f6-103">Creates a storage table.</span></span>

## <span data-ttu-id="244f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="244f6-104">SYNTAX</span></span>

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="244f6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="244f6-105">DESCRIPTION</span></span>
<span data-ttu-id="244f6-106">Командлет **New-AzStorageTable** создает таблицу хранилища, связанную с учетной записью хранения в Azure.</span><span class="sxs-lookup"><span data-stu-id="244f6-106">The **New-AzStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="244f6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="244f6-107">EXAMPLES</span></span>

### <span data-ttu-id="244f6-108">Пример 1: создание таблицы хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="244f6-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

<span data-ttu-id="244f6-109">Эта команда создает таблицу хранилища с именем tableabc.</span><span class="sxs-lookup"><span data-stu-id="244f6-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="244f6-110">Пример 2: создание нескольких таблиц хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="244f6-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

<span data-ttu-id="244f6-111">Эта команда создает несколько таблиц.</span><span class="sxs-lookup"><span data-stu-id="244f6-111">This command creates multiple tables.</span></span>
<span data-ttu-id="244f6-112">Он использует метод **Split** класса **String** .NET и передает имена в конвейере.</span><span class="sxs-lookup"><span data-stu-id="244f6-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="244f6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="244f6-113">PARAMETERS</span></span>

### <span data-ttu-id="244f6-114">-Context</span><span class="sxs-lookup"><span data-stu-id="244f6-114">-Context</span></span>
<span data-ttu-id="244f6-115">Указывает контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="244f6-115">Specifies the storage context.</span></span>
<span data-ttu-id="244f6-116">Чтобы создать его, можно использовать командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="244f6-116">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="244f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="244f6-117">-DefaultProfile</span></span>
<span data-ttu-id="244f6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="244f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="244f6-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="244f6-119">-Name</span></span>
<span data-ttu-id="244f6-120">Задает имя новой таблицы.</span><span class="sxs-lookup"><span data-stu-id="244f6-120">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="244f6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="244f6-121">CommonParameters</span></span>
<span data-ttu-id="244f6-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="244f6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="244f6-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="244f6-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="244f6-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="244f6-124">INPUTS</span></span>

### <span data-ttu-id="244f6-125">System. String</span><span class="sxs-lookup"><span data-stu-id="244f6-125">System.String</span></span>

### <span data-ttu-id="244f6-126">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="244f6-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="244f6-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="244f6-127">OUTPUTS</span></span>

### <span data-ttu-id="244f6-128">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="244f6-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="244f6-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="244f6-129">NOTES</span></span>

## <span data-ttu-id="244f6-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="244f6-130">RELATED LINKS</span></span>

[<span data-ttu-id="244f6-131">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="244f6-131">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)

[<span data-ttu-id="244f6-132">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="244f6-132">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


