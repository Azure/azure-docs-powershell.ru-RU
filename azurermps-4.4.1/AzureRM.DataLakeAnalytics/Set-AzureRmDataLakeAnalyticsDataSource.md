---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 258db8a7dc1d771b73ea4c4fa373b1861847b820
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733768"
---
# <span data-ttu-id="48171-101">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="48171-101">Set-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="48171-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48171-102">SYNOPSIS</span></span>
<span data-ttu-id="48171-103">Изменение сведений об источнике данных учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="48171-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48171-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48171-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48171-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48171-105">DESCRIPTION</span></span>
<span data-ttu-id="48171-106">Командлет **Set-AzureRmDataLakeAnalyticsDataSource** изменяет сведения об источнике данных учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="48171-106">The **Set-AzureRmDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="48171-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48171-107">EXAMPLES</span></span>

### <span data-ttu-id="48171-108">Пример 1: изменение клавиши доступа для источника данных</span><span class="sxs-lookup"><span data-stu-id="48171-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="48171-109">Эта команда изменяет ключ доступа, хранящийся в источнике данных хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="48171-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="48171-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48171-110">PARAMETERS</span></span>

### <span data-ttu-id="48171-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="48171-111">-AccessKey</span></span>
<span data-ttu-id="48171-112">Указывает новый ключ доступа источника данных хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="48171-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48171-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="48171-113">-Account</span></span>
<span data-ttu-id="48171-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="48171-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="48171-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="48171-115">-Blob</span></span>
<span data-ttu-id="48171-116">Указывает имя источника данных хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="48171-116">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48171-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48171-117">-ResourceGroupName</span></span>
<span data-ttu-id="48171-118">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="48171-118">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48171-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48171-119">-DefaultProfile</span></span>
<span data-ttu-id="48171-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="48171-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48171-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48171-121">CommonParameters</span></span>
<span data-ttu-id="48171-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48171-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48171-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48171-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48171-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48171-124">INPUTS</span></span>

## <span data-ttu-id="48171-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48171-125">OUTPUTS</span></span>

### <span data-ttu-id="48171-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="48171-126">None</span></span>

## <span data-ttu-id="48171-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="48171-127">NOTES</span></span>

## <span data-ttu-id="48171-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48171-128">RELATED LINKS</span></span>

[<span data-ttu-id="48171-129">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="48171-129">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="48171-130">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="48171-130">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)


