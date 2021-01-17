---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: ad741d955399b355534074737741b153d8d48690
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402543"
---
# <span data-ttu-id="a7ee6-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a7ee6-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="a7ee6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7ee6-102">SYNOPSIS</span></span>
<span data-ttu-id="a7ee6-103">Получает сведения о файле или папке в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a7ee6-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a7ee6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a7ee6-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7ee6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7ee6-105">DESCRIPTION</span></span>
<span data-ttu-id="a7ee6-106">Для получения сведений о файле или папке в магазине Data Lake Store можно получить подробные сведения о файле или папке **Get-AzDataLakeStoreItem.**</span><span class="sxs-lookup"><span data-stu-id="a7ee6-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a7ee6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a7ee6-107">EXAMPLES</span></span>

### <span data-ttu-id="a7ee6-108">Пример 1. Просмотр сведений о файле из магазина Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="a7ee6-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="a7ee6-109">Эта команда получает сведения о файлеTest.csv из магазина Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a7ee6-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="a7ee6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7ee6-110">PARAMETERS</span></span>

### <span data-ttu-id="a7ee6-111">-Account</span><span class="sxs-lookup"><span data-stu-id="a7ee6-111">-Account</span></span>
<span data-ttu-id="a7ee6-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a7ee6-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a7ee6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7ee6-113">-DefaultProfile</span></span>
<span data-ttu-id="a7ee6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7ee6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7ee6-115">-Path</span><span class="sxs-lookup"><span data-stu-id="a7ee6-115">-Path</span></span>
<span data-ttu-id="a7ee6-116">Путь к магазину данных для получения сведений об элементе, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="a7ee6-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="a7ee6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7ee6-117">CommonParameters</span></span>
<span data-ttu-id="a7ee6-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7ee6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7ee6-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7ee6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7ee6-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7ee6-120">INPUTS</span></span>

### <span data-ttu-id="a7ee6-121">System.String</span><span class="sxs-lookup"><span data-stu-id="a7ee6-121">System.String</span></span>

### <span data-ttu-id="a7ee6-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="a7ee6-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="a7ee6-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7ee6-123">OUTPUTS</span></span>

### <span data-ttu-id="a7ee6-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a7ee6-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="a7ee6-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a7ee6-125">NOTES</span></span>

## <span data-ttu-id="a7ee6-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7ee6-126">RELATED LINKS</span></span>

[<span data-ttu-id="a7ee6-127">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a7ee6-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="a7ee6-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="a7ee6-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="a7ee6-129">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a7ee6-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="a7ee6-130">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a7ee6-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="a7ee6-131">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a7ee6-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="a7ee6-132">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a7ee6-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="a7ee6-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a7ee6-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="a7ee6-134">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a7ee6-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


