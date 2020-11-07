---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
ms.openlocfilehash: 83f44ced24587340f063f24a17036184115cf299
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93913034"
---
# <span data-ttu-id="9af69-101">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9af69-101">Test-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="9af69-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9af69-102">SYNOPSIS</span></span>
<span data-ttu-id="9af69-103">Проверка существования файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9af69-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9af69-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9af69-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9af69-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9af69-105">DESCRIPTION</span></span>
<span data-ttu-id="9af69-106">Командлет **Test-AzDataLakeStoreItem** проверяет наличие файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9af69-106">The **Test-AzDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9af69-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9af69-107">EXAMPLES</span></span>

### <span data-ttu-id="9af69-108">Пример 1: Проверка файла</span><span class="sxs-lookup"><span data-stu-id="9af69-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="9af69-109">Эта команда проверяет, существует ли Test.csv файла в учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="9af69-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="9af69-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9af69-110">PARAMETERS</span></span>

### <span data-ttu-id="9af69-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="9af69-111">-Account</span></span>
<span data-ttu-id="9af69-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9af69-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af69-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af69-113">-DefaultProfile</span></span>
<span data-ttu-id="9af69-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9af69-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9af69-115">-Path</span><span class="sxs-lookup"><span data-stu-id="9af69-115">-Path</span></span>
<span data-ttu-id="9af69-116">Указывает путь к Data Lake Store для тестируемого элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="9af69-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af69-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="9af69-117">-PathType</span></span>
<span data-ttu-id="9af69-118">Указывает тип проверяемого элемента.</span><span class="sxs-lookup"><span data-stu-id="9af69-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="9af69-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9af69-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9af69-120">Необходимые</span><span class="sxs-lookup"><span data-stu-id="9af69-120">Any</span></span> 
- <span data-ttu-id="9af69-121">Файл</span><span class="sxs-lookup"><span data-stu-id="9af69-121">File</span></span> 
- <span data-ttu-id="9af69-122">Нее</span><span class="sxs-lookup"><span data-stu-id="9af69-122">Folder</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType
Parameter Sets: (All)
Aliases:
Accepted values: Any, File, Folder

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af69-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af69-123">CommonParameters</span></span>
<span data-ttu-id="9af69-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9af69-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af69-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9af69-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af69-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9af69-126">INPUTS</span></span>

### <span data-ttu-id="9af69-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9af69-127">System.String</span></span>

### <span data-ttu-id="9af69-128">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="9af69-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="9af69-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + PathType</span><span class="sxs-lookup"><span data-stu-id="9af69-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="9af69-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9af69-130">OUTPUTS</span></span>

### <span data-ttu-id="9af69-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9af69-131">System.Boolean</span></span>

## <span data-ttu-id="9af69-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="9af69-132">NOTES</span></span>

## <span data-ttu-id="9af69-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9af69-133">RELATED LINKS</span></span>

[<span data-ttu-id="9af69-134">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9af69-134">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="9af69-135">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9af69-135">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="9af69-136">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9af69-136">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="9af69-137">Присоединиться к AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9af69-137">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="9af69-138">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9af69-138">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="9af69-139">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9af69-139">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)


