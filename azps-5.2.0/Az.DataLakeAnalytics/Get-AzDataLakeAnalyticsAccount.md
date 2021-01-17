---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1894e5a79660558163d9b95ce49f1736ea002bf9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416508"
---
# <span data-ttu-id="d58ef-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d58ef-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="d58ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d58ef-102">SYNOPSIS</span></span>
<span data-ttu-id="d58ef-103">Сведения об учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d58ef-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="d58ef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d58ef-104">SYNTAX</span></span>

### <span data-ttu-id="d58ef-105">GetAllInSubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d58ef-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d58ef-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d58ef-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d58ef-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="d58ef-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d58ef-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d58ef-108">DESCRIPTION</span></span>
<span data-ttu-id="d58ef-109">Чтобы **получить сведения об учетной** записи Azure Data Lake Analytics, можно получить сведения о ее учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d58ef-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="d58ef-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d58ef-110">EXAMPLES</span></span>

### <span data-ttu-id="d58ef-111">Пример 1. Просмотр сведений об учетной записи Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="d58ef-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="d58ef-112">Эта команда получает сведения об учетной записи ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="d58ef-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="d58ef-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d58ef-113">PARAMETERS</span></span>

### <span data-ttu-id="d58ef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d58ef-114">-DefaultProfile</span></span>
<span data-ttu-id="d58ef-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d58ef-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d58ef-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d58ef-116">-Name</span></span>
<span data-ttu-id="d58ef-117">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d58ef-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d58ef-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d58ef-118">-ResourceGroupName</span></span>
<span data-ttu-id="d58ef-119">Имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d58ef-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d58ef-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d58ef-120">CommonParameters</span></span>
<span data-ttu-id="d58ef-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d58ef-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d58ef-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d58ef-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d58ef-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d58ef-123">INPUTS</span></span>

### <span data-ttu-id="d58ef-124">System.String</span><span class="sxs-lookup"><span data-stu-id="d58ef-124">System.String</span></span>

## <span data-ttu-id="d58ef-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d58ef-125">OUTPUTS</span></span>

### <span data-ttu-id="d58ef-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d58ef-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="d58ef-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="d58ef-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="d58ef-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d58ef-128">NOTES</span></span>

## <span data-ttu-id="d58ef-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d58ef-129">RELATED LINKS</span></span>

[<span data-ttu-id="d58ef-130">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d58ef-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d58ef-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d58ef-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d58ef-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d58ef-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d58ef-133">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d58ef-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


