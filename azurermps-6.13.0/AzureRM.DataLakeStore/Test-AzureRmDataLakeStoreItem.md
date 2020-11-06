---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: e9410c8bd63a123f275f6e644971870b998deea0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567762"
---
# <span data-ttu-id="c8596-101">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c8596-101">Test-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="c8596-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8596-102">SYNOPSIS</span></span>
<span data-ttu-id="c8596-103">Проверка существования файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c8596-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8596-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8596-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8596-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8596-105">DESCRIPTION</span></span>
<span data-ttu-id="c8596-106">Командлет **Test-AzureRmDataLakeStoreItem** проверяет наличие файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c8596-106">The **Test-AzureRmDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c8596-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8596-107">EXAMPLES</span></span>

### <span data-ttu-id="c8596-108">Пример 1: Проверка файла</span><span class="sxs-lookup"><span data-stu-id="c8596-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="c8596-109">Эта команда проверяет, существует ли Test.csv файла в учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="c8596-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="c8596-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8596-110">PARAMETERS</span></span>

### <span data-ttu-id="c8596-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c8596-111">-Account</span></span>
<span data-ttu-id="c8596-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c8596-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c8596-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8596-113">-DefaultProfile</span></span>
<span data-ttu-id="c8596-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8596-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8596-115">-Path</span><span class="sxs-lookup"><span data-stu-id="c8596-115">-Path</span></span>
<span data-ttu-id="c8596-116">Указывает путь к Data Lake Store для тестируемого элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="c8596-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c8596-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="c8596-117">-PathType</span></span>
<span data-ttu-id="c8596-118">Указывает тип проверяемого элемента.</span><span class="sxs-lookup"><span data-stu-id="c8596-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="c8596-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c8596-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c8596-120">Необходимые</span><span class="sxs-lookup"><span data-stu-id="c8596-120">Any</span></span> 
- <span data-ttu-id="c8596-121">Файл</span><span class="sxs-lookup"><span data-stu-id="c8596-121">File</span></span> 
- <span data-ttu-id="c8596-122">Нее</span><span class="sxs-lookup"><span data-stu-id="c8596-122">Folder</span></span>

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

### <span data-ttu-id="c8596-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8596-123">CommonParameters</span></span>
<span data-ttu-id="c8596-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8596-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8596-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8596-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8596-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8596-126">INPUTS</span></span>

### <span data-ttu-id="c8596-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c8596-127">System.String</span></span>

### <span data-ttu-id="c8596-128">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="c8596-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="c8596-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + PathType</span><span class="sxs-lookup"><span data-stu-id="c8596-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="c8596-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8596-130">OUTPUTS</span></span>

### <span data-ttu-id="c8596-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c8596-131">System.Boolean</span></span>

## <span data-ttu-id="c8596-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8596-132">NOTES</span></span>

## <span data-ttu-id="c8596-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8596-133">RELATED LINKS</span></span>

[<span data-ttu-id="c8596-134">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c8596-134">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c8596-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c8596-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c8596-136">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c8596-136">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c8596-137">Присоединиться к AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c8596-137">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c8596-138">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c8596-138">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c8596-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c8596-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)


