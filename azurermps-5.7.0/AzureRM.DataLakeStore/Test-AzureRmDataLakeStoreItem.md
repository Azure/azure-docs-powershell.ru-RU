---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: bf754e335753efc5350d3c0979db9f0f7057f010
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734033"
---
# <span data-ttu-id="666b0-101">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="666b0-101">Test-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="666b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="666b0-102">SYNOPSIS</span></span>
<span data-ttu-id="666b0-103">Проверка существования файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="666b0-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="666b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="666b0-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="666b0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="666b0-105">DESCRIPTION</span></span>
<span data-ttu-id="666b0-106">Командлет **Test-AzureRmDataLakeStoreItem** проверяет наличие файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="666b0-106">The **Test-AzureRmDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="666b0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="666b0-107">EXAMPLES</span></span>

### <span data-ttu-id="666b0-108">Пример 1: Проверка файла</span><span class="sxs-lookup"><span data-stu-id="666b0-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="666b0-109">Эта команда проверяет, существует ли Test.csv файла в учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="666b0-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="666b0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="666b0-110">PARAMETERS</span></span>

### <span data-ttu-id="666b0-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="666b0-111">-Account</span></span>
<span data-ttu-id="666b0-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="666b0-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="666b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="666b0-113">-DefaultProfile</span></span>
<span data-ttu-id="666b0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="666b0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666b0-115">-Path</span><span class="sxs-lookup"><span data-stu-id="666b0-115">-Path</span></span>
<span data-ttu-id="666b0-116">Указывает путь к Data Lake Store для тестируемого элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="666b0-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="666b0-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="666b0-117">-PathType</span></span>
<span data-ttu-id="666b0-118">Указывает тип проверяемого элемента.</span><span class="sxs-lookup"><span data-stu-id="666b0-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="666b0-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="666b0-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="666b0-120">Необходимые</span><span class="sxs-lookup"><span data-stu-id="666b0-120">Any</span></span> 
- <span data-ttu-id="666b0-121">Файл</span><span class="sxs-lookup"><span data-stu-id="666b0-121">File</span></span> 
- <span data-ttu-id="666b0-122">Нее</span><span class="sxs-lookup"><span data-stu-id="666b0-122">Folder</span></span>

```yaml
Type: PathType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, File, Folder

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="666b0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="666b0-123">CommonParameters</span></span>
<span data-ttu-id="666b0-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="666b0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="666b0-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="666b0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="666b0-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="666b0-126">INPUTS</span></span>

### <span data-ttu-id="666b0-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="666b0-127">None</span></span>
<span data-ttu-id="666b0-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="666b0-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="666b0-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="666b0-129">OUTPUTS</span></span>

### <span data-ttu-id="666b0-130">логических</span><span class="sxs-lookup"><span data-stu-id="666b0-130">bool</span></span>
<span data-ttu-id="666b0-131">Значение true или false, указывающее на существование указанного файла или папки.</span><span class="sxs-lookup"><span data-stu-id="666b0-131">True or false indicating the existence of the specified file or folder.</span></span>

## <span data-ttu-id="666b0-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="666b0-132">NOTES</span></span>

## <span data-ttu-id="666b0-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="666b0-133">RELATED LINKS</span></span>

[<span data-ttu-id="666b0-134">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="666b0-134">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="666b0-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="666b0-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="666b0-136">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="666b0-136">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="666b0-137">Присоединиться к AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="666b0-137">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="666b0-138">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="666b0-138">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="666b0-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="666b0-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)


