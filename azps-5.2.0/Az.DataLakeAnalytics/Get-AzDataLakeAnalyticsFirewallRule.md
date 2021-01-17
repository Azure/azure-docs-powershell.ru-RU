---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 40c44ff157fca6a276cac8ece508e9d540b526ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400100"
---
# <span data-ttu-id="0cdf8-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0cdf8-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="0cdf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cdf8-102">SYNOPSIS</span></span>
<span data-ttu-id="0cdf8-103">Извлекает правило брандмауэра или список правил брандмауэра из учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0cdf8-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="0cdf8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0cdf8-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cdf8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0cdf8-105">DESCRIPTION</span></span>
<span data-ttu-id="0cdf8-106">Для получения правила брандмауэра или списка правил брандмауэра из учетной записи Azure Data Lake Analytics извлекается правило брандмауэра или список правил брандмауэра. </span><span class="sxs-lookup"><span data-stu-id="0cdf8-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0cdf8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0cdf8-107">EXAMPLES</span></span>

### <span data-ttu-id="0cdf8-108">Пример 1. Получите правило брандмауэра</span><span class="sxs-lookup"><span data-stu-id="0cdf8-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="0cdf8-109">Эта команда получает правило брандмауэра "мое правило брандмауэра" из учетной записи ContosoAdlAcct.</span><span class="sxs-lookup"><span data-stu-id="0cdf8-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="0cdf8-110">Пример 2. Список всех правил брандмауэра</span><span class="sxs-lookup"><span data-stu-id="0cdf8-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="0cdf8-111">Эта команда получает все правила брандмауэра из учетной записи ContosoAdlAcct</span><span class="sxs-lookup"><span data-stu-id="0cdf8-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="0cdf8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0cdf8-112">PARAMETERS</span></span>

### <span data-ttu-id="0cdf8-113">-Account</span><span class="sxs-lookup"><span data-stu-id="0cdf8-113">-Account</span></span>
<span data-ttu-id="0cdf8-114">Учетная запись Data Lake Analytics для получения правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="0cdf8-114">The Data Lake Analytics account to get the firewall rule from</span></span>

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

### <span data-ttu-id="0cdf8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cdf8-115">-DefaultProfile</span></span>
<span data-ttu-id="0cdf8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0cdf8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cdf8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0cdf8-117">-Name</span></span>
<span data-ttu-id="0cdf8-118">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="0cdf8-118">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cdf8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cdf8-119">-ResourceGroupName</span></span>
<span data-ttu-id="0cdf8-120">Имя группы ресурсов, под которой нужно получить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="0cdf8-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cdf8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cdf8-121">CommonParameters</span></span>
<span data-ttu-id="0cdf8-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cdf8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cdf8-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cdf8-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cdf8-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0cdf8-124">INPUTS</span></span>

### <span data-ttu-id="0cdf8-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0cdf8-125">System.String</span></span>

## <span data-ttu-id="0cdf8-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0cdf8-126">OUTPUTS</span></span>

### <span data-ttu-id="0cdf8-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0cdf8-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="0cdf8-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0cdf8-128">NOTES</span></span>

## <span data-ttu-id="0cdf8-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0cdf8-129">RELATED LINKS</span></span>
