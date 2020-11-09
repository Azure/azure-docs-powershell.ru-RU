---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1894e5a79660558163d9b95ce49f1736ea002bf9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313634"
---
# <span data-ttu-id="1f941-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1f941-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="1f941-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f941-102">SYNOPSIS</span></span>
<span data-ttu-id="1f941-103">Получение сведений об учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1f941-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="1f941-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f941-104">SYNTAX</span></span>

### <span data-ttu-id="1f941-105">GetAllInSubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1f941-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f941-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1f941-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f941-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="1f941-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f941-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f941-108">DESCRIPTION</span></span>
<span data-ttu-id="1f941-109">Командлет **Get-AzDataLakeAnalyticsAccount** получает сведения о учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1f941-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="1f941-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f941-110">EXAMPLES</span></span>

### <span data-ttu-id="1f941-111">Пример 1: получение сведений об учетной записи Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="1f941-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="1f941-112">Эта команда получает сведения о учетной записи с именем ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="1f941-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="1f941-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f941-113">PARAMETERS</span></span>

### <span data-ttu-id="1f941-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f941-114">-DefaultProfile</span></span>
<span data-ttu-id="1f941-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1f941-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f941-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1f941-116">-Name</span></span>
<span data-ttu-id="1f941-117">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1f941-117">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="1f941-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f941-118">-ResourceGroupName</span></span>
<span data-ttu-id="1f941-119">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1f941-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="1f941-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f941-120">CommonParameters</span></span>
<span data-ttu-id="1f941-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f941-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f941-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f941-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f941-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f941-123">INPUTS</span></span>

### <span data-ttu-id="1f941-124">System. String</span><span class="sxs-lookup"><span data-stu-id="1f941-124">System.String</span></span>

## <span data-ttu-id="1f941-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f941-125">OUTPUTS</span></span>

### <span data-ttu-id="1f941-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1f941-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="1f941-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="1f941-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="1f941-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f941-128">NOTES</span></span>

## <span data-ttu-id="1f941-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f941-129">RELATED LINKS</span></span>

[<span data-ttu-id="1f941-130">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1f941-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1f941-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1f941-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1f941-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1f941-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1f941-133">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1f941-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


