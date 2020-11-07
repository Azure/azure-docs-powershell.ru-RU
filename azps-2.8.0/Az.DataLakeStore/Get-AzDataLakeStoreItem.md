---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: b3118c11fa794fef71836a580e272ec481c72147
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721317"
---
# <span data-ttu-id="e8ed8-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e8ed8-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="e8ed8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ed8-103">Получает сведения о файле или папке в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e8ed8-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e8ed8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8ed8-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8ed8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8ed8-105">DESCRIPTION</span></span>
<span data-ttu-id="e8ed8-106">Командлет **Get-AzDataLakeStoreItem** получает сведения о файле или папке в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e8ed8-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e8ed8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8ed8-107">EXAMPLES</span></span>

### <span data-ttu-id="e8ed8-108">Пример 1: получение сведений о файле из Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="e8ed8-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="e8ed8-109">Эта команда получает сведения о файле Test.csv из Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e8ed8-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="e8ed8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8ed8-110">PARAMETERS</span></span>

### <span data-ttu-id="e8ed8-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="e8ed8-111">-Account</span></span>
<span data-ttu-id="e8ed8-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e8ed8-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e8ed8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ed8-113">-DefaultProfile</span></span>
<span data-ttu-id="e8ed8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8ed8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8ed8-115">-Path</span><span class="sxs-lookup"><span data-stu-id="e8ed8-115">-Path</span></span>
<span data-ttu-id="e8ed8-116">Указывает путь к Data Lake Store, из которого требуется получить сведения об элементе, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="e8ed8-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="e8ed8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ed8-117">CommonParameters</span></span>
<span data-ttu-id="e8ed8-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8ed8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ed8-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8ed8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ed8-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8ed8-120">INPUTS</span></span>

### <span data-ttu-id="e8ed8-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e8ed8-121">System.String</span></span>

### <span data-ttu-id="e8ed8-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="e8ed8-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="e8ed8-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8ed8-123">OUTPUTS</span></span>

### <span data-ttu-id="e8ed8-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e8ed8-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="e8ed8-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8ed8-125">NOTES</span></span>

## <span data-ttu-id="e8ed8-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8ed8-126">RELATED LINKS</span></span>

[<span data-ttu-id="e8ed8-127">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e8ed8-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="e8ed8-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="e8ed8-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="e8ed8-129">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e8ed8-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="e8ed8-130">Присоединиться к AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e8ed8-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="e8ed8-131">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e8ed8-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="e8ed8-132">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e8ed8-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="e8ed8-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e8ed8-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="e8ed8-134">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e8ed8-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


