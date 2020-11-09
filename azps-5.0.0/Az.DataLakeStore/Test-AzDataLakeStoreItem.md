---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
ms.openlocfilehash: 1629e987386998e642df1390ec391444500a6c44
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313208"
---
# <span data-ttu-id="c6e9f-101">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c6e9f-101">Test-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="c6e9f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6e9f-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e9f-103">Проверка существования файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c6e9f-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c6e9f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6e9f-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6e9f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6e9f-105">DESCRIPTION</span></span>
<span data-ttu-id="c6e9f-106">Командлет **Test-AzDataLakeStoreItem** проверяет наличие файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c6e9f-106">The **Test-AzDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c6e9f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6e9f-107">EXAMPLES</span></span>

### <span data-ttu-id="c6e9f-108">Пример 1: Проверка файла</span><span class="sxs-lookup"><span data-stu-id="c6e9f-108">Example 1: Test a file</span></span>
```powershell
PS C:\>Test-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="c6e9f-109">Эта команда проверяет, существует ли Test.csv файла в учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="c6e9f-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

### <span data-ttu-id="c6e9f-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c6e9f-110">Example 2</span></span>

<span data-ttu-id="c6e9f-111">Проверка существования файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c6e9f-111">Tests the existence of a file or folder in Data Lake Store.</span></span> <span data-ttu-id="c6e9f-112">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="c6e9f-112">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Test-AzDataLakeStoreItem -Account 'ContosoADL' -Path '/MyFiles/Test.csv' -PathType Any
```

## <span data-ttu-id="c6e9f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6e9f-113">PARAMETERS</span></span>

### <span data-ttu-id="c6e9f-114">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c6e9f-114">-Account</span></span>
<span data-ttu-id="c6e9f-115">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c6e9f-115">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c6e9f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6e9f-116">-DefaultProfile</span></span>
<span data-ttu-id="c6e9f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6e9f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6e9f-118">-Path</span><span class="sxs-lookup"><span data-stu-id="c6e9f-118">-Path</span></span>
<span data-ttu-id="c6e9f-119">Указывает путь к Data Lake Store для тестируемого элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="c6e9f-119">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c6e9f-120">-PathType</span><span class="sxs-lookup"><span data-stu-id="c6e9f-120">-PathType</span></span>
<span data-ttu-id="c6e9f-121">Указывает тип проверяемого элемента.</span><span class="sxs-lookup"><span data-stu-id="c6e9f-121">Specifies the type of item to test.</span></span>
<span data-ttu-id="c6e9f-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c6e9f-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6e9f-123">Необходимые</span><span class="sxs-lookup"><span data-stu-id="c6e9f-123">Any</span></span> 
- <span data-ttu-id="c6e9f-124">Файл</span><span class="sxs-lookup"><span data-stu-id="c6e9f-124">File</span></span> 
- <span data-ttu-id="c6e9f-125">Нее</span><span class="sxs-lookup"><span data-stu-id="c6e9f-125">Folder</span></span>

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

### <span data-ttu-id="c6e9f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e9f-126">CommonParameters</span></span>
<span data-ttu-id="c6e9f-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6e9f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e9f-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6e9f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e9f-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6e9f-129">INPUTS</span></span>

### <span data-ttu-id="c6e9f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c6e9f-130">System.String</span></span>

### <span data-ttu-id="c6e9f-131">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="c6e9f-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="c6e9f-132">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + PathType</span><span class="sxs-lookup"><span data-stu-id="c6e9f-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="c6e9f-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6e9f-133">OUTPUTS</span></span>

### <span data-ttu-id="c6e9f-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c6e9f-134">System.Boolean</span></span>

## <span data-ttu-id="c6e9f-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6e9f-135">NOTES</span></span>

## <span data-ttu-id="c6e9f-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6e9f-136">RELATED LINKS</span></span>

[<span data-ttu-id="c6e9f-137">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c6e9f-137">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="c6e9f-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c6e9f-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="c6e9f-139">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c6e9f-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="c6e9f-140">Присоединиться к AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c6e9f-140">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="c6e9f-141">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c6e9f-141">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="c6e9f-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c6e9f-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

