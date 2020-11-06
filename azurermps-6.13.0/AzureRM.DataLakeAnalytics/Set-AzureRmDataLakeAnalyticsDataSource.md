---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 8aae62ccbf79f2b3c59f6009aa5233daf00853fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566504"
---
# <span data-ttu-id="60a94-101">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="60a94-101">Set-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="60a94-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="60a94-102">SYNOPSIS</span></span>
<span data-ttu-id="60a94-103">Изменение сведений об источнике данных учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="60a94-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60a94-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="60a94-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60a94-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60a94-105">DESCRIPTION</span></span>
<span data-ttu-id="60a94-106">Командлет **Set-AzureRmDataLakeAnalyticsDataSource** изменяет сведения об источнике данных учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="60a94-106">The **Set-AzureRmDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="60a94-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="60a94-107">EXAMPLES</span></span>

### <span data-ttu-id="60a94-108">Пример 1: изменение клавиши доступа для источника данных</span><span class="sxs-lookup"><span data-stu-id="60a94-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="60a94-109">Эта команда изменяет ключ доступа, хранящийся в источнике данных хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="60a94-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="60a94-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="60a94-110">PARAMETERS</span></span>

### <span data-ttu-id="60a94-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="60a94-111">-AccessKey</span></span>
<span data-ttu-id="60a94-112">Указывает новый ключ доступа источника данных хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="60a94-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="60a94-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="60a94-113">-Account</span></span>
<span data-ttu-id="60a94-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="60a94-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="60a94-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="60a94-115">-Blob</span></span>
<span data-ttu-id="60a94-116">Указывает имя источника данных хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="60a94-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="60a94-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a94-117">-DefaultProfile</span></span>
<span data-ttu-id="60a94-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="60a94-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60a94-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60a94-119">-ResourceGroupName</span></span>
<span data-ttu-id="60a94-120">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="60a94-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="60a94-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a94-121">CommonParameters</span></span>
<span data-ttu-id="60a94-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="60a94-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a94-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60a94-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a94-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="60a94-124">INPUTS</span></span>

### <span data-ttu-id="60a94-125">System. String</span><span class="sxs-lookup"><span data-stu-id="60a94-125">System.String</span></span>

## <span data-ttu-id="60a94-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="60a94-126">OUTPUTS</span></span>

### <span data-ttu-id="60a94-127">System. void</span><span class="sxs-lookup"><span data-stu-id="60a94-127">System.Void</span></span>

## <span data-ttu-id="60a94-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="60a94-128">NOTES</span></span>

## <span data-ttu-id="60a94-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60a94-129">RELATED LINKS</span></span>

[<span data-ttu-id="60a94-130">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="60a94-130">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="60a94-131">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="60a94-131">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)


