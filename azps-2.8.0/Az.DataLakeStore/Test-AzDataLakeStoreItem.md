---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
ms.openlocfilehash: c79e8c225fbbc901d9c39eed85d795cf27d6d1d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721257"
---
# <span data-ttu-id="a386d-101">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a386d-101">Test-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="a386d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a386d-102">SYNOPSIS</span></span>
<span data-ttu-id="a386d-103">Проверка существования файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a386d-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a386d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a386d-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a386d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a386d-105">DESCRIPTION</span></span>
<span data-ttu-id="a386d-106">Командлет **Test-AzDataLakeStoreItem** проверяет наличие файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a386d-106">The **Test-AzDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a386d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a386d-107">EXAMPLES</span></span>

### <span data-ttu-id="a386d-108">Пример 1: Проверка файла</span><span class="sxs-lookup"><span data-stu-id="a386d-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="a386d-109">Эта команда проверяет, существует ли Test.csv файла в учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="a386d-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="a386d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a386d-110">PARAMETERS</span></span>

### <span data-ttu-id="a386d-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="a386d-111">-Account</span></span>
<span data-ttu-id="a386d-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a386d-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a386d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a386d-113">-DefaultProfile</span></span>
<span data-ttu-id="a386d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a386d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a386d-115">-Path</span><span class="sxs-lookup"><span data-stu-id="a386d-115">-Path</span></span>
<span data-ttu-id="a386d-116">Указывает путь к Data Lake Store для тестируемого элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="a386d-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="a386d-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="a386d-117">-PathType</span></span>
<span data-ttu-id="a386d-118">Указывает тип проверяемого элемента.</span><span class="sxs-lookup"><span data-stu-id="a386d-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="a386d-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a386d-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a386d-120">Необходимые</span><span class="sxs-lookup"><span data-stu-id="a386d-120">Any</span></span> 
- <span data-ttu-id="a386d-121">Файл</span><span class="sxs-lookup"><span data-stu-id="a386d-121">File</span></span> 
- <span data-ttu-id="a386d-122">Нее</span><span class="sxs-lookup"><span data-stu-id="a386d-122">Folder</span></span>

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

### <span data-ttu-id="a386d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a386d-123">CommonParameters</span></span>
<span data-ttu-id="a386d-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a386d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a386d-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a386d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a386d-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a386d-126">INPUTS</span></span>

### <span data-ttu-id="a386d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a386d-127">System.String</span></span>

### <span data-ttu-id="a386d-128">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="a386d-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="a386d-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + PathType</span><span class="sxs-lookup"><span data-stu-id="a386d-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="a386d-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a386d-130">OUTPUTS</span></span>

### <span data-ttu-id="a386d-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a386d-131">System.Boolean</span></span>

## <span data-ttu-id="a386d-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="a386d-132">NOTES</span></span>

## <span data-ttu-id="a386d-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a386d-133">RELATED LINKS</span></span>

[<span data-ttu-id="a386d-134">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a386d-134">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="a386d-135">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a386d-135">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="a386d-136">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a386d-136">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="a386d-137">Присоединиться к AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a386d-137">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="a386d-138">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a386d-138">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="a386d-139">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a386d-139">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)


