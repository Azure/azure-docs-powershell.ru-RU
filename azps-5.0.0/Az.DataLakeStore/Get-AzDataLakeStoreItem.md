---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: ad741d955399b355534074737741b153d8d48690
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313370"
---
# <span data-ttu-id="ba099-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba099-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="ba099-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba099-102">SYNOPSIS</span></span>
<span data-ttu-id="ba099-103">Получает сведения о файле или папке в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ba099-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ba099-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba099-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba099-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba099-105">DESCRIPTION</span></span>
<span data-ttu-id="ba099-106">Командлет **Get-AzDataLakeStoreItem** получает сведения о файле или папке в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ba099-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ba099-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba099-107">EXAMPLES</span></span>

### <span data-ttu-id="ba099-108">Пример 1: получение сведений о файле из Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ba099-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="ba099-109">Эта команда получает сведения о файле Test.csv из Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ba099-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="ba099-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba099-110">PARAMETERS</span></span>

### <span data-ttu-id="ba099-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="ba099-111">-Account</span></span>
<span data-ttu-id="ba099-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ba099-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ba099-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba099-113">-DefaultProfile</span></span>
<span data-ttu-id="ba099-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba099-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba099-115">-Path</span><span class="sxs-lookup"><span data-stu-id="ba099-115">-Path</span></span>
<span data-ttu-id="ba099-116">Указывает путь к Data Lake Store, из которого требуется получить сведения об элементе, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="ba099-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ba099-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba099-117">CommonParameters</span></span>
<span data-ttu-id="ba099-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba099-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba099-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba099-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba099-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba099-120">INPUTS</span></span>

### <span data-ttu-id="ba099-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ba099-121">System.String</span></span>

### <span data-ttu-id="ba099-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="ba099-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="ba099-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba099-123">OUTPUTS</span></span>

### <span data-ttu-id="ba099-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba099-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="ba099-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba099-125">NOTES</span></span>

## <span data-ttu-id="ba099-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba099-126">RELATED LINKS</span></span>

[<span data-ttu-id="ba099-127">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba099-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="ba099-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="ba099-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="ba099-129">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba099-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="ba099-130">Присоединиться к AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba099-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="ba099-131">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba099-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="ba099-132">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba099-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="ba099-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba099-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="ba099-134">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba099-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)

