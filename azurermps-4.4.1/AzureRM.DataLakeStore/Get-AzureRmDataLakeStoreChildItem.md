---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
ms.openlocfilehash: 51b27c5dcffc36e45946d9fd2b0c842cfe17cdaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733757"
---
# <span data-ttu-id="69ba5-101">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="69ba5-101">Get-AzureRmDataLakeStoreChildItem</span></span>

## <span data-ttu-id="69ba5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="69ba5-102">SYNOPSIS</span></span>
<span data-ttu-id="69ba5-103">Получает список элементов в папке для Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="69ba5-103">Gets the list of items in a folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69ba5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="69ba5-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69ba5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69ba5-105">DESCRIPTION</span></span>
<span data-ttu-id="69ba5-106">Командлет **Get-AzureRmDataLakeStoreChildItem** получает список элементов в папке для Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="69ba5-106">The **Get-AzureRmDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="69ba5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="69ba5-107">EXAMPLES</span></span>

### <span data-ttu-id="69ba5-108">Пример 1: получение дочерних элементов для папки</span><span class="sxs-lookup"><span data-stu-id="69ba5-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="69ba5-109">Эта команда возвращает дочерние элементы для папки MyFiles.</span><span class="sxs-lookup"><span data-stu-id="69ba5-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="69ba5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="69ba5-110">PARAMETERS</span></span>

### <span data-ttu-id="69ba5-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="69ba5-111">-Account</span></span>
<span data-ttu-id="69ba5-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="69ba5-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="69ba5-113">-Path</span><span class="sxs-lookup"><span data-stu-id="69ba5-113">-Path</span></span>
<span data-ttu-id="69ba5-114">Указывает путь к папке Data Lake Store для папки, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="69ba5-114">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ba5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ba5-115">-DefaultProfile</span></span>
<span data-ttu-id="69ba5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69ba5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69ba5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ba5-117">CommonParameters</span></span>
<span data-ttu-id="69ba5-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="69ba5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ba5-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69ba5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ba5-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="69ba5-120">INPUTS</span></span>

## <span data-ttu-id="69ba5-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="69ba5-121">OUTPUTS</span></span>

### <span data-ttu-id="69ba5-122">IEnumerable<DataLakeStoreItem></span><span class="sxs-lookup"><span data-stu-id="69ba5-122">IEnumerable<DataLakeStoreItem></span></span>
<span data-ttu-id="69ba5-123">Список файлов и папок в Data Lake Store по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="69ba5-123">The list of Data Lake Store files and folders under the specified path.</span></span>

## <span data-ttu-id="69ba5-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="69ba5-124">NOTES</span></span>

## <span data-ttu-id="69ba5-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69ba5-125">RELATED LINKS</span></span>

