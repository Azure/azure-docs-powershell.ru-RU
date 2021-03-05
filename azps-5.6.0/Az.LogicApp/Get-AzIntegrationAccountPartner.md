---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
ms.openlocfilehash: 1819f8978ef29235743f9b4095d770f3b34c4b9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960584"
---
# <span data-ttu-id="3e73a-101">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3e73a-101">Get-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="3e73a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e73a-102">SYNOPSIS</span></span>
<span data-ttu-id="3e73a-103">Получает партнеров по интеграции учетных записей.</span><span class="sxs-lookup"><span data-stu-id="3e73a-103">Gets integration account partners.</span></span>

## <span data-ttu-id="3e73a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3e73a-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e73a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e73a-105">DESCRIPTION</span></span>
<span data-ttu-id="3e73a-106">Для получения партнеров по учетной записи из группы ресурсов можно получить партнеров по интеграции с **Get-AzIntegrationAccountPartner.**</span><span class="sxs-lookup"><span data-stu-id="3e73a-106">The **Get-AzIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="3e73a-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя партнера.</span><span class="sxs-lookup"><span data-stu-id="3e73a-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="3e73a-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="3e73a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3e73a-109">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="3e73a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3e73a-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="3e73a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3e73a-111">Если не задан параметр обязательного шаблона, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="3e73a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3e73a-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3e73a-112">EXAMPLES</span></span>

### <span data-ttu-id="3e73a-113">Пример 1. Получить партнера по интеграции с учетной записью</span><span class="sxs-lookup"><span data-stu-id="3e73a-113">Example 1: Get an integration account partner</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="3e73a-114">Эта команда возвращает партнера по интеграции с именем IntegrationAccountPartner22.</span><span class="sxs-lookup"><span data-stu-id="3e73a-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="3e73a-115">Пример 2. Интеграция партнеров учетной записи с использованием имени учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="3e73a-115">Example 2: Get an integration account partners by using an integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="3e73a-116">Эта команда возвращает партнеров по интеграции с учетной записью IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="3e73a-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="3e73a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e73a-117">PARAMETERS</span></span>

### <span data-ttu-id="3e73a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e73a-118">-DefaultProfile</span></span>
<span data-ttu-id="3e73a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3e73a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e73a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3e73a-120">-Name</span></span>
<span data-ttu-id="3e73a-121">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="3e73a-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e73a-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="3e73a-122">-PartnerName</span></span>
<span data-ttu-id="3e73a-123">Указывает имя партнера по учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="3e73a-123">Specifies the name of the integration account partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e73a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e73a-124">-ResourceGroupName</span></span>
<span data-ttu-id="3e73a-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3e73a-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e73a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e73a-126">CommonParameters</span></span>
<span data-ttu-id="3e73a-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e73a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e73a-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e73a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e73a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e73a-129">INPUTS</span></span>

### <span data-ttu-id="3e73a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3e73a-130">System.String</span></span>

## <span data-ttu-id="3e73a-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3e73a-131">OUTPUTS</span></span>

### <span data-ttu-id="3e73a-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3e73a-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="3e73a-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3e73a-133">NOTES</span></span>

## <span data-ttu-id="3e73a-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e73a-134">RELATED LINKS</span></span>

[<span data-ttu-id="3e73a-135">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3e73a-135">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="3e73a-136">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3e73a-136">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="3e73a-137">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3e73a-137">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


