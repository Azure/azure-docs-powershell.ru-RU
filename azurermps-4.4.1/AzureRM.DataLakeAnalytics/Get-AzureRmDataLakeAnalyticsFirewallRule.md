---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 99acce24389a02c8fb50f5b313841319f813feaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569543"
---
# <span data-ttu-id="bab1a-101">Get-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bab1a-101">Get-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="bab1a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bab1a-102">SYNOPSIS</span></span>
<span data-ttu-id="bab1a-103">Получение правила брандмауэра или списка правил брандмауэра из учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bab1a-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bab1a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bab1a-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bab1a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bab1a-105">DESCRIPTION</span></span>
<span data-ttu-id="bab1a-106">Командлет **Get-AzureRmDataLakeAnalyticsFirewallRule** извлекает правило брандмауэра или список правил брандмауэра из учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bab1a-106">The **Get-AzureRmDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="bab1a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bab1a-107">EXAMPLES</span></span>

### <span data-ttu-id="bab1a-108">Пример 1: получение правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="bab1a-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="bab1a-109">Эта команда получает правило брандмауэра с именем "Мое правило брандмауэра" из учетной записи "ContosoAdlAcct".</span><span class="sxs-lookup"><span data-stu-id="bab1a-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="bab1a-110">Пример 2: список всех правил брандмауэра</span><span class="sxs-lookup"><span data-stu-id="bab1a-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="bab1a-111">Эта команда получает все правила брандмауэра из учетной записи "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="bab1a-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="bab1a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bab1a-112">PARAMETERS</span></span>

### <span data-ttu-id="bab1a-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="bab1a-113">-Account</span></span>
<span data-ttu-id="bab1a-114">Учетная запись Data Lake Analytics, из которой нужно получить правило межсетевого экрана</span><span class="sxs-lookup"><span data-stu-id="bab1a-114">The Data Lake Analytics account to get the firewall rule from</span></span>

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

### <span data-ttu-id="bab1a-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bab1a-115">-Name</span></span>
<span data-ttu-id="bab1a-116">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="bab1a-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="bab1a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bab1a-117">-ResourceGroupName</span></span>
<span data-ttu-id="bab1a-118">Имя группы ресурсов, в которой требуется получить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="bab1a-118">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="bab1a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bab1a-119">-DefaultProfile</span></span>
<span data-ttu-id="bab1a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bab1a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bab1a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bab1a-121">CommonParameters</span></span>
<span data-ttu-id="bab1a-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bab1a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bab1a-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bab1a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bab1a-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bab1a-124">INPUTS</span></span>

### <span data-ttu-id="bab1a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="bab1a-125">System.String</span></span>

## <span data-ttu-id="bab1a-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bab1a-126">OUTPUTS</span></span>

### <span data-ttu-id="bab1a-127">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bab1a-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>
<span data-ttu-id="bab1a-128">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule, Microsoft. Azure. Commands. DataLakeAnalytics, Version = 2.5.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="bab1a-128">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule, Microsoft.Azure.Commands.DataLakeAnalytics, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bab1a-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="bab1a-129">NOTES</span></span>

## <span data-ttu-id="bab1a-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bab1a-130">RELATED LINKS</span></span>

