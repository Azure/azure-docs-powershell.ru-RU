---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
ms.openlocfilehash: cf6d2f4da1803e5c9403803ea7231b55c13d7243
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079577"
---
# <span data-ttu-id="3d174-101">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3d174-101">Get-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="3d174-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d174-102">SYNOPSIS</span></span>
<span data-ttu-id="3d174-103">Получение партнеров по учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="3d174-103">Gets integration account partners.</span></span>

## <span data-ttu-id="3d174-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d174-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d174-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d174-105">DESCRIPTION</span></span>
<span data-ttu-id="3d174-106">Командлет **Get-AzIntegrationAccountPartner** получает партнеров учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3d174-106">The **Get-AzIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="3d174-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя партнера.</span><span class="sxs-lookup"><span data-stu-id="3d174-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="3d174-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="3d174-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3d174-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="3d174-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3d174-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="3d174-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3d174-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="3d174-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3d174-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d174-112">EXAMPLES</span></span>

### <span data-ttu-id="3d174-113">Пример 1: получение партнера учетной записи для интеграции</span><span class="sxs-lookup"><span data-stu-id="3d174-113">Example 1: Get an integration account partner</span></span>
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

<span data-ttu-id="3d174-114">Эта команда получает партнера учетной записи интеграции с именем IntegrationAccountPartner22.</span><span class="sxs-lookup"><span data-stu-id="3d174-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="3d174-115">Пример 2: получение партнеров по учетной записи интеграции с помощью имени учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="3d174-115">Example 2: Get an integration account partners by using an integration account name</span></span>
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

<span data-ttu-id="3d174-116">Эта команда получает партнеров учетной записи интеграции для учетной записи интеграции с именем IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="3d174-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="3d174-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d174-117">PARAMETERS</span></span>

### <span data-ttu-id="3d174-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d174-118">-DefaultProfile</span></span>
<span data-ttu-id="3d174-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3d174-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d174-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3d174-120">-Name</span></span>
<span data-ttu-id="3d174-121">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="3d174-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="3d174-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="3d174-122">-PartnerName</span></span>
<span data-ttu-id="3d174-123">Указывает имя партнера учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="3d174-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="3d174-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d174-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d174-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3d174-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3d174-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d174-126">CommonParameters</span></span>
<span data-ttu-id="3d174-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d174-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d174-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d174-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d174-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d174-129">INPUTS</span></span>

### <span data-ttu-id="3d174-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3d174-130">System.String</span></span>

## <span data-ttu-id="3d174-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d174-131">OUTPUTS</span></span>

### <span data-ttu-id="3d174-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3d174-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="3d174-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d174-133">NOTES</span></span>

## <span data-ttu-id="3d174-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d174-134">RELATED LINKS</span></span>

[<span data-ttu-id="3d174-135">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3d174-135">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="3d174-136">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3d174-136">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="3d174-137">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3d174-137">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)

