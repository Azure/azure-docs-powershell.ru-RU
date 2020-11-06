---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: e873a7f4a825ed84172d098dfa0f8cb631cc3f7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563576"
---
# <span data-ttu-id="03ea1-101">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="03ea1-101">Set-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="03ea1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="03ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="03ea1-103">Изменение сведений об источнике данных учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="03ea1-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03ea1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="03ea1-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03ea1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03ea1-105">DESCRIPTION</span></span>
<span data-ttu-id="03ea1-106">Командлет **Set-AzureRmDataLakeAnalyticsDataSource** изменяет сведения об источнике данных учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="03ea1-106">The **Set-AzureRmDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="03ea1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="03ea1-107">EXAMPLES</span></span>

### <span data-ttu-id="03ea1-108">Пример 1: изменение клавиши доступа для источника данных</span><span class="sxs-lookup"><span data-stu-id="03ea1-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="03ea1-109">Эта команда изменяет ключ доступа, хранящийся в источнике данных хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="03ea1-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="03ea1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="03ea1-110">PARAMETERS</span></span>

### <span data-ttu-id="03ea1-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="03ea1-111">-AccessKey</span></span>
<span data-ttu-id="03ea1-112">Указывает новый ключ доступа источника данных хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="03ea1-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ea1-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="03ea1-113">-Account</span></span>
<span data-ttu-id="03ea1-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="03ea1-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="03ea1-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="03ea1-115">-Blob</span></span>
<span data-ttu-id="03ea1-116">Указывает имя источника данных хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="03ea1-116">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ea1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ea1-117">-DefaultProfile</span></span>
<span data-ttu-id="03ea1-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="03ea1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03ea1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03ea1-119">-ResourceGroupName</span></span>
<span data-ttu-id="03ea1-120">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="03ea1-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ea1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ea1-121">CommonParameters</span></span>
<span data-ttu-id="03ea1-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="03ea1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ea1-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03ea1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ea1-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="03ea1-124">INPUTS</span></span>

### <span data-ttu-id="03ea1-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="03ea1-125">None</span></span>
<span data-ttu-id="03ea1-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="03ea1-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="03ea1-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="03ea1-127">OUTPUTS</span></span>

### <span data-ttu-id="03ea1-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="03ea1-128">None</span></span>

## <span data-ttu-id="03ea1-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="03ea1-129">NOTES</span></span>

## <span data-ttu-id="03ea1-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03ea1-130">RELATED LINKS</span></span>

[<span data-ttu-id="03ea1-131">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="03ea1-131">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="03ea1-132">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="03ea1-132">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)


