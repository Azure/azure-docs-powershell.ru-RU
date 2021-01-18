---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507702"
---
# <span data-ttu-id="db90e-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="db90e-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="db90e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db90e-102">SYNOPSIS</span></span>
<span data-ttu-id="db90e-103">Создание объекта диапазона BLOB-объектов для восстановления учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="db90e-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="db90e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="db90e-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db90e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db90e-105">DESCRIPTION</span></span>
<span data-ttu-id="db90e-106">**Cmdlet New-AzStorageBlobRangeToRestore** создает объект диапазона BLOB-объектов, который можно использовать в restore-AzStorageBlobRange.</span><span class="sxs-lookup"><span data-stu-id="db90e-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="db90e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="db90e-107">EXAMPLES</span></span>

### <span data-ttu-id="db90e-108">Пример 1. Создание диапазона lob-lob для восстановления</span><span class="sxs-lookup"><span data-stu-id="db90e-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="db90e-109">Эта команда создает диапазон BLOB-целей для восстановления, который начинается с контейнера1/blob1 (включая) и заканчивается на container2/blob2 (исключая).</span><span class="sxs-lookup"><span data-stu-id="db90e-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="db90e-110">Пример 2. Создание диапазона lob-lob, который будет восстанавливать из первого BLOB-решения в алфавитном порядке в определенный (исключаемая)</span><span class="sxs-lookup"><span data-stu-id="db90e-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="db90e-111">Эта команда создает диапазон BLOB-lob, который будет восстанавливать из первого BLOB-части в алфавитном порядке в определенный контейнер BLOB-2/blob2 (исключая).</span><span class="sxs-lookup"><span data-stu-id="db90e-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="db90e-112">Пример 3. Создание диапазона lob-lob, который будет восстанавливать из определенного BLOB-решения (включая) в последний BLOB-проект в алфавитном порядке</span><span class="sxs-lookup"><span data-stu-id="db90e-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="db90e-113">Эта команда создает диапазон BLOB-то, который будет восстановлен из определенного контейнера BLOB-1/blob1 (включая) в последний BLOB-проект в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="db90e-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="db90e-114">Пример 4. Создание диапазона lob-lob,который будет восстанавливать все BLOB-бизнесы</span><span class="sxs-lookup"><span data-stu-id="db90e-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="db90e-115">Эта команда создает диапазон BLOB-команд, который будет восстанавливать все BLOB-lob-ы.</span><span class="sxs-lookup"><span data-stu-id="db90e-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="db90e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db90e-116">PARAMETERS</span></span>

### <span data-ttu-id="db90e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db90e-117">-DefaultProfile</span></span>
<span data-ttu-id="db90e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db90e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db90e-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="db90e-119">-EndRange</span></span>
<span data-ttu-id="db90e-120">Укажите диапазон восстановления BLOB-то еще.</span><span class="sxs-lookup"><span data-stu-id="db90e-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="db90e-121">Конечный диапазон исключается из BLOB-тона восстановления.</span><span class="sxs-lookup"><span data-stu-id="db90e-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="db90e-122">Настроив его в качестве пустой strng, можно восстановить до конца.</span><span class="sxs-lookup"><span data-stu-id="db90e-122">Set it as empty strng to restore to the end.</span></span>

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

### <span data-ttu-id="db90e-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="db90e-123">-StartRange</span></span>
<span data-ttu-id="db90e-124">Укажите диапазон начала восстановления BLOB-ля.</span><span class="sxs-lookup"><span data-stu-id="db90e-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="db90e-125">Диапазон запуска будет включен в список BLOB-тонов восстановления.</span><span class="sxs-lookup"><span data-stu-id="db90e-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="db90e-126">Настроив ее как пустую строку для восстановления с начала.</span><span class="sxs-lookup"><span data-stu-id="db90e-126">Set it as empty string to restore from begining.</span></span>

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

### <span data-ttu-id="db90e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db90e-127">CommonParameters</span></span>
<span data-ttu-id="db90e-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db90e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db90e-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db90e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db90e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db90e-130">INPUTS</span></span>

### <span data-ttu-id="db90e-131">Нет</span><span class="sxs-lookup"><span data-stu-id="db90e-131">None</span></span>

## <span data-ttu-id="db90e-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="db90e-132">OUTPUTS</span></span>

### <span data-ttu-id="db90e-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="db90e-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="db90e-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="db90e-134">NOTES</span></span>

## <span data-ttu-id="db90e-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db90e-135">RELATED LINKS</span></span>
