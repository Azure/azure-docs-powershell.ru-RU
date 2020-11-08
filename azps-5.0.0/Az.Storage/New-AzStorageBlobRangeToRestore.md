---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247175"
---
# <span data-ttu-id="9fc1e-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="9fc1e-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="9fc1e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9fc1e-102">SYNOPSIS</span></span>
<span data-ttu-id="9fc1e-103">Создает объект диапазона BLOB-объектов для восстановления учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9fc1e-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="9fc1e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9fc1e-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fc1e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fc1e-105">DESCRIPTION</span></span>
<span data-ttu-id="9fc1e-106">Командлет **New-AzStorageBlobRangeToRestore** создает объект диапазона BLOB, который можно использовать в Restore-AzStorageBlobRange.</span><span class="sxs-lookup"><span data-stu-id="9fc1e-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="9fc1e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9fc1e-107">EXAMPLES</span></span>

### <span data-ttu-id="9fc1e-108">Пример 1: Создание диапазона больших двоичных объектов для восстановления</span><span class="sxs-lookup"><span data-stu-id="9fc1e-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="9fc1e-109">Эта команда создает диапазон больших двоичных объектов для восстановления, который начинается с container1/blob1 (include) и заканчивается на container2/blob2 (исключить).</span><span class="sxs-lookup"><span data-stu-id="9fc1e-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="9fc1e-110">Пример 2: создает диапазон BLOB-объектов, который будет восстанавливаться из первого большого двоичного объекта в алфавитном порядке, в определенный блоб (исключить).</span><span class="sxs-lookup"><span data-stu-id="9fc1e-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="9fc1e-111">Эта команда создает диапазон BLOB-объектов, который будет восстанавливаться из первого большого двоичного файла в алфавитном порядке, в определенный блоб container2/blob2 (исключить).</span><span class="sxs-lookup"><span data-stu-id="9fc1e-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="9fc1e-112">Пример 3: создает диапазон BLOB-объектов, который будет восстанавливаться с определенного большого двоичного объекта (include) до последнего BLOB в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="9fc1e-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="9fc1e-113">Эта команда создает диапазон больших двоичных объектов, который будет восстанавливаться с определенного блоба container1/blob1 (include) до последнего BLOB в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="9fc1e-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="9fc1e-114">Пример 4: Создание диапазона BLOB-объектов, в котором будут восстановлены все большие двоичные объекты</span><span class="sxs-lookup"><span data-stu-id="9fc1e-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="9fc1e-115">Эта команда создает диапазон BLOB-объектов, который восстанавливает все большие двоичные объекты.</span><span class="sxs-lookup"><span data-stu-id="9fc1e-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="9fc1e-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9fc1e-116">PARAMETERS</span></span>

### <span data-ttu-id="9fc1e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fc1e-117">-DefaultProfile</span></span>
<span data-ttu-id="9fc1e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9fc1e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc1e-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="9fc1e-119">-EndRange</span></span>
<span data-ttu-id="9fc1e-120">Укажите конечный диапазон для восстановления BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="9fc1e-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="9fc1e-121">Конечный диапазон будет исключен из восстановления больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="9fc1e-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="9fc1e-122">Установите для него пустое strng, чтобы вернуться к концу.</span><span class="sxs-lookup"><span data-stu-id="9fc1e-122">Set it as empty strng to restore to the end.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc1e-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="9fc1e-123">-StartRange</span></span>
<span data-ttu-id="9fc1e-124">Укажите диапазон начала восстановления BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="9fc1e-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="9fc1e-125">Начальный диапазон будет включен в восстановление больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="9fc1e-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="9fc1e-126">Установите для него пустую строку, чтобы восстановить ее с начала.</span><span class="sxs-lookup"><span data-stu-id="9fc1e-126">Set it as empty string to restore from begining.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc1e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fc1e-127">CommonParameters</span></span>
<span data-ttu-id="9fc1e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9fc1e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fc1e-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fc1e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fc1e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9fc1e-130">INPUTS</span></span>

### <span data-ttu-id="9fc1e-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="9fc1e-131">None</span></span>

## <span data-ttu-id="9fc1e-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fc1e-132">OUTPUTS</span></span>

### <span data-ttu-id="9fc1e-133">Microsoft. Azure. Commands. Management. Storage. Models. PSBlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="9fc1e-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="9fc1e-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="9fc1e-134">NOTES</span></span>

## <span data-ttu-id="9fc1e-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9fc1e-135">RELATED LINKS</span></span>
