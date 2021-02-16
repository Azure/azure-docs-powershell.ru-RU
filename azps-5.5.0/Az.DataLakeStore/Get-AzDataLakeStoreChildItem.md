---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: 6123cacd35eb0a683ec2103ea00e2e06a2d80cd2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222660"
---
# <span data-ttu-id="57c5b-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="57c5b-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="57c5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57c5b-102">SYNOPSIS</span></span>
<span data-ttu-id="57c5b-103">Получает список элементов в папке в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="57c5b-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="57c5b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="57c5b-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57c5b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57c5b-105">DESCRIPTION</span></span>
<span data-ttu-id="57c5b-106">Для получения списка элементов в папке Магазина "Озеро данных" возвращается список элементов из папки **Get-AzDataLakeStoreChildItem.**</span><span class="sxs-lookup"><span data-stu-id="57c5b-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="57c5b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="57c5b-107">EXAMPLES</span></span>

### <span data-ttu-id="57c5b-108">Пример 1. Получить элементы ребенка для папки</span><span class="sxs-lookup"><span data-stu-id="57c5b-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="57c5b-109">Эта команда возвращает элементы для папки MyFiles.</span><span class="sxs-lookup"><span data-stu-id="57c5b-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="57c5b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57c5b-110">PARAMETERS</span></span>

### <span data-ttu-id="57c5b-111">-Account</span><span class="sxs-lookup"><span data-stu-id="57c5b-111">-Account</span></span>
<span data-ttu-id="57c5b-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="57c5b-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="57c5b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57c5b-113">-DefaultProfile</span></span>
<span data-ttu-id="57c5b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57c5b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57c5b-115">-Path</span><span class="sxs-lookup"><span data-stu-id="57c5b-115">-Path</span></span>
<span data-ttu-id="57c5b-116">Путь к папке в магазине "Озеро данных", начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="57c5b-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="57c5b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c5b-117">CommonParameters</span></span>
<span data-ttu-id="57c5b-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57c5b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c5b-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57c5b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c5b-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57c5b-120">INPUTS</span></span>

### <span data-ttu-id="57c5b-121">System.String</span><span class="sxs-lookup"><span data-stu-id="57c5b-121">System.String</span></span>

### <span data-ttu-id="57c5b-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="57c5b-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="57c5b-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57c5b-123">OUTPUTS</span></span>

### <span data-ttu-id="57c5b-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="57c5b-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="57c5b-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="57c5b-125">NOTES</span></span>

## <span data-ttu-id="57c5b-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57c5b-126">RELATED LINKS</span></span>
