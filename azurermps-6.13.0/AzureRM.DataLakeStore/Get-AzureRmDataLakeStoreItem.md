---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a1e70286364fea53062a75b7ac886834803c3674
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568185"
---
# <span data-ttu-id="e9f94-101">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e9f94-101">Get-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="e9f94-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e9f94-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f94-103">Получает сведения о файле или папке в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e9f94-103">Gets the details of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9f94-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e9f94-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9f94-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9f94-105">DESCRIPTION</span></span>
<span data-ttu-id="e9f94-106">Командлет **Get-AzureRmDataLakeStoreItem** получает сведения о файле или папке в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e9f94-106">The **Get-AzureRmDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e9f94-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e9f94-107">EXAMPLES</span></span>

### <span data-ttu-id="e9f94-108">Пример 1: получение сведений о файле из Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="e9f94-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="e9f94-109">Эта команда получает сведения о файле Test.csv из Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e9f94-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="e9f94-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e9f94-110">PARAMETERS</span></span>

### <span data-ttu-id="e9f94-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="e9f94-111">-Account</span></span>
<span data-ttu-id="e9f94-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e9f94-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e9f94-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9f94-113">-DefaultProfile</span></span>
<span data-ttu-id="e9f94-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9f94-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9f94-115">-Path</span><span class="sxs-lookup"><span data-stu-id="e9f94-115">-Path</span></span>
<span data-ttu-id="e9f94-116">Указывает путь к Data Lake Store, из которого требуется получить сведения об элементе, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="e9f94-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="e9f94-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f94-117">CommonParameters</span></span>
<span data-ttu-id="e9f94-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e9f94-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f94-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9f94-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f94-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e9f94-120">INPUTS</span></span>

### <span data-ttu-id="e9f94-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e9f94-121">System.String</span></span>

### <span data-ttu-id="e9f94-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="e9f94-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="e9f94-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9f94-123">OUTPUTS</span></span>

### <span data-ttu-id="e9f94-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e9f94-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="e9f94-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="e9f94-125">NOTES</span></span>

## <span data-ttu-id="e9f94-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9f94-126">RELATED LINKS</span></span>

[<span data-ttu-id="e9f94-127">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e9f94-127">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e9f94-128">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="e9f94-128">Get-AzureRmDataLakeStoreChildItem</span></span>](./Get-AzureRmDataLakeStoreChildItem.md)

[<span data-ttu-id="e9f94-129">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e9f94-129">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e9f94-130">Присоединиться к AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e9f94-130">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e9f94-131">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e9f94-131">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e9f94-132">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e9f94-132">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e9f94-133">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e9f94-133">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e9f94-134">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e9f94-134">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


