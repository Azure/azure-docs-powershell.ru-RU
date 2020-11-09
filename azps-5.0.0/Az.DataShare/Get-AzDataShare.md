---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
ms.openlocfilehash: a4c63e22427e3ae0b666bb7d99b8217a990657c2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313058"
---
# <span data-ttu-id="3181a-101">Get-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="3181a-101">Get-AzDataShare</span></span>

## <span data-ttu-id="3181a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3181a-102">SYNOPSIS</span></span>
<span data-ttu-id="3181a-103">Получение сведений об общих ресурсах данных.</span><span class="sxs-lookup"><span data-stu-id="3181a-103">Get information about Data Shares.</span></span>

## <span data-ttu-id="3181a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3181a-104">SYNTAX</span></span>

### <span data-ttu-id="3181a-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3181a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShare -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3181a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3181a-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3181a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3181a-107">DESCRIPTION</span></span>
<span data-ttu-id="3181a-108">Командлет **Get-AzDataShare** получает сведения о ресурсах общих данных в службе общих данных Azure accoount.</span><span class="sxs-lookup"><span data-stu-id="3181a-108">The **Get-AzDataShare** cmdlet gets information about data shares in an Azure data share accoount.</span></span>
<span data-ttu-id="3181a-109">Если вы задаете имя общего доступа к данным, этот командлет получает сведения об этом общем доступе к данным.</span><span class="sxs-lookup"><span data-stu-id="3181a-109">If you specify the name of a data share, this cmdlet gets information about that data share.</span></span>
<span data-ttu-id="3181a-110">Если имя не задано, этот командлет получает сведения обо всех общих ресурсах в учетной записи для общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="3181a-110">If you do not specify a name, this cmdlet gets information about all of the data shares in an Azure data share account.</span></span>

## <span data-ttu-id="3181a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3181a-111">EXAMPLES</span></span>

### <span data-ttu-id="3181a-112">Пример 1: получение определенного общего доступа к данным</span><span class="sxs-lookup"><span data-stu-id="3181a-112">Example 1 : Get a specific data share</span></span>
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

<span data-ttu-id="3181a-113">Эта команда отображает сведения о AdsShare общего доступа к данным в WikiAdsAccount учетной записи для общего доступа к данным Azure и группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3181a-113">This command displays information about data share AdsShare in the Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="3181a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3181a-114">PARAMETERS</span></span>

### <span data-ttu-id="3181a-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="3181a-115">-AccountName</span></span>
<span data-ttu-id="3181a-116">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="3181a-116">Azure data share account name</span></span>

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

### <span data-ttu-id="3181a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3181a-117">-DefaultProfile</span></span>
<span data-ttu-id="3181a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3181a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3181a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3181a-119">-Name</span></span>
<span data-ttu-id="3181a-120">Имя общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="3181a-120">Azure data share name</span></span>

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

### <span data-ttu-id="3181a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3181a-121">-ResourceGroupName</span></span>
<span data-ttu-id="3181a-122">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="3181a-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="3181a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3181a-123">-ResourceId</span></span>
<span data-ttu-id="3181a-124">Идентификатор ресурса общего ресурса данных Azure</span><span class="sxs-lookup"><span data-stu-id="3181a-124">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="3181a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3181a-125">CommonParameters</span></span>
<span data-ttu-id="3181a-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3181a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3181a-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3181a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3181a-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3181a-128">INPUTS</span></span>

### <span data-ttu-id="3181a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3181a-129">System.String</span></span>

## <span data-ttu-id="3181a-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3181a-130">OUTPUTS</span></span>

### <span data-ttu-id="3181a-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="3181a-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="3181a-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="3181a-132">NOTES</span></span>

## <span data-ttu-id="3181a-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3181a-133">RELATED LINKS</span></span>
