---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: b1a570d2821606944d4afde21919dad8832ed380
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732266"
---
# <span data-ttu-id="707c0-101">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="707c0-101">Get-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="707c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="707c0-102">SYNOPSIS</span></span>
<span data-ttu-id="707c0-103">Получает сведения о файле или папке в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="707c0-103">Gets the details of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="707c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="707c0-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="707c0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="707c0-105">DESCRIPTION</span></span>
<span data-ttu-id="707c0-106">Командлет **Get-AzureRmDataLakeStoreItem** получает сведения о файле или папке в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="707c0-106">The **Get-AzureRmDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="707c0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="707c0-107">EXAMPLES</span></span>

### <span data-ttu-id="707c0-108">Пример 1: получение сведений о файле из Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="707c0-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="707c0-109">Эта команда получает сведения о файле Test.csv из Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="707c0-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="707c0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="707c0-110">PARAMETERS</span></span>

### <span data-ttu-id="707c0-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="707c0-111">-Account</span></span>
<span data-ttu-id="707c0-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="707c0-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="707c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="707c0-113">-DefaultProfile</span></span>
<span data-ttu-id="707c0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="707c0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="707c0-115">-Path</span><span class="sxs-lookup"><span data-stu-id="707c0-115">-Path</span></span>
<span data-ttu-id="707c0-116">Указывает путь к Data Lake Store, из которого требуется получить сведения об элементе, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="707c0-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="707c0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="707c0-117">CommonParameters</span></span>
<span data-ttu-id="707c0-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="707c0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="707c0-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="707c0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="707c0-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="707c0-120">INPUTS</span></span>

### <span data-ttu-id="707c0-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="707c0-121">None</span></span>
<span data-ttu-id="707c0-122">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="707c0-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="707c0-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="707c0-123">OUTPUTS</span></span>

### <span data-ttu-id="707c0-124">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="707c0-124">DataLakeStoreItem</span></span>
<span data-ttu-id="707c0-125">Файл или папка по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="707c0-125">The file or folder at the path specified.</span></span>

## <span data-ttu-id="707c0-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="707c0-126">NOTES</span></span>

## <span data-ttu-id="707c0-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="707c0-127">RELATED LINKS</span></span>

[<span data-ttu-id="707c0-128">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="707c0-128">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="707c0-129">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="707c0-129">Get-AzureRmDataLakeStoreChildItem</span></span>](./Get-AzureRmDataLakeStoreChildItem.md)

[<span data-ttu-id="707c0-130">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="707c0-130">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="707c0-131">Присоединиться к AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="707c0-131">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="707c0-132">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="707c0-132">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="707c0-133">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="707c0-133">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="707c0-134">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="707c0-134">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="707c0-135">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="707c0-135">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


