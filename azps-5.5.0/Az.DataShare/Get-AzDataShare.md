---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
ms.openlocfilehash: a4c63e22427e3ae0b666bb7d99b8217a990657c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220188"
---
# <span data-ttu-id="f1254-101">Get-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="f1254-101">Get-AzDataShare</span></span>

## <span data-ttu-id="f1254-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1254-102">SYNOPSIS</span></span>
<span data-ttu-id="f1254-103">Получите сведения о информационных акциях.</span><span class="sxs-lookup"><span data-stu-id="f1254-103">Get information about Data Shares.</span></span>

## <span data-ttu-id="f1254-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f1254-104">SYNTAX</span></span>

### <span data-ttu-id="f1254-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f1254-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShare -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1254-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1254-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1254-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1254-107">DESCRIPTION</span></span>
<span data-ttu-id="f1254-108">**Cmdlet Get-AzDataShare** получает сведения об акциях данных в accoount в области обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="f1254-108">The **Get-AzDataShare** cmdlet gets information about data shares in an Azure data share accoount.</span></span>
<span data-ttu-id="f1254-109">Если указать имя для нужного поделиться данными, этот cmdlet получит сведения об этом поделиться данными.</span><span class="sxs-lookup"><span data-stu-id="f1254-109">If you specify the name of a data share, this cmdlet gets information about that data share.</span></span>
<span data-ttu-id="f1254-110">Если имя не указано, этот cmdlet получает сведения обо всех данных в учетной записи azure data share.</span><span class="sxs-lookup"><span data-stu-id="f1254-110">If you do not specify a name, this cmdlet gets information about all of the data shares in an Azure data share account.</span></span>

## <span data-ttu-id="f1254-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f1254-111">EXAMPLES</span></span>

### <span data-ttu-id="f1254-112">Пример 1. Получить определенный объем данных</span><span class="sxs-lookup"><span data-stu-id="f1254-112">Example 1 : Get a specific data share</span></span>
```
PS C:\>Get-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="f1254-113">Эта команда отображает сведения о совместном использование данных AdsShare в учетной записи обмена данными Azure WikiAdsAccount и группе ресурсов ADS.</span><span class="sxs-lookup"><span data-stu-id="f1254-113">This command displays information about data share AdsShare in the Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="f1254-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1254-114">PARAMETERS</span></span>

### <span data-ttu-id="f1254-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f1254-115">-AccountName</span></span>
<span data-ttu-id="f1254-116">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="f1254-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1254-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1254-117">-DefaultProfile</span></span>
<span data-ttu-id="f1254-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1254-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1254-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f1254-119">-Name</span></span>
<span data-ttu-id="f1254-120">Имя обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="f1254-120">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1254-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1254-121">-ResourceGroupName</span></span>
<span data-ttu-id="f1254-122">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="f1254-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1254-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1254-123">-ResourceId</span></span>
<span data-ttu-id="f1254-124">ИД ресурса для azure data share</span><span class="sxs-lookup"><span data-stu-id="f1254-124">The resource id of the azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1254-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1254-125">CommonParameters</span></span>
<span data-ttu-id="f1254-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1254-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1254-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1254-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1254-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1254-128">INPUTS</span></span>

### <span data-ttu-id="f1254-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f1254-129">System.String</span></span>

## <span data-ttu-id="f1254-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f1254-130">OUTPUTS</span></span>

### <span data-ttu-id="f1254-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="f1254-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="f1254-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f1254-132">NOTES</span></span>

## <span data-ttu-id="f1254-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1254-133">RELATED LINKS</span></span>
