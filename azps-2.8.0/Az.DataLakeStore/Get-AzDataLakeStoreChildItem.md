---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: 828418095c7e77a7ee484d00e9d4d3f6f4a9927b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721330"
---
# <span data-ttu-id="debc2-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="debc2-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="debc2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="debc2-102">SYNOPSIS</span></span>
<span data-ttu-id="debc2-103">Получает список элементов в папке для Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="debc2-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="debc2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="debc2-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="debc2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="debc2-105">DESCRIPTION</span></span>
<span data-ttu-id="debc2-106">Командлет **Get-AzDataLakeStoreChildItem** получает список элементов в папке для Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="debc2-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="debc2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="debc2-107">EXAMPLES</span></span>

### <span data-ttu-id="debc2-108">Пример 1: получение дочерних элементов для папки</span><span class="sxs-lookup"><span data-stu-id="debc2-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="debc2-109">Эта команда возвращает дочерние элементы для папки MyFiles.</span><span class="sxs-lookup"><span data-stu-id="debc2-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="debc2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="debc2-110">PARAMETERS</span></span>

### <span data-ttu-id="debc2-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="debc2-111">-Account</span></span>
<span data-ttu-id="debc2-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="debc2-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="debc2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="debc2-113">-DefaultProfile</span></span>
<span data-ttu-id="debc2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="debc2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="debc2-115">-Path</span><span class="sxs-lookup"><span data-stu-id="debc2-115">-Path</span></span>
<span data-ttu-id="debc2-116">Указывает путь к папке Data Lake Store для папки, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="debc2-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="debc2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="debc2-117">CommonParameters</span></span>
<span data-ttu-id="debc2-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="debc2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="debc2-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="debc2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="debc2-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="debc2-120">INPUTS</span></span>

### <span data-ttu-id="debc2-121">System. String</span><span class="sxs-lookup"><span data-stu-id="debc2-121">System.String</span></span>

### <span data-ttu-id="debc2-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="debc2-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="debc2-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="debc2-123">OUTPUTS</span></span>

### <span data-ttu-id="debc2-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="debc2-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="debc2-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="debc2-125">NOTES</span></span>

## <span data-ttu-id="debc2-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="debc2-126">RELATED LINKS</span></span>
