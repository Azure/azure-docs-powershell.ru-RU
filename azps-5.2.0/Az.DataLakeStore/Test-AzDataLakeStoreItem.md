---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
ms.openlocfilehash: 1629e987386998e642df1390ec391444500a6c44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417572"
---
# <span data-ttu-id="475d0-101">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="475d0-101">Test-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="475d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="475d0-102">SYNOPSIS</span></span>
<span data-ttu-id="475d0-103">Проверяет, существует ли файл или папка в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="475d0-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="475d0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="475d0-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="475d0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="475d0-105">DESCRIPTION</span></span>
<span data-ttu-id="475d0-106">**Cmdlet Test-AzDataLakeStoreItem** проверяет наличие файлов или папок в магазине Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="475d0-106">The **Test-AzDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="475d0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="475d0-107">EXAMPLES</span></span>

### <span data-ttu-id="475d0-108">Пример 1. Проверка файла</span><span class="sxs-lookup"><span data-stu-id="475d0-108">Example 1: Test a file</span></span>
```powershell
PS C:\>Test-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="475d0-109">Эта команда проверяет, существует ли Test.csv в учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="475d0-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

### <span data-ttu-id="475d0-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="475d0-110">Example 2</span></span>

<span data-ttu-id="475d0-111">Проверяет, существует ли файл или папка в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="475d0-111">Tests the existence of a file or folder in Data Lake Store.</span></span> <span data-ttu-id="475d0-112">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="475d0-112">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Test-AzDataLakeStoreItem -Account 'ContosoADL' -Path '/MyFiles/Test.csv' -PathType Any
```

## <span data-ttu-id="475d0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="475d0-113">PARAMETERS</span></span>

### <span data-ttu-id="475d0-114">-Account</span><span class="sxs-lookup"><span data-stu-id="475d0-114">-Account</span></span>
<span data-ttu-id="475d0-115">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="475d0-115">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="475d0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="475d0-116">-DefaultProfile</span></span>
<span data-ttu-id="475d0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="475d0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="475d0-118">-Path</span><span class="sxs-lookup"><span data-stu-id="475d0-118">-Path</span></span>
<span data-ttu-id="475d0-119">Путь к тестуемого элемента в data Lake Store, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="475d0-119">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="475d0-120">-PathType</span><span class="sxs-lookup"><span data-stu-id="475d0-120">-PathType</span></span>
<span data-ttu-id="475d0-121">Определяет тип проверяемого элемента.</span><span class="sxs-lookup"><span data-stu-id="475d0-121">Specifies the type of item to test.</span></span>
<span data-ttu-id="475d0-122">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="475d0-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="475d0-123">Любая</span><span class="sxs-lookup"><span data-stu-id="475d0-123">Any</span></span> 
- <span data-ttu-id="475d0-124">Файл</span><span class="sxs-lookup"><span data-stu-id="475d0-124">File</span></span> 
- <span data-ttu-id="475d0-125">Папка</span><span class="sxs-lookup"><span data-stu-id="475d0-125">Folder</span></span>

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

### <span data-ttu-id="475d0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="475d0-126">CommonParameters</span></span>
<span data-ttu-id="475d0-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="475d0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="475d0-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="475d0-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="475d0-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="475d0-129">INPUTS</span></span>

### <span data-ttu-id="475d0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="475d0-130">System.String</span></span>

### <span data-ttu-id="475d0-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="475d0-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="475d0-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span><span class="sxs-lookup"><span data-stu-id="475d0-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="475d0-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="475d0-133">OUTPUTS</span></span>

### <span data-ttu-id="475d0-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="475d0-134">System.Boolean</span></span>

## <span data-ttu-id="475d0-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="475d0-135">NOTES</span></span>

## <span data-ttu-id="475d0-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="475d0-136">RELATED LINKS</span></span>

[<span data-ttu-id="475d0-137">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="475d0-137">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="475d0-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="475d0-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="475d0-139">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="475d0-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="475d0-140">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="475d0-140">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="475d0-141">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="475d0-141">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="475d0-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="475d0-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

